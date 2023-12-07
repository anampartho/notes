06-12-2023 11:36 PM

Status: #idea
Tags: #typescript 

# Why use TypeScript?

## To clarify the intent of the author

By default, we can write good [[JavaScript]] code. But the problem is, when a someone else comes into the codebase, they might not know about the intent of the author of the code. Which can introduce some mistakes.

For example, the following code can be confusing to someone who does not know about the intent of the author:

```js
function add(a, b) {
	return a + b;
}
```

What does this mean? Are `a` and `b` both `string`? Or are they `number`s? What if someone makes the following changes to the codebase?

```js
function add(a, b, c = 0) {
	return a + b + c;
}
```

What if the main intent of this function was to concatenate two strings?

[[Reference Notes/TypeScript|TypeScript]] can provide a simple way out:

```ts
function add(a: number, b: number): number {
	return a + b;
}
```

The above code clearly defines that both the argument `a` and `b` are of type `number` and the function will also return a value which will be of type `number`. So the new person, will get a clear understanding on how this function should be changed if needed.

## Has potential to move some kinds of errors from [[runtime]] to [[compile time]]

1. `null` or `undefined` values
2. Breaking of internal code contracts

## Foundation for great code authoring experience

In-editor completion etc.

---
# References

1. [[TypeScript Fundamentals, v3#Introduction]]