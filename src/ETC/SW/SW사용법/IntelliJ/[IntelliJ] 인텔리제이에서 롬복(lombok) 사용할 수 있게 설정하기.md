# [IntelliJ] 인텔리제이에서 롬복(lombok) 사용할 수 있게 설정하기

![](https://velog.velcdn.com/images/chrios99/post/cbe3c51d-ffac-4df4-b36b-5f410b147f10/image.png)

사진 출처 : https://namu.wiki/w/IntelliJ%20IDEA
## lombok 사용할 수 있게 설정하기.
> lombok를 활성화시켜주면 lombok를 사용할 수 있다.

### 설정 방법①
> 파일 만드는 과정에서 설정한 것들 중 그래들을 클릭하면 build.gradle파일이 자동으로 만들어져 있을 것이다. 이 파일을 클릭하여 들어간다.

### 설정 방법②
> 들어간 그래들 파일의 코드를 복사하고 chapgpt 같은 ai사이트에 붙여넣기하고 환경 : 자바 버전( Ex)자바 21), 인텔리제이, 일반 자바 프로젝트 라고 적고 shift enter를 눌러 줄을 바꾼 후, 롬북을 쓰고 싶어 라고 입력한다.

### 설정 방법③
> 이렇게 하면 chatgpt에서 답을 준다. dependencies란에 관한 코드가 나오는데 이 코드를 복사하고 build.gradle 파일의 dependencies의 {} 안에 내용을 붙여넣기하여 바꾼다.

### 설정 방법④
> 이후, 롬북의 버전을 최신으로 바꿔줘야 한다. 롬북의 최신 버전 정보를 알기 위해  org.projectlombok:lombok를 구글에 검색하면 Maven Repository 사이트가 나오는데 이 사이트에 들어가서 확인한다. 현재 롬북의 최신 버전은 1.18.30이다.
```java

dependencies{
	implementation 'org.projectlombok:lombok:1.18.30'
	annotationProcessor 'org.projectlombok:lombok:1.18.30'
}

```
그러므로 위의 코드처럼 고친다.

### 설정 방법⑤
> 또한 테스트 환경에서도 롬복을 사용하기 위해

```java
dependencies{
	//롬북 추가
    implementation 'org.projectlombok:lombok:1.18.30'
    annotationProcessor 'org.projectlombok:lombok:1.18.30'
	
    //테스트 환경에서 롬북 사용
    testImplementation 'org.projectlombok:lombok:1.18.30'
    testAnnotationProcessor 'org.projectlombok:lombok:1.18.30'
}
```
이 코드 내용을 복사 + 붙여넣기 하여 build.gradle 파일의 dependencies 란를 수정한다.

### 설정 방법⑥
> 그 후, 오른쪽에 있는 코끼리 버튼을 누른다. 코끼리 버튼은 코드를 수정할 때마다 build.gradle에서 나온다.

### 마무리
> 이렇게 롬북을 설정하고 나면 @Getter, @Setter라고 치면 켓터와 셋터를 만들 수 있다.