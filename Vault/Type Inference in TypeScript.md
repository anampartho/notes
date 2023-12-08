07-12-2023 11:05 PM

Status: #idea
Tags: #typescript 

# Type Inference in TypeScript

In [[Reference Notes/TypeScript|TypeScript]] there are several places where [[Type Inference]] is used to determine the type of a variable, when there is no [[Explicit Type Annotation]].

For example,

```ts
const b = 'another string';
```

The type of the variable `a` is inferred to be `string`. Because, we have initialized the variable `a` with the value `another string`, [[Reference Notes/TypeScript|TypeScript]] will infer the type of the variables type as `string`.

When [[Type Inference]] is made from several expressions, then the types of those expressions are used to calculate the inferred type of the variable. For example:

```ts
const arr = ['hello', 'world', 21];
```

the type of the array `arr` will be inferred as `(string|number)[]` because, inside the array, we have set data which are of type `string` and `number`.

## Contextual Typing

[[Type Inference]] in typescript can also work in "the other direction as well".

For example, in the following example, [[Reference Notes/TypeScript|TypeScript]] will throw an error, because, on the `console.log`, [[Reference Notes/TypeScript|TypeScript]] infers the type of the argument `mouseEvent` based on `window.onmousedown`. So here, the type is inferred on the right side based on the left side of the expression.

```typescript
window.onmousedown = function (mouseEvent) {
	console.log(mouseEvent.button);
	console.log(mouseEvent.kangaroo);
};
```


---
# References

1. [Type Inference](https://www.typescriptlang.org/docs/handbook/type-inference.html)