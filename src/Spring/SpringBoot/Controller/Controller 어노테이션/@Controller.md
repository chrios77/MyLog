# @Controller

## @Controller
```java
@Controller
public class MyController {
    @RequestMapping("/hello")
    public String sayHello() {
        return "Hello, World!";
    }
}
```

@Controller는 클래스 레벨에서 사용되는 어노테이션이다. 이 어노테이션은 해당 클래스가 컨트롤러의 역할을 수행하게 한다는 것을 스프링 프레임워크에게 알려주는 역할을 한다.

컨트롤러는 일반적으로 사용자의 요청을 처리하고, 적절한 응답을 반환하는 역할을 한다. 이를 위해 @RequestMapping, @GetMapping, @PostMapping 등의 메소드 레벨 어노테이션과 함께 사용된다.

더 쉽게 표현하면 @Controller는 마치 학교에서 선생님이 학생들의 요구를 받아 답변하는 것과 같은 역할을 한다고 보면 된다. 이 선생님(@Controller)은 학생들이 어떤 질문을 할지(@RequestMapping) 알고 있어서, 그 질문에 따라 적절한 답변을 준비한다.

예를 들어, '오늘 급식은 뭐야?'라는 질문에는 '김치찌개'라는 답을 하듯이, @Controller는 사용자의 요청에 따라 적절한 응답을 준비해서 돌려준다. 이런 식으로, @Controller는 사용자의 요청을 받고 그에 대한 응답을 하는 역할을 하게 된다.
