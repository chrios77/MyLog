# git remote -v , git remote add

## 연결되어있는 원격 리포지터리 목록 확인
git remote -v
->연결되어있는 원격 리포지터리 목록 확인, 현재는 없음

### 원격 리포지터리에 연결하기.
git remote add origin 저장소 주소
->원격 리포지터리 연결
-> 메인이라는 의미로 origin을 사용하는 것일 뿐, 다른 단어가 와도 된다.

### 연결되어있는 원격 리포지터리 목록 확인
git remote -v
->연결되어있는 원격 리포지터리 목록, origin 출력됨(2줄 나옴)

### 현재 로컬 저장소의 main 브랜치를 origin으로 보내기.
git push origin main # 현재 로컬 저장소의 main 브랜치를 원격지 중 origin 으로 보낸다. origin 에도 main 브랜치가 생성됨