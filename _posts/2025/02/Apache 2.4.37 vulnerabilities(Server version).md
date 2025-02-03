---
layout: single
title: Apache 2.4.37 서버 버전 정보 제한
categories: Vulnerability
tags: [Apache httpd]
toc: True
---

보안취약점 조치 권고 사항
Apache 응답 헤더에서 서버 버전을 최소화하는 설정

## 작업 전

![Before](/images/2025/02/2025-02-03-rocky Apache vul Before.png)
기본 설정값에선 서버 정보와 Apache 버전 정보 등이 출력된다.


## **1. `ServerTokens` 설정 변경**

- `ServerTokens Full` → Apache 버전, 운영체제 정보까지 포함 (예: `Apache/2.4.57 (Rocky Linux)`)
- `ServerTokens OS` → 운영체제 정보까지 포함 (예: `Apache/2.4.57 (Unix)`)
- `ServerTokens Minor` → 세부 버전 포함 (예: `Apache/2.4`)
- **`ServerTokens Prod`** → "Apache"만 표시됨 (**보안 권장**)

## **2. `ServerSignature` 설정 변경**

- `On` → Apache 에러 페이지 및 디렉터리 목록에서 서버 정보 노출 (예: `Apache/2.4.57 (Rocky Linux)`)
- **`Off`** → 서버 정보 숨김 (**보안 권장**)

## 3. `Header unset`을 이용한 추가 정보 제거(미적용)

mod_headers 모듈을 사용하는 방법도 있다고 하는데 해보진 않았다(참고용)
```
/etc/httpd/conf/httpd.conf
...

<IfModule mod_headers.c>
    Header unset Server
    Header always unset X-Powered-By
</IfModule>

```

---
## httpd.conf 수정

```bash
/etc/httpd/conf/httpd.conf

...

# 보안취약점 조치 (apache 정보 표시 제한)
ServerTokens Prod
ServerSignature Off
```


## Apache 재시작

```
# 설정 파일 문법 확인 
sudo apachectl configtest 
# Syntax OK 확인

# Apache 재시작 
sudo systemctl restart httpd
```

![After](/images/2025/02/2025-02-03-rocky Apache vul After.png)
이제 Server 의 출력 값이 Apache로만 나오는 것을 확인할 수 있다.
