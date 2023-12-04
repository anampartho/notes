#leetcode #recursion #loop #medium

# Details

Implement `pow(x, n)`, which calculates `x` raised to the power `n` (i.e., $x^n$).

**Example 1:**

```
Input: x = 2.00000, n = 10
Output: 1024.00000
```

**Example 2:**

```
Input: x = 2.10000, n = 3
Output: 9.26100
```

**Example 3:**

```
Input: x = 2.00000, n = -2
Output: 0.25000
Explanation: 2-2 = 1/22 = 1/4 = 0.25
```

**Constraints:**

-  $-100.0 < x < 100.0$
- $-2^{31} <= n <= 2^{31-1}$
- $n$ is an integer.
- Either $x$ is not zero or $n > 0$.
- $-10^4 <= xn <= 10^4$

# Solution

```java
class Solution {
    public double myPow(double x, int n) {
        if (x == 0) {
            return 0;
        }

        if (n == 0) {
            return 1;
        }

        if (n % 2 == 0) {
            return myPow(x * x, n / 2);
        }

        if (n < 0) {
            return myPow(1/x, -n);
        }

        return x * myPow(x * x, (n - 1) / 2);

    }
}
```

```javascript
/**
 * @param {number} x
 * @param {number} n
 * @return {number}
 */
var myPow = function(x, n) {
    if (n == 0 || x == 1) {
        return 1;
    }

    if (x == 0) {
        return 0;
    }

    if (n % 2 == 0) {
        return myPow(x * x, n / 2);
    }

    if (n < 0) {
        return myPow(1 / x, -n);
    }

    return x * myPow(x * x, (n - 1) / 2);
};
```

```python
class Solution:
    def myPow(self, x: float, n: int) -> float:
        if x == 1 or n == 0:
            return 1
        
        if x == 0:
            return 0
        
        if n % 2 == 0:
            return self.myPow(x * x, n / 2)

        if n < 0:
            return self.myPow(1 / x, -n)
        
        return x * self.myPow(x * x, (n - 1) / 2)
```


## See Also
1. https://leetcode.com/problems/powx-n/