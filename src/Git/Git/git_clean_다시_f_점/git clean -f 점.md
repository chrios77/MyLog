# git checkout .을 해도 안되는 경우? git clean -f .

git checkout .을 해도 안되는 경우가 있다. 이런 경우 **git checkout -f .** 을 한다. 그러나 아무리 이 명령어를 사용해도 남아있을 수 있다. 왜냐면 변경된 것이 아니라 추가된 경우에 이렇게 될 수 있다.
**참고)** 이 명령어에서 -f는 force를 의미하는데 이는 강제로 진행하라는 의미이다.

아무리 **git checkout -f .** 을 해줘도 추가한 것이 남아 있다면
**git clean -fd**를 사용해라. 이러면 아예 추가한 것을 삭제를 해버린다.