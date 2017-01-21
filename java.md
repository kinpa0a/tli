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
