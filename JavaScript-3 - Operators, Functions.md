## Operators in JavaScript:

1. **Arithmetic Operators:**
   - Used for arithmetic operations such as addition, subtraction, multiplication, division, and modulus.
   - Examples:
     ```javascript
     let x = 10;
     let y = 5;
     let sum = x + y; // Addition
     let difference = x - y; // Subtraction
     let product = x * y; // Multiplication
     let quotient = x / y; // Division
     let remainder = x % y; // Modulus (Remainder after division)
     ```

2. **Assignment Operators:**
   - Used to assign values to variables.
   - Examples:
     ```javascript
     let x = 10;
     x += 5; // Equivalent to: x = x + 5;
     x -= 3; // Equivalent to: x = x - 3;
     x *= 2; // Equivalent to: x = x * 2;
     x /= 4; // Equivalent to: x = x / 4;
     ```

3. **Comparison Operators:**
   - Used to compare two values and return a boolean result.
   - Examples:
     ```javascript
     let a = 10;
     let b = 5;
     let isEqual = (a === b); // Strict Equality (true if equal)
     let isNotEqual = (a !== b); // Strict Inequality (true if not equal)
     let greaterThan = (a > b); // Greater Than (true if a is greater)
     let lessThan = (a < b); // Less Than (true if a is less)
     let greaterOrEqual = (a >= b); // Greater Than or Equal To
     let lessOrEqual = (a <= b); // Less Than or Equal To
     ```

4. **Logical Operators:**
   - Used to perform logical operations on boolean values.
   - Examples:
     ```javascript
     let x = true;
     let y = false;
     let andResult = x && y; // Logical AND (true if both are true)
     let orResult = x || y; // Logical OR (true if at least one is true)
     let notResult = !x; // Logical NOT (true if operand is false)
     ```

5. **Unary Operators:**
   - Operate on a single operand.
   - Examples:
     ```javascript
     let x = 10;
     let y = -x; // Unary Minus (Negation)
     let z = ++x; // Increment x by 1 and assign to z
     let w = --x; // Decrement x by 1 and assign to w
     ```

6. **Ternary Operator (Conditional Operator):**
   - Evaluates a condition and returns one of two values based on the result.
   - Syntax: `condition ? value1 : value2`
   - Example:
     ```javascript
     let age = 20;
     let message = (age >= 18) ? "You are an adult" : "You are a minor";
     ```

Understanding these operators is crucial for manipulating data and controlling the flow of execution in JavaScript programs. Regular practice and application reinforce comprehension.
## Functions
Functions are essential for organizing and reusing code. They can be defined in several ways:

1. **Function Declaration:**
   - Traditional way of defining a function.
   - Syntax: `function functionName(parameters) { // code }`
   - Example:
     ```javascript
     function greet(name) {
         console.log(`Hello, ${name}!`);
     }
     ```

2. **Function Expression:**
   - Assigning a function to a variable.
   - Syntax: `const functionName = function(parameters) { // code }`
   - Example:
     ```javascript
     const greet = function(name) {
         console.log(`Hello, ${name}!`);
     };
     ```

3. **Arrow Function (ES6):**
   - A concise way to write functions, especially for anonymous functions.
   - Syntax: `const functionName = (parameters) => { // code }`
   - Example:
     ```javascript
     const greet = (name) => {
         console.log(`Hello, ${name}!`);
     };
     ```

4. **Function Constructor:**
   - Using the `Function` constructor to create a function object.
   - Syntax: `const functionName = new Function('parameters', 'code')`
   - Example:
     ```javascript
     const greet = new Function('name', 'console.log(`Hello, ${name}!`)');
     ```

Each method has its advantages and use cases, but they all serve the purpose of defining reusable blocks of code.

## Summary

**JavaScript Concepts Revision Notes:**

1. **Functions:**
   - Functions are reusable blocks of code.
   - Defined using the `function` keyword followed by a name and curly braces `{}`.
   - Can take parameters and return values.
   - Example:
     ```javascript
     function calculateArea(width, height) {
         return width * height;
     }
     ```

2. **Operators:**
   - Arithmetic operators perform mathematical operations.
   - Comparison operators compare values and return true or false.
   - Assignment operators assign values to variables.
   - Example:
     ```javascript
     let sum = 10 + 5; // Addition
     let isEqual = (5 === 5); // Strict equality comparison
     let x = 10; 
     x += 5; // Equivalent to: x = x + 5;
     ```

3. **Strings:**
   - Used for representing text data.
   - Declared using single quotes (`'`), double quotes (`"`), or backticks (\`\`).
   - Template literals allow embedding variables or expressions.
   - Example:
     ```javascript
     const name = "John";
     const greeting = `Hello, ${name}!`;
     ```

4. **Conditionals:**
   - Used to execute code based on conditions.
   - Commonly used statements: `if`, `else if`, `else`.
   - Example:
     ```javascript
     let x = 10;
     if (x > 0) {
         console.log("Positive");
     } else {
         console.log("Negative or Zero");
     }
     ```

5. **Events:**
   - Events are actions that occur in the browser.
   - Event listeners are used to respond to events.
   - Example:
     ```javascript
     const button = document.querySelector("button");
     button.addEventListener("click", function() {
         console.log("Button clicked!");
     });
     ```

6. **Loops:**
   - Loops repeat a block of code until a condition is met.
   - Common types: `for`, `while`, `do-while`.
   - Example:
     ```javascript
     for (let i = 0; i < 5; i++) {
         console.log(i);
     }
     ```

7. **Objects:**
   - Objects are collections of related data and functionality.
   - Properties hold values, and methods are functions stored as object properties.
   - Example:
     ```javascript
     const person = {
         name: "John",
         age: 30,
         greet: function() {
             console.log(`Hello, my name is ${this.name}`);
         }
     };
     ```

These notes provide a concise overview of key JavaScript concepts for quick revision. Practice examples and experimenting with code will reinforce understanding.



---
tags:
- #JavaScript
---
