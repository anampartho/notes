Recursion is a method, where a complex problem is broken down into smaller problems and based on the solution of those smaller problems the complex is solved. So a solution to a complex problem depends on the solution of the smaller problems derived from the complex problem. 

In basic terms in programming, if a function calls itself inside the function body, then it is called a recursive function. There must be a base condition inside the function body, so that the recursive call to itself can stop. Without the condition, there will be an infinite loop of function calls.

This term is used in mathematics rather frequently. For example:
- $n^{th}$ Factorial:  $n! = n * (n - 1)!$ - here, we find the factorial of $n$ by getting the factorial of $n - 1$ first, and to get the factorial of $n - 1$ it will also try to get the factorial of $n - 2$ so on and so forth. This is a recursive function call.
- $n^{th}$ Fibonacci: $F(n) = F(n - 1) + F(n - 2)$ - in this, the $n^{th}$ fibonacci depends on the fibonacci of $n - 1$ and $n - 2$. So we are breaking down the problem into smaller problems.


## Phases

Recursion has two phases. One is Ascending and Descending phase.

1. In the function body, before calling itself, if there is a statement, that is run at function calling time. This is the ascending phase.
2. If any operation has to be done based on the return value of the function or any other operation has to be done after a function call has ended, that is done on the return time or the descending phase.

## Types of Recursion

1. Tail Recursion
2. Head Recursion
3. Tree Recursion
4. Indirect Recursion
5. Nested Recursion

### Tail Recursion

If a function calls itself, and the recursive call is the last statement of that function and no other operation is remaining, then it is called a tail recursion. Most of the time, loops are better than tail recursion because the space complexity can be lower in loops.

### Head Recursion

If a function calls itself before any other statement, then it is a head recursion.

### Tree Recursion

If a function has more than one call to itself then it is called a tree recursion.

### Indirect Recursion

If two or more functions call each other an create a cycle, then it is a nested recursion. For example, `function a` calls `function b` and `function b` calls `function c` and ultimately `function c` calls `function a` then it is a nested recursion.

### Nested Recursion

If a recursive function passes a parameter as a recursive call, then it is a nested recursion.


## Code Examples

1. [[Factorial of n]]

### Find sum of  `0` to `n`

- Java:

```java
public class Main {
	public static void main(String[] args) {
		System.out.println("Sum of 0 to 10 is " + sum(10));
		// Output: Sum of 0 to 10 is 55
	}

	public static int sum(int n) {
		if (n > 0) {
			return n + sum(n - 1);
		}

		return 0;
	}
}
```

- JS:

```javascript
const sum = (n) => {
	if (n > 0) {
		return n + sum(n - 1);
	}

	return 0;
}

console.log(`Sum of 0 to 10 is ${sum(10)}`);
// Output: Sum of 0 to 10 is 55
```

- Python:

```python
def sum(n):
	if n > 0:
		return n * sum(n - 1)

	return 1

num = 10
print("Sum of 0 to ", num, " is ", sum(num))
# Output: Sum of 0 to 10 is 55
```