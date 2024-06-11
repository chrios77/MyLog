# [IntelliJ] 인텔리제이에서 새 프로젝트 창 열 때마다 해줘야 하는 설정 

![](https://velog.velcdn.com/images/chrios99/post/544cb813-425b-4b6f-872b-e26a2e0073ae/image.png)

사진 출처 : https://namu.wiki/w/IntelliJ%20IDEA
## 설정①
메뉴 => File => Settings => Build, Execution, Deployment => Compiler

Build project automatically : 체크

사실 이 설정은 스프링부트 프로젝트에서만 하면 됩니다.

일반 자바프로젝트에서는 필요없음

## 설정②
>메뉴 => File => Settings => Build, Execution, Deployment => Build Tools => Gradle => Build and run using : IntelliJ IDEA
**이렇게 하면 인텔리제이의 내장 그래들을 사용하기 때문에 조금 더 빌드가 빨라진다**

>메뉴 => File => Settings => Build, Execution, Deployment => Build Tools => Gradle => Run tests using : IntelliJ IDEA
**이렇게 하면 인텔리제이의 내장 그래들을 사용하기 때문에 조금 더 빌드가 빨라진다**

## 설정③
설정②한 상태에서 Gradle JVM 바에 Project SDK라고 되어있는지 확인.
