---
layout: single
title: PARA Folder Structure
categories: Productivity
tags: methodology
toc: True
---

제텔카스텐과 관련된 내용을 종종 찾아보다가 알게 된 PARA 기법을 obsidian에서 사용해보려고 한다.

## 1.기본 PARA 폴더 구조 (예시)

`Vault(or Root Folder)`
 `├── 10_Projects`
 `│    ├── ProjectA_웹사이트개발`
 `│    ├── ProjectB_논문작성`
 `│    └── ProjectC_이벤트준비`
 `│`
 `├── 20_Areas`
 `│    ├── Health (운동, 식단, 건강검진 등)`
 `│    ├── Finance (가계부, 투자, 보험 등)`
 `│    ├── Career (이력, 학습 계획 등)`
 `│    └── Family (가족 일정, 가계 약속 등)`
 `│`
 `├── 30_Resources`
 `│    ├── Programming (언어별 자료, 참고 노트)`
 `│    ├── Writing (글쓰기 팁, 작문 자료)`
 `│    ├── Books (독서 메모, 독후감)`
 `│    └── Etc (기타 관심 주제)`
 `│`
 `└── 40_Archive`
      `├── (완료된 프로젝트)`  
      `│    ├── ProjectA_2023_웹사이트개발`
      `│    └── ...`
      `├── (휴면 상태 Areas)`  
      `└── (구버전 Resources 등)`

---
### 1) Projects 폴더

- 기한이나 목표가 명확한 작업(진행 중인 것만)
- 예: “ProjectA_웹사이트개발”, “ProjectB_논문작성”, “프로그램 런칭 이벤트 준비” 등
- 보통 프로젝트별 서브폴더(자료·문서·노트 등)를 둠
- 프로젝트가 끝나면 해당 폴더 전체를 Archive 폴더로 옮겨 보관

### 2) Areas 폴더

- 지속적으로 관리가 필요한 영역(끝나는 시점이 없는 항목)
- 예: Health, Finance, Career, Family, Hobby 등
- 프로젝트처럼 매일 신경 쓸 필요는 없지만, 관심이 사라지면 문제가 생길 수 있는 “책임 영역”
- 영역 내 정보가 늘어나면, 필요에 따라 세부 서브폴더를 추가 가능 (예: Finance 내부에 회계·세무, 투자 등)

### 3) Resources 폴더

- 주제 또는 관심사별 참고 자료를 모아두는 곳
- 특정 목적·기한이 없지만 “언젠가 쓸만한” 지식, 정보, 기사, 책 메모 등
- 예: Programming, Writing, Books, Cooking, Travel 등
- 필요하면 더 세분화해도 되지만, “최소한의 주제 구분”만 해두면 관리가 쉬움

### 4) Archive 폴더

- 현재는 필요 없는 자료
    - 예: 완료된 프로젝트, 관심이 떨어진 리소스, 당분간 보지 않을 영역 등
- 완전히 삭제하지 않고 이 폴더에 보관해두었다가, 다시 필요해지면 꺼내어 사용 가능
- Projects나 Areas, Resources 폴더에서 휴면 상태로 전환될 때 이동

---

## 2. 선택적으로 추가할 폴더

### (a) Inbox / Temp

- 임시 보관함(Inbox) 역할을 하는 폴더
- 아직 어디로 옮겨야 할지 결정 못한 노트를 임시로 두는 장소
- 노트가 쌓이면, 주기적으로 PARA 4폴더 중 하나로 옮겨 정리

### (b) Templates

- 자주 쓰는 템플릿(Front Matter, Markdown 양식 등)을 넣어두는 폴더
- Obsidian이나 Zettlr 같은 툴에서 템플릿 관리를 지원하면, 전용 폴더를 만들어두면 편함

### (c) References / Literature

- 학술·논문, 참고문헌 등이 많은 경우 유용
- Resources 내부에 서브폴더로 두거나, 별도 References라는 상위 폴더를 만들어 관리하기도 함
- “일반 리소스”와 “학술 자료”를 구분해 두면 관리가 편해짐

