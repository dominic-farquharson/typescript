# TypeScript

* TypeScript is a language for application-scale JavaScript. TypeScript adds optional types, classes, and modules to JavaScript. TypeScript supports tools for large-scale JavaScript applications for any browser, for any host, on any OS. TypeScript compiles to readable, standards-based JavaScript.
* TypeScript is an open-source programming language developed and maintained by Microsoft. It is a strict syntactical superset of JavaScript, and adds optional static typing to the language.

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

## Classes

Finally, let’s extend the example one last time with classes. TypeScript supports new features in JavaScript, like support for class-based object-oriented programming.

Here we’re going to create a Student class with a constructor and a few public fields. Notice that classes and interfaces play well together, letting the programmer decide on the right level of abstraction.

Also of note, the use of public on arguments to the constructor is a shorthand that allows us to automatically create properties with that name.

```js
class Student {
    fullName: string;
    constructor(public firstName: string, public middleInitial: string, public lastName: string) {
        this.fullName = firstName + " " + middleInitial + " " + lastName;
    }
}

interface Person {
    firstName: string;
    lastName: string;
}

function greeter(person : Person) {
    return "Hello, " + person.firstName + " " + person.lastName;
}

let user = new Student("Jane", "M.", "User");

document.body.innerHTML = greeter(user);
```

## Resources

* [TypeScript in 5 minutes](http://www.typescriptlang.org/docs/handbook/typescript-in-5-minutes.html)
* [TypeScript repo](https://github.com/Microsoft/TypeScript)
