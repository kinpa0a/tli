**저작권(?)이 있는 듯해서 내용은 따로 정리**

<https://docs.oracle.com/javase/tutorial>

<https://docs.oracle.com/javase/tutorial/java/nutsandbolts/datatypes.html>

<https://docs.oracle.com/javase/tutorial/java/nutsandbolts/arrays.html>

<https://docs.oracle.com/javase/tutorial/java/nutsandbolts/operators.html>

<https://docs.oracle.com/javase/tutorial/java/nutsandbolts/expressions.html>

<https://docs.oracle.com/javase/tutorial/java/nutsandbolts/flow.html>

<https://docs.oracle.com/javase/tutorial/java/javaOO/classes.html>

<https://docs.oracle.com/javase/tutorial/java/javaOO/object.html>

<https://docs.oracle.com/javase/tutorial/java/javaOO/nested.html>
* need to read it one more time

<https://docs.oracle.com/javase/tutorial/java/javaOO/enum.html>
* (???) 오브젝트의 프라이빗 메소드는 스태틱 메서드에서 접근 못하나?
* (???) 인스턴스 메소드에서 그 인스턴스의 프라이빗 변수를 바로 참조 가능한가?

<https://docs.oracle.com/javase/tutorial/java/annotations/index.html>
* Declaration
  ```
    @inteface AnnotationTypeName {
      AnnotationTypeElementType annotationTypeElementName default annotationTypeElementDefaultValue;
    }
  ```
* (???) annotation type이라는건 한 형태의 어노테이션. 하나의 선언된 어노테이션을 말하는 듯. 클래스 선언하는 것도 클래스 타입을 선언한다고 표현하나?

처음에 자바를 공부할 때 이정도는 너무 어렵다고 생각했거나 아직 여기를 볼 차례가 아니야 하고 가볍게 넘겼던 부분들이 낯설다. 반대로 알게되는 것(?)도 더 많다. 몰랐던 것이 많았던 탓이다. 지금까지는 nested class, enum, annotation 정도.

<https://docs.oracle.com/javase/tutorial/java/IandI/createinterface.html>

한글로 쓰면 자꾸 깨져서 엉망진창 영어로..나중에 내가 이걸 읽고 이해할 수 있을지는 모르겠다.

Long time no see!

<https://docs.oracle.com/javase/tutorial/essential/exceptions/runtime.html>
not mean that not use runtime exception but don't use it with an intention to avoid handing it
if then, it means no need to handle it with catch or specify anymore but handle it at the one point(ex. exception handling) when I throw a common sometimes custom runtime exception in a catch clause

```
Generally speaking, do not throw a RuntimeException or create a subclass of RuntimeException simply because you don't want to be bothered with specifying the exceptions your methods can throw.
```

try -> try with resources -> catch -> finally 

<https://docs.oracle.com/javase/tutorial/essential/io/index.html>

file io에 대한 인터페이스가 일관성이 부족하다는 느낌을 받는다. 그리고 결국 os에 직접 무엇을 하는게 아니라 어플리케이션이라는 하나의 레이어가 있는 것이라 동작이 완벽하지 않다. os 디펜던시도 심하다. 조심히 써야할 것 같다.

<https://docs.oracle.com/javase/tutorial/essential/io/notification.html>

java에 별 클래스가 다 있구나. 제대로 모르고 쓰는구나. 근데 이런 라이브러리들은 대부분 날 것 같아서(네이티브 코드?를 래핑한 건데도) 보통은 한 번 더 래핑한 외부의 커스텀 라이브러리를 갖다 쓰게 되는 것 같다. 라이브러리를 제공하는 입장이 아니라면 사실 잘 모를지도?


It took me too long to read and understand java tutorial up to file io.
I've learned that I don't need to focus on each words or setences of a documen considered as a "reference".
Read fast even though I couldn't remember all. Because I might forget almost every things that I've read.
What I really remember is where the information is or what kinds of topics I can find from it.
