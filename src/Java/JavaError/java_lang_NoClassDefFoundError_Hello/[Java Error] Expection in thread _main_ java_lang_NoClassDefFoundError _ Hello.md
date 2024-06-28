# [Java Error] Expection in thread "main" java.lang.NoClassDefFoundError : Hello

### **Expection in thread "main" java.lang.NoClassDefFoundError : Hello**
이 에러는** Hello라는 이름을 가진 클래스를 찾을 수 없다**는 에러이다. 이 에러가 발생하면 Hello라는 이름의 **클래스의 철자가 옳바른지 확인한다**. 만약 클래스 이름의 **철자에 이상이 없다면 클래스 파일이 생성되어 있는자 확인**해보자. 이 부분에서 말하는 클래스 파일은 확장자가 .class로 되어있는 파일을 말한다. 예를 들어, 파일명.java가 정상적으로 컴파일됐다면 클래스 파일인 파일명.class가 있어야 한다. 만약, 클래스 파일이 있는데도 이 에러 메시지가 등장한다면 클래스 패스(classpath), 즉, 클래스 경로의 설정이 바르게 설정되어있는지 확인해보자.

**참고)** 클래스 이름은 철자의 대소문자가 모두 일치해야한다.