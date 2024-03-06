Functions in JavaScript - Basics

JavaScript Function

A function in JavaScript is a piece of reusable code that, when called or executed, completes a certain operation or computation.

The function keyword, the function name, any optional parameters in parentheses, and the code block encased in curly brackets are used to define functions. They can be called by preceding the function name with the parenthesized parameters.

Functions can also be supplied as arguments to other functions, set to variables, and returned as values by other functions. JavaScript functions are a core component of the language and are often utilized to develop modular code and create complicated applications.

Functions are used to make code less repetitive, more reusable, more modular, and simpler to comprehend. They are crucial for creating intricate software systems and are a fundamental idea in the majority of programming languages.

Example of a simple JavaScript function:

```
// Defining the function
function sum(num1, num2) {
  console.log(num1 + num2);
}

// Calling the function
sum(3, 6);      // Output: 9
```

This code defines a function called sum which is taking two arguments num1 and num2 and outputs sum using the + operator.

Example of a simple JavaScript function which will calculate the area of a rectangle:

```
function calculateArea(width, height) {
  let area = width * height;
  console.log(area);
}

// Call the function with arguments
calculateArea(5, 10);
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Function Declarations

In JavaScript, function declarations are one of the fundamental ways to define and create reusable blocks of code that can be called later in the program. They allow you to encapsulate logic and operations, making your code more organized and easier to maintain.

Here's the syntax for a function declaration:

```
function functionName(parameter1, parameter2) {
  // Function body: code that is executed when the function is called
  // You can use parameters and perform operations here
  return result; // Optional: You can return a value from the function
}
```

Let's break down the components of a function declaration:

function: This keyword is used to declare a function in JavaScript.

functionName: Replace this with the desired name for your function. It should follow the rules for variable naming (e.g., no spaces, can't start with a number).

parameters: These are placeholders for values that you can pass to the function when calling it. They are optional, and you can have none or multiple parameters.

Function body: This is the block of code enclosed within curly braces {}. It contains the logic and operations the function will perform.

return: You can use the return keyword to specify the value that the function will produce and send back when called. If there is no return statement, the function will implicitly return undefined.

Here's an example of a simple function declaration:

```
function greet(name) {
  return `Hello, ${name}!`;
}

const message = greet("Rohan");
console.log(message);

// Output
"Hello, Rohan!"
```

In this example, the greet function takes a name parameter and returns a greeting message using that parameter.

Function declarations are hoisted in JavaScript, which means they can be called before they are defined in the code. This makes them accessible throughout the entire scope in which they are declared.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Calling a Function

In JavaScript, calling a function is the process of executing the code inside the function's body. When you call a function, you use its name followed by parentheses (). If the function has any parameters, you can pass arguments to those parameters within the parentheses. The function will then be executed with the provided arguments, and it may return a value if it contains a return statement.

Here's how you call a function in JavaScript:

```
// Function declaration
function sayHello(name) {
  console.log(`Hello, ${name}!`);
}

// Function call with argument
sayHello("John");

// Output
"Hello, John!"
```

In this example, the function sayHello is declared with one parameter name. When the function is called with the argument "John", the code inside the function's body will execute, printing "Hello, John!" to the console.

Functions can also return values. Here's an example of a function that calculates the sum of two numbers and returns the result:

```
function add(a, b) {
  return a + b;
}

const result = add(3, 5);
console.log(result);

// Output
8
```

In this case, the function add takes two parameters a and b and returns their sum. When the function is called with add(3, 5), it evaluates to 8, which is then stored in the variable result and printed to the console.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

“return” keyword

The return keyword in JavaScript is used to specify the value that a function should produce and send back when called. When a function encounters a return statement, it immediately exits the function and returns the specified value to the caller. If there is no return statement in the function, it implicitly returns undefined.

Here's an example of a function using the "return" keyword:

```
function add(a, b) {
  return a + b;
}

const result = add(3, 5);
console.log(result);

// Output
8
```

In this example, the add function takes two parameters, a and b, and returns their sum using the return keyword.

The return keyword is vital when you want a function to produce a specific result or value that can be used in other parts of your code. It enables you to pass data between the function and the calling code, making functions powerful tools for encapsulating and reusing logic within JavaScript programs.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Parameters & Arguments

The functions we've developed so far carry out a task without input. Certain functions, however, can accept inputs and use those inputs to carry out a task.

In JavaScript functions, parameters and arguments are essential concepts related to passing data into and out of functions. They are often used to customize the behavior of functions and make them reusable with different values.

1. Parameters: Parameters are placeholders or variables defined in the function's declaration. They act as local variables within the function's body, representing the values that the function expects to receive when it is called. Parameters are listed inside the parentheses () when declaring a function.

```
function greet(name) {
  console.log(`Hello, ${name}!`);
}
```

In this example, name is a parameter of the greet function. When the function is called, you can pass a value as an argument for name.

2. Default Parameters: In JavaScript, default parameters allow you to specify default values for function parameters. If a function is called without providing a value for a parameter, the default value is used instead. This feature was introduced in ECMAScript 6 (ES6) and provides a convenient way to handle missing or undefined arguments.

Here's the syntax for defining default parameters in a function:

```
function functionName(parameter1 = defaultValue1, parameter2 = defaultValue2) {
  // Function body
}
```

If a value for parameter1 is not provided when the function is called, it will take on the value of defaultValue1, and if parameter2 is not provided, it will take on the value of defaultValue2.

Example:

```
function greet(name = "Guest") {
  console.log(`Hello, ${name}!`);
}