---

## 3. 유지·운용 팁

- **핵심 질문**: 노트가 “언제, 어떻게, 왜 필요해질까?”
    
    - **Projects**: 단기 목표 달성을 위한 자료
    - **Areas**: 장기 책임이 있는 영역
    - **Resources**: 참고용 데이터 (필수는 아님)
    - **Archive**: 지금은 필요 없지만 버리긴 아까운 자료
      
- **노트의 용도 변화 예시**
    
    - 리소스가 프로젝트에 필요해지면 → Projects 폴더로 이동 (또는 링크)
    - 프로젝트가 끝나면 → Archive로 이동
    - 예전에는 꾸준히 관리했지만 지금은 안 쓰는 영역 → Archive로 이동
- **가급적 ‘최소한의’ 하위 폴더만 사용**
    
    - PARA의 본래 목적은 “복잡한 폴더 분류”를 줄이고 목적별로 단순화하려는 것
    - 너무 세부적으로 폴더를 쪼개기보다는, 필요할 때 그때 추가해도 늦지 않음
- **백링크, 태그 적극 활용 (특히 Obsidian 등)**
    
    - 폴더가 달라도 노트 간 링크·태그로 쉽게 연결 가능
- **정기 점검**
    
    - 한 달 또는 분기별로 “Projects가 너무 많지 않은지?”, “완료된 프로젝트를 Archive로 옮길지?”를 확인
    - PARA 구조를 깔끔하게 유지하는 데 도움이 됨

---

## 4. 마무리

위 예시는 가장 일반적인 PARA 폴더 구조지만, 사람마다 다르게 구성해도 문제 없음.  
중요한 것은 **폴더 구조가 복잡해지지 않도록 단순함을 유지**하고,  
**필요에 따라 노트를 자유롭게 이동**시키는 PARA의 원칙을 지키는 것.

> **핵심 요약**
> 
> - **Projects**: 현재 진행 중(또는 곧 시작할) 목표·기한이 있는 작업
> - **Areas**: 장기적으로 돌봐야 하는 책임·영역
> - **Resources**: 필요할 때 참고 가능한 데이터·정보 저장소
> - **Archive**: 더는 활성 상태가 아닌 자료를 보관하는 폴더

---
## 참고 스크립트(PARA 예시 구조 폴더 생성)

