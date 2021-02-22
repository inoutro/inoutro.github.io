---
layout: post
comments: true
title: Git command 정리
categories: [Dev]

---

# Github 명령어 정리

git을 통해 작업을 할 때 주로 사용하는 명령어를 기억하기 위해 정리한 포스팅

해당 포스팅은 앞으로도 git을 통해 작업을 진행하면서 업데이트하기

1. Git 초기 세팅
   - git config --global user.name "John Doe"
   - git config --global user.email johndoe@example.com
2. clone
   - git clone "해당 github repository HTTPS" : 작업하고자 하는 repository를 local로 복제하기
3. branch 사용 : branch는 일종의 가지치기로 현재 master의 내용을 가져와서 작업할 수 있는 공간을 만들어줌
   - git branch : 로컬에 있는 branch 확인 및 내가 사용하고 있는 branch 확인
   - git branch -r : 원격에 존재하는 branch list 확인
   - git branch -a : 로컬, 원격 branch 모두 확인
   - git branch "이름" : 해당 이름으로 branch 생성
   - git branch -d "이름" : 해당 이름의 branch 삭제
4. checkout 사용 : branch 간 이동할 때 사용하는 명령어 (방을 checkout 하다..?)
   - git checkout "이름" : 해당 이름의 branch로 이동
   - git checkout -t "원격 저장소 branch 이름" : 원격 저장소 branch를 로컬에 생성하면서 해당 branch로 checkout(이동)
   - git checkout -b "생성할 이름" "원격 저장소 branch 이름" : 원격 저장소 branch를 로컬에 생성할 이름을 지정해서 해당 branch로 checkout
5. pull / fetch : 원격에 변경된 내용을 내 로컬에 업데이트 하는건데, pull을 주로 사용해서, fetch와의 차이 나중에 확인해보기
   - git pull : 원격에 업데이트된 내용을 내 로컬에 업데이트하여 merge
   - git fetch : 원격에 업데이트된 내용을 내 로컬에 업데이트
6. status
   - git status : 현재 local에서 변화된 내용이 있는지 확인할 수 있는 명령어
7. add - commit - push
   - git add "파일 명" : 작업한 내용을 커밋하기 위한 목록에 추가하는 작업
     (git status를 통해 작업한 내용이 빨간색으로 표시된 것을 볼 수 있고, 해당 파일을 add하면 commit할 수 있도록 초록색 글씨로 변함)
   - git commit -m "메시지" : add하여 commit 목록에 올라간 파일을 commit하여서 작업 업데이트
   - git push origin "branch 이름" : 내가 작업한 branch 원격에 push, 이 작업을 하면 원격 branch 공간에서 바뀜(?)



