# Details

Given a number n, find the sum of the first natural numbers.

**Example 1:**

```
Input: 3
Output: 6
Explanation: 1 + 2 + 3 = 6
```

**Example 2:**

```
Input: 5
Output: 15 
Explanation: 1 + 2 + 3 + 4 + 5 = 15
```

# Solution

```java
public class Main {
	public static void main(String[] args) {
		System.out.println(sum(5));
		// Output: 15
	}

	public static double sum(int n) {
		if (n > 0) {
			return n + sum(n - 1);
		}

		return 0;
	}
}
```

```javascript
/**
 * @param {number} n
 * @return {number}
 */
var sum = function(x, n) {
    if (n > 0) {
        return n + sum(n - 1);
    }

	return 0;
};
```

```python
class Solution:
    def sum(self, n: int) -> int:
        if > 0:
            return n + self.sum(n - 1)

		return 0
```