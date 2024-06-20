# Cannot find module './App.svelte' or its corresponding type declarations

![](https://velog.velcdn.com/images/chrios99/post/0d284288-f6d0-43b5-9ec2-9eb603518919/image.png)

### 상황
"실전 스벨트 & 스벨트킷 입문, 하마구치 교헤이 저" 의 1장에 나오는 간단한 예시를 통해 스벨트를 학습하던 중 이런 오류 메시지가 나오면서 실행 시 다른 내용이 브라우저에 보여졌다.

### 해결
그래서 이 오류 메시지를 구글링하였더니 참고 문헌을 하나 발견하였다. jsconfig.json 파일의 tsconfig.json 파일에서 chekJs를 확인했을 때, true로 되어있었고 이를 false로 바꾸었다.

그러나 해결이 되지 않았다.

그래서 다른 참고 문헌을 찾아 나섰고 결국 발견했다.

tsconfig.json 파일에 다음과 같은 코드를 추가해주고 VS code를 닫았다가 다시 시작하였더니 해결되었다.
```javascript
"moduleResolution": "node",
```

> 참고 문헌:
1. https://ziszini.tistory.com/183
2. https://www.inflearn.com/questions/849251/%EC%95%84%EB%9E%98%EC%99%80-%EA%B0%99%EC%9D%80-%EC%97%90%EB%9F%AC%EA%B0%80-%EB%B0%9C%EC%83%9D%ED%95%A9%EB%8B%88%EB%8B%A4-%E3%85%9C%E3%85%9C