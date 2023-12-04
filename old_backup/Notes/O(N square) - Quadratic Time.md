#time-complexity #big-o 

For the time complexity of $O(n^2)$ an algorithm's time to complete will be proportional to the square of the amount of data.

If we pass $3$ data, then the algorithm will take $3^2$ time to complete.

## Code Examples
---
### Bubble Sort

```javascript
const bubbleSort = (arr) => {
	const len = arr.length;

	for (let i = 0; i < len; i++) {
		for (let j = 0; j < len; j++) {
			if (arr[j] > arr[j + 1]) {
				const temp = arr[j];
				arr[j] = arr[j + 1];
				arr[i] = temp;
			}
		}
	}
}
```

_In this example we see an implementation of **`bubble sort`** using the nested for loop. In this case, the algorithm takes $n^2$ time where $n$ is the length of the array_

## See Also
1. [Big O Notations](https://youtu.be/V6mKVRU1evU?t=532)
2. [[Bubble Sort]]