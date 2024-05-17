---
layout: post
title: "Exploring JavaScript ES6 Features"
categories: misc
---
ECMAScript 6 (ES6) introduced many new features that make JavaScript more powerful and easier to write. Let's explore some of the most important ones.
## JavaScript ES6 features

### Arrow Functions

Arrow functions provide a concise syntax for writing function expressions.

```javascript
const add = (a, b) => a + b;
console.log(add(2, 3)); // Outputs: 5
```
### Template Literals
Template literals allow for easier string interpolation and multi-line strings.

```javascript
const name = 'Alice';
const greeting = `Hello, ${name}! How are you?`;
console.log(greeting); // Outputs: Hello, Alice! How are you?
```
### Destructuring Assignment
Destructuring makes it easier to extract values from arrays and objects.

```javascript
const [first, second] = [1, 2];
console.log(first, second); // Outputs: 1 2

const { name, age } = { name: 'Alice', age: 25 };
console.log(name, age); // Outputs: Alice 25
```

### Default Parameters
Default parameters allow you to specify default values for function parameters.
```javascript
function greet(name = 'Guest') {
  return `Hello, ${name}!`;
}

console.log(greet()); // Outputs: Hello, Guest!
console.log(greet('Alice')); // Outputs: Hello, Alice!
```
## Conclusion
ES6 brought significant improvements to JavaScript, making it more expressive and easier to work with. Embracing these features can help you write cleaner and more efficient code.