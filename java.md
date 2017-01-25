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

An *expression* is a construct made up of variables, operators, and method invocations that evaluates to a single value.
A *statement* forms a complete unit of execution.
A *block* is a group of zero or more statements between balanced braces.

* state의 개념이 매우 모호하다.

https://docs.oracle.com/javase/tutorial/java/nutsandbolts/flow.html

* Deciding when to omit the braces is a matter of personal taste. Omitting them can make the code more brittle.
 * = 안써도 되긴한데 헷갈릴거야(?)
* if state - Once a condition is satisfied, the appropriate statements are executed and the remaining conditions are not evaluated.
* the switch statement can have a number of possible execution paths. 
* possible switch expression : with the byte, short, char, int, Enum Types, String, Character, Byte, Short, and Integer
* A statement in the switch block can be labeled with one or *more* case or default labels.
* An if-then-else statement can test expressions based on ranges of values or conditions, whereas a switch statement tests expressions based only on a single integer, enumerated value, or String object.
*  Each break statement terminates the enclosing switch statement. Control flow continues with the first statement following the switch block.
* Ensure that the expression in any switch statement is not null to prevent a NullPointerException from being thrown.

* (???) switch state 설명할 때 expreission, state, block 등등 다양한 용어를 쓰는데 다른 control flow state 설명할 때와는 다르게 처음에 저런 용어들을 이용해서 포맷을 설명해주지 않아서 무엇을 가르키는지 한참 헤맸다. 
 * ex) 
 while (expression) {
      statement(s)
 }

* If the variable that controls a for statement is not needed outside of the loop, it's best to declare the variable in the initialization expression. The names i, j, and k are often used to control for loops; declaring them within the initialization expression limits their life span and reduces errors. 
* We recommend using this form[for (type element : array)] of the for statement instead of the general form whenever possible.
* The break statement has two forms: labeled and unlabeled.
 * break문에 label 있다는 사실을 처음 알았다! continue에도 있다!
* An unlabeled break statement terminates the innermost.
* A labeled break terminates the outer.
* You can use an unlabeled break to terminate a switch, or, while, or do-while loop.

* (???) 아래 구문의 흐름을 완전 잘못 읽어냈다. else는 가장 가까운(?) if문에 연결되는구나!
if (aNumber >= 0)
    if (aNumber == 0)
        System.out.println("first string");
else System.out.println("second string");
System.out.println("third string"); 

* to make the control flow easier to understand : spaces, line breaks and braces.
