# How JavaScript Works

This repository contains detailed explanations and examples of how JavaScript works under the hood. It covers fundamental concepts like the global execution context, call stack, memory heap, hoisting, closures, and more.

## Introduction

JavaScript is a high-level, interpreted programming language that conforms to the ECMAScript specification. It is widely used for web development to create interactive and dynamic web pages. JavaScript executes annything using it's functionality of creating Globle Execution Context and assigning values to it. Everything happens here!!!
Let's understand more!

## Global Execution Context

### Definition

The global execution context is the default or base execution context in which JavaScript code starts its execution when a script first runs. It consists of two phases: the creation phase and the execution phase.
- Creation Phase is also known as Memory Phase, where javascript assigns memory to functions and variables.
- Execution Phase is where our javascript code executes, JS executes it's function using a stack.

### Creation/ Memory Phase
During the creation phase, the JavaScript engine performs the following steps:
1. Creates the global object (in browsers, this is the `window` object).
2. Creates the `this` object, which points to the global object.
3. Sets up a memory space for storing variables and function declarations (which is knows as `hoisting`).

### Execution Phase
In the execution phase, the JavaScript engine executes the code line by line. It assigns values to variables and executes functions using function stack.

### Example

```javascript
console.log(x); // Output: undefined (due to hoisting)
var x = 10;
console.log(x); // Output: 10

function greet() {
    console.log("Hello, World!");
}

greet(); // Output: Hello, World!
