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


<https://docs.oracle.com/javase/tutorial/>
```
Trails Covering the Basics

These trails are available in book form as The Java Tutorial, Sixth Edition. To buy this book, refer to the box to the right.
Getting Started — An introduction to Java technology and lessons on installing Java development software and using it to create a simple program.
Learning the Java Language — Lessons describing the essential concepts and features of the Java Programming Language.
Essential Java Classes — Lessons on exceptions, basic input/output, concurrency, regular expressions, and the platform environment.
Collections — Lessons on using and extending the Java Collections Framework.
Date-Time APIs — How to use the java.time pages to write date and time code.
```

한 번 다 훑었다!

leftover...

/**/ 멀티라인 되나? 
/***/ 으로 자바독 생성해보기

i +3 을 한다고 i가 바뀌진 않지만 i++ => i = 1 + i => i += 1

이렇게 표시하니까 헷갈린다..포스트 픽스가 가장 우선 순위가 낮은거 아니야? evaluate 할 때 기준인가?(이전에 포스트 픽스가 있었으면 먼저 계산하고 들어가니?)

스위치 스테이트 익스프레션 블럭 라벨 따위가 뭘 가르키는디

statement expression 차이

varargs 쓸 때 마지막 파라미터에 값 안넘겨도 되나? including none!

%n은 뭐지?

파라미터로 스트링 받아서 변환하기 이 전값도 바뀌나!

primitive type도 로컬 밸류일때 이니셜라이징 안굄??

이니셜라이즈의 의미

스태틱을 쓰는건 클래스 하나에 고정된 값을 쓰고 싶다는 것..오호..

프라이빗 스태틱도 어떨 때 쓰는지 조금 알겠다. 클래스 변수(그러니까 값이 한 번만 저장되는) 이지만 맘대로 바꾸면 안되는

고정된 스트링 같은 경우는 스태틱(private static으로 쓰는게 맞겠구나)

어짜피 값 바뀌면 다시 컴파일 해야하는거 아닌가?! 왜 굳이 노트로 해놨는지 이해가 안된다

스태틱 메서드도 상속이 되나?

protected static?

nested class에 대해서 읽어봄적은 있지만 낯선느낌? 개인적으로 별로 안좋아하는듯?

static nested class 는 outer 클래스의 클래스 변수레 다이렉트로 접근가능한가?

member method에서 스태틱 변수 바로 참조 되나?

static methods의 local class도 스태틱 변수 선언 안되겠지?

익명클래스 멤버변수항당 안됨?

-------절취선 이넘 시작

오브젝트의 프라이빗 메소드는 스태틱 메서드에서 접근 못하나?

인스턴스 메소드에서 그 인스턴스의 프라이빗 변수를 바로 참조 가능한가?

어렵다는 이유로 살짝 봤던(?) 내용은 역시 부족한 부분이 많다. 새롭다ㅡ

-------절취선 어노테이션 시작

can be 인가 should be 인가

type annotation?

annotation type이라는건 그냥 한 형태의 어노테이션. 하나의 어노테이션을 말하는 듯. 클래스 선언하는 것도 클래스 타입을 선언한다고 표현하나?

can be 인가 should be 인가 -> can be. 거기 있는 걸 쓸 수도 있고 @interface 이용해서 만들 수도 있고ㅡ

어노테이션의 @와 자바독의 @를 어떻게 비교하나?
주석 유무?

어노테이션은 강제하지 않는다. 도와줄 뿐이다.

그러니까 실제 문제가 다 해결된다고/됐다고 보면 안된다.

@Nonnull은 헬퍼인데 @schedule은 음..헬퍼지

기능에 영향을 주나 아니나의 차이를 판별하는게 쉽지 않다..


어노테이션이 없을 때 원하는 기능이 실행되느냐 아닌가의 문제일까?

@Deprecated 가 @deprecated 없어도 동작은 되나

nested type?

인터페이스에 메소드 이름 같은애 있으면??


이해가 잘 안감. 복수의 구현 상속(?) 사실 변수도 같은 맥락에서 상속하면 되는 거 아님?

hide and override what is the difference?

interface의 메소드 같은게 암묵적으로 public인건 접근 범위가 어짜피 인터페이스 자체의 접근범위와 동일하게 되기 때문인가?


인터페이스는 오픈되는 인터랙션의 대응이므로
퍼블릭인게 맞는 것 같기도 원래 의도 상?

naming strategy 클래스 살펴보기

메소드 시그니처 같은데 리턴타입 다른 메소드 선언이 가능한가...

hide와 override 는 뭐가 다른거임 ㅋ 변수 처리를 어떻게 할 것인가가 언어 설계의 큰 고민중 하나인듯

clonable 은 메소드 없는 인터페이스인가

더블이 소수점 아닌갚

Long Integer 는 서로 형변환이 자동으로 되지 않는구나
primitive 타입만 그렇고..

래퍼 클래스를 == 비교했는데 특정 숫자까지만 객체 주소가 아니라 밸류로 비교해서 됐었던 거니 다른 이야기

string으로 변환하는 세개 중에 뭘쓰지?

오토박싱/언박싱이 안될때는?

그냥 1 + newInteger(2) 도 되나

ㅡㅡㅡ제네릭
제네틱 타입 아규먼트 안남기면 어케됨

?을 Object로 인식하면 E도 Object로 인식하면 되지 않나


와일드 카드 자체가 뭐든지 될 수 있고 난 알 수 없어 = 마치 제네릭이 없는 거랑 같은 로 타입?

컴파일타임에 제네릭 타입 정보가 사라진다.

----io
스트림의 하이어라키

해쉬 그런애드 차이


이퀄스가 값 같으먄 된다고?
retain remove 이런 것을 집합 연산이랑 연결하는데 재밌었다


컬렉션 이름질 때 최종 결과물이 뭐냐 혹은 뭘 담기 위한 거냐에 따라 하는군

컴패러블 doc 읽어보래 컴페어투 메소드의 조겅!


트리셋은 컴패어블 구현된애만 엘리먼트로 갖나?

sorted set이 변경되면 subset이 바뀌나? 아님 그대로인가?  변경될 수 있다는 건 어떤 의미일까?
셋은 애드할 때 이퀄스로 비교하나?


솔티드 셋은 이퀄스가 폴스여도 컴페어블이 0이면 애드 안되나?

iteratio time이 의미하는 것이 무엇인지

해시셋은 카파시티에 영향을 받고 링크드해시셋과 트리셋은 영향를 안받는다는게 어떤 음이니지

구아바캐시가 무슨 맵으러 되어있었지

enum key가 뭐지

bound / backed by

java의 null은 false 인가?

callable도 thread 상속했너

fixed thread는 쓰레드 재사용하능건가? 그러다가 중간에 terminate 되면 죽는거?

재사용 안하면..시스템이 허용하는 만큼만 쓰레드를 생산하는 장점은 있겠지만

메모리 관리에 대한 비용은 여전힌 것 아닌가(물론 그조차 감당 가능한 정도로만 하겠지만)

thread executor를 왜 새로 만드셔ㅛ을까?

folk/join을 쓰면 진짜 멀티 프로세스로 움직이나?

아토믹 배리어블

원래 인트 더하기 빼기...가 아니라 롸이트 리드가 아토믹 하다는 거였ㄱ 나...






