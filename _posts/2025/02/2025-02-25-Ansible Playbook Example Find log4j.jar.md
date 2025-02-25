---
layout: single
title: Ansible Playbook Example Find log4j.jar
categories: Ansible
tags:
  - Ansible
  - Vulnerability
toc: true
---
### 배경
운영중인 시스템의 고객(기관)에게서 보안조치 권고 공문이 왔다.
각 서버에 접속하여 log4j.jar 파일이 있는지부터 확인하게 됐다.
해당 취약점은 2021년에 큰 이슈가 된 것 같고 자바와 관련된 프로그램 같은 것들은 거의 연관돼있어서 더욱 영향이 컸던 것 같다.
**Apache 'Log4j' 취약점 보안패치 권고** 참고 
https://www.ncsc.go.kr:4018/main/cop/bbs/selectBoardArticle.do?bbsId=SecurityAdvice_main&nttId=12438
https://www.soft2000.com/26950

### 확인 명령어
```bash
find / -name "log4j*.jar" 2>/dev/null
```

gpt한테 물어보니 이외에도 몇가지가 더 있었는데 해당 명령어들로는 확인이 어려웠다.
#### 참고용 명령어
```bash
## 1. 패키지 관리자 확인
# Debian/Ubuntu
dpkg -l | grep log4j

# RHEL/CentOS
rpm -qa | grep log4j

# Alpine Linux
apk list --installed | grep log4j

## 2. Java 클래스패스 확인
java -cp your-application.jar org.apache.logging.log4j.core.util.Version

## 3. Java 프로세스 확인
ps aux | grep java
# 출력된 Java 프로세스 ID
sudo lsof -p <JAVA_PROCESS_ID> | grep log4j

## 4. Maven 또는 Gradle 프로젝트
# Maven, pom.xml
grep -A 5 "log4j" pom.xml

# Gradle, build.gradle
grep -A 5 "log4j" build.gradle

```

몇 개 서버가 log4j.jar 파일들이 있었고 최근에 조금 사용해보게 된 Ansible으로 결과 값을 따로 저장해보았다.

### Ansible Playbook : find_log4j.yml
```yaml
- name: Find Log4j Files on Servers
  hosts: all
  gather_facts: yes
  tasks:
    - name: Run find command to locate log4j JAR files
      shell: "find / -name 'log4j*.jar' 2>/dev/null"
      register: log4j_results
      ignore_errors: yes

    - name: Create result directory
      delegate_to: localhost
      file:
        path: "./log4j_results"
        state: directory
      run_once: true

    - name: Save output to file if log4j files are found
      delegate_to: localhost
      run_once: false
      when: log4j_results.stdout != ""
      vars:
        output_file: "log4j_results/{{ inventory_hostname }}_{{ ansible_date_time.date }}_{{ ansible_date_time.hour }}{{ ansible_date_time.minute }}.txt"
      copy:
        content: "{{ log4j_results.stdout }}"
        dest: "{{ output_file }}"

```

```bash
# playbook 실행
ansible-playbook find_log4j.yml

# 실행결과
log4j_results/
├── server1_2025-02-25_1530.txt
├── server2_2025-02-25_1530.txt

```

이렇게 출력 값이 존재하는 호스트에서 찾은 Log4j JAR 파일의 경로를 저장했다.
결과적으로 최근에 구축한 시스템이어서 대부분 log4j 2.17.0 이상을 사용하고 있었고 
한두 개 정도 확인 해봐야 할 게 존재하는 것 같다.