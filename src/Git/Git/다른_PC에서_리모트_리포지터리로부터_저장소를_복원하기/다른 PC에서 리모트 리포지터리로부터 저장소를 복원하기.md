# 다른 PC에서 리모트 리포지터리로부터 저장소를 복원하기

### 작업 폴더 생성
윈도우즈면 Ctrl + Shift + n눌러서 폴더를 만든다.

### 로컬 저장소 생성
>git init

### 변수 확인
git config --global init.defaultBranch # 확인
git config --global init.defaultBranch main

### 사용자 이메일 확인
git config --global user.email # 사용자 email 확인
git config --global user.email "깃허브에 가입할 때 사용한 이메일 혹은 자주사용하는 이메일" # 안되어 있으면

### 사용자 이름 확인
git config --global user.name # 사용자 이름 확인
git config --global user.name "깃허브 ID" # 안되어 있으면

### 연결되어있는 원격 리포지터리 목록 확인
git remote -v
->연결되어 있는 원격 리포지터리 목록, 현재는 없음

### 원결 리포지터리와 연결하기.
git remote add origin 저장소 주소
원격 리포지터리 연결

### 연결되어있는 원격 리포지터리 목록 확인
git remote -v
->연결되어 있는 원격 리포지터리 목록, origin 출력됨

### origin에 있는 main 브랜치의 내용을 현재 리포지터리(저장소)의 메인 브랜치에 복사하기.
git pull origin main
->origin 에 있는 main 브랜치의 내용을 현재 리포지터리(저장소)의 메인 브랜치에 복사(다운로드)