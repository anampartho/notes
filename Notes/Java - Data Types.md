#java #data-types #programming-language 

# Primitive Data Types

These are the data types which are built into the Java Programming Language. There are mainly four categories of primitive data types in java.

1. Integer
2. Floating Point
3. Character
4. Boolean

## Integer Types

These types only contain rounded numbers. No decimal numbers are allowed. The difference between each type is the amount of data they can store (Please don't try to memorize the min and max values!).

Reminder: To mark a long integer, we need to add `L` after the value.

| Type      | Bits | Min Value       | Max Value          | Literal Form |
| --------- | ---- | --------------- | ------------------ | ------------ |
| **byte**  | 8    | -128            | 127                | 0            |
| **short** | 16   | -32768          | 32767              | 0            |
| **int**   | 32   | -2147483648     | 2147483647         | 0            |
| **long**  | 64   | -2<sup>63</sup> | 2<sup>63</sup> - 1 | 0L           |

```java
byte maxItems = 20;
short currentSalary = 10000;
int yearlySalary = 120000;
long ditanceToNextGalaxy = 2147483648L; // This is not the distance to the next galaxy!
```

## Floating Point Types

These types only contain decimal values. These cannot contain rounded numbers. This is why these types are called floating-point types. The difference between `float` and `double` is the Smallest Positive Value and Largest Positive Value.

| Type       | Bits | Smallest Positive Value | Largest Positive Value | Literal Form |
| ---------- | ---- | ----------------------- | ---------------------- | ------------ |
| **float**  | 32   | 1.4X10<sup>-45</sup>    | 3.4X10<sup>38</sup>    | 0.0f         |
| **double** | 64   | 4.9X10<sup>-324</sup>   | 1.7X10<sup>308</sup>   | 0.0 or 0.0d             |

```java
float valueOfpi = 3.1415f;
double valueOfPiMoreAccurate = 3.141592653589793;

```


## Character Data Types

This type only contains a single Unicode character or its Unicode value.

```java
char firstCharMyName = 'T';
char letterT = '\u0054'; // T

```


## Boolean Types

This only contains the literal value `true` or `false`.

```java
boolean notUnderstandingJava = true;
boolean isJavaEasy = false;

```