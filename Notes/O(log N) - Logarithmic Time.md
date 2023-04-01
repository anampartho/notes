#time-complexity #big-o #needs-review

In **`O(log N)`** time complexity, as the input size grows, the number of operations decreases.

In the Binary Search algorithm, the data passed to the algorithm decreases by roughly 50% each time through the algorithm. Because of which, this algorithm has a time complexity of **`O(log N)`**

## Code Examples
---
##### Binary Search

```javascript
const binarySearch = (sortedArray, key) => {
    let start = 0;
    let end = sortedArray.length - 1;

    while (start <= end) {
        let middle = Math.floor((start + end) / 2);

        if (sortedArray[middle] === key) {
            return middle;
        } else if (sortedArray[middle] < key) {
            start = middle + 1;
        } else {
            end = middle - 1;
        }
    }
	// key wasn't found
    return -1;
}
```

_In binary search, everytime the loop runs, the data is cut into half. Which is why binary search jas a time complexity of **`O(log N)`**_

## See Also
1. [Big O Notations](https://youtu.be/V6mKVRU1evU?t=691)
2. [Logarithms and Exponents in Complexity Analysis](https://towardsdatascience.com/logarithms-exponents-in-complexity-analysis-b8071979e847)
3. [[Binary Search]]