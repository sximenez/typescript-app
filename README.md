# TypeScript

JavaScript is a permissive language.

You don't need to declare variable types, it infers them for you based on their values.

The upside: flexibility in code writing and debugging.

The downside: type misinterpretation potentially leading to bugs.

To solve this, TypeScript steps in as a sort of security layer.

It allows to explicitly type variables within JS code.

## Compiling TypeScript

TypeScript files use the `.ts` extension.

```Terminal
tsc greeter.ts
```

This creates a `.js` file with TypeScript functionality.

## Interfaces

An interface specifies the **structure** of an object. **They don't generate code**.

```Typescript
interface Person {
  firstName: string;
  lastName: string;
}

function greeter(person: Person) {
  return "Hello " + person.firstName + person.lastName;
}

let user = { firstName: "hello", lastName: "world" };

document.body.textContent = greeter(user);
```

## Classes

Opposed to interfaces, classes do **generate code**.

Classes are very frequent in _object-oriented programming_ (OOP).

Classes and interfaces "play well together".

By using a constructor with `public` arguments, we can create objects with those properties.

```Typescript
class Student {
  fullName: string;
  constructor(public firstName: string, public lastName: string) {
    this.fullName = firstName + "" + lastName;
  }
}

interface Person {
  firstName: string;
  lastName: string;
}

function greeter(person: Person) {
  return "Hello " + person.firstName + person.lastName;
}

let user = { firstName: "hello", lastName: "world" };

document.body.textContent = greeter(user);
```

Compile to use TS within `.js` files.

## Further notes
