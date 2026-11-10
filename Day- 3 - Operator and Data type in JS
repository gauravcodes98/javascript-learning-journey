# 🚀 Day 03 – JavaScript Operators, Type Conversion & Comparisons

![JavaScript](https://img.shields.io/badge/JavaScript-ES6%2B-yellow?style=for-the-badge&logo=javascript)
![Day](https://img.shields.io/badge/Day-03-blue?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)

> Day 03 of my JavaScript learning journey. Today, I explored JavaScript operators, type conversion, comparison rules, and how JavaScript handles numbers internally.

## 📚 Topics Covered

1. Primitive vs Object Types – Value vs Reference
2. Introduction to Operators
3. Assignment Operators
4. Arithmetic Operators
5. Comparison Operators
6. Logical Operators
7. Truthy and Falsy Values
8. Bitwise Operators
9. Other Important Operators
10. Operator Precedence
11. Floating-Point Precision in JavaScript
12. Type Conversion (Implicit & Explicit)
13. String, Number and Boolean Conversion
14. Strict vs Loose Equality
15. Relational Comparison Operators

---

## 1. Primitive vs Object Types

JavaScript values are divided into two families:

| Feature | Primitives | Objects |
|---|---|---|
| Stored and copied as | Value | Reference |
| Mutable | No | Yes |
| Comparison | Actual values | Object identity/reference |
| Examples | Number, String, Boolean | Object, Array, Function |

### JavaScript Value Structure

```text
Every JavaScript Value
│
├── Primitive Types (By Value)
│   ├── Number
│   ├── String
│   ├── Boolean
│   ├── Undefined
│   ├── Null
│   ├── BigInt
│   └── Symbol
│
└── Objects (By Reference)
    ├── Object {}
    ├── Array []
    ├── Function
    └── Other Objects
```

---

## 2. Introduction to Operators

An **operator** is a special symbol or keyword used to perform an operation on values.

- **Operator:** Symbol that performs an operation.
- **Operands:** Values on which an operator works.
- **Expression:** Combination of operators and operands that evaluates to a value.

Example:

```javascript
let result = 5 + 10;
console.log(result); // 15
```

Here:
- `+` is the operator.
- `5` and `10` are operands.
- `5 + 10` is an expression.
- `15` is the result.

---

## 3. Assignment Operators

Assignment operators assign values to variables.

### Basic Assignment

```javascript
let score = 100;
```

### Compound Assignment Operators

| Operator | Example | Equivalent |
|---|---|---|
| `=` | `x = y` | Assign y to x |
| `+=` | `x += y` | `x = x + y` |
| `-=` | `x -= y` | `x = x - y` |
| `*=` | `x *= y` | `x = x * y` |
| `/=` | `x /= y` | `x = x / y` |
| `%=` | `x %= y` | `x = x % y` |
| `**=` | `x **= y` | `x = x ** y` |

### Practical Example

```javascript
let level = 10;

level += 5;
console.log(level); // 15

level *= 2;
console.log(level); // 30
```

---

## 4. Arithmetic Operators

Arithmetic operators perform mathematical calculations.

| Operator | Name | Example |
|---|---|---|
| `+` | Addition | `10 + 5 = 15` |
| `-` | Subtraction | `10 - 5 = 5` |
| `*` | Multiplication | `10 * 5 = 50` |
| `/` | Division | `10 / 5 = 2` |
| `**` | Exponentiation | `2 ** 3 = 8` |
| `%` | Modulus / Remainder | `10 % 3 = 1` |
| `++` | Increment | Increase by 1 |
| `--` | Decrement | Decrease by 1 |

### Modulus Operator

The `%` operator returns the remainder after division.

```javascript
console.log(10 % 3); // 1
console.log(10 % 2); // 0
```

It is useful for checking whether a number is even or odd.

### Increment and Decrement

**Postfix:** Returns the original value, then increments.

**Prefix:** Increments first, then returns the new value.

```javascript
let postfix = 5;
let prefix = 5;

console.log(postfix++); // 5
console.log(postfix);   // 6

console.log(++prefix);  // 6
console.log(prefix);    // 6
```

---

## 5. Comparison Operators

Comparison operators compare two values and return a Boolean (`true` or `false`).

| Operator | Meaning |
|---|---|
| `>` | Greater than |
| `<` | Less than |
| `>=` | Greater than or equal to |
| `<=` | Less than or equal to |
| `==` | Loose equality |
| `===` | Strict equality |
| `!=` | Loose inequality |
| `!==` | Strict inequality |

### Strict vs Loose Equality

**Loose Equality (`==`)**

Compares values after performing type coercion when necessary.

```javascript
console.log(7 == "7");   // true
console.log(0 == false); // true
```

**Strict Equality (`===`)**

Compares both value and type without type coercion.

```javascript
console.log(7 === "7");   // false
console.log(0 === false); // false
```

**Best Practice:** Prefer `===` and `!==` to avoid unexpected type conversions.

---

## 6. Logical Operators

Logical operators combine or invert expressions.

| Operator | Name | Meaning |
|---|---|---|
| `&&` | AND | Both conditions must be truthy |
| `||` | OR | At least one condition must be truthy |
| `!` | NOT | Inverts truthiness |

### Logical AND (`&&`)

Returns the right operand if the left operand is truthy. Otherwise, returns the left operand.

```javascript
let user = null;

if (user && user.name === "Admin") {
    console.log("Welcome Admin");
}
```

The second condition is not evaluated because `user` is falsy.

### Logical OR (`||`)

Returns the first truthy operand or the last operand if none are truthy.

```javascript
let username = "";

let displayName = username || "Guest";

console.log(displayName); // Guest
```

### Logical NOT (`!`)

Converts a value to Boolean and inverts it.

```javascript
let isLoggedIn = false;

if (!isLoggedIn) {
    console.log("Please log in.");
}
```

---

## 7. Truthy and Falsy Values

Every JavaScript value has an inherent Boolean value when used in a logical context.

### The 6 Falsy Values

1. `false`
2. `0`
3. `""` (empty string)
4. `null`
5. `undefined`
6. `NaN`

### Examples

```javascript
console.log(Boolean(false));     // false
console.log(Boolean(0));         // false
console.log(Boolean(""));        // false
console.log(Boolean(null));      // false
console.log(Boolean(undefined)); // false
console.log(Boolean(NaN));        // false
```

Everything else is truthy, including:

```javascript
console.log(Boolean("false")); // true
console.log(Boolean([]));      // true
console.log(Boolean({}));      // true
```

---

## 8. Bitwise Operators

Bitwise operators work on the binary representation of numbers.

Do not confuse bitwise operators (`&`, `|`) with logical operators (`&&`, `||`).

| Operator | Name | Example |
|---|---|---|
| `&` | AND | `5 & 3 = 1` |
| `|` | OR | `5 | 3 = 7` |
| `^` | XOR | `5 ^ 3 = 6` |
| `~` | NOT | `~5 = -6` |
| `<<` | Left Shift | `5 << 1 = 10` |
| `>>` | Right Shift | `5 >> 1 = 2` |

### Binary Representation

```text
5 = 101
3 = 011

AND:
101
011
---
001 = 1

XOR:
101
011
---
110 = 6
```

### Practical Examples

```javascript
console.log(5 & 3);  // 1
console.log(5 | 3);  // 7
console.log(5 ^ 3);  // 6
console.log(~5);     // -6
console.log(5 << 1); // 10
console.log(5 >> 1); // 2
```

---

## 9. Other Important Operators

### A. typeof Operator

Returns a string indicating the type of a value.

```javascript
console.log(typeof 42);      // "number"
console.log(typeof "hello"); // "string"
console.log(typeof null);    // "object"
```

### B. Ternary Operator (`? :`)

A compact alternative to an `if...else` statement.

**Syntax:**

```javascript
condition ? expressionIfTrue : expressionIfFalse;
```

Example:

```javascript
let age = 20;

let message = (age >= 18)
    ? "You can vote."
    : "You cannot vote yet.";

console.log(message); // You can vote.
```

---

## 10. Operator Precedence

Operator precedence determines the order in which operators are evaluated.

For example, multiplication has higher precedence than addition.

```javascript
let result = 2 + 3 * 5;

console.log(result); // 17
```

Using parentheses changes the evaluation order:

```javascript
let result = (2 + 3) * 5;

console.log(result); // 25
```

**Best Practice:** Use parentheses whenever the intended order of operations might not be obvious.

---

## 11. How Numbers Are Stored in JavaScript

### Why does `0.1 + 0.2` produce `0.30000000000000004`?

Computers represent numbers internally using binary (Base 2), while humans generally write decimal numbers (Base 10).

Some decimal fractions cannot be represented exactly in binary. JavaScript's Number type uses IEEE 754 double-precision floating-point representation, so tiny rounding errors can occur.

### Understanding the Concept

The binary representation of `0.1` repeats:

```text
0.1 (Decimal)
≈ 0.0001100110011... (Binary)
```

Similarly:

```text
0.2 (Decimal)
≈ 0.001100110011... (Binary)
```

These binary fractions continue repeating, so they cannot be stored exactly as finite binary fractions.

### Practical Example

```javascript
console.log(0.1 + 0.2);
// 0.30000000000000004

console.log(0.1 + 0.2 === 0.3);
// false
```

### Why Does This Happen?

1. Decimal fractions such as 0.1 and 0.2 have repeating binary representations.
2. Floating-point storage uses finite precision.
3. Rounding introduces tiny errors.
4. Arithmetic operations can produce results slightly different from the expected decimal result.

**Key Takeaway:** Be careful when comparing floating-point numbers directly.

---

## 12. Type Conversion in JavaScript

Type Conversion (also called Type Casting) means converting a value from one data type to another.

JavaScript supports two main types:

### A. Implicit Conversion (Coercion)

JavaScript automatically converts values during certain operations.

Example:

```javascript
console.log("5" + 2); // "52"
console.log("5" - 2); // 3
```

Implicit conversion can sometimes lead to unexpected results.

### B. Explicit Conversion

The developer intentionally converts a value into another type.

This is generally clearer and easier to understand.

The basic pattern:

| Required Type | Function |
|---|---|
| Number | `Number()` |
| String | `String()` |
| Boolean | `Boolean()` |

---

## 13. Converting to String

The `String()` function converts a value into a string.

```javascript
let num = 123;
let strNum = String(num);

console.log(strNum); // "123"

let bool = true;
let strBool = String(bool);

console.log(strBool); // "true"

let value = null;
let strNull = String(value);

console.log(strNull); // "null"

let arr = [1, 2];
let strArr = String(arr);

console.log(strArr); // "1,2"
```

---

## 14. Converting to Number

### Method 1: Number()

The `Number()` function converts a value into a number when possible.

| Input | Output |
|---|---|
| `"123"` | 123 |
| `" 123 "` | 123 |
| `"123.45"` | 123.45 |
| `true` | 1 |
| `false` | 0 |
| `null` | 0 |
| `undefined` | NaN |
| `"hello"` | NaN |

Example:

```javascript
let str = "99.5";
let num = Number(str);

console.log(num); // 99.5

let strSpaces = "   100   ";
console.log(Number(strSpaces)); // 100

let invalidStr = "apple";
console.log(Number(invalidStr)); // NaN
```

### Method 2: parseInt() and parseFloat()

These methods parse a string from left to right and stop when they encounter a character that cannot be part of the number.

- `parseInt()` extracts an integer.
- `parseFloat()` extracts a floating-point number.

```javascript
console.log(parseInt("100px"));     // 100
console.log(parseFloat("3.14em"));  // 3.14

console.log(parseInt("Chapter 2")); // NaN

console.log(Number("100px"));       // NaN
```

### Method 3: Unary Plus (`+`)

The unary plus operator converts a value to a number.

```javascript
let str = "50";

let num = +str;

console.log(num); // 50
```

---

## 15. Converting to Boolean

### Boolean() Function

The `Boolean()` function converts a value into `true` or `false`.

### The 6 Falsy Values

```javascript
Boolean(false);     // false
Boolean(0);         // false
Boolean("");        // false
Boolean(null);      // false
Boolean(undefined); // false
Boolean(NaN);       // false
```

### Truthy Values

Everything else is truthy.

```javascript
Boolean(100);       // true
Boolean("hello");   // true
Boolean("false");   // true
Boolean([]);        // true
Boolean({});        // true
```

---

## 16. How to Compare Values in JavaScript

JavaScript comparison behavior depends on which comparison operator is used.

### A. Strict Equality (`===`, `!==`)

Strict equality compares types and values without type coercion.

Rules:

1. If types are different, the result is false.
2. If types are the same, values are compared.
3. Objects and arrays are compared by reference.
4. `NaN === NaN` is always false.
5. `null` and `undefined` are only strictly equal to themselves.

Examples:

```javascript
console.log(7 === "7"); // false
console.log(10 === 10); // true

console.log(null === undefined); // false

console.log(NaN === NaN); // false

let a = {};
let b = {};

console.log(a === b); // false
```

### B. Loose Equality (`==`, `!=`)

Loose equality uses type coercion according to JavaScript's abstract equality comparison rules.

Important rules:

1. Same types: compare like strict equality.
2. `null == undefined` returns true.
3. String and number: the string is converted to a number.
4. Boolean: converted to a number (`true` → 1, `false` → 0).
5. Object and primitive: the object is converted to a primitive before comparison.

Examples:

```javascript
console.log(7 == "7"); // true

console.log(0 == false); // true

console.log(null == undefined); // true

console.log(true == 1); // true
```

**Best Practice:** Prefer strict equality (`===`) unless you specifically need loose equality behavior.

### C. Relational Operators (`<`, `>`, `<=`, `>=`)

These operators compare values.

Important rules:

1. Objects are converted to primitive values when necessary.
2. If both operands are strings, they are compared lexicographically (dictionary order).
3. Otherwise, both operands are converted to numbers.
4. `true` becomes 1 and `false` becomes 0.
5. `null` becomes 0.
6. `undefined` becomes NaN.
7. If either numeric result is NaN, the comparison returns false.

Examples:

```javascript
console.log(10 > 5);      // true

console.log("apple" < "banana"); // true

console.log("10" > 5);    // true

console.log(true > false); // true

console.log(null >= 0);   // true

console.log(undefined > 0); // false
```

### Comparison Decision Tree

**1. Is the operator `===` or `!==`?**

- No type coercion.
- Check type and value.

**2. Is the operator `==` or `!=`?**

- Same types: compare values.
- `null` and `undefined`: equal under loose equality.
- Boolean involved: convert to number.
- String and number: convert string to number.
- Object involved: convert object to primitive.

**3. Is the operator `<`, `>`, `<=`, or `>=`?**

- Both operands strings: dictionary comparison.
- Otherwise: numeric comparison.
- If a number becomes NaN, the result is false.

---

## 🔑 Key Takeaways

After completing Day 03, I learned:

- Difference between primitive and object types.
- What operators and operands are.
- Assignment and arithmetic operators.
- Prefix and postfix increment.
- Strict and loose equality.
- Logical operators and short-circuiting.
- Truthy and falsy values.
- Bitwise operators.
- Ternary operator and operator precedence.
- Floating-point precision and binary representation.
- Implicit and explicit type conversion.
- Converting values into String, Number and Boolean.
- JavaScript comparison algorithms.

## 📈 JavaScript Learning Progress

| Day | Topic | Status |
|---|---|---|
| Day 01 | Introduction to JavaScript | ✅ Completed |
| Day 02 | Variables and Data Types | ✅ Completed |
| Day 03 | Operators, Type Conversion & Comparisons | ✅ Completed |
| Day 04 | Upcoming Lecture | ⏳ |

## 👨‍💻 About Me

**Gaurav Sharma**

B.Tech CSE Student | JavaScript Learner

- GitHub: [@gauravcodes98](https://github.com/gauravcodes98)

## 🎯 My Learning Goal

My goal is to build strong JavaScript fundamentals through consistent learning, practical coding, and real-world projects.

**Learn → Understand → Practice → Build → Repeat**

#JavaScript #Operators #TypeConversion #WebDevelopment #LearningInPublic #CodingJourney
