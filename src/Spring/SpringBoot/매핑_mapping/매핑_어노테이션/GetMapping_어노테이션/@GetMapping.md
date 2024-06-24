# @GetMapping

### @GetMapping
@GetMapping은 스프링 프레임워크에서 사용하는 매핑 어노테이션 중 하나로, 어떤 HTTp GET 요청을 처리하는 메소드에 달 수 있다.

### @GetMapping이 사용되는 위치
@GetMapping는 Spring MVC 중에 컨트롤러에 사용된다. 정확히는 컨트롤러 역할을 하는 클래스에 사용된다.

### @GetMapping의 역할
@GetMapping는 클라이언트가 서버에 어떤 리소스를 요청한 후, 서버가 해당 요청을 처리하는 역할을 맡고 있다.

### @GetMapping가 내부적으로 하는 일
@GetMapping은 내부적으로 @RequestMapping에
method = RequestMapping.GET을 설정하는 역할을 수행한다.
그러나 @GetMapping은 보다 간결하고 명시적이게 GET 요청을 처리하도록 설계되어 있으므로 @GetMapping을 사용하면 요청 URL 경로, 파라미터 등을 통해 클라이언트의 요청을 세밀하게 제어할 수 있게 된다.

예를 들어, 사용자의 정보를 조회하는 API를 구현한다면
```java
@GetMapping("/users/{userId}")
```
를 메서드에 달아주면 해당 메서드가 useId에 해당하는 사용자 정보를 조회하는 GET 요청을 처리하도록 할 수 있다.

이 때, @PathVariable 등을 함꼐 사용하여, 요청 URL 경로에서 변수 값을 추출하는 등의 작업도 수행할 수 있다.

### @GetMapping이 사용되는 상황
@GetMapping은 주로 데이터를 조회하거나 어떤 페이지를 보여줄 때 사용된다.

예를 들어, 사용자 목록, 상품 정보 조회, 특정 사용자의 상세 정보 페이지 등을 클라이언트에 제공할 때 GET 방식으로 요청을 받아 처리한다. 이는 HTTP GET이 서버의 상태를 변경하지 않고, 주로 데이터를 요청하는데 사용되기 때문이다.

따라서 @GetMapping은 어떤 데이터를 조회하거나어떤 리소스를 읽어오는 경우에 적합하다.

### @GetMapping과 함께 사용되는 어노테이션
@GetMapping과 함꼐 사용되는 어노테이션은 다양하다.

대표적인 어노테이션으로 @PathVariable, @RequestParam, @RequestHeader, @RequestBody, @ModelAttribute가 있다.

이외에도 @CookieValue, @SessionAttribute, @MatrixVariable, @CrossOrigin 등 다양하다.

### @GetMapping에 사용되는 속성
@GetMapping에 사용되는 속성들 중에 대표적인 것들은 value, path, params, headers, consumes, produces가 있다. 