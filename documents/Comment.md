## 주석

```java
public class CommentJava {
    public static void main(String[] args) {
        System.out.println("hello java1"); // hello java 1
//        System.out.println("hello java2");

        /*
        System.out.println("hello java3");
        System.out.println("hello java4");
         */

        System.out.println("hello java3" /*문자열 출력*/);
    }
}
```
- `//`: 한 줄 주석으로 `//`으로 표기한 부분 오른쪽으로 모두 주석처리 된다. 
- `/* */`: `/*`가 시작된 부분부터 `*/` 끝나는 부분까지 실행이된다. 자바 문법 어디에든 넣을 수 있다. 그냥 실행될 때 `/*` 부터 `*/`까지는 없다고 간주한다고 보면 된다.