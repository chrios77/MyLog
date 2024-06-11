# [IntelliJ] 인텔리제이에서 스프링 부트 프로젝트 만들고 설정하기

![](https://velog.velcdn.com/images/chrios99/post/8bcac6b4-bef4-4255-8927-a79b3f473a42/image.png)

사진 출처 : https://namu.wiki/w/IntelliJ%20IDEA

### 프로젝트 생성법 ①
인텔리제이에 접속한다. 만약, 프로젝트가 켜져 있는 상태라면 close를 한다. close를 하고 나면 나오는 화면에서 오른쪽 위에 있는 New Project를 클릭한다. New Project를 클릭하여 나오는 창에서 왼쪽 에 있는 Generators란에 3번째에 있는 Spring Initializar를 클릭한다. 설정할 것들을 설정해주고(Group -> 수정하면 Package name도 바낀다, JDK, Java) next를 클릭한다. Spring Boot DevTools, Lombok를 체크해주고 Web를 클릭한 후, Spring Web을 체크한다. 이 외에도 설정해줄 것들이 있을 수 있는데 그것은 차차 추가하도록 하자.

> [File] => [Close Project] => [New Project] => [Spring Initializar] => [create]

### 프로젝트 생성법 ②
프로젝트를 생성했으니 설정해줄 것들을 해줘야 한다.
> 1. **[File]** => **[Settings...]** => **[Build, Execution, Deployment]** => **[Compiler]** => **[Build project automatically]** 체크 => **[Apply]** 클릭 => **[Ok]** 클릭
>
>
> 2. **[File]** => **[Settings...]** => **[Build, Execution, Deployment]** => **[Build Tools]** => **[Gradle]** =>  **[Build and run using]**란의 **Gradle (Default)**을 **Intellij IDEA**로 바꾼다. => **[Apply]** 클릭 => **[Ok]** 클릭
>
>
> 3. **[File]** => **[Settings...]** => **[Build, Execution, Deployment]** => **[Build Tools]** => **[Gradle]** => **[Run tests using]**란의 **Gradle (Default)**을 **Intellij IDEA**로 바꾼다. => **[Apply]** 클릭 => **[Ok]** 클릭
>
>
> 4. **[File]** => **[Settings...]** => **[Editor]** => **[File Encodings]** 클릭 => **[Default encoding for properties files]**란의 **<Properties Default ISO-8859-1>**을 **UTF-8**로 바꾼다. => **[Apply]** 클릭 => **[Ok]** 클릭
>
>
> 5. **[File]** => **[Settings...]** => [돋보기 있는 창]에 **fly** 검색 => **[Optimize imports on fly]** 체크 => **[Apply]** 클릭 => **[Ok]** 클릭
>
>
> 6. **[File]** => **[Settings...]** => **[Project Settings]** => **[SDK]**에 제대로 JDK가 되어있는지 확인, 안되있으면 원하는 JDK로 수정 => **[Apply]** 클릭 => **[Ok]** 클릭
>
>
> 7. **[File]** => **[Settings...]** => **[Project Settings]** => **[Modules]** => **[Language level]란**에 **[Project default]**라고 되어 있는지 확인, 안 돼있으면 [Project default]로 수정 => **[Apply]** 클릭 => **[Ok]** 클릭

### 추가할 기능 넣기
> 1. **[인텔리제이]** 접속
>
>
> 2. **[build.gradle]** 파일 클릭
>
>
> 3. **dependencies** 찾기
>
>
4. **dependencies의 블럭**({}을 블럭이라고 한다.) 사이에 추가하고 싶은 기능을 **Spring initalizr 사이트**의 **Dependencies**에 있는 **ADD DEPENDENCIES...**을 톨해 추가(ADD DEPENDENCIES...창을 열고 원하는 기능을 클릭하면 자동으로 추가된다.)
>
>
> 5. 원하는 기능을 다 추가한 다음 [EXPLORE]를 클릭
>
>
> 6. [EXPLORE] 창의 **dependencies** 찾기
>
>
> 7. **dependencies의 블럭 내용**을 드레그 후 복사
>
>
> 8. [인텔리제이]에 있는 **dependencies**란에 붙여넣기.

**참고1)** 만약, **dependencies**란을 [EXPLORE] 창에서 모두 복사한 경우, 인텔리제이의 **dependencies**란에 붙여넣기할 때 **dependencies**란을 모두 드레드하고 붙여넣기하면 된다.

**참고2)** Spring initalizr 사이트 주소는 https://start.spring.io/이다.
