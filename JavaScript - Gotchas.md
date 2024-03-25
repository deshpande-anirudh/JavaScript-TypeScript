#### 1. outputResult() has to be inside the add() function
#### 2. parseInt(new_value.value) is a must, since its always going to be the text

```javascript
let currentResult = 0;
function add() {
	const new_value = document.getElementById("input-number");
	currentResult = currentResult + parseInt(new_value.value);
	const calculationDescription = `${currentResult} = 	${currentResult} + 10;`;
	outputResult(currentResult, calculationDescription);
}

let add_button = document.getElementById("btn-add");
add_button.addEventListener('click', add);
```

#### 3. Is there a parseBoolean? 
JavaScript does not have a built-in `parseBoolean()` function like it does for parsing numbers with `parseInt()` and `parseFloat()`. However, you can easily create your own function to parse strings to boolean values. Here's a simple example of how you could implement such a function:

```javascript
function parseBoolean(str) {
    // Convert the string to lowercase for case-insensitive comparison
    str = str.toLowerCase().trim();

    // Evaluate common representations of true and false
    if (str === "true" || str === "1" || str === "yes" || str === "y") {
        return true;
    } else if (str === "false" || str === "0" || str === "no" || str === "n") {
        return false;
    }

    // If none of the above conditions match, return null
    return null;
}

// Example usage:
console.log(parseBoolean("true"));  // Output: true
console.log(parseBoolean("False")); // Output: false
console.log(parseBoolean("YES"));   // Output: true
console.log(parseBoolean("n"));     // Output: false
console.log(parseBoolean("invalid"));// Output: null
```
#### 4. Is there an "undefined" in javascript? how is it different from "null"? Is it the same in typescript?

Yes, there is an `undefined` value in JavaScript. It represents a variable that has been declared but has not been assigned a value. 

Here's a simple example:

```javascript
var x;
console.log(x); // Output: undefined
```

In the above code, `x` is declared but not assigned any value explicitly, so its value is `undefined`.

`null`, on the other hand, is a special value in JavaScript that represents the absence of a value. It's typically used to explicitly indicate that a variable does not contain any meaningful value.

Here's an example:

```javascript
var y = null;
console.log(y); // Output: null
```

In this case, `y` has been explicitly assigned the value `null`, indicating that it does not currently reference any meaningful object or value.

The key difference between `undefined` and `null` is that `undefined` typically indicates a variable that has been declared but not yet assigned any value, while `null` typically indicates a deliberate absence of a value. However, in many cases, they can be used interchangeably, and JavaScript will often coerce them to be equal under loose equality (`==`) comparisons. However, under strict equality (`===`), they are not the same because they represent different types.

In TypeScript, `undefined` and `null` behave similarly to JavaScript, but TypeScript adds more strictness and type annotations.

1. **Undefined**: In TypeScript, just like in JavaScript, a variable that has been declared but not initialized will have the type `undefined`.

    ```typescript
    let x: number; // Declared but not initialized
    console.log(x); // Output: undefined
    ```

2. **Null**: Similarly, `null` represents the absence of a value. It can be explicitly assigned to a variable, and its type will be `null`.

    ```typescript
    let y: string | null = null; // Explicitly assigned null
    console.log(y); // Output: null
    ```

In TypeScript, the main difference compared to JavaScript is the type system. TypeScript adds static typing, allowing you to define types for variables, function parameters, and return values. This helps catch errors at compile-time rather than runtime.

Additionally, TypeScript introduces the concept of strict null checks (enabled by default since TypeScript 2.0), which helps catch common errors related to `null` and `undefined`. When strict null checks are enabled, variables of type `undefined` or `null` cannot be assigned to variables of other types without a type assertion or a check for nullability.

Here's an example:

```typescript
let z: number = null; // Error: Type 'null' is not assignable to type 'number'

// To allow null, you need to explicitly specify the type as a union
let nullableString: string | null = null;
```

So, while the behavior of `undefined` and `null` is similar between JavaScript and TypeScript, TypeScript provides additional features to catch errors related to these values at compile-time.
