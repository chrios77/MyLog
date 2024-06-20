# application.properties의 이름 수정, 서버 포트-8020, 서버 실행, 깃 연결

### application.properties의 이름 수정
[src] 폴더 클릭 => [main] 폴더 클릭 => [resources] 폴더 클릭 => application.properties를 마우스 우클릭 => [Refactor]클릭 => [Rename] 클릭 => application.properties의 이름을 application.yml이라고 수정 => [Refactor] 클릭

### 서버 포트-8020
application.yml 파일에 아래 코드를 적는다. port 왼쪽의 공간은 띄어쓰기 2번을 한 것이다.

```
server:
  port: 8020
```

### 서버 실행
java 소스 파일에 들어가서 run를 누른다. 눌렀을 때 나오는 창에서 8020이 나와있다면 잘 싱행되고 있는 것이다.

### 깃 연결
git 터미널에서 git init, git add . , git commit -m "코드 설명" , git push origin main을 순서대로 적는다.
**참고)** git commit -m "코드 설명"에서 코드 설명에는 처음 시작을 하는 것이니 setting이라고 적어주면 된다.