### Bash(Linux, Mac)
create_para_structure.sh
chmod +x create_para_structure.sh
./create_para_structure.sh
```
#!/usr/bin/env bash

# 0. 최상위 폴더를 "PARA_Vault"라고 가정 (원하시면 다른 이름으로 바꾸세요)
#    그리고 그 안에 폴더들을 만들겠습니다.
mkdir -p PARA_Vault
cd PARA_Vault

###############################################################################
# 1. Inbox (임시 보관함)
###############################################################################
mkdir -p 01_Inbox

cat <<EOF > 01_Inbox/DraftNotes.md
# Draft Notes
이곳은 임시 작성 노트 모음입니다.
EOF

cat <<EOF > 01_Inbox/Idea_Sketches.md
# Idea Sketches
이곳은 아이디어 스케치/메모입니다.
EOF

cat <<EOF > 01_Inbox/TempLinks.md
# Temporary Links
임시로 저장한 링크 목록을 보관합니다.
EOF


###############################################################################
# 2. Projects (10_Projects)
###############################################################################
mkdir -p 10_Projects/ProjectA_BlogRedesign/{01_Research,02_Planning,03_Execution,04_Deliverables}
mkdir -p 10_Projects/ProjectB_AppDevelopment/{01_Requirements,02_Design,03_Implementation,04_Testing}
mkdir -p 10_Projects/ProjectC_ConferencePreparation

# 예시 파일들 추가
cat <<EOF > 10_Projects/ProjectA_BlogRedesign/01_Research/CompetitorAnalysis.md
# Competitor Analysis
- 경쟁사 사이트 분석 내용...
EOF

cat <<EOF > 10_Projects/ProjectA_BlogRedesign/01_Research/DesignTrends2024.md
# 2024 Design Trends
- 2024년 디자인 트렌드 조사...
EOF

cat <<EOF > 10_Projects/ProjectA_BlogRedesign/02_Planning/ProjectScope.md
# Project Scope
- 블로그 리디자인 범위 정의...
EOF

cat <<EOF > 10_Projects/ProjectA_BlogRedesign/02_Planning/TaskBreakdown.md
# Task Breakdown
- 주요 작업 항목 리스트...
EOF

cat <<EOF > 10_Projects/ProjectA_BlogRedesign/03_Execution/ContentDrafts.md
# Content Drafts
- 작성할 텍스트 초안...
EOF

cat <<EOF > 10_Projects/ProjectA_BlogRedesign/03_Execution/VisualAssets.md
# Visual Assets
- 로고, 컬러팔레트, 이미지 자료...
EOF

cat <<EOF > 10_Projects/ProjectA_BlogRedesign/04_Deliverables/FinalMockup.md
# Final Mockup
- 최종 목업 및 산출물 설명...
EOF

cat <<EOF > 10_Projects/ProjectB_AppDevelopment/01_Requirements/SystemRequirements.md
# System Requirements
- 앱 개발 요구사항 정리...
EOF

cat <<EOF > 10_Projects/ProjectB_AppDevelopment/02_Design/AppDesign.md
# App Design
- UI/UX 구조...
EOF


###############################################################################
# 3. Areas (20_Areas)
###############################################################################
mkdir -p 20_Areas/{Career,Finance,Health,Family,Hobby}

# Career 서브폴더
mkdir -p 20_Areas/Career/{01_Resume,02_Professional_Development,03_Meeting_Notes,04_Goals}
cat <<EOF > 20_Areas/Career/01_Resume/Resume_2024.md
# Resume (2024)
- 이력서 초안...
EOF
cat <<EOF > 20_Areas/Career/02_Professional_Development/CoursesToTake.md
# Courses To Take
- 수강 예정/희망 강의 리스트...
EOF
cat <<EOF > 20_Areas/Career/04_Goals/YearlyCareerGoals.md
# Yearly Career Goals
- 연간 커리어 목표...
EOF

# Finance 서브폴더
mkdir -p 20_Areas/Finance/{01_Budget,02_Investments,03_Taxes,04_Insurance}
cat <<EOF > 20_Areas/Finance/01_Budget/2024_Budget_Planning.md
# 2024 Budget Planning
- 올해 예산 계획...
EOF
cat <<EOF > 20_Areas/Finance/02_Investments/Stock_Portfolio.md
# Stock Portfolio
- 주식 보유 현황...
EOF

# Health, Family, Hobby 등은 간단 예시만
cat <<EOF > 20_Areas/Health/Workout_Routines.md
# Workout Routines
- 운동 루틴 정리...
EOF

cat <<EOF > 20_Areas/Family/FamilyCalendar.md
# Family Calendar
- 가족 일정 관리...
EOF

cat <<EOF > 20_Areas/Hobby/Guitar.md
# Guitar
- 기타 연습 노트...
EOF


###############################################################################
# 4. Resources (30_Resources)
###############################################################################
mkdir -p 30_Resources/{Programming,Writing,Books,Languages,Travel}

# Programming 서브폴더
mkdir -p 30_Resources/Programming/{01_Python,02_JavaScript,03_SQL,04_DevOps}
cat <<EOF > 30_Resources/Programming/01_Python/PythonBasics.md
# Python Basics
- 파이썬 기초 문법, 예제...
EOF
cat <<EOF > 30_Resources/Programming/01_Python/PythonDataScience.md
# Python for Data Science
- 데이터 사이언스용 라이브러리...
EOF
cat <<EOF > 30_Resources/Programming/03_SQL/SQLCheatsheet.md
# SQL Cheatsheet
- SQL 구문 요약...
EOF

# Writing
mkdir -p 30_Resources/Writing
cat <<EOF > 30_Resources/Writing/Writing_Tips.md
# Writing Tips
- 글쓰기 팁 모음...
EOF

# Books
mkdir -p 30_Resources/Books/01_Summary_Reviews
cat <<EOF > 30_Resources/Books/01_Summary_Reviews/Book_DeepWork_Review.md
# [독후감] 딥 워크 (Deep Work)
- 핵심 내용, 소감...
EOF

# Languages
mkdir -p 30_Resources/Languages/{English,Chinese,Spanish}
cat <<EOF > 30_Resources/Languages/English/EnglishPractice.md
# English Practice
- 영어 표현, 문법 정리...
EOF

# Travel
mkdir -p 30_Resources/Travel/{Seoul,Tokyo,Paris,London}
cat <<EOF > 30_Resources/Travel/Seoul/SeoulFoodGuide.md
# Seoul Food Guide
- 서울 맛집 리스트...
EOF


###############################################################################
# 5. Archive (40_Archive)
###############################################################################
mkdir -p 40_Archive/{Projects_Completed,Areas_Inactive,Resources_Old}

cat <<EOF > 40_Archive/ArchiveReadme.md
# Archive
현재는 활성 상태가 아닌 자료를 보관하는 폴더입니다.
EOF


###############################################################################
# 6. Templates (99_Templates)
###############################################################################
mkdir -p 99_Templates

cat <<EOF > 99_Templates/TPL_ProjectKickoff.md
---
title: "Project Kickoff Template"
date: 2024-01-01
---
# [프로젝트 이름] Kickoff

## 목적
- ...

## 범위
- ...

## 일정
- ...
EOF

cat <<EOF > 99_Templates/TPL_MeetingMinutes.md
---
title: "Meeting Minutes"
date: 2024-01-01
---
# 회의록 템플릿

- 일시:
- 참석자:

## 주요 안건
1. ...
2. ...

## 결정사항
- ...
EOF

echo "모든 폴더와 파일이 생성되었습니다!"
```

