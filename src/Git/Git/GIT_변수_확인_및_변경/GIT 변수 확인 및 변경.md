# GIT 변수 확인 및 변경->git config --global init.defaultBranch

### GIT 변수 확인 및 변경
**확인** : git config --global 변수명
**->**git config --global init.defaultBranch

**변경** : git config --global 변수명 새_값
**->** git config --global init.defaultBranch main
**->** 위의 명령어를 입력하면  ~/Desktop/git-work 옆에 있는 (master)를 main으로 바꾼다.

**=>** 이 명령어에서 사용한 옵션인 --global을 사용하면 --global를 사용한 사항을 터미널에서 영구적으로 반영한다.

### 마무리
변경 후 잘 되었는 지 알고 싶다면 확인 명령어 git config --global init.defaultBranch 를 한 번 더 입력해주면 된다. 입력해주면 그 밑에 main이라고 출력해준다. 