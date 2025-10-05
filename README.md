# Shell Commands Lecture Note (Lab 5)

학번: 202432682  
이름: 김민서  

---

## I/O Redirection: Standard Output
- 기본적으로 표준 출력은 화면에 나타남.
- `>` : 명령어 결과를 파일로 저장. (예: `ls > out.txt`)
- `cat` : 텍스트 파일 내용을 출력.
- `>>` : 기존 파일 끝에 결과를 추가(append). 파일이 없으면 새로 생성.

## I/O Redirection: Standard Input
- 기본적으로 표준 입력은 키보드.
- `<` : 파일 내용을 입력으로 사용. (예: `sort < input.txt`)
- `<` 와 `>` 를 같이 쓸 수 있음.

## Pipelines (`|`)
- 파이프라인은 앞 명령어의 출력을 뒤 명령어 입력으로 연결.
- 예: `command1 | command2 | command3`

## Expansion
- 특수 문자들은 쉘에서 특별한 의미로 확장됨.

## Tip: Backslash
- `\` : 긴 명령어를 여러 줄에 입력할 수 있게 함.

## Permissions (권한)
- Linux는 다중 사용자 시스템이며, 파일과 디렉토리에는 소유자/그룹/기타 사용자별 권한이 있음.
- 권한 변경: `chmod`
  - 예: `chmod 600 word.txt` → 소유자는 읽기/쓰기, 나머지는 접근 불가
  - `chmod`는 8진수로 권한을 지정 (예: 6=rw-, 4=r--, 0=---).

## Superuser
- 시스템 전체 권한을 가진 관리자 계정.
- 일부 명령어는 `sudo`가 필요.
- superuser 모드 종료: `exit`

## Text Editors
- CLI 기반: nano, vim 등
- GUI 기반: gedit 등

## Shell Script
- 명령어 모음을 스크립트 파일로 작성하고 실행 가능.
- Windows에서 nano 문제가 있으면 메모장 등 다른 편집기로 작성 후 실행 가능.

## Tip: History
- `history` : 이전에 입력한 명령어 목록 확인.
- `history > file.txt` : 기록을 파일로 저장.

## wget
- 인터넷에서 파일 다운로드. (예: `wget URL`)

## curl
- 인터넷을 통해 데이터 전송, 업로드, 다운로드.  
- 예: `curl [옵션] [URL]`

## grep
- 파일 내 텍스트 검색 도구.
- 예: `grep "search_term" file.txt`
- 주요 옵션:
  - `-i`: 대소문자 구분 없이 검색
  - `-v`: 검색어가 없는 줄 출력
  - `-n`: 줄 번호 함께 출력
  - `-r`: 하위 디렉토리까지 재귀적 검색
- 정규표현식 지원:  
  - `.*` : 0회 이상 임의 문자  
  - `^` : 줄의 시작  
  - `$` : 줄의 끝  

---

## Summary
- 이번 강의에서는 입력/출력 리다이렉션, 파이프라인, 권한, superuser, 편집기, 스크립트, 기록(history), 네트워크 명령어(wget, curl), 텍스트 검색(grep)까지 다룸.
- 시험/실습 대비: 각 명령어 기본 사용법과 옵션 숙지 필수.
