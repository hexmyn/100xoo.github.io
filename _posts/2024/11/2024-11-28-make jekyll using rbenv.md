---
layout: single
title: 우분투에 brew 설치하기
categories: Linux
tags: ubuntu, brew
toc: True
---

설치환경
Hyper-V
ubuntu-24.04.1-desktop
bash

### **rbenv란?**

`rbenv`는 Ruby 버전 관리 도구입니다. 이를 사용하면 단일 시스템에서 여러 Ruby 버전을 설치하고 관리할 수 있습니다. Ruby 프로젝트마다 다른 Ruby 버전을 필요로 할 때 매우 유용합니다.
비슷하게 rbenv를 포크해서 만든 pyenv가 있습니다.

---

### **rbenv의 주요 특징**
1. **다중 Ruby 버전 관리**:
   - 시스템 전역, 특정 프로젝트, 또는 현재 쉘 세션에서 다른 Ruby 버전을 사용할 수 있습니다.

2. **경량 설계**:
   - 별도의 쉘 실행 환경을 만들지 않고, 심볼릭 링크와 환경 변수(`PATH`)를 활용하여 작동합니다.
   - 다른 도구(예: `rvm`)보다 설정과 실행이 간단합니다.

3. **플러그인 확장**:
   - 기본 기능 외에도 플러그인을 통해 Ruby 빌드 관리(`ruby-build` 등), 버전 자동 전환 등 다양한 기능을 추가할 수 있습니다.

---


## rbenv 설치하기
https://github.com/rbenv/rbenv?tab=readme-ov-file#installation

