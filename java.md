https://docs.oracle.com/javase/tutorial

https://docs.oracle.com/javase/tutorial/java/nutsandbolts/datatypes.html

* Primitive values do not share state with other primitive values.
* In Java SE 8 and later, you can use the int data type to represent an unsigned 32-bit integer, which has a minimum value of 0 and a maximum value of 2^32-1. Use the Integer class to use int data type as an unsigned integer. long same as int. ex) divideUnsigned
* float should never be used for precise values, such as currency. For that, you will need to use the java.math.BigDecimal class instead.
* (??) This data type represents one bit of information, but its "size" isn't something that's precisely defined.
* Enclosing your character string within double quotes will automatically create a new String object. String objects are immutable, which means that once created, their values cannot be changed.
* Data Type	Default Value (for fields)
byte	0
short	0
int	0
long	0L
float	0.0f
double	0.0d
char	'\u0000'
String (or any object)  	null
boolean	false

* Local variables are slightly different; the compiler never assigns a default value to an uninitialized local variable. Accessing an uninitialized local variable will result in a compile-time error.
* A literal is the source code representation of a fixed value; literals are represented directly in your code without requiring computation.
* long : use the upper case letter L because the lower case letter l
* literal (weird..)
int i1 = 1;
int i2 = 1L; (x)

long l1 = 1;
long l2 = 1L;

float f1  = 123.4; (x)
float f2  = 123.4F;

double d1 = 123.4;
double d2 = 123.4F;

* Always use 'single quotes' for char literals and "double quotes" for String literals.
* (??) Unicode escape sequences may be used elsewhere in a program (such as in field names, for example), not just in char or String literals.
* In Java SE 7 and later, any number of underscore characters (_) can appear anywhere between digits in a numerical literal. This feature can improve the readability of your code.


https://docs.oracle.com/javase/tutorial/java/nutsandbolts/arrays.html

* Sorting an array into ascending order. This can be done either sequentially, using the sort method, or concurrently, using the parallelSort method introduced in Java SE 8. Parallel sorting of large arrays on multiprocessor systems is faster than sequential array sorting.
  * http://stackoverflow.com/questions/17328077/difference-between-arrays-sort-and-arrays-parallelsort : 정확히 이해는 안됨
* (Good!) Becoming familiar with common compiler errors will make it easier to recognize bugs in your code.


https://docs.oracle.com/javase/tutorial/java/nutsandbolts/operators.html

* The code result++; and ++result; will both end in result being incremented by one. The only difference is that the prefix version (++result) evaluates to the incremented value, whereas the postfix version (result++) evaluates to the original value.
  * 이렇게 적어놓고 https://docs.oracle.com/javase/tutorial/java/nutsandbolts/operators.html <- 여기에 있는 표에는 postfix가 제일 우선 순위가 높다고 나와 있어서 헷갈렸다. 같은 줄에 있을 때 postfix가 prefix보다 먼저 연산된다는 의미가 아니라 expression을 평가(evaluation)하는 시점 기준으로 이전에 특정 변수에 postfix로 ++나 --가 붙어 있을 경우 먼저 연산이 일어난다는 의미인 것 같다.
* (?? negates an expression) The Unary Operator "-" : Unary minus operator; negates an expression
* The instanceof operator compares an object to a specified type. You can use it to test if an object is an instance of a class, an instance of a subclass, or an instance of a class that implements a particular interface.
* null is not an instance of anything
* (?? 비트연산 잘 모르겠다) The unsigned right shift operator ">>>" shifts a zero into the leftmost position, while the leftmost position after ">>" depends on sign extension.

https://docs.oracle.com/javase/tutorial/java/nutsandbolts/expressions.html
