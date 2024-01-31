## 변수
```java
package variable;

public class Var2 {
    public static void main(String [] args) {
        int a;
        a = 10;

        System.out.println(a);
        System.out.println(a);
        System.out.println(a);
    }
}
```
- 변수를 사용할 때는 타입 키워드로 선언해 줘야 한다. `int a;`의 변수 `a`를 int라는 타입으로 선언하겠다는 의미이다.

### 변수의 값 바꾸기
```java
package variable;

public class Var3 {
    public static void main(String[] args) {
        int a;
        a = 10;
        System.out.println(a);
        a = 50;
        System.out.println(a);
    }
}
```
- 변수의 초기값을 `10`을 입력하였다. 변수 a에는 `10`이란 값이 들어있다.
- 변수의 값을 `50`으로 바꾸었다. 변수 a는 `50`이란 값을 가지고 있다.

```java
package variable;
public class Var5 {
    public static void main(String[] args) {
        int a;
        a = 1;
        System.out.println(a);

        int b = 2;
        System.out.println(b);

        int c = 3, d = 4;
        System.out.println(c);
        System.out.println(d);
    }
}
```

```java
int a;
a = 1;
```
- 변수를 선언할 때는 정의하지 않다가 그 다음 코드에서 초기화한다. 변수 a에 1이란 값이 들어 있기 때문에 `System.out.println(a);`의 결과 값은 1이 나온다.

```java
int b = 2;
```
- 변수를 선언함과 동시에 변수를 초기화한다.

```java
int c = 3, d = 4;
```
- 변수를 여럿 선언함과 동시에 변수를 초기화 하였다.

### 초기화를 하지 않으면?
```java
package variable;

public class Var6 {
    public static void main(String[] args) {
        int a;
        System.out.println(a);
    }
}
```
- `java: variable a might not have been initialized`라는 에러가 발생한다.
- 변수는 메모리의 어떤 위치를 확보하는 것이다. 변수에 값을 할당하는 것은 해당 메모리의 위치에 값을 0과 1의 기계어로 변환 해 넣는 과정이다.
- 하지만 메모리는 어떤 값을 저장하고 있던 장소로 변수를 초기화하지 않으면 알 수 없는 값이 메모리에 기록되어 있을 때 해당 값을 그대로 사용할 수가 있다. 자바에서는 컴파일할 때 변수의 초기화를 하지 못하게 막지만, C언어와 같은 저수준의 언어를 사용하면 변수를 초기화하지 않으면 메모리의 값을 그대로 사용하게 된다.
- 같은 패키지에 컴파일 위와 같이 컴파일 불가능한 파일이 있다면 동일 패키지 내의 다른 파일도 컴파일이 되지 않으므로 주의하자.
- 따라서 다음과 같이 주석을 친다.
```java
public class Var6 {
    public static void main(String[] args) {
        int a;
//        /*
//         * 주석을 지우면 에러가 발생
//         */
//        System.out.println(a);
    }
}
```
