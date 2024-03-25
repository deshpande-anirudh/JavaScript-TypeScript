## Naming conventions
- Variables are data containers used to store information needed for program execution.
    ```javascript
    let userName = 'John'; // Variable declaration with initial value
    ```
	- In JavaScript, variables are declared using the `let` keyword followed by a name and an optional initial value.
	- Variables can be reassigned to new values during program execution.
    ```javascript
    userName = 'Jane'; // Reassigning the variable with a new value
    ```
	- Constants are similar to variables but are declared using the `const` keyword.
    ```javascript
    const PI = 3.14; // Constant declaration with initial value
    ```
	- Constants cannot be reassigned after initialization, making them suitable for storing values that do not change.
    ```javascript
    PI = 3.14159; // Error: Assignment to constant variable
    ```
	- Constants help in maintaining clarity and readability in code by indicating that certain values are constant throughout the program.

**Standard Practices:**
- Use camelCase: Begin variable names with a lowercase letter and capitalize subsequent words.
	- Example: `currentResult`, `totalAmountOfUsers`
- Choose descriptive names: Select names that clearly indicate the purpose or content of the variable.
	- Example: `userName` instead of `userInput`
- Be consistent: Maintain uniformity in naming conventions throughout the codebase for improved readability and understanding.
- Follow community guidelines: Adhere to widely accepted conventions and best practices to ensure code consistency and collaboration.

**Not Recommended:**
- Avoid starting variable names with digits: Variable names should not begin with numbers.
	- Example: `1stVariableName` (not recommended)
- Avoid special characters in names: Except for `_` and `$`, avoid using special characters in variable names.
	- Example: `total-amount-of-users` (not recommended)
- Do not use reserved keywords: Avoid using JavaScript reserved keywords as variable names to prevent conflicts and confusion.
	- Example: `let` or `const` as variable names (not recommended)

**Camel vs. kebab case:** 
In JavaScript, camelCase and kebab-case are two different conventions used for naming variables, functions, or identifiers.

1. **CamelCase**: In camelCase, the first letter of each word except the first is capitalized, and there are no spaces between words. For example:
   - `myVariableName`
   - `calculateTotalPrice`
   - `firstName`

2. **Kebab-case**: In kebab-case, words are separated by hyphens (`-`) and all letters are typically lowercase. For example:
   - `my-variable-name`
   - `calculate-total-price`
   - `first-name`

The choice between camelCase and kebab-case often depends on the coding convention being followed or personal/team preference.

- **CamelCase** is more commonly used in JavaScript, especially for variables and function names.
- **Kebab-case** is often used for naming in CSS, URLs, or HTML attributes.

For instance, in HTML, kebab-case is preferred for attribute names, while camelCase is more common for JavaScript variable and function names. Here's an example:

```html
<button id="submit-button" class="btn-primary">Submit</button>
```

In JavaScript:

```javascript
let submitButton = document.getElementById('submit-button');
submitButton.addEventListener('click', function() {
    // do something
});
```

In this example, `id` and `class` attributes in HTML use kebab-case, while the JavaScript variable `submitButton` uses camelCase.

## Data types
- **Numbers:** Used for numeric values, including integers (whole numbers) and floating-point numbers (numbers with decimal places).
    - Example: `3`, `-3`, `22.956`
- **Strings:** Represented by text enclosed within single quotes, double quotes, or backticks. Used for textual data such as user names, messages, or descriptions.
    - Example: `'Hello'`, `"World"`, `` `JavaScript` ``




---
tags:
  - #JavaScript
-----



