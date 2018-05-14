# TypeScript

## Type annotations

Type annotations in TypeScript are lightweight ways to record the intended contract of the function or variable. In this case, we intend the greeter function to be called with a single string parameter.

TypeScript will let you know that you have called a function with an unexpected number of parameters. TypeScript can offer static analysis based on both the structure of your code, and the type annotations you provide.

```js
function greeter(person: string) {
  return 'Hello, ' + person;
}

let user = 'Jane User';

document.body.innerHTML = greeter(user);
```

## Interfaces

Let’s develop our sample further. Here we use an interface that describes objects that have a firstName and lastName field. In TypeScript, two types are compatible if their internal structure is compatible. This allows us to implement an interface just by having the shape the interface requires, without an explicit implements clause.

```js
interface Person {
  firstName: string;
  lastName: string;
}

function greeter(person: Person) {
  return 'Hello, ' + person.firstName + ' ' + person.lastName;
}

let user = { firstName: 'Jane', lastName: 'User' };

document.body.innerHTML = greeter(user);
```

## Resources

* [TypeScript in 5 minutes](http://www.typescriptlang.org/docs/handbook/typescript-in-5-minutes.html)
