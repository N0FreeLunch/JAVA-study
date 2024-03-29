## 자바의 기본타입
```java
public class Var7 {
    public static void main(String[] args) {
        int a = 100;
        double b = 0.5;
        boolean c = true;
        char d = 'A';
        String e = "Hello Java";

        System.out.println(a);
        System.out.println(b);
        System.out.println(c);
        System.out.println(d);
        System.out.println(e);
    }
}
```
- `int a = 100;`는 정수 타입이다.
- `double b = 0.5;`는 부동소수점 타입으로 실수를 다룬다.
- `boolean c = true`는 불리언 타입으로 `true`, `false`의 값만 온다.
- `char d = 'A'`는 하나의 문자를 가리키는 타입이다. 싱글 쿼트
- `String e = "Hello Java"`는 문자열 타입이다. `char`와 달리 여러 문자를 나열한 집합이다.

### 문자와 문자열
- 문자는 싱글 쿼트 `'` `'`으로 하나의 글자를 감싼다.
- 문자열은 더블 쿼드 `"` `"`으로 문자열을 감싼다.
- 문자는 하나의 글자만 받을 수 있는 반면, 문자열을 글자가 많아질 수록 동적으로 메모리를 늘려 저장하는 범위를 증가시킨다.

### 타입의 특징
- 선언된 변수의 타입과 다른 타입의 종류의 값을 대입할 수 없다.
- `int z = "백원""`과 같은 코드는 에러를 발생시킨다.

### 리터럴
- 개발자가 직접 넣는 값을 리터럴이라고 한다.
```java
int a = 100;
double b = 0.5;
boolean c = true;
char d = 'A';
String e = "Hello Java";
```
- 위에서 리터럴은 `100`, `0.5`, `true`, `'A'`, `"Hello Java"`는 리터럴에 해당한다.

## 타입의 범위
```java
public class Var8 {
    public static void main(String[] args) {
        byte b = 127;
        short s = 32767;
        int i = 2147483647;
        long l = 9223372036854775807L;
        float f = 10.8f;
        double d = 10.0;
    }
}
```
- 각 타입은 범위를 가지고 있다.
- `byte b = 127`는 괜찮지만, `byte bb = 32767`는 컴파일 에러가 발생한다.
- `short s = 32767`는 괜찮지만, `short ss = 2147483647`는 컴파일 에러가 발생한다.
- 각 타입은 담을 수 있는 수의 범위를 가지고 있고, 담을 수 있는 범위를 초과한 범위의 값을 넣으면 컴파일 에러가 발생한다.
- 이런 다양한 타입이 존재하는 이유는 메모리를 최적화하기 위해서이다. 작은 범위의 메모리를 사용할 수록 메모리를 적게 사용할 수 있지만, 다양한 범위의 값을 할당하지 못하기 때문에 더 큰 값을 넣어야 할 때 변수의 범위를 변경해야 하는 경우가 생긴다.
- 하지만 이런 메모리 사용은 수 기가 이상의 메모리를 제공하는 컴퓨터에서 아주 작은 값이므로 너무 최적화된 범위의 타입이 아닌 적당한 타입의 값을 사용한다.

### 주의
- 자바에서 리터럴 수는 기본적으로 int 형이므로 int 보타 큰 범위의 수를 사용할 때는 `long l = 9223372036854775807L`과 같이 L을 마지막에 적어 주어야 한다.

### 실무에서 거의 사용하지 않는 타입
#### byte
- 표현의 길이가 너무 작아서 실무에서 잘 사용되지 않는다.
- 파일은 바이트 단위로 다루기 때문에 파일 전송, 복사 등에 상용된다.

#### short
- 표현의 길이가 너무 작아 쓰지 않는다. 실무에서도 거의 쓰는 경우가 없다.

#### float
- 부동 소수점의 정밀도가 낮기 때문에 정밀도가 높은 double을 무조건 사용한다.

#### char
- 문자 하나를 사용하더라도 문자열을 쓰면 되기 때문에 문자열을 주로 사용하도록 한다.
