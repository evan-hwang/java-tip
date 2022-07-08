# 반복문과 스트림

## 반복문
반복문은 특정 조건이 달성될 때 까지 코드 블록을 반복해서 실행하는 것을 뜻한다. 반복문으로는 `for`, `while` 그리고 `foreach`가 있다.



### for문
```java
for (statement 1; statement 2; statement 3) {
  // code block to be executed
}
```
***기본 문법***

- statement 1 : 코드 블럭 실행 전에 한번만 호출된다.
- statement 2 : 코드 블럭이 실행되는 조건을 정의한다.
- statement 3 : 코드 블럭 실행 이후 매번 호출된다.

```java
for (int i = 0; i < 5; i++) {
  System.out.println(i);
}
```
***예시***

- statement 1 : 반복문 시작 전 `i`가 0으로 초기화된다.
- statement 2 : 코드 블럭 실행 전 `i`가  5보다 작은지 검사한다. 조건이 참이라면 코드 블럭을 실행하고, 거짓이라면 반복문을 종료한다.
- statement 3 : 코드 블럭 실행 후 `i++`를 실행한다.

```
0
1
2
3
4
```

***결과***



### while문

```java
while (condition) {
  // code block to be executed
}
```

***기본 문법***
condition을 만족할 때 까지 코드 블럭을 반복 실행한다.

```java
int i = 0;
while (i < 5) {
  System.out.println(i);
  i++;
}
```

***예시***

- `i`가 5 미만일 때 까지 코드 블럭을 실행한다.

```
0
1
2
3
4
```

***결과***



### foreach 문

[Array](https://www.w3schools.com/java/java_arrays.asp) 타입에 쓸 수 있는 반복문이다.

```java
for (type variableName : arrayName) {
  // code block to be executed
}
```

***기본 문법***

```java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
for (String i : cars) {
  System.out.println(i);
}
```

***예시***

```
Volvo
BMW
Ford
Mazda
```

***결과***



## 스트림

위에서 다룬 반복문만으로도 충분히 코드블럭을 반복 실행시킬 수 있는데, 스트림은 왜 필요한 것일까?



### 함수형 프로그래밍

Java는 객체지향 언어이기 때문에 기본적으로 [함수형 프로그래밍](https://mangkyu.tistory.com/111)이 불가능하다. 하지만 JDK8부터 Stream API와 람다식, 함수형 인터페이스 등을 지원하면서 Java를 이용해 함수형으로 프로그래밍할 수 있는 API 들을 제공해주고 있다. 그 중에서 Stream API는 데이터를 추상화하고, 처리하는데 자주 사용되는 함수들을 정의해두었다. 여기서 데이터를 추상화하였다는 것은 데이터의 종류에 상관 없이 같은 방식으로 데이터를 처리할 수 있다는 것을 의미하며, 그에 따라 재사용성을 높일 수 있다.



### Stream API의 특징

- 원본의 데이터를 변경하지 않는다.
- 일회용이다.
- 내부 반복으로 작업을 처리한다.




- parallel

- for를 stream으로 바꿨을 때 성능
- 함수형 프로그래밍
- 선언형 프로그래밍



## 참고

- [w3schools](https://www.w3schools.com/java/java_while_loop.asp)
