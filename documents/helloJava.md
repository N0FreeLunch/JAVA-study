## 자바 코드의 기본 구조

```java
public class HelloJava {
    public static void main(String [] args) {
        System.out.println("hello java");
    }
}
```

### class 
```java
public class HelloJava {
    
}
```
- `{ }`는 블록이다. 클래스나 메소드 내부의 구문이 시작과 끝을 알려준다.

### method
```java
    public static void main(String [] args) {
        System.out.println("hello java");
    }
```
- `main`: 메소드의 이름을 쓰는 부분으로 `main`이라는 이름은 자바 프로그램의 코드 실행의 첫 번째 지점이다.
- `String`: 타입의 첫 글자는 대문자이다. 여기서는 문자열 `String` 타입이 사용되었다.
- `[]`:
- `args`: 매개변수명이다. 
- `System.out.println`: 
- `;`: 표현식(값이 위치하는 곳)이 끝나는 지점에는 세미콜론을 필수적으로 요구한다.
- `    `: 자바는 들여쓰기를 할 때 기본적으로 스페이스 4칸의 들여쓰기를 한다. 4칸이 필수는 아니지만 대부분 4칸을 사용한다.

### 순차적인 실행
```java
public class HelloJava {
    public static void main(String [] args) {
        System.out.println("hello java1");
        System.out.println("hello java2");
        System.out.println("hello java3");
    }
}
```
- 클래스의 블록에서는 정해진 문법만을 사용해야 하지만, 메소드의 블록 안에서는 값을 사용할 수 있다.
- 이 값의 실행 순서는 대체로 위에서 아래로, 왼쪽에서 오른쪽으로 차례로 실행이 된다. 값을 만드는 하나의 단위가 끝나고 세미콜론이 붙여지면 그 다음 코드가 순차적으로 실행이 된다.
따라서 결과는 
```
hello java1
hello java2
hello java3
```

## Tip
- `public static void main(String [] args)`의 첫 글자를 따서 `psvm`이라고 입력하면 인텔리제이가 자동완성을 해 준다.
- `System.out.println("hello java");`은 `sout`라고 입력하면 인텔리제이가 자동완성을 해 준다.
- 