brew나 apt 등으로 설치 가능하지만 현재 out of date로 인해 git 설치를 추천합니다.
저는 brew로 설치하겠습니다.
brew를 설치하는 방법은 이전 게시물 참고하셔도 괜찮을 것 같아요
(https://jongminlee.me/linux/Install-Brew-On-Linux/)

```
# brew로 rbenv 설치
brew install rbenv
```

### git으로 직접 설치했을 경우(brew나 apt 이외 설치 시)
build environments를 설치해야한다고 합니다.
https://github.com/rbenv/ruby-build/wiki#suggested-build-environment
저는 brew로 설치해서 생략했습니다.

```
# Ubuntu/Debian/Mint
apt-get install autoconf patch build-essential rustc libssl-dev libyaml-dev libreadline6-dev zlib1g-dev libgmp-dev libncurses5-dev libffi-dev libgdbm6 libgdbm-dev libdb-dev uuid-dev

# RHEL/CentOS
dnf install -y autoconf gcc patch bzip2 openssl-devel libffi-devel readline zlib-devel gdbm ncurses-devel tar perl-FindBin

# REHL 9
dnf install -y autoconf gcc patch bzip2 openssl-devel libffi-devel readline zlib-devel gdbm ncurses-devel tar perl-FindBin

# Rocky 9(RHEL 9의 명령에 추가적으로 필요한 것 같음)
dnf --enablerepo=crb install libyaml-devel
```

### **rbenv의 주요 명령어**
- **현재 사용 중인 Ruby 버전 확인**:
  ```bash
  rbenv version
  ```

- **사용 가능한 Ruby 버전 확인**:
  ```bash
  rbenv versions
  ```

- **Ruby 버전 설치** (ruby-build 플러그인 필요):
  ```bash
  rbenv install <version>
  ```

- **프로젝트별 Ruby 버전 설정**:
  ```bash
  rbenv local <version>
  ```

- **전역 Ruby 버전 설정**:
  ```bash
  rbenv global <version>
  ```

- **설치된 Ruby 버전 삭제**:
  ```bash
  rbenv uninstall <version>
  ```

---

### rbenv install

rbenv install -l 으로 stable 버전을 확인
```
rbenv install 3.3.6

rbenv versions

cd $yourprojectdir

rbenv local 3.3.6

rbenv version
# 3.3.6 (set by /home/user/$yourprojectdir/.ruby-version)
```


### install bundler

gem은 ruby의 패키지매니저 같은 개념이고
bundler는 의존성 도구라고 합니다.

```
gem install bundler
```

#### 에러 해결 : zlib 패키지 설치 및 ruby re-install

gem install bundler를 실행했는데
아래와 같은 오류가 났습니다.
zlib이 없어서 나는 오류라고 하네요

```bash
❯ gem install bundler
<internal:/home/mybu/.rbenv/versions/3.3.6/lib/ruby/3.3.0/rubygems/core_ext/kernel_require.rb>:136:in `require': cannot load such file -- zlib (LoadError)
        from <internal:/home/mybu/.rbenv/versions/3.3.6/lib/ruby/3.3.0/rubygems/core_ext/kernel_require.rb>:136:in `require'
        from /home/mybu/.rbenv/versions/3.3.6/lib/ruby/3.3.0/rubygems/util.rb:48:in `inflate'
        from /home/mybu/.rbenv/versions/3.3.6/lib/ruby/3.3.0/rubygems/source.rb:149:in `fetch_spec'
        from /home/mybu/.rbenv/versions/3.3.6/lib/ruby/3.3.0/rubygems/resolver/api_specification.rb:93:in `spec'
        from /home/mybu/.rbenv/versions/3.3.6/lib/ruby/3.3.0/rubygems/resolver/installer_set.rb:99:in `add_always_install'
        from /home/mybu/.rbenv/versions/3.3.6/lib/ruby/3.3.0/rubygems/dependency_installer.rb:318:in `resolve_dependencies'
        from /home/mybu/.rbenv/versions/3.3.6/lib/ruby/3.3.0/rubygems/commands/install_command.rb:198:in `install_gem'
        from /home/mybu/.rbenv/versions/3.3.6/lib/ruby/3.3.0/rubygems/commands/install_command.rb:223:in `block in install_gems'
        from /home/mybu/.rbenv/versions/3.3.6/lib/ruby/3.3.0/rubygems/commands/install_command.rb:216:in `each'
        from /home/mybu/.rbenv/versions/3.3.6/lib/ruby/3.3.0/rubygems/commands/install_command.rb:216:in `install_gems'
        from /home/mybu/.rbenv/versions/3.3.6/lib/ruby/3.3.0/rubygems/commands/install_command.rb:162:in `execute'
        from /home/mybu/.rbenv/versions/3.3.6/lib/ruby/3.3.0/rubygems/command.rb:326:in `invoke_with_build_args'
        from /home/mybu/.rbenv/versions/3.3.6/lib/ruby/3.3.0/rubygems/command_manager.rb:253:in `invoke_command'
        from /home/mybu/.rbenv/versions/3.3.6/lib/ruby/3.3.0/rubygems/command_manager.rb:194:in `process_args'
        from /home/mybu/.rbenv/versions/3.3.6/lib/ruby/3.3.0/rubygems/command_manager.rb:152:in `run'
        from /home/mybu/.rbenv/versions/3.3.6/lib/ruby/3.3.0/rubygems/gem_runner.rb:56:in `run'
        from /home/mybu/.rbenv/versions/3.3.6/bin/gem:12:in `<main>'
```


필요한 패키지를 설치한 후 에러났던 버전을 재설치했습니다.
(재설치 이후 정상적으로 gem이 작동했습니다.)

```
sudo apt install -y zlib1g zlib1g-dev

rbenv uninstall 3.3.6

rbenv install 3.3.6
```

### install jekyll

gemfile이나 gemspec이 있는 프로젝트에선 아래로 넘어가시면 됩니다.

```
gem install jekyll
```

**새로운 Jekyll 프로젝트 생성**

1. **Jekyll 사이트 생성**:
   ```bash
   jekyll new my-blog
   ```

   - `my-blog` 폴더가 생성되며, 기본 Jekyll 파일이 포함됩니다.

2. **프로젝트 디렉터리로 이동**:
   ```bash
   cd my-blog
   ```

3. **의존성 설치**:
   프로젝트 루트에서 Bundler를 사용해 gem 의존성을 설치합니다:
   ```bash
   bundle install
   ```

4. **로컬 서버 실행**:
   ```bash
   bundle exec jekyll serve
   ```

5. **웹사이트 확인**:
   - 브라우저에서 [http://localhost:4000](http://localhost:4000)로 접속하여 결과 확인.


#### gemspec으로 패키지 설치하기
저는 minimal-mistakes를 사용중이여서 gemspec을 이용해서 패키지를 설치했습니다.
https://github.com/mmistakes/minimal-mistakes

gemfile이 없다면 새로 생성합니다.
아래는 저의 gemfile 내용입니다.
```
# Gemfile
source "https://rubygems.org"
gemspecs
gem "webrick", "~> 1.7"
gem "minimal-mistakes-jekyll"%
```

그리고 bundle을 실행합니다.

```
❯ bundle
Fetching gem metadata from https://rubygems.org/...........
Resolving dependencies...
Fetching rake 13.2.1
...
```

gemfile에 정의된 내용으로 필요한 패키지들이 설치됐습니다.


```
bundle exec jekyll serve
```
