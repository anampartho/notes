#java #variable #programming-language

Java is a strongly typed language. To declare a variable we need to specify its type:

```java
int a = 1;
String name = 'Tashrik';

// Declaration
int dataValue;

// assignment
dataValue = 30;

// initialization (don't run this line, it will cause error)
int dataValue = 30;
```

Variables' names can contain letters and numbers, but they cannot start with a number.

Java permits its user to change a value of a variable:

```java
int dayOfWeek = 2;

dayOfWeek = 3;
```

But to make a variable unchangeable, we use the `final` keyword:

```java
final int currentCentury = 21;

currentCentury = 22;
// ERROR: java: cannot assign a value to final variable a
```

Redeclaring a variable is not allowed:

```java
int a = 10;

int a = 20;
// ERROR: java: variable a is already defined in method main(java.lang.String[])
```