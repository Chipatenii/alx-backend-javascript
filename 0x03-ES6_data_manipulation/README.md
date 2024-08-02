
# ES6 Data Manipulation

## Introduction

This project covers the essential methods and data structures introduced in ES6 for effective data manipulation in JavaScript. The main topics include array methods (`map`, `filter`, and `reduce`), typed arrays, and the `Set`, `Map`, `WeakMap`, and `WeakSet` data structures.

## Table of Contents

1. [Array Methods](#array-methods)
   - [map()](#map)
   - [filter()](#filter)
   - [reduce()](#reduce)
2. [Typed Arrays](#typed-arrays)
3. [Data Structures](#data-structures)
   - [Set](#set)
   - [Map](#map)
   - [WeakMap](#weakmap)
   - [WeakSet](#weakset)

## Array Methods

### map()

The `map()` method creates a new array populated with the results of calling a provided function on every element in the calling array.

```javascript
const numbers = [1, 2, 3, 4];
const doubled = numbers.map(num => num * 2);
console.log(doubled); // [2, 4, 6, 8]
```

### filter()

The `filter()` method creates a new array with all elements that pass the test implemented by the provided function.

```javascript
const numbers = [1, 2, 3, 4];
const evenNumbers = numbers.filter(num => num % 2 === 0);
console.log(evenNumbers); // [2, 4]
```

### reduce()

The `reduce()` method executes a reducer function on each element of the array, resulting in a single output value.

```javascript
const numbers = [1, 2, 3, 4];
const sum = numbers.reduce((accumulator, currentValue) => accumulator + currentValue, 0);
console.log(sum); // 10
```

## Typed Arrays

Typed Arrays provide a mechanism for accessing raw binary data. These arrays are used to handle binary data directly and come in various types like `Int8Array`, `Uint8Array`, `Float32Array`, etc.

```javascript
const buffer = new ArrayBuffer(16);
const int32View = new Int32Array(buffer);
int32View[0] = 42;
console.log(int32View[0]); // 42
```

## Data Structures

### Set

A `Set` is a collection of unique values. Iteration through the elements of a set follows the order of insertion.

```javascript
const set = new Set([1, 2, 3, 4, 4]);
console.log(set); // Set { 1, 2, 3, 4 }
```

### Map

A `Map` object holds key-value pairs and remembers the original insertion order of the keys.

```javascript
const map = new Map();
map.set('a', 1);
map.set('b', 2);
console.log(map.get('a')); // 1
```

### WeakMap

A `WeakMap` is similar to a `Map` but only holds weak references to its keys, which must be objects. This allows for garbage collection if there are no other references to the object.

```javascript
const weakMap = new WeakMap();
const obj = {};
weakMap.set(obj, 'value');
console.log(weakMap.get(obj)); // 'value'
```

### WeakSet

A `WeakSet` is similar to a `Set` but only holds weak references to its objects, allowing for garbage collection.

```javascript
const weakSet = new WeakSet();
const obj = {};
weakSet.add(obj);
console.log(weakSet.has(obj)); // true
```
