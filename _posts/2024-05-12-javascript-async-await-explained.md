---
layout: post
title: "JavaScript Async/Await Explained"
categories: misc
---

Async/await is a modern syntax for handling asynchronous operations in JavaScript, built on top of Promises. It makes asynchronous code look and behave more like synchronous code, making it easier to read and understand.

## Using Async/Await

To use `await`, you must be inside an `async` function.

```javascript
async function fetchData() {
  try {
    const response = await fetch('https://api.example.com/data');
    const data = await response.json();
    console.log(data);
  } catch (error) {
    console.error('Error:', error);
  }
}

fetchData();
```
## Error Handling
Error handling with async/await is straightforward using try and catch.

```javascript
async function getUserData() {
  try {
    const response = await fetch('https://api.example.com/user');
    if (!response.ok) {
      throw new Error('Network response was not ok');
    }
    const data = await response.json();
    console.log(data);
  } catch (error) {
    console.error('Fetch error:', error);
  }
}

getUserData();
```

## Sequential Execution
Async/await makes it easy to execute asynchronous operations sequentially.

```javascript
async function sequentialTasks() {
  const response1 = await fetch('https://api.example.com/data1');
  const data1 = await response1.json();
  console.log(data1);

  const response2 = await fetch('https://api.example.com/data2');
  const data2 = await response2.json();
  console.log(data2);
}

sequentialTasks();
```

## Conclusion
Async/await simplifies working with asynchronous code in JavaScript, providing a more readable and maintainable approach compared to traditional promise chaining.