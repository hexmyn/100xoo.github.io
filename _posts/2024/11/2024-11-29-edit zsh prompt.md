---
layout: single
title: zsh 프롬프트 수정(ohmyzsh)
categories: Linux
tags: zsh
toc: True
---

ubuntu 24.04.1
zsh
ohmyzsh

현재 ohmyzsh의 agnoster 테마를 사용 중인데 불필요한 부분을 수정하려고 합니다.
chatgpt에 물어보니 몇가지 방법을 알려주니 참고하면 좋을 것 같아요.
저는 2번 방법의 Powerlevel10k을 설치하고 ohmyzsh에서 테마를 변경하여 진행했습니다.

---

### 방법 1: 기본 테마 변경

#### 1. **현재 테마 확인**
`~/.zshrc` 파일에서 사용 중인 테마를 확인합니다.

```bash
nano ~/.zshrc
```

- `ZSH_THEME` 항목을 찾습니다. 예:
  ```bash
  ZSH_THEME="robbyrussell"
  ```

#### 2. **테마 변경**
테마를 변경하려면 다른 테마 이름으로 수정한 후 Zsh를 재로드
ex:
```bash
ZSH_THEME="agnoster"
```

Zsh 재로드:
```bash
source ~/.zshrc
```

---

### 방법 2: 프롬프트 사용자 정의 (Powerlevel10k 추천)

#### 1. **Powerlevel10k 설치 (추천 테마)**

Powerlevel10k는 강력한 커스터마이징 옵션을 제공하는 테마입니다.

```bash
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/themes/powerlevel10k
```

`~/.zshrc` 파일에서 테마를 `powerlevel10k/powerlevel10k`로 변경합니다:
```bash
ZSH_THEME="powerlevel10k/powerlevel10k"
```

Zsh를 재로드한 후 설정 마법사를 실행합니다:
```bash
source ~/.zshrc
```

마법사에서 `user@machine` 표시 여부를 설정할 수 있습니다.

#### 2. **Powerlevel10k 설정 파일 수동 수정**
`~/.p10k.zsh` 파일에서 `user@machine` 관련 항목을 수정하거나 비활성화합니다:
```bash
typeset -g POWERLEVEL9K_LEFT_PROMPT_ELEMENTS=(context dir vcs)
```
- `context`: 사용자 및 호스트 정보를 제어합니다.
- 제거하려면 배열에서 `context`를 삭제합니다.


저는 LEFT가 아니라 RIGHT에 존재하는 user@hostname과 관련된 element인 context를 주석처리했습니다.

```
# my ~/.p10k.zsh
  # The list of segments shown on the left. Fill it with the most important segments.
  typeset -g POWERLEVEL9K_LEFT_PROMPT_ELEMENTS=(
    # =========================[ Line #1 ]=========================
    # os_icon               # os identifier
    dir                     # current directory
    vcs                     # git status
    # =========================[ Line #2 ]=========================
    newline                 # \n
    prompt_char             # prompt symbol
  )
  
typeset -g POWERLEVEL9K_RIGHT_PROMPT_ELEMENTS=(
    # =========================[ Line #1 ]=========================
    status                  # exit code of the last command
    command_execution_time  # duration of the last command
	...
    #  context                 # user@hostname
)
```

수정이 완료되면 zsh 재실행

```bash
source ~/.zshrc
```
---

직접 zshrc를 수정하는 방식인데 powerlevel10k를 사용하고 있어서 따로 안건드렸습니다.


### 방법 3: 기존 테마에서 프롬프트 직접 수정

#### 1. **프롬프트 관련 설정**
Zsh 프롬프트는 `$PROMPT`와 `$RPROMPT` 변수로 구성됩니다.

- `$PROMPT`: 왼쪽 프롬프트
- `$RPROMPT`: 오른쪽 프롬프트

#### 2. **커스터마이징**
`~/.zshrc` 파일에 직접 설정을 추가합니다. 예:

- `user@machine` 제거:
  ```bash
  PROMPT='%1~ %# '
  ```
  - `%1~`: 현재 디렉터리
  - `%#`: 일반 사용자 `$`, 루트 사용자 `#`

- 사용자 이름과 호스트명을 변경:
  ```bash
  PROMPT='[custom_user@custom_machine] %1~ %# '
  ```

#### 3. **Zsh 재로드**
```bash
source ~/.zshrc
```

---

powerlevel10k를 사용하지 않고 ohmyzsh의 theme 파일을 직접 수정할 수 있습니다.
기존 테마파일을 복사해서 수정하는게 좋을 것 같습니다.

### 방법 4: 테마 파일 직접 수정

Oh My Zsh의 테마 파일을 수정하여 프롬프트를 변경할 수도 있습니다.

#### 1. **사용 중인 테마 파일 열기**
테마 파일은 `~/.oh-my-zsh/themes/` 디렉터리에 있습니다. 사용 중인 테마를 확인한 뒤 해당 파일을 수정합니다.

예:
```bash
nano ~/.oh-my-zsh/themes/robbyrussell.zsh-theme
```

#### 2. **`PROMPT` 또는 `RPROMPT` 수정**
예를 들어, `PROMPT`를 아래와 같이 변경할 수 있습니다:
```bash
PROMPT='[custom_user@custom_machine] %~ %# '
```

#### 3. **Zsh 재로드**
```bash
source ~/.zshrc
```

---

### 추가 팁

1. **프롬프트 동적 변경**:
   프롬프트를 동적으로 변경하려면 `PROMPT`에 조건문을 추가합니다. 예:
   ```bash
   if [[ $USER == "root" ]]; then
       PROMPT='[root@%m] %~ %# '
   else
       PROMPT='[user@%m] %~ %# '
   fi
   ```

2. **`context`만 표시 변경**:
   Powerlevel10k를 사용하는 경우, `context` 설정을 조정하여 사용자와 호스트 표시를 변경할 수 있습니다:
   ```bash
   typeset -g POWERLEVEL9K_CONTEXT_TEMPLATE='custom_user@custom_machine'
   ```

---

