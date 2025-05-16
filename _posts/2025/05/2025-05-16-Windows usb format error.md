---
layout: single
title: Windows USB format impossible error(RAW)
categories: OS
tags: [Windows]
toc: False
---

![Windows Disk Partion](/images/2025/05/Windows Disk Partion.png)


리눅스 설치를 위해 포맷을 자주 했었던 USB를 오랜만에 사용하려고 했는데 제대로 인식이 안되고 저런 상태로 나왔습니다.

해당 에러는 cmd를 관리자 권한으로 실행한 이후 아래 명령어를 입력하면 됩니다.
clean까지만 입력하면 gui 포맷 창이 뜨니 거기서 포맷을 해도 상관 없을 것 같습니다.

```
diskpart
list disk
select disk 2 ← USB 번호 확인해서 입력
clean ← 전체 디스크 초기화
create partition primary
format fs=ntfs quick
assign
exit
```