### PowerShell(Windows)
1. 메모장(또는 VSCode)에서 새 파일을 열어, 아래 코드 전체를 그대로 복사/붙여넣기
2. 메뉴 [다른 이름으로 저장] → 인코딩을 UTF-8 with BOM(VSCode에서는 “UTF-8 with BOM” 또는 “UTF-8 (BOM 포함)”)으로 지정
3. 파일명을 create_para_structure.ps1로 저장
4. PowerShell 열기
(필요 시) Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
5. 스크립트 위치로 이동 (예: cd C:\Scripts\)
6. .\create_para_structure.ps1 실행
7. “=== PARA 폴더구조 생성 완료! ===” 메시지 확인
	
```
# --------------------------------------------
# create_para_structure.ps1
# PowerShell script to create a PARA folder structure
# --------------------------------------------

# (선택) 콘솔 출력 인코딩을 UTF-8로 설정
[Console]::OutputEncoding = [System.Text.Encoding]::UTF8

# PowerShell 내장 기본 출력 인코딩
$PSDefaultParameterValues['Out-File:Encoding'] = 'UTF8'

Write-Host "=== PARA 폴더구조 생성 시작 (UTF-8) ==="

# 0. 상위 폴더 (PARA_Vault) 만들고 이동
New-Item -ItemType Directory -Name "PARA_Vault" -Force | Out-Null
Set-Location ".\PARA_Vault"

#---------------------------
# 1. Inbox (01_Inbox)
#---------------------------
New-Item -ItemType Directory "01_Inbox" -Force | Out-Null

Set-Content -Path ".\01_Inbox\DraftNotes.md" -Encoding UTF8 -Value "# Draft Notes`r`n이곳은 임시 작성 노트 모음입니다."
Set-Content -Path ".\01_Inbox\Idea_Sketches.md" -Encoding UTF8 -Value "# Idea Sketches`r`n이곳은 아이디어 스케치/메모입니다."
Set-Content -Path ".\01_Inbox\TempLinks.md" -Encoding UTF8 -Value "# Temporary Links`r`n임시로 저장한 링크 목록을 보관합니다."

#---------------------------
# 2. Projects (10_Projects)
#---------------------------
New-Item -ItemType Directory "10_Projects" -Force | Out-Null

# ProjectA_BlogRedesign
New-Item -ItemType Directory ".\10_Projects\ProjectA_BlogRedesign" -Force | Out-Null
New-Item -ItemType Directory ".\10_Projects\ProjectA_BlogRedesign\01_Research" -Force | Out-Null
New-Item -ItemType Directory ".\10_Projects\ProjectA_BlogRedesign\02_Planning" -Force | Out-Null
New-Item -ItemType Directory ".\10_Projects\ProjectA_BlogRedesign\03_Execution" -Force | Out-Null
New-Item -ItemType Directory ".\10_Projects\ProjectA_BlogRedesign\04_Deliverables" -Force | Out-Null

Set-Content -Path ".\10_Projects\ProjectA_BlogRedesign\01_Research\CompetitorAnalysis.md" -Encoding UTF8 -Value "# Competitor Analysis`r`n- 경쟁사 사이트 분석 내용..."
Set-Content -Path ".\10_Projects\ProjectA_BlogRedesign\01_Research\DesignTrends2024.md" -Encoding UTF8 -Value "# 2024년 디자인 트렌드 조사`r`n- 최신 UI/UX 참고 자료..."

Set-Content -Path ".\10_Projects\ProjectA_BlogRedesign\02_Planning\ProjectScope.md" -Encoding UTF8 -Value "# Project Scope`r`n- 블로그 리디자인 범위 정의..."
Set-Content -Path ".\10_Projects\ProjectA_BlogRedesign\02_Planning\TaskBreakdown.md" -Encoding UTF8 -Value "# Task Breakdown`r`n- 주요 작업 항목 리스트..."

Set-Content -Path ".\10_Projects\ProjectA_BlogRedesign\03_Execution\ContentDrafts.md" -Encoding UTF8 -Value "# Content Drafts`r`n- 작성할 텍스트 초안..."
Set-Content -Path ".\10_Projects\ProjectA_BlogRedesign\03_Execution\VisualAssets.md" -Encoding UTF8 -Value "# Visual Assets`r`n- 로고, 컬러 팔레트, 이미지 자료..."

Set-Content -Path ".\10_Projects\ProjectA_BlogRedesign\04_Deliverables\FinalMockup.md" -Encoding UTF8 -Value "# Final Mockup`r`n- 최종 목업 및 산출물 설명..."

# ProjectB_AppDevelopment
New-Item -ItemType Directory ".\10_Projects\ProjectB_AppDevelopment" -Force | Out-Null
New-Item -ItemType Directory ".\10_Projects\ProjectB_AppDevelopment\01_Requirements" -Force | Out-Null
New-Item -ItemType Directory ".\10_Projects\ProjectB_AppDevelopment\02_Design" -Force | Out-Null
New-Item -ItemType Directory ".\10_Projects\ProjectB_AppDevelopment\03_Implementation" -Force | Out-Null
New-Item -ItemType Directory ".\10_Projects\ProjectB_AppDevelopment\04_Testing" -Force | Out-Null

Set-Content -Path ".\10_Projects\ProjectB_AppDevelopment\01_Requirements\SystemRequirements.md" -Encoding UTF8 -Value "# System Requirements`r`n- 앱 개발 요구사항 정리..."
Set-Content -Path ".\10_Projects\ProjectB_AppDevelopment\02_Design\AppDesign.md" -Encoding UTF8 -Value "# App Design`r`n- UI/UX 구조..."

# ProjectC_ConferencePreparation
New-Item -ItemType Directory ".\10_Projects\ProjectC_ConferencePreparation" -Force | Out-Null


#---------------------------
# 3. Areas (20_Areas)
#---------------------------
New-Item -ItemType Directory "20_Areas" -Force | Out-Null

# Career
New-Item -ItemType Directory ".\20_Areas\Career" -Force | Out-Null
New-Item -ItemType Directory ".\20_Areas\Career\01_Resume" -Force | Out-Null
New-Item -ItemType Directory ".\20_Areas\Career\02_Professional_Development" -Force | Out-Null
New-Item -ItemType Directory ".\20_Areas\Career\03_Meeting_Notes" -Force | Out-Null
New-Item -ItemType Directory ".\20_Areas\Career\04_Goals" -Force | Out-Null

Set-Content -Path ".\20_Areas\Career\01_Resume\Resume_2024.md" -Encoding UTF8 -Value "# Resume (2024)`r`n- 이력서 초안..."
Set-Content -Path ".\20_Areas\Career\02_Professional_Development\CoursesToTake.md" -Encoding UTF8 -Value "# Courses To Take`r`n- 수강 예정/희망 강의 리스트..."
Set-Content -Path ".\20_Areas\Career\04_Goals\YearlyCareerGoals.md" -Encoding UTF8 -Value "# Yearly Career Goals`r`n- 연간 커리어 목표..."

# Finance
New-Item -ItemType Directory ".\20_Areas\Finance" -Force | Out-Null
New-Item -ItemType Directory ".\20_Areas\Finance\01_Budget" -Force | Out-Null
New-Item -ItemType Directory ".\20_Areas\Finance\02_Investments" -Force | Out-Null
New-Item -ItemType Directory ".\20_Areas\Finance\03_Taxes" -Force | Out-Null
New-Item -ItemType Directory ".\20_Areas\Finance\04_Insurance" -Force | Out-Null

Set-Content -Path ".\20_Areas\Finance\01_Budget\2024_Budget_Planning.md" -Encoding UTF8 -Value "# 2024 Budget Planning`r`n- 올해 예산 계획..."
Set-Content -Path ".\20_Areas\Finance\02_Investments\Stock_Portfolio.md" -Encoding UTF8 -Value "# Stock Portfolio`r`n- 주식 보유 현황..."

# Health
New-Item -ItemType Directory ".\20_Areas\Health" -Force | Out-Null
Set-Content -Path ".\20_Areas\Health\Workout_Routines.md" -Encoding UTF8 -Value "# Workout Routines`r`n- 운동 루틴 정리..."

# Family
New-Item -ItemType Directory ".\20_Areas\Family" -Force | Out-Null
Set-Content -Path ".\20_Areas\Family\FamilyCalendar.md" -Encoding UTF8 -Value "# Family Calendar`r`n- 가족 일정 관리..."

# Hobby
New-Item -ItemType Directory ".\20_Areas\Hobby" -Force | Out-Null
Set-Content -Path ".\20_Areas\Hobby\Guitar.md" -Encoding UTF8 -Value "# Guitar`r`n- 기타 연습 노트..."


#---------------------------
# 4. Resources (30_Resources)
#---------------------------
New-Item -ItemType Directory "30_Resources" -Force | Out-Null

# Programming
New-Item -ItemType Directory ".\30_Resources\Programming" -Force | Out-Null
New-Item -ItemType Directory ".\30_Resources\Programming\01_Python" -Force | Out-Null
New-Item -ItemType Directory ".\30_Resources\Programming\02_JavaScript" -Force | Out-Null
New-Item -ItemType Directory ".\30_Resources\Programming\03_SQL" -Force | Out-Null
New-Item -ItemType Directory ".\30_Resources\Programming\04_DevOps" -Force | Out-Null

Set-Content -Path ".\30_Resources\Programming\01_Python\PythonBasics.md" -Encoding UTF8 -Value "# Python Basics`r`n- 파이썬 기초 문법, 예제..."
Set-Content -Path ".\30_Resources\Programming\01_Python\PythonDataScience.md" -Encoding UTF8 -Value "# Python for Data Science`r`n- 데이터 사이언스용 라이브러리..."
Set-Content -Path ".\30_Resources\Programming\03_SQL\SQLCheatsheet.md" -Encoding UTF8 -Value "# SQL Cheatsheet`r`n- SQL 구문 요약..."

# Writing
New-Item -ItemType Directory ".\30_Resources\Writing" -Force | Out-Null
Set-Content -Path ".\30_Resources\Writing\Writing_Tips.md" -Encoding UTF8 -Value "# Writing Tips`r`n- 글쓰기 팁 모음..."

# Books
New-Item -ItemType Directory ".\30_Resources\Books" -Force | Out-Null
New-Item -ItemType Directory ".\30_Resources\Books\01_Summary_Reviews" -Force | Out-Null

Set-Content -Path ".\30_Resources\Books\01_Summary_Reviews\Book_DeepWork_Review.md" -Encoding UTF8 -Value "# [독후감] 딥 워크 (Deep Work)`r`n- 핵심 내용, 소감..."

# Languages
New-Item -ItemType Directory ".\30_Resources\Languages" -Force | Out-Null
New-Item -ItemType Directory ".\30_Resources\Languages\English" -Force | Out-Null
New-Item -ItemType Directory ".\30_Resources\Languages\Chinese" -Force | Out-Null
New-Item -ItemType Directory ".\30_Resources\Languages\Spanish" -Force | Out-Null

Set-Content -Path ".\30_Resources\Languages\English\EnglishPractice.md" -Encoding UTF8 -Value "# English Practice`r`n- 영어 표현, 문법 정리..."

# Travel
New-Item -ItemType Directory ".\30_Resources\Travel" -Force | Out-Null
New-Item -ItemType Directory ".\30_Resources\Travel\Seoul" -Force | Out-Null
New-Item -ItemType Directory ".\30_Resources\Travel\Tokyo" -Force | Out-Null
New-Item -ItemType Directory ".\30_Resources\Travel\Paris" -Force | Out-Null
New-Item -ItemType Directory ".\30_Resources\Travel\London" -Force | Out-Null

Set-Content -Path ".\30_Resources\Travel\Seoul\SeoulFoodGuide.md" -Encoding UTF8 -Value "# Seoul Food Guide`r`n- 서울 맛집 리스트..."


#---------------------------
# 5. Archive (40_Archive)
#---------------------------
New-Item -ItemType Directory "40_Archive" -Force | Out-Null
New-Item -ItemType Directory ".\40_Archive\Projects_Completed" -Force | Out-Null
New-Item -ItemType Directory ".\40_Archive\Areas_Inactive" -Force | Out-Null
New-Item -ItemType Directory ".\40_Archive\Resources_Old" -Force | Out-Null

Set-Content -Path ".\40_Archive\ArchiveReadme.md" -Encoding UTF8 -Value "# Archive`r`n현재는 활성 상태가 아닌 자료를 보관하는 폴더입니다."


#---------------------------
# 6. Templates (99_Templates)
#---------------------------
New-Item -ItemType Directory "99_Templates" -Force | Out-Null

Set-Content -Path ".\99_Templates\TPL_ProjectKickoff.md" -Encoding UTF8 -Value @"
---
title: "Project Kickoff Template"
date: 2024-01-01
---
# [프로젝트 이름] Kickoff

## 목적
- ...

## 범위
- ...

## 일정
- ...
"@

Set-Content -Path ".\99_Templates\TPL_MeetingMinutes.md" -Encoding UTF8 -Value @"
---
title: "Meeting Minutes"
date: 2024-01-01
---
# 회의록 템플릿

- 일시:
- 참석자:

## 주요 안건
1. ...
2. ...

## 결정사항
- ...
"@

Write-Host "=== PARA 폴더구조 생성 완료! ==="
Write-Host "폴더: PARA_Vault"

```
