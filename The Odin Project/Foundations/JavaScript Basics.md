This module covers the fundamentals of JavaScript, from variables and operators to complex concepts like the DOM, functions and problem solving. It's designed to provide you with the core knowledge you need to make web pages interactive.

## 💻 Getting Started with JavaScript

- JavaScript is used to make web pages interactive.
- Most JavaScript code in the Foundations course will run in the browser.
- You can run JavaScript code in an HTML file using `<script>` tags.
- Use the browser's developer console (right-click, "Inspect" or "Inspect Element," then "Console") to see output.
- The command `console.log()` prints to the developer console.
- Use the Live Preview extension in VS Code to automatically update the browser when you save your file.
- You can also include JavaScript in a webpage through an external `.js` file, similar to linking CSS files.
- External `.js` files are used for more complex scripts.

## 🧰 Variables and Data Types

### 📦 Variables

- Variables are "storage containers" for data.
- Declare variables using `let` or `const` keywords.
- `let` allows you to re-assign a variable's value.
    - Example: `let age = 11; age = 54;`
- `const` declares a constant variable that cannot be re-assigned.
    - Trying to re-assign a `const` variable will throw an error.
- `var` is an older way to declare variables, but it is not recommended as it has quirks that `let` and `const` address.

### 🔢 Numbers

- Numbers are fundamental for programming logic.
- JavaScript can perform basic mathematical operations.
- Use `console.log()` to see the results of calculations.
    - Example: `console.log(23 + 97)` will output `120`.

### 🧵 Strings

- A string is a piece of text.
- Strings are a fundamental building block of the language.
- Explore string manipulation methods in the MDN tutorial on strings in JavaScript.
    - String methods include `replace` and `slice`.
- A method is functionality built into the language or specific data types.

### 🎭 Other Data Types

- There are **eight** data types in JavaScript:
    - `Number`, `String`, `Boolean`, `Symbol`, `BigInt`, `Null`, `Undefined`
    - **Object** is the only non-primitive data type.
- Single, double, and backtick quotes can be used for strings.
- Backtick quotes allow embedding variables/expressions in a string.
    - Use `${variable}` to embed a variable in a string.
- String concatenation is the term for joining strings together.

### 🚦 Conditionals

- Conditionals allow computers to make decisions.
- Comparison operators are used to make comparisons.
- Logical operators include AND (`&&`), OR (`||`), and NOT (`!`).
- Truthy and falsy values affect how conditional statements are evaluated.
    - Falsy values include `0`, `""`, `null`, `undefined`, `NaN`.
- An `if/else` conditional allows for executing code blocks based on a condition.
- A `switch` statement is useful for multiple conditions.

## ⚙️ Operators

- JavaScript has logical and mathematical operators.
- The Modulo (`%`) operator returns the remainder of a division.
- `==` checks for equality, while `===` checks for equality and type.
- `NaN` (Not a Number) is a result you can receive when you perform illegal number operations.
- The unary plus operator (`+`) can convert string representations of integers to numbers (e.g., `+"10"` becomes `10`).
- Increment (`++`) and decrement (`--`) operators change a number by one.
    - Prefixing and postfixing these operators affects when the value is changed.
- Operator precedence determines the order in which operations are performed.

## 🧰 Functions

### 📝 Defining and Invoking Functions

- Functions bundle code into reusable packages.
- A function is defined using the `function` keyword followed by a name, parameters in parentheses, and a code block in curly braces.
    - Example: `function add7(number) { return number + 7; }`.
- Parameters are placeholders for values passed into a function.
- Arguments are the actual values passed to a function when it is called.
- Invoke a function by writing its name followed by parentheses, and any arguments.
    - Example: `add7(10)`
- A function's return value is the result of calling the function.
- You can pass a function call as an argument to another function.

### 🎯 Function Scope

- Function scope refers to the visibility and accessibility of variables within a function.
- A variable declared inside a function is only accessible within that function.

### ➡️ Return Values

- A return value is what a function gives back to where it was called.
- Use the `return` keyword to specify the return value.

