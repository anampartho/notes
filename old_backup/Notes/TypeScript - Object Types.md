#types #typescript #todo

Objects are different in typescript and in js. In typescript `object types` are used to represent javascript objects.

In the following example, we see `anonymous` and `named` typescript `object types`:

```typescript
// Anonymous
const greet = (person: {name: string; age: number}) {
	return `Hello ${person.name}`;
}

// Named using an interface
interface Person {
	name: string;
	age: number;
}

const greet = (person: Person) {
	return `Hello ${person.name}`;
}

// Named using a type
type Person = {
	name: string;
	age: number;
}

const greet = (person: Person) {
	return `Hello ${person.name}`;
}
```

## See Also
1. [Object Types](https://www.typescriptlang.org/docs/handbook/2/objects.html)