---
layout: post
title: "JavaScript Modules: Import and Export"
categories: misc
---

JavaScript modules allow you to break up your code into separate files and import them when needed. This helps in organizing your code better and makes it more maintainable.

## Exporting Modules

You can export variables, functions, or classes from a module.

```javascript
// module.js
export const name = 'Alice';
export function greet() {
  console.log('Hello, world!');
}
```

## Importing Modules
Import the exported members into another file.

```javascript
// main.js
import { name, greet } from './module.js';

console.log(name); // Outputs: Alice
greet(); // Outputs: Hello, world!
```
## Default Exports
A module can have a default export, which can be imported without curly braces.

```javascript
// module.js
export default function() {
  console.log('This is the default export!');
}

// main.js
import myFunction from './module.js';
myFunction(); // Outputs: This is the default export!
```

## Renaming Imports
You can rename imports to avoid naming conflicts.

```javascript
// module.js
export const name = 'Alice';
export const age = 25;

// main.js
import { name as userName, age as userAge } from './module.js';
console.log(userName, userAge); // Outputs: Alice 25
```

## Conclusion
JavaScript modules provide a clean and efficient way to organize and reuse code. By using import and export, you can keep your code modular and maintainable.