### 💫 Anonymous and Arrow Functions

- Anonymous functions are functions without a name.
- Arrow functions are a concise way to write functions.

### 📜 Function Expressions

- A function expression is when a function is assigned to a variable.
- A function declaration is when a function is declared using the `function` keyword.

### 📞 Call Stack

- The call stack keeps track of the order functions are called and how return values are passed back.

## 🐞 Understanding Errors

- Error messages provide information about problems in your code.
- Errors have a type and a message, and also show the file and line number where the error occurred.
- The stack trace shows the sequence of function calls that led to the error.
- **Common types of errors**:
    - **`ReferenceError`**: Variable is not defined.
    - **`SyntaxError`**: Code is written incorrectly.
    - **`TypeError`**: Operation or method is used with an incompatible type.
- Use the browser's developer console to identify errors.
- Google errors to find solutions on StackOverflow or in documentation.
- Use the debugger to troubleshoot more complex issues.
- `console.log()` helps with quick debugging.
- Warnings are messages that provide insight on potential problems, but do not necessarily crash a program.

## 🧠 Problem Solving

- Problem-solving is the most important skill for a developer.
- **Three stages of problem solving:**
    - **Understand the problem**: Write it down, reword it, draw diagrams.
    - **Plan**: Determine inputs, outputs, and the steps necessary to get the desired output.
    - **Divide and conquer**: Break the problem into subproblems.
- **Algorithm**: A recipe for solving a problem, defining the steps for the computer.
- **Pseudocode**: Writing the logic of a program in natural language.
- Don't try to solve the big problem in one go.
- Start with the smallest or simplest subproblem.
- Solving a subproblem can reveal the next subproblem.

## 🧰 Developer Tools

- Developer Tools help with JavaScript development.
- Open Developer Tools:
    - Chrome Menu > More Tools > Developer Tools
    - Right-click on a page and select "Inspect"
    - Keyboard shortcut: F12 or Ctrl + Shift + C (Mac: Opt + Cmd + C)
- Use the "Elements" tab to view and edit HTML.
- Use the "Console" tab to run code and view output.
- You can change the screen size using the Device Mode.
- Use breakpoints to pause code execution and debug.

## 🚀 Project: Rock Paper Scissors

- Create a Rock Paper Scissors game in the console.
- Create functions for computer and human choices and for playing a round.
- Keep track of scores.
- Display the winner.

### ➡️ Revisiting Rock Paper Scissors with a UI

- Use branches in Git to add a UI to the game.
- Create buttons for each choice.
- Use event listeners on the buttons.
- Display the results using DOM methods.
- Keep track of the score, announce a winner, refactor your code if necessary.
- Merge your feature branch into the main branch.

## 🧹 Clean Code

- Most of a developer's time is spent reading, not writing code.
- Aim for **readability** and **maintainability**.
- Use **descriptive** variable and function names.
- Use a consistent naming system (e.g., camelCase).
- Variables should start with a noun or adjective; functions should start with a verb.
- Use **searchable** names instead of "magic values".
- Limit line lengths and use proper indentation.
- Semicolons are mostly optional in JavaScript, but using them is recommended.
- Comments should explain the **why**, not the **how**.
- Use git to track changes and deleted code, not comments.
- Avoid redundant comments.
- Good code can often speak for itself without comments.

## 🗂️ Arrays and Loops

### 📦 Arrays

- Arrays are ordered collections of items.
- They can store multiple values in a single variable.
- Arrays are useful for organizing and manipulating data.
- See the W3Schools JavaScript Arrays documentation.
- Access elements in an array using their index (starting at 0).
    - Example: `myArray` to access the first element.
- Change an array element by assigning a new value at a given index.
    - Example: `myArray = "new value";`
- Useful array properties include `.length`, which returns the number of items in an array.
- Useful array methods include `.push()`, `.pop()`, `.slice()`, `.splice()`.

### 🔁 Loops

