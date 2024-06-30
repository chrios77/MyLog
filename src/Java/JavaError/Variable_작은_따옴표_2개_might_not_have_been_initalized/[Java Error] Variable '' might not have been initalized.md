# [Java Error] Variable '' might not have been initalized

![](https://velog.velcdn.com/images/chrios99/post/8b95e53f-ed6a-4683-bccf-220e9c554b97/image.png)

### Variable '' might not have been initalized
개인 블로그를 만들어보기 위해 DTO를 작성하고 보니 인텔리제이에서 위와 같은 에러 메시지를 내보냈다. 이 3가지 에러들 중
```java
Variable 'title' might not have been initialized
```
를 해석해보면 "변수 'title'은 초기화되지 않았을 수도 있다." 라는 뜻이다.

이 에러를 만났을 때 순간 당황했다. 또 뭔가 이상했다. 그래서 바로 코드를 뜯어보았다.

그 순간 아차 싶었다. 기본 생성자와 클래스의 철자가 서로 달랐다. 그래서 철자를 수정했더니 바로 없어졌다..

### 오늘의 교훈
Variable '' might not have been initalized라는 에러가 나오면 일단 철자가 이상한 부분이 없는지 찾아보고 그래도 없으면 구글링을 해보자.