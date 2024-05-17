---
layout: post
title: "Understanding JavaScript Closures"
categories: misc
---

## Introduction

Closures are one of the most powerful and often misunderstood features in JavaScript. They allow functions to retain access to variables from their containing scope even after that scope has exited.

## What is a Closure?

A closure is created when a function is defined inside another function, and the inner function retains access to the outer function's variables.

```javascript
function outerFunction() {
  let outerVariable = 'I am from outer scope';

  function innerFunction() {
    console.log(outerVariable);
  }

  return innerFunction;
}

const closure = outerFunction();
closure(); // Outputs: I am from outer scope
```
## Practical Uses of Closures
### Data Privacy
Closures are often used to create private variables.
```javascript
function createCounter() {
  let count = 0;

  return {
    increment: function() {
      count++;
      return count;
    },
    decrement: function() {
      count--;
      return count;
    }
  };
}

const counter = createCounter();
console.log(counter.increment()); // Outputs: 1
console.log(counter.decrement()); // Outputs: 0
```
## Function Factories
Closures can be used to create factory functions that generate new functions with preset arguments.

```javascript
function createGreeting(greeting) {
  return function(name) {
    return `${greeting}, ${name}!`;
  };
}

const sayHello = createGreeting('Hello');
console.log(sayHello('Alice')); // Outputs: Hello, Alice!
```
## Conclusion
Understanding closures is essential for mastering JavaScript. They enable powerful patterns like data encapsulation and higher-order functions.