- Loops execute a block of code repeatedly.
- For loops, while loops, and do-while loops are available in JavaScript.
- A `break` statement exits a loop prematurely.
- A `continue` statement skips the current iteration and continues with the next one.

### 🧪 Test Driven Development (TDD)

- Test Driven Development is the practice of writing tests before writing code.
- TDD is more productive than writing code without tests.
- Automated tests help ensure the code works correctly.

## 🕸️ DOM Manipulation and Events

### 🌳 The DOM

- The Document Object Model (DOM) is a tree-like representation of a webpage.
- It is a tree of "nodes" with parent/child and sibling relationships.
- "Element" nodes are the most commonly used for DOM manipulation.

### 🎯 Targeting Nodes

- Use "selectors" to target specific nodes.
    - Use CSS-style selectors, e.g., `document.querySelector("#container")`, `document.querySelectorAll(".myClass")`.
    - Use relational selectors, e.g., `element.firstElementChild`, `element.previousElementSibling`.
- `querySelector()` returns the first matching element.
- `querySelectorAll()` returns a NodeList of all matching elements.
- A NodeList is not an array but can be converted to one using `Array.from()` or the spread operator.

### 🔨 DOM Methods

- `document.createElement()` creates a new element in memory.
- `parentNode.appendChild(childNode)` appends the child node to the end of the parent node.
- `parentNode.insertBefore(newNode, referenceNode)` inserts the new node before the reference node.
- `parentNode.removeChild(child)` removes a child node from the DOM.
- `element.setAttribute()` sets an element's attribute.
- `element.getAttribute()` gets an element's attribute.
- `element.removeAttribute()` removes an element's attribute.
- `element.classList.add()` adds a class to an element.
- `element.classList.remove()` removes a class from an element.
- `element.classList.toggle()` toggles a class on an element.
- `element.textContent` adds text content to an element, which is preferred for text over innerHTML.
- `element.innerHTML` renders HTML inside an element, but use sparingly to avoid security risks.
- Include JavaScript at the bottom of your HTML file to ensure the DOM is fully loaded before it is run.
- Or, link the script tag in the `<head>` of your HTML file and use the `defer` attribute.

### 👂 Events

- Events are actions that occur on a webpage (e.g., clicks, keypresses).
- **Three ways to use events:**
    1. HTML element attributes (e.g., `<button onclick="myFunction()">` ).
    2. DOM node `on` properties (e.g., `btn.onclick = myFunction;` ).
    3. Event listeners (e.g., `btn.addEventListener("click", myFunction);`).
- Event listeners are preferred for flexibility and separation of concerns.
- Named functions help to clean up your code.
- An event listener passes in an event object, which contains useful data about the event (e.g., `e.target` refers to the clicked element).
- A callback is a function passed as an argument into another function.
- Attach listeners to groups of nodes by using `querySelectorAll` and a loop (or `.forEach`).
- Useful events include `click`, `dblclick`, `keydown`, and `keyup`.

## ➕ Objects

### 📦 Object Basics

- Objects are collections of key-value pairs.
- They are a non-primitive data type that can store complex entities.
- Objects can contain strings, numbers, arrays, and even functions.
- Primitives (e.g., numbers, strings) contain copies of data; objects contain references to data.
- Mutating (changing the data within) an object affects all references to it.
- Reassigning a variable to a new object does not affect other variables that reference the original object.

### 🪄 Array Methods

- `Array.prototype.map()` transforms each element of an array and returns a new array.
- `Array.prototype.filter()` selects elements that pass a test and returns a new array.
- `Array.prototype.reduce()` combines all elements of an array into a single value and returns a single value.

## ➕ Project: Calculator

- Create an on-screen calculator using HTML, CSS, and JavaScript.
- Create functions for basic math operations: add, subtract, multiply, and divide.
- Create a function `operate()` that takes an operator and two numbers.
- Create an HTML calculator with buttons and a display.
- Populate the display when digit buttons are clicked.
- Store first and second numbers and then `operate()` on them when the equals button is pressed.
- Display the result after the operation is performed.
- Handle edge cases, errors, and unexpected inputs.
