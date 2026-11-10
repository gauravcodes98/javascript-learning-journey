# 🚀 Day 02: Data Types in JavaScript

![JavaScript](https://img.shields.io/badge/JavaScript-Learning-yellow?style=for-the-badge&logo=javascript)
![Day](https://img.shields.io/badge/Day-02-blue?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)

## 📖 Introduction

In Day 02 of my JavaScript learning journey, I studied how JavaScript handles different types of values, how variables work, and how data is stored and accessed in memory.

## 📚 Topics Covered

1. Why Do We Need Data Types?
2. JavaScript and Dynamic Typing
3. Variables in JavaScript (`var`, `let`, `const`)
4. Primitive Data Types
5. Object Type (Non-Primitive)
6. Value vs Reference
7. The `typeof` Operator

---

## 1. Why Do We Need Data Types?

Computer memory stores information in bytes (0s and 1s). But the same binary data can represent different things depending on how it is interpreted.

For example, `01001000` could represent:

- Number 72
- Character 'H'
- Part of a memory address
- A boolean value, depending on representation

**That's why Data Types are important.**

A data type tells the computer:

1. How many bytes may be used for a value.
2. What operations make sense on that value.

## 2. JavaScript and Dynamic Typing

In Java, we declare the data type before using a variable:

```java
int x = 5;
```

JavaScript is a **Dynamically Typed Language**.

This means:
- We don't need to explicitly declare the data type.
- A variable can hold different types of values.
- The type is determined at runtime.

Example:

```javascript
let value = 5;
console.log(value); // 5

value = "Hello";
console.log(value); // Hello
```

## 3. Variables in JavaScript

JavaScript provides three main keywords to declare variables:

- `var`
- `let`
- `const`

### A. const

`const` declares a block-scoped variable whose reference cannot be reassigned.

**Features:**

1. Scope: Block Scope.
2. Reassignment: Not allowed.
3. Initialization: Mandatory.
4. Hoisting: Hoisted but not initialized; remains in the Temporal Dead Zone (TDZ).
5. Mutability: Object properties and array elements can still be modified.

Example:

```javascript
// Block Scope
if (true) {
  const PI = 3.14159;
}

// console.log(PI); // ReferenceError

// Reassignment
const GREETING = "Hello";
// GREETING = "Hi"; // TypeError

// Mutability
const CONFIG = { port: 8080 };
CONFIG.port = 3000;

console.log(CONFIG.port); // 3000

// Temporal Dead Zone
// console.log(MY_CONST); // ReferenceError
const MY_CONST = 100;
```

### B. let

`let` declares a block-scoped variable that can be reassigned.

**Features:**

1. Scope: Block Scope.
2. Reassignment: Allowed.
3. Initialization: Optional.
4. Default Value: `undefined` if not initialized.
5. Hoisting: Hoisted but not initialized; remains in TDZ.

Example:

```javascript
// Block Scope
for (let i = 0; i < 3; i++) {
  // i is available inside this block
}

// console.log(i); // ReferenceError

// Reassignment
let counter = 0;
counter = 1;

console.log(counter); // 1

// Initialization
let name;
console.log(name); // undefined

name = "Alice";

// Temporal Dead Zone
// console.log(myLetVar); // ReferenceError
let myLetVar = "test";
```

### C. var

`var` declares a function-scoped or globally scoped variable.

**Features:**

1. Scope: Function Scope.
2. Reassignment: Allowed.
3. Redeclaration: Allowed.
4. Initialization: Optional; defaults to `undefined`.
5. Hoisting: Declaration is hoisted and initialized with `undefined`.

Example:

```javascript
// Function Scope (not Block Scope)
if (true) {
  var leak = "I am visible outside the if-block";
}

console.log(leak);

// Hoisting
console.log(myVar); // undefined

var myVar = "Hello";

console.log(myVar); // Hello

// Redeclaration
var x = 10;
var x = 20;

console.log(x); // 20
```

### Difference Between var, let and const

| Feature | var | let | const |
|---|---|---|---|
| Scope | Function | Block | Block |
| Reassignable | Yes | Yes | No |
| Redeclarable | Yes | No | No |
| Hoisted Value | undefined | TDZ | TDZ |
| Global Object | Attaches to window | Does not attach | Does not attach |
| Modern Practice | Avoid | Reassignable values | Default choice |

---

## 4. Primitive Data Types

Primitive data types are fundamental and immutable values.

JavaScript has seven primitive data types.

### 1. String

Represents textual data.

Strings can use single quotes, double quotes, or backticks.

```javascript
let name = "Alice";
let greeting = 'Hello, World!';
let template = `User: ${name}`;

console.log(name);
console.log(greeting);
console.log(template);
```

### 2. Number

Represents integer and floating-point numbers.

Special values include:
- Infinity
- -Infinity
- NaN (Not a Number)

```javascript
let integerValue = 100;
let floatValue = 3.14;
let notANumber = NaN;
let infinity = Infinity;

console.log(integerValue);
console.log(floatValue);
console.log(notANumber);
console.log(infinity);
```

### 3. Boolean

Represents two possible values: `true` or `false`.

```javascript
let isActive = true;
let isComplete = false;

console.log(isActive);
console.log(isComplete);
```

### 4. Undefined

Represents an unassigned value.

```javascript
let user;

console.log(user); // undefined
```

### 5. Null

Represents the intentional absence of an object value.

```javascript
let data = null;

console.log(data); // null
```

**Difference between null and undefined:**

| undefined | null |
|---|---|
| Value is not assigned | Intentional absence of value |
| Automatically occurs in uninitialized variables | Explicitly assigned by developer |

### 6. BigInt

Represents integers larger than the maximum safe integer value that the Number type can represent exactly.

```javascript
const veryLargeNumber = 9007199254740991n;

const anotherBigInt = BigInt(9007199254740992);

console.log(veryLargeNumber);
console.log(anotherBigInt);
```

### 7. Symbol

Represents a unique identifier. Symbols can be used as unique object property keys.

```javascript
const id1 = Symbol('id');
const id2 = Symbol('id');

console.log(id1 === id2); // false
```

---

## 5. Object Type (Non-Primitive)

An object is a mutable collection of key-value pairs (properties).

Unlike primitive values, variables assigned to objects hold a reference to the object's location in memory.

### A. Object Literals

```javascript
let person = {
  firstName: "John",
  lastName: "Doe",
  age: 30
};

console.log(person);
```

### B. Arrays

Arrays are specialized objects used for ordered collections.

```javascript
let numbers = [10, 20, 30, 40];

console.log(numbers);
```

### C. Functions

Functions are also special objects in JavaScript.

```javascript
function greet() {
  console.log("Hello");
}

greet();
```

### Other Built-in Objects

- Date
- RegExp
- Map
- Set

---

## 6. Value vs Reference

This is an important distinction between primitive and object types.

### A. Primitive Values are Assigned by Value

When a primitive value is assigned to another variable, its value is copied.

```javascript
let a = 10;
let b = a;

b = 20;

console.log(a); // 10
console.log(b); // 20
```

Changing `b` does not affect `a`.

### B. Objects are Assigned by Reference

When an object is assigned to another variable, the reference is copied. Both variables point to the same object.

```javascript
let obj1 = { value: 10 };

let obj2 = obj1;

obj2.value = 20;

console.log(obj1.value); // 20
console.log(obj2.value); // 20
```

Changing the object through `obj2` is also visible through `obj1`.

### Comparison

| Primitive | Object |
|---|---|
| Value is copied | Reference is copied |
| Independent values | Can share the same object |
| Examples: String, Number, Boolean | Examples: Object, Array |

---

## 7. The typeof Operator

The `typeof` operator is used to determine the data type of a variable or value at runtime.

**Syntax:**

```javascript
typeof value;
```

### Examples

```javascript
typeof "Hello";       // "string"
typeof 42;            // "number"
typeof true;          // "boolean"
typeof undefined;     // "undefined"
typeof 10n;           // "bigint"
typeof Symbol('id');  // "symbol"

typeof { a: 1 };      // "object"
typeof [1, 2, 3];     // "object"
typeof function(){}; // "function"
typeof null;          // "object"
```

### Important Observations

- `typeof` returns a string.
- Arrays return `"object"`.
- Functions return `"function"`.
- `typeof null` returns `"object"` due to a historical JavaScript behavior.

---

## 8. Key Learnings

After completing this lecture, I understood:

- Why data types are required.
- How JavaScript handles dynamic typing.
- The differences between `var`, `let`, and `const`.
- Block scope and function scope.
- Hoisting and Temporal Dead Zone (TDZ).
- All seven primitive data types.
- Objects, arrays, and functions.
- Difference between value and reference.
- How to use the `typeof` operator.

## 📈 Learning Progress

| Day | Topic | Status |
|---|---|---|
| Day 01 | Introduction to JavaScript | ✅ Completed |
| Day 02 | Variables and Data Types in JavaScript | ✅ Completed |
| Day 03 | Upcoming Lecture | ⏳ |

## 👨‍💻 About Me

**Gaurav Sharma**

B.Tech CSE Student | JavaScript Learner

GitHub: [@gauravcodes98](https://github.com/gauravcodes98)

## 🎯 Learning Philosophy

**Learn → Understand → Practice → Build → Repeat**

Building strong programming fundamentals through daily learning and hands-on practice.

#JavaScript #DataTypes #WebDevelopment #LearningInPublic #CodingJourney
