### 마크다운

[마크다운공식]([Markdown Cheat Sheet | Markdown Guide](https://www.markdownguide.org/cheat-sheet/))

### 

# GIT

1. README.md

2. gitignore(깃 다 무시하는거)
   -->이 2개는 레퍼지토리 최상위 파일로 만들고 시작하면 편함

### 명령어

git config --global user.email "~@.com"

git config --global user.name "name"

git config --list

cd . . ->상위 폴더로 이동
cd 원하는 폴더

### 로컬저장소

Repository 생성 : `git init`

변경사항 stage 에 추가 : `git add 파일이름 |(스페이스) .`

변경사항 commit : `git commit -m "commit message"`

git 상태 확인 : `git status`

git 커밋 로그 확인 : `git log [--oneline]`

원격저장소 추가 : `git remote add {저장소이름} {원격저장소url}`

`` ex) `git remote add origin https://lab.ssafy.com/s12/d02/gumi02.git` ``

### 원격저장소

원격 저장소 로컬 컴퓨터에 복사 : `git clone 원격저장소 url .`

원격 저장소 업데이트 내용 로컬 컴퓨터로 당겨오기 :

`git pull {원격저장소이름} {브랜치 이름}` ex) `git pull origin master`

로컬 컴퓨터 업데이트 내용 원격저장소로 업로드 :

`git push {원격저장소이름} {브랜치 이름}` ex) `git push origin master`





- 커밋 메시지 적다가 이상한 화면 뜸
  esc -> i -> 변경사항 작성 -> esc -> :wq(저장하고 종료) / :q!(강제종료)

- 원격 저장소를 로컬 컴퓨터(집)에 복사하기
1. 로컬 컴퓨터(집)에 빈폴더 생성
2. 깃 배쉬 열기
3. git clone https://lab.ssafy.com/s12/d02/gumi02.git .
- 원격 저장소에 변경된 내용을 로컬 저장소(집)에 다운받기
  git pull origin master

- 로컬 저장소(집) 내용을 원격 저장소에 올리기
  git remote add origin https://lab.ssafy.com/chaeyong0320/til.git
  git push origin master

- 강의장 컴터에서 원격 저장소에 올리기
  git add .
  git commit -m ""
  git push origin master

- 집에서 원격 저장소 연결하기
  git clone 주소

- 집에서 한 내용 강의장에서 보기
  ---집---
  git add .
  git commit -m "" -->집 컴터에 저장됨
  git push origin master
  --강의장--
  git pull origin master
  
  꼭 커밋하고 푸시해야함! 푸시 안하고 다른 로컬에서 푸시하면 충돌!



- **자료랑 강사님 자료랑 충돌나면 원래 깃 폴더 버리고 새로 만들어서 깃 클론하고
  강사님거 받음됨 
  아니면 충돌난 파일 일일히 수정하고 다시 푸시하면 됨