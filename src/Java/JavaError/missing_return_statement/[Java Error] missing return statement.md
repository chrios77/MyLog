# [Java Error] missing return statement

## missing return statement가 발생하는 원인
missing return statement이라는 오류가 발생하는 원인은 메서드가 반환 값(return value)을 요구하는데, 모든 실행 경로에서 실제로 값을 반환하지 않을 때 발생한다.

또한, 모든 조건문이나 루프 내에서도 적어도 하나의 return 문이 실행되어야 하며, 그렇지 않으면 컴파일러는 'missing return statement' 오류를 발생시킨다.

## 해결법
조건문과 루프는 return를 적어주면 해결될 것이고 메서드는 메서드의 반환 타입과 반환 값의 타입이 같게 해주면 된다.

### 모든 조건문 처리
조건문(if, else if, else)을 사용하는 경우, 모든 조건에서 반환값을 제공해야 한다.

또한, 모든 조건을 고려했는지 확인해야 하며, 어떤 조건도 충족되지 않을 경우를 대비해 else 구문에서도 반환값을 제공해야 한다.

다음은 예시이다.
```java
int exampleMethod(boolean condition) {
    if (condition) {
        return 1;
    } else {
        return 0;
    }
}
```

### 루프(반복문) 내에서 반환하기
루프(for, while) 내에서도 특정 조건이 만족될 때 반환할 수 있지만, 루프가 종료된 후에도 값이 반환되어야 한다.

루프 내에서 모든 경우에 반환값을 제공할 수 없다면, 루프 밖에서도 반환값을 제공해야 한다.

다음은 예시이다.
```java
int exampleMethod(int[] array) {
    for (int value : array) {
        if (value > 10) {
            return value;
        }
    }
    return -1; // 루프를 완료한 후 반환
}
```

### 반환 타입과 일치하는 값 반환
메서드의 반환 타입과 실제 반환하는 값의 타입이 일치해야 한다.

예를 들어, 메서드가 String을 반환하도록 선언되었다면, 반드시 String 타입의 값을 반환해야 한다.

### 모든 실행 경로에서 반환하기
메서드 내에서 가능한 모든 실행 경로를 고려하여, 어떤 경로를 통해 실행되더라도 반드시 반환값이 있도록 해야 한다. 이는 조건문이나 루프뿐만 아니라, 예외 처리를 포함한 모든 상황에서도 고려되어야 한다.

다음은 예시이다.
```java
int exampleMethod(boolean condition) {
    if (condition) {
        return 1;
    }
    // 조건이 false일 때도 처리
    return 0;
}
```
