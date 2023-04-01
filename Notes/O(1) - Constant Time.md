#time-complexity #big-o 

**`O(1)`** or **`constant time`** means that the algorithm takes the same time to run regardless of the data size.

## Code Examples
---
##### Finding the first item on an array:

```javascript
const myArr = [1, 2, 3]
console.log(myArr[0])
```

_Here, no matter how big **`myArr`** is, finding the first element of the array will always take the same amount of time. So, accessing the first item of an array has an `O(1)` time complexity or the algorithm is said to be **`constant time`** or **`O(1) time`**._

##### Adding an item to an array:

```javascript
const myArr = [0, 1, 2]
myArr.push(3)
```

_In this code snippet, no matter how big **`myArr`** is, adding a new element to the array will always take the same time. So, adding a new item to an array has an `O(1)` time complexity, or the algorithm is said to be **`constant time`** / **`O(1) time`**._


## See Also
1. [Constant Complexity - O(1)](https://www.educative.io/courses/mastering-data-structures-and-sorting-algorithms-in-javascript/YMMOjJAvAlA)
2. [Big O Notations](https://youtu.be/V6mKVRU1evU?t=234)