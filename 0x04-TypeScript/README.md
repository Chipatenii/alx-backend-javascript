# TypeScript Learning Objectives

## Introduction

This project outlines the key learning objectives for mastering TypeScript, covering basic types, interfaces, classes, functions, DOM manipulation, generic types, namespaces, declaration merging, ambient namespaces, and basic nominal typing.

## Table of Contents

1. [Basic Types in TypeScript](#basic-types-in-typescript)
2. [Interfaces, Classes, and Functions](#interfaces-classes-and-functions)
3. [Working with the DOM and TypeScript](#working-with-the-dom-and-typescript)
4. [Generic Types](#generic-types)
5. [Namespaces](#namespaces)
6. [Merging Declarations](#merging-declarations)
7. [Ambient Namespace for Importing External Libraries](#ambient-namespace-for-importing-external-libraries)
8. [Basic Nominal Typing with TypeScript](#basic-nominal-typing-with-typescript)

## Basic Types in TypeScript

Understanding and using the basic types in TypeScript, such as `number`, `string`, `boolean`, `array`, `tuple`, `enum`, `any`, `void`, `null`, and `undefined`.

```typescript
let isDone: boolean = false;
let decimal: number = 6;
let color: string = "blue";
let list: number[] = [1, 2, 3];
let tuple: [string, number];
tuple = ["hello", 10];
```

## Interfaces, Classes, and Functions

Defining and implementing interfaces, creating classes with properties and methods, and writing functions with type annotations.

```typescript
interface Person {
  firstName: string;
  lastName: string;
}

class Student implements Person {
  constructor(public firstName: string, public lastName: string) {}
}

function greeter(person: Person) {
  return "Hello, " + person.firstName + " " + person.lastName;
}
```

## Working with the DOM and TypeScript

Manipulating the Document Object Model (DOM) using TypeScript, including accessing and modifying HTML elements.

```typescript
const button = document.createElement('button');
button.textContent = "Click me";
button.onclick = () => alert("Button clicked");
document.body.appendChild(button);
```

## Generic Types

Using generics to create reusable and flexible components, functions, and classes that work with a variety of data types.

```typescript
function identity<T>(arg: T): T {
  return arg;
}

let output = identity<string>("myString");
let outputNumber = identity<number>(100);
```

## Namespaces

Organizing code into logical groups and avoiding name collisions by using namespaces.

```typescript
namespace Geometry {
  export interface Shape {
    area(): number;
  }

  export class Circle implements Shape {
    constructor(public radius: number) {}
    area(): number {
      return Math.PI * this.radius * this.radius;
    }
  }
}

let circle = new Geometry.Circle(10);
console.log(circle.area());
```

## Merging Declarations

Combining multiple declarations into a single entity to extend the functionality of existing code.

```typescript
interface Box {
  height: number;
  width: number;
}

interface Box {
  scale: number;
}

let box: Box = { height: 5, width: 6, scale: 10 };
```

## Ambient Namespace for Importing External Libraries

Utilizing ambient namespaces to import and use external libraries in TypeScript projects.

```typescript
declare namespace SomeLibrary {
  function doSomething(): void;
}

SomeLibrary.doSomething();
```

## Basic Nominal Typing with TypeScript

Applying nominal typing principles to ensure type safety by using unique type identifiers.

```typescript
type USD = { _type: 'USD'; amount: number };
type EUR = { _type: 'EUR'; amount: number };

let priceUSD: USD = { _type: 'USD', amount: 10 };
let priceEUR: EUR = { _type: 'EUR', amount: 10 };

// This will cause a type error
// priceUSD = priceEUR;
```
