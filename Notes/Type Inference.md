#types #typescript 

The automatic detection of the type of an expression is called `type inference`.

## Common Example in TypeScript

In typescript, we can declare the type of a variable by using a `:`. It is called a explicit type annotation. At the same time, we do not need to do that, as typescript will infer the type of a variable based on its value. 

```typescript
// Setting the type of 'a' to a string by a manual type annotation
const a: string = 'a string';

// Inferring the type
const b = 'another string'; // it is same as const b: string = 'another string'
```

## Contextual Typing

Type inference in typescript can also work in "the other direction as well".

For example, in the following example, typescript will throw an error, because, on the console logs, typescript infers the type of `mouseEvent` based on `window.onmousedown`. So here, the type is inferred on the right side based on the left side of the expression.

```typescript
window.onmousedown = function (mouseEvent) {
	console.log(mouseEvent.button);
	console.log(mouseEvent.kangaroo);
};
```