- **JavaScript Basics:**
	- JavaScript is a computer language used to make websites more interactive.
	- It's like the magic behind the scenes that makes things happen on web pages.
	- Originally called LiveScript, but later renamed JavaScript.
	- Despite the name similarity, it's not related to Java.

- **Purpose of JavaScript:**
	- JavaScript makes web pages more fun and interesting to use.
	- It adds interactivity, allowing things to happen instantly without reloading the page.
	- For example, clicking buttons or filling out forms triggers instant responses, thanks to JavaScript.

- **Impact of JavaScript:**
	- JavaScript is essential for modern web development.
	- It enhances user experience by making web pages dynamic and engaging.
	- It's like adding extra sparkle to your internet experience!
## Simple example

#### HTML

```html
<!DOCTYPE html>

<html lang="en">

<head>

<meta charset="UTF-8" />

<meta name="viewport" content="width=device-width, initial-scale=1.0" />

<meta http-equiv="X-UA-Compatible" content="ie=edge" />

<title>JavaScript (Very) Basics</title>

<link rel="preconnect" href="https://fonts.googleapis.com">

<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

<link

href="https://fonts.googleapis.com/css2?family=Madimi+One&family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&display=swap"

rel="stylesheet">

<link rel="stylesheet" href="assets/styles/app.css" />

<script src="assets/scripts/app.js" defer></script>

</head>

  

<body>

<div id="backdrop"></div>

<header id="main-header">

<h1>Welcome to this "JavaScript!</h1>

</header>

<main>

<section id="about-this-course">

<header>

<h2>About this Course</h2>

</header>

<article>

<h2>What is JavaScript?</h2>

<p>

JavaScript is a

<a href="#" class="info-modal"

data-text="That means that code is not pre-compiled but instead evaluated, compiled and executed at runtime (e.g. when the browser executes the script).">dynamic,

interpreted</a>

and

<a href="#" class="info-modal"

data-text="Weakly typed languages assign types (like 'number') to variables (data containers) at runtime - i.e. you (the developer) can't set the types you want to use in certain places in advance. Only indirectly by making sure you're always working with the correct values.">weakly

typed</a>

programming language which was built with the purpose of running in

host environments (e.g. inside of a webpage in the browser).

</p>

</article>

</section>

</main>

</body>

  

</html>
```

### Javascript to display the modal
Note: 
- HTML always executes from top to bottom
- When a script is imported on the HTML. A script is also executed from top to bottom. 

```javascript
// Retrieve the backdrop element
const backdropElement = document.getElementById('backdrop');

// Select all elements with the class 'info-modal'
const modalLinkElements = document.querySelectorAll('.info-modal');

// Declare a variable to hold the reference to the modal element
let infoModal;

// Function to toggle the backdrop visibility
function toggleBackdrop() {
  backdropElement.classList.toggle('visible');
}

// Function to present the info modal
function presentInfoModal(event) {
  // Retrieve the text associated with the clicked element
  const text = event.target.dataset.text;
  
  // Toggle backdrop visibility
  toggleBackdrop();
  
  // Create the modal element dynamically
  infoModal = document.createElement('div');
  infoModal.classList.add('modal'); // Add the 'modal' class to the modal element
  
  // Populate the modal with content
  infoModal.innerHTML = `
    <h2>More Details</h2>
    <p>${text}</p>
  `;
  
  // Create a close button
  const closeButton = document.createElement('button');
  closeButton.addEventListener('click', hideInfoModal); // Add event listener to hide the modal when the close button is clicked
  closeButton.textContent = 'Okay'; // Set the text content of the close button
  infoModal.appendChild(closeButton); // Append the close button to the modal
  
  // Append the modal to the document body
  document.body.appendChild(infoModal);
}

// Function to hide the info modal
function hideInfoModal() {
  toggleBackdrop(); // Toggle backdrop visibility
  document.body.removeChild(infoModal); // Remove the modal element from the document body
}

// Add event listeners to each modal link element
for (const linkElement of modalLinkElements) {
  linkElement.addEventListener('click', presentInfoModal); // When clicked, call the presentInfoModal function
}

// Add event listener to the backdrop element to hide the modal when clicked
backdropElement.addEventListener('click', hideInfoModal);

```