greet();
greet("John");

// Output
"Hello, Guest!"   (no argument provided, default parameter used)
"Hello, John!"    (argument "John" provided, default parameter ignored)
```

In this example, the greet function has a default parameter name = "Guest". When the function is called without an argument, the default value "Guest" is used. If an argument is provided, the default parameter is overridden by the provided value.

Default parameters enhance the flexibility and readability of functions by providing sensible defaults for missing arguments, reducing the need for explicit checks for undefined values inside the function.

3. Arguments: Arguments are the actual values passed to the function when it is called. They correspond to the parameters defined in the function's declaration and provide the data with which the function will operate.

```
greet("John");
```

In this example, "John" is an argument passed to the greet function. The function will use this argument to replace the name parameter within the function's body and produce the output "Hello, John!".

In summary, parameters are variables declared in the function's declaration that act as placeholders for values, while arguments are the actual values passed to the function when it is called. By providing arguments when calling a function, you can customize its behavior and perform operations with different data. Parameters and arguments make functions flexible and reusable in JavaScript code.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Helper Functions

Helper functions, also known as utility functions or helper methods, are functions in programming that are created to assist other functions or modules by performing specific tasks or providing reusable functionality. They are designed to handle repetitive or complex tasks, making code more organized, modular, and easier to maintain.

Here's an example of a helper function that calculates the area of a rectangle:

```
function calculateRectangleArea(width, height) {
  return width * height;
}


const area = calculateRectangleArea(5, 10);
console.log(area);

// Output
50
```

In this example, calculateRectangleArea is a helper function that takes width and height as parameters and returns their product. This function can be reused in various parts of the program or combined with other functions to perform more complex calculations.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Use cases of Helper Function

Using helper functions helps improve code maintainability, readability, and organization by promoting the principle of Don't Repeat Yourself (DRY). They are a fundamental part of building scalable and maintainable software systems.

1. Modularize Code: By isolating specific tasks into helper functions, you can break down complex operations into smaller, more manageable pieces, making the code easier to read and understand.

Let's say you have a complex task that involves multiple steps, such as uploading a file, parsing its contents, and saving the results to a database. You can break down this task into smaller functions and call them sequentially:

```
function uploadFile() {
  // code to upload file
}

function parseFile() {
  // code to parse file contents
}

function saveToDatabase(data) {
  // code to save data to database
}

uploadFile();
let data = parseFile();
saveToDatabase(data);
```

2. Reusability: Helper functions can be used in multiple places within a program or across different projects, promoting code reuse and reducing redundancy.

Let's say you have a function called calculateArea that calculates the area of a rectangle. You can call this function multiple times with different parameters to calculate the area of different rectangles:

```
function calculateArea(length, width) {
  return length * width;
}


let area1 = calculateArea(5, 10); // returns 50
let area2 = calculateArea(3, 7); // returns 21
```

3. Encapsulation: They allow you to encapsulate specific logic or operations, hiding the implementation details from the main functions, and promoting abstraction.

Let's say you have a function called toggleButton that toggles the state of a button between on and off. Instead of manipulating the button directly in your code, you can encapsulate this behavior in a function and call it whenever you need to toggle the button:

```
function toggleButton(button) {
  if (button.getAttribute('data-state') === 'on') {
    button.setAttribute('data-state', 'off');
    button.textContent = 'Off';
  } else {
    button.setAttribute('data-state', 'on');
    button.textContent = 'On';
  }
}

let myButton = document.querySelector('#my-button');
toggleButton(myButton); // toggles button state
```

4. Scope: Functions have their own scope, which means they can access and modify variables within their scope, but not outside of it. This can help prevent naming collisions and make your code more secure.

Let's say you have a function called calculateTotal that calculates the total cost of an order. Within this function, you define a variable called subtotal. This variable is only accessible within the scope of the function, and cannot be accessed or modified from outside of it:

```
function calculateTotal(items) {
  let subtotal = 0;
  for (let item of items) {
    subtotal += item.price;
  }
  let tax = subtotal * 0.1;
  let total = subtotal + tax;
  return total;
}

let myItems = [
  { name: 'Widget', price: 9.99 },
  { name: 'Gadget', price: 14.99 },
  { name: 'Doohickey', price: 4.99 }
];

let myTotal = calculateTotal(myItems); // returns 31.47
```

5. Error Handling: Helper functions can be used to handle error scenarios, input validation, or provide fallback options when things go wrong.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------


Summary

What did we learn?

Functions are defined using the function keyword, followed by the function name, optional parameters in parentheses, and a code block enclosed in curly brackets.

JavaScript functions can be called by preceding the function name with the parenthesized parameters.

Function declarations define a function with a name or identifier, similar to variable declarations.

Functions can be called multiple times and can accept inputs through parameters.

Default parameters allow for predetermined values when a function is called without an or undefined argument.

The return keyword sends data from a function call back to the calling code, allowing the output to be stored in a variable for further use.
