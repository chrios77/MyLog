# [Postman] 401 Unauthorized

![](https://velog.velcdn.com/images/chrios99/post/de1aef7b-84e3-42fa-bf6f-1c50e2b73b26/image.png)

> 사진 출처 : https://ko.wikipedia.org/wiki/%ED%8C%8C%EC%9D%BC:Postman_%28software%29.png

![](https://velog.velcdn.com/images/chrios99/post/2706b5d1-972a-4e23-b91a-dbc2d00e4a7b/image.png)

![](https://velog.velcdn.com/images/chrios99/post/8ffd89c1-f99c-4dc6-ad2a-ea84ec0f0851/image.png)

### 401 Unauthorized
개인 블로그를 만들어보며 POST API를 호출하기 위해 postman를 사용하여 테스트를 좀 할 필요가 생겨 사용하다 401 Unauthorized라는 오류 메시지를 마주하게 되었다.

![](https://velog.velcdn.com/images/chrios99/post/79edd826-5a12-4e08-93c6-7b57361d9539/image.png)

![](https://velog.velcdn.com/images/chrios99/post/92083412-de67-4c49-b9a1-3484061def25/image.png)


### 해결법

Insomnia나 Postman으로 POST API를 호출할 때 Spring Security에서 에부의 접근을 막기 때문에 Postman에서 401 Unauthorized 에러가 나타난다.

그래서 build.gradle 파일에서 Spring Security 부분을 주석 처리하였다.

이후에 서버를 재실행하고 Postman에서 Send 버튼을 눌러 POST API를 호출하였더니 201 Created 상태코드가 나타나며 Body가 성공적으로 나온다.

> 참고 문헌:
1. https://velog.io/@boat_417/230622-spring-%ED%9A%8C%EC%9B%90%EA%B0%80%EC%9E%85