### Note: 
The "defer" attribute in HTML tags is used to specify that the execution of the script should be deferred until after the HTML content of the page has been fully parsed and displayed. Here's what it does:
1. **Delay Execution:** When a script is included with the "defer" attribute, it tells the browser to continue parsing the HTML content while asynchronously downloading the script. The script will then be executed after the HTML parsing is complete.
2. **Order Preservation:** Multiple scripts with the "defer" attribute will be executed in the order they appear in the HTML document, ensuring that dependencies are resolved correctly.
3. **Improved Page Load Performance:** By deferring script execution, the browser can render the page without waiting for potentially long-running scripts to finish. This can result in faster page load times and a better user experience.
4. **Access to DOM:** Scripts with the "defer" attribute have access to the fully parsed HTML document and can manipulate the DOM immediately upon execution.

Overall, the "defer" attribute is useful for optimizing page load times and ensuring scripts are executed in the correct order without blocking the rendering of the page.
## Execution process

- **Javascript Execution Process:**
    - Javascript code is executed by a Javascript engine, which is built into environments like web browsers.
    - In browsers, engines like V8 (in Chrome) or SpiderMonkey (in Firefox) parse the Javascript code, compile it into machine code for faster execution, and then execute it.
    - Modern engines often optimize code execution by starting with uncompiled code, compiling it dynamically while executing, and switching to compiled code for better performance.
    - Javascript execution typically occurs on a single thread within the operating system, even in multi-threaded environments.

- **Interpreted vs. Compiled:**
    - Interpreted means that the code is read and executed line-by-line at runtime by the Javascript engine.
    - Compiled involves converting code into machine code before execution, resulting in faster execution but requiring an additional step before running.

- **Dynamic Typing:**
    - Javascript is dynamically typed, meaning variable types are determined at runtime rather than being explicitly declared.
    - This allows for flexibility but can lead to unexpected behavior if types are not managed carefully.

- **Weakly Typed:**
    - Weakly typed languages do not enforce strict type constraints, allowing variables to be implicitly coerced between different types.
    - This can lead to subtle bugs if not handled properly, but it also provides flexibility and convenience in coding.
## Dynamic interpretation and weekly typing

- **Dynamic Interpreted Language:**
	- JavaScript is dynamic and interpreted, meaning it's not pre-compiled like languages such as C++.
	- Code is evaluated and executed at runtime, allowing for changes to the code during execution.
	- You can dynamically switch the type of data stored in variables during runtime, which is not allowed in statically compiled languages.
-
- **Weakly Typed Language:**
	- JavaScript is weakly typed, which means data types are inferred automatically.
	- You don't need to explicitly declare the type of data a variable will hold in advance.
	- JavaScript is forgiving in terms of data types, allowing variables to hold different types of data without throwing errors.
	
- **Implications:**
	- The dynamic nature of JavaScript enables on-the-fly compilation and interpretation, allowing for dynamic changes to code and data types during runtime.
	- While this flexibility can be powerful, it also requires careful handling to avoid unexpected behavior.
	- Understanding these concepts is crucial for working effectively with JavaScript, especially when dealing with variables and data manipulation.

## Runs on an Host environment
Here are the summarized notes:

- **Host Environments:**
	- JavaScript can run in various environments, with the most common being the browser.
	- Browsers have built-in JavaScript engines, allowing them to execute JavaScript code.
	- JavaScript can also run on the server-side using platforms like Node.js, enabling server-side scripting.

- **Purpose of JavaScript:**
	- JavaScript was initially designed to enhance web pages by making them more dynamic.
	- It allows for changes to web pages without reloading, enabling interaction with HTML, CSS, and HTTP requests.
	- JavaScript's capabilities extend beyond the browser, with Node.js enabling server-side scripting.

- **Browser Environment Limitations:**
	- JavaScript in the browser is sandboxed for security reasons, restricting access to local file systems and operating systems. => Any website can not access my browser. 
	- This prevents unauthorized access and ensures a safe browsing experience for users.

- **Node.js:**
	- Node.js is a runtime environment for executing JavaScript outside of the browser.
		- Javascript extracted out of V8 engine from Chrome
	- It allows access to local file systems and operating systems, making it suitable for building web servers and server-side applications.
	- While it lacks direct manipulation of HTML and CSS like browser-side JavaScript, it offers powerful server-side capabilities.



---
tags:
- #JavaScript
---
