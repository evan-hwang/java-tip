# 접근제어자(access modifiers)





## 클래스에서

### 클래스의 디폴트 접근 제어자는 무엇인가요?

- 클래스에 접근 제어자가 명시되지 않으면 디폴트 클래스라고 부른다.
- 디폴트 클래스는 같은 패키지 안에서만 보인다.
- 디폴트 클래스는 기본적으로 패키지 접근이다.



```java
package com.rithus.classmodifiers.defaultaccess.a;

/* No public before class. So this class has default access*/
class DefaultAccessClass {
	//Default access is also called package access    
}
```

***기준 클래스***

```java
package com.rithus.classmodifiers.defaultaccess.a;

public class AnotherClassInSamePackage {
    //DefaultAccessClass and AnotherClassInSamePackage 
    //are in same package.
    //So, DefaultAccessClass is visible.
    //An instance of the class can be created.    
    DefaultAccessClass defaultAccess;
}
```

***같은 패키지에서의 접근***

```java
package com.rithus.classmodifiers.defaultaccess.b;

public class ClassInDifferentPackage {
    //Class DefaultAccessClass and Class ClassInDifferentPackage
    //are in different packages (*.a and *.b)
    //So, DefaultAccessClass is not visible to ClassInDifferentPackage
    
    //Below line of code will cause compilation error if uncommented
    //DefaultAccessClass defaultAccess; //COMPILE ERROR!!    
}
```

***다른 패키지에서 접근 불가***



## 추상 클래스에서



## 인터페이스에서



## 람다에서





## 참고 

- https://www.w3schools.com/java/java_modifiers.asp