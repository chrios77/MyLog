# Github Flow⑤ Github Flow 협업 작업 흐름

## Github Flow 협업 작업 흐름
### 이슈 할당
GITHUB) 이슈 할당, 이슈 1(enhancement)
-> 상사가 본인에게 할당된 일 찾기 or 미할당된 일을 본인 스스로 할당 or 본인 스스로 이슈 생성

-> 이슈 할당
1) 깃허브 레포지터리에서 Issue에 들어간다
   2)New Issue 클릭
3) Add a title 란에 할 일을 적는다.
4) Assignees에 해당 일을 할 사람을 적는다.(적어도 되고 안 적어도 된다.)
5) Labels에 이 일의 성격을 적는다.(bug는 버그 고치는 것, document는 문서 고치는 것, enhancement는 새로운 기능을 추가하는 것이다.)
6) 할 일을 Add a description 란에 적는다.( Add a description란에 적을 때 - [ ] 를 꼭 적어줘라. 이걸 적어주면 할 일을 완료했다는 의미로 체크를 할 수 있게 네모 칸이 하나 나온다.)

-> 만약 이슈가 5개면 브랜치도 5개이다. 이슈란 상사가 적어놓은 해야 할 일의 리스트이다.

### git pull origin main
main) git pull origin main
-> 내 로컬의 main 브랜치 최신화

## git branch
main) git branch
-> 현재 브랜치 종류 확인

### git checkout -b
main) git checkout -b e/1
-> e/1라는 브랜치 생성 및 이동
-> 브랜치명은 마음대로 적어도 되지만 추천되는 방식이 존재한다. 브랜치명은 이슈의 라벨 이름/이슈 번호 형태로 만든다.

### 작업
e/1) 작업
-> 코드 작성 및 수정

### git add && git commit -m
e/1) git add && git commit -m "작업한 내용 간단 설명"
-> 추가, 커밋

### git log --oneline --graph --decorate --all
git log --oneline --graph --decorate --all
-> 전체 브랜치의 커밋흐름을 확인

### 작업
e/1) 작업
-> 코드 작성 및 수정

### git add && git commit -m
e/1) git add && git commit -m "작업한 내용 간단 설명"
-> 추가, 커밋

### git log --oneline --graph --decorate --all
git log --oneline --graph --decorate --all
-> 전체 브랜치의 커밋흐름을 확인

### git push origin e/1
main) git push origin e/1
-> 로컬의 e/1 브랜치를 원격지로 푸시

### PR 생성, 2번 PR 생성
GITHUB) PR(e/1 => main) 생성, 2번 PR 생성
-> e/1 브랜치에서 main 브랜치로 보내고 싶은 PR입니다!!!.

-> PR 생성하기
1) 깃허브 레포지포리 접속
2) Pull request 게시판 클릭
3) new pull request 클릭
4) compare 칸을 원하는 브랜치로 바꾼다. (원하는 브랜치에 있는 것을 main 브랜치에 반영하고 싶다는 의미이다)
5) create pull request 클릭
6) 박스에 내용 적고 하단에 create pull request 클릭
7) 만들면 PR 번호가 생기는데 보통 2번이라고 나온다. 그 이유는 이슈와 PR이 서로 번호를 공유하기 때문에 이슈 1를 만든 상태에서 PR를 만들면 그 다음 순서인 2를 번호로 가지는 것이다.

**참고)** PR를 만들면 main 브랜치에 커밋한 것과 같을까? 아니다.
PR은 main 브랜치에 커밋하기 위한 신청일 뿐이다. 이렇게 PR를 생성하면 나를 제외한 다른 팀원이 해당 내용에 대해 판단을 하고 허가를 내린다. 그 후에 main 브랜치에 방영이 된다.

### 그 다음 과정

GITHUB PR 2번) 투표
-> 팀원들끼리 내용을 확인하고 투표를 한다. 혼자하는 거면 이렇게 할 필요가 없다.

GITHUB PR 2번) 투표 통과
-> 투표로 통과가 된다.

GITHUB PR 2번) 반영(squash merge 방식 추천)
-> Continuous integration has not been set up란의 초록 버튼에는 merge, rebase, sqaush가 있다. 이 중에서 squash and merge를 선택하고 클릭한 후 confirm squash and merge 를 클릭해줘라. 이렇게 되면 반영이 된다.

GITHUB PR 2번) e/1 브랜치 삭제
1) code 게시판으로 이동
2) 브랜치 이동하는 칸을 눌러서 view all branches 클릭
3) 삭제를 원하는 브랜치의 바의 제일 오른쪽에 있는 휴지통 아이콘을 클릭
4) 어떤 창이 나오는데 delete 클릭

GITHUB ISSUE 1) 닫기(해당 일이 마무리되었다는 사실을 다른 팀원들도 알 수 있도록)
-> 안 닫으면 다른 팀원이 작업를 안한 줄 알고 해당 작업을 해버리고 닫아버림.

1) 이슈 게시판 클릭
2) 하단에 close issue 클릭

### git checkout main
e/1) git checkout main
-> 작업이 끝났으니 다시 main 브랜치로 이동

### git branch -D e/1
main) git branch -D e/1
-> e/1 브랜치 삭제

### git fetch --prune
main) git fetch --prune
-> 내 컴퓨터에 혹시나 남아있을지 모르는 원격지 브랜치 e/1에 대한 흔적 제거

### git pull origin main
main) git pull origin main
-> 내 로컬의 main 브랜치 최신화

### 마무리
깃허브 플로우는 이슈 게시판을 통해 작업할 일을 할당받기 전까지는 절대로 일하지 않는다.

본인 스스로 일을 해야겠다고 생각될 때 스스로 이슈를 만들어야 한다.
그 후, 번호가 생기면 작업하는 곳으로 가서 본인 컴퓨터의 main 브랜치를 최신화시킨다.

다음으로 브랜치를 새로 만든 후, 작업과 add, commit를 반복한다.
작업을 완료하고 나면 푸쉬를 하고 PR를 생성한 후, 다른 팀원들이 투표를 하는 과정을 거쳐 통과가 되면 반영이 된다.

다시 내 컴퓨터로 돌아와서 checkout를 하고 -D 옵션을 사용하여 작업한 브랜치를 없앤다.(PR이 끝났기 때문에 필요가 없어진다.)

깃허브 이슈 게시판에 들어가서 본인이 완료한 작업의 이슈를 닫는다.
git fetch --prune 명령어를 통해 혹시나 있을지 모르는 이전에 작업한 브랜치의 흔적을 없앤다.