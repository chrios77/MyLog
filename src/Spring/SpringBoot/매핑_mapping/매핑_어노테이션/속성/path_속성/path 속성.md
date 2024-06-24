# path 속성

### path 속성 및 역할
path 속성은 Spring 프레임워크의 @RequestMapping, @GetMapping, @PostMapping, @PutMapping, @DeleteMapping, @PatchMapping 등 여러 매핑 어노테이션에서 사용된다. 또한, path 속성은 HTTP 요청을 처리할 때 해당 요청이 어떤 URL 경로에 매핑되는지를 지정하는데 사용된다.

path 속성은 value 속성과 하는 기능이 같다. 그래서 value 속성을 path 속성으로 바꾸어 사용해도 된다. 즉, path를 사용하는 것은 value를 사용하는 것과 같은 효과를 가진다.

### path 속성의 형식
path 속성은 문자열 배열로 기술되며 하나 이상의 URL 경로를 지정할 수 있다. path 속성을 사용하여 여러 URL을 지정할 수도 있는데 이때는 {}를 사용한다.
```java
@GetMapping(path = "/example")
public String getExample() {
    // 메서드 내용
}
```

```java
@GetMapping(path = {"/example", "/exampleAlias"})
public String getExample() {
    // 메서드 내용
}
```

### value 속성, path 속성을 생략하다.
Spring 프레임워크에서는 @GetMapping을 사용하여 어떤 메서드를 HTTP GET 요청에 대한 경로와 연결할 수 있다. 이 때 value 속성이나 path 속성에 경로를 지정함으로써, 해당 경로로 들어오는 요청이 엉떤 메서드에 의해 처리 될지를 정의한다.

보통 @GetMapping에서 URL을 지정할 때 value 속성이나 path 속성을 생략하여
```java
@GetMapping("/home")
```

### path 속성 사용 시 주의사항
path 속성을 사용할 때 주의할 점은 동일한 컨트롤러 내에서 같은 경로를 가진 중복 매핑은 허용되지 않는다. 즉, 동일한 경로로 매핑된 두 메서드가 있을 경우, Spring은 애플리케이션을 시작할 때 오류를 발생시킨다. 또한, 경로를 지정할 때는 애플리케이션 전체에서의 경로 중복, 컨텍스트 루트, 서블릿 매핑 등에 대한 영향을 고려해야 한다.

### 마무리
path 속성을 통해 개발자는 Spring 애플리케이션에서 HTTP 요청의 처리 경로를 명확하게 정의하고 관리할 수 있으며, 이는 애플리케이션의 URL 설계와 구조를 체계적으로 만드는 데 중요한 역할을 한다.