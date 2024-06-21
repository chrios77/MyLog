# @Builder

### 빌더 패턴(Builder Pattern)
빌더 패턴이란 간략히 말하면 객체 생성에 관련된 디자인 패턴이다. 빌더 클래스를 통해 객체 생성 과정을 캡슐화하는데 이렇게 함으로써, 최종적으로 생성되는 객체의 표현과 생성과정을 분리해 동일한 생성 과정을 분리해 동일한 생성 과정을 통해 서로 다른 표현의 객체를 생성할 수 있게 해준다.

또한, 자바에서 인스턴스를 생성할 때, 생성자만을 통해 생성하는데 발생하는 어려움을 해결하기 위해 고안된 패턴 중에 하나다.

예를 들어, 생성자의 인자(매개변수)로 너무 많은 인자가 넘겨지는 경우 어떤 인자가 어떤 값을 나타내는지 확인하기 어렵다.
또, 어떤 인스턴스의 경우, 특정 인자만으로 생성해야 하는 경우가 발생하는데 이런 경우 특정 인자에 해당하는 값을 null로 전달해줘야 한다. 이는 코드의 가독성과 관련하여 매우 좋지 않다.

```java
// Product 클래스
class Coffee {
    private String type;
    private boolean sugar;
    private boolean milk;
    
    public String toString() {
        return this.type + " Coffee " + (this.sugar ? ", Sugar" : "") + (this.milk ? ", Milk" : "");
    }
    
    // Coffee 객체를 생성하기 위한 CoffeeBuilder 정적 멤버 클래스
    static class CoffeeBuilder {
        private Coffee coffee;
        
        public CoffeeBuilder() {
            this.coffee = new Coffee();
        }
        
        public CoffeeBuilder type(String type) {
            coffee.type = type;
            return this;
        }
        
        public CoffeeBuilder sugar(boolean value) {
            coffee.sugar = value;
            return this;
        }
        
        public CoffeeBuilder milk(boolean value) {
            coffee.milk = value;
            return this;
        }
        
        public Coffee build() {
            return coffee;
        }
    }
}

// 사용 예시
public class BuilderPatternExample {
    public static void main(String[] args) {
        Coffee coffee = new Coffee.CoffeeBuilder().type("Espresso").sugar(true).milk(true).build();
        System.out.println(coffee.toString());
        // 출력: Espresso Coffee , Sugar, Milk
        
        Coffee americano = new Coffee.CoffeeBuilder().type("Americano").sugar(false).milk(false).build();
        System.out.println(americano.toString());
        // 출력: Americano Coffee
    }
}
```
위의 코드처럼 빌더 패턴의 고드는 길다. 이렇게 자주 활용할 수 있는데 긴 코드를 기술하기에는 시간 소모도 되고 약간의 귀찮음이 생긴다. 그래서 만들어진 어노테이션이 @Builder다.

### @Builder
@Builder는 빌더 패턴을 스프링에서 구현하게 해준다. @Builder는 롬복(lombok)에 기술되어 있으므로 롬복을 설치해준 후 임포트하면 보통 활용할 수 있다. @Builder는 편리하고 명확하게 객체를 생성할 수 있게 도와준다. 또한, 빌더 패턴을 통해 인스턴스를 만들 때 특정 필드를 특정 값으로 초기화하고 싶다면 @Builder.Default를 사용하면 된다. @Builder는 기본 값 설정을 위해 사용한다. 보통 @Builder를 사용하면 모든 필드가 기본적으로 0, null, false 등의 기본 값을 가지게 된다.

@Builder는 보통 클래스에 달아준다. 이렇게 하면 서버를 시작할 때 스프링이 읽고 빌더 패턴 코드를 빌드한다. 또한, @Builder를 생성자에 달아주면 생성자에 포함된 필드만 빌더에 포함한다.

@Builder를 클래스 레벨에서 사용하려면 @NoArgsConstructor와 @AllArgsConstructor가 필요하다.

```java
import lombok.Builder;
import lombok.ToString;

@Builder
@ToString
public class Coffee {
    private String type;
    private boolean sugar;
    private boolean milk;
}

public class BuilderExample {
    public static void main(String[] args) {
        Coffee coffee = Coffee.builder()
                              .type("Espresso")
                              .sugar(true)
                              .milk(true)
                              .build();
        System.out.println(coffee.toString());
        // 출력: Coffee(type=Espresso, sugar=true, milk=true)
    }
}
```
위의 코드를 보면 @Builder 어노테이션을 Coffee 클래스에 적용하면, Lombok은 Coffee 클래스의 빌더 클래스를 자동으로 생성한다.  이 빌더 클래스를 사용하여 type, sugar, milk 필드를 설정하고, build() 메소드를 호출하여 최종적으로 Coffee 객체를 생성한다. @ToString 어노테이션은 객체를 문자열로 쉽게 표현하기 위해 추가한 것이다. 이처럼 @Builder는 코드의 가독성과 유지보수성을 향상시키는 데 큰 도움을 줍니다. 복잡한 객체를 생성할 때 필요한 많은 생성자나 세터 메소드를 줄일 수 있고, 객체의 필드가 변경되더라도 빌더 사용 코드를 수정할 필요가 없어 코드의 안정성도 높아집니다.

### @Builder.Default
@Builder.Default는 @Builder를 클래스에 달아주면 사용할 수 있으며 @Builder.Default를 사용하면 초기화할 값을 정할 수 있다.

위의 @Builder에서 보통 @Builder를 사용하면 모든 필드가 기본적으로 0, null, false 등의 기본 값을 가지게 된다.고 설명하였었다. 여기서 나오는 0, null, false 등의 기본 값을 수정하기 위해 @Builder.Default를 사용한다.

> 출처:
https://charliezip.tistory.com/17
https://asfirstalways.tistory.com/350
https://jiwontip.tistory.com/59
https://pamyferret.tistory.com/67
https://esoongan.tistory.com/82
https://leeborn.tistory.com/entry/Java-Builder-%EC%96%B4%EB%85%B8%ED%85%8C%EC%9D%B4%EC%85%98-%EA%B8%B0%EB%B3%B8%EA%B0%92-%EC%82%AC%EC%9A%A9%ED%95%98%EA%B8%B0-Builder-Default
https://velog.io/@hsbang_thom/Lombok-Builder.Default
https://velog.io/@wnajsldkf/Builder-%ED%8C%A8%ED%84%B4%EC%9D%B4%EB%9E%80