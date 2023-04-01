#time-complexity #big-o 

**`O(N)`** or **`linear time`** means that the algorithm's running time will increase linearly with the input size.

So the time to complete the algorithm will grow in direct proportion to the amount of data.

**My Take:** Let's say we have an algorithm with a time complexity of **`O(N)`**. So when **`N = 2`**, then the algorithm will take **`t`** time to run, and when **`N = 4`**, then the algorithm will take **`t * 2`** time to run because the amount of data has doubled and the time complexity grows in direct proportion to the size of the input.

```javascript
const arr1 = ['a', 'b'];
const arr2 = ['a', 'b', 'c', 'd'];
```

Here we can see that **`arr1`** has **`2`** items and **`arr2`** has **`4`**. So if we first pass **`arr1`** and then pass **`arr2`** inside **`findInArray`**, then the algorithm will take twice much time in the case of **`arr2`** to finish in relation to the time taken to finish **`arr1`**.

*If for **`arr1`**, **`findInArray`** takes 2 seconds to run, then for **`arr2`**, **`findInArray`** will take 4 seconds to run. Because the time complexity of **`findInArray`** is **`O(N)`** or **`O(N) time`** or **`linear time`**.*

## Code Examples
---
##### Finding an item in an array (linear search)

```javascript
const arr1 = ['a', 'b'];
const arr2 = ['a', 'd', 'e', 'b'];

const findInArray = (toFind, inArray) => {
	let message = 'Item not found!';
	const startTime = new Date();

	for (let i = 0; i < inArray.length; i++) {
		if (inArray[i] === toFind) {
			message = `Item found at index ${i}!`;
		}
	}

	const endTime = new Date()

	message += ` Time to execute ${endTime - startTime}ms.`

	return message;
}

console.log(findInArray('b', arr1));
console.log(findInArray('b', arr2));

```

*In this code snippet (also known as linear search), if for **`arr1`**, **`findInArray`** takes 2 seconds to run, then for **`arr2`**, **`findInArray`** will take 4 seconds to run (by theory). Because the time complexity of **`findInArray`** is **`O(N)`** or **`O(N) time`** or **`linear time`**.*

## See Also
1. [Big O Notations](https://youtu.be/V6mKVRU1evU?t=295)
2. [Time complexity](https://en.wikipedia.org/wiki/Time_complexity#Linear_time)