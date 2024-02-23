Introduction to JavaScript

What is JavaScript?

JavaScript is a programming language that is primarily used for creating dynamic web pages and web applications.

--------------------------------------------------------------------------------------------------------------------------------------------------------------

What are the features of JavaScript?

Some key features of JavaScript include:
It is a client-side scripting language.
It is interpreted and dynamically typed.
It supports object-oriented programming.
It provides a rich set of built-in functions and libraries.

--------------------------------------------------------------------------------------------------------------------------------------------------------------

Why Dynamically Typed Language?

In the world of programming, dynamically-typed languages stand out as the ones where the interpreter assigns the variable's type at runtime based on its value at the moment. This feature allows for greater flexibility in coding, as well as faster prototyping and testing.
It's unnecessary to declare the variable type when declaring a variable explicitly.

--------------------------------------------------------------------------------------------------------------------------------------------------------------


Need for JavaScript

Limitations and Constraints of the Webpage Created with HTML & CSS:

This simple static HTML currently lacks responsiveness but includes images, text, buttons, and other UI features.
The website needs to be utilized from a business or a customer standpoint.

JavaScript is useful because it provides the following advantages:

Our system is lightning-fast because it runs code locally instead of contacting the server.
Create highly responsive interfaces and elevate the user experience with ease.
JavaScript does not require a compilation step. Instead, an interpreter in the browser reads over the JavaScript code, interprets each line, and runs it.
Enhance functionality on the fly without server latency, providing a seamless experience for your users.

--------------------------------------------------------------------------------------------------------------------------------------------------------------

What makes them so well-loved by programmers?

As of today, there are 1.9 billion websites on the Internet, with 95% of them utilizing JavaScript in some capacity.
To improve the functionality of certain websites and web applications, try disabling JavaScript access on your web browser. JavaScript is responsible for managing the interactivity of the web, and turning it off may cause some sites to appear less engaging.
Additionally, developers appreciate it for its user-friendly nature, making it easy to learn and become proficient in. Even with no prior coding experience, one can create stunning projects with the knowledge of JavaScript. For businesses, this translates to a reliable pool of competent JavaScript developers always at the ready.
Other than simplicity, JavaScript is also known for its speed and versatility. It can be used for the following programming projects:
Add interactive elements to your website
Develop web and mobile applications
Create web servers
Develop games

--------------------------------------------------------------------------------------------------------------------------------------------------------------

Why is JavaScript Popular?

Versatility: JavaScript is primarily used for front-end development, but it can also be used for server-side programming with Node.js. This flexibility allows developers to work across the full stack with a single language.

Browser compatibility: JavaScript is supported by all modern web browsers, making it an essential tool for creating interactive and dynamic websites that work across different platforms and devices.

Ease of learning: JavaScript has a relatively simple syntax and is considered easier to learn compared to some other programming languages.

Large community and ecosystem: JavaScript has a massive community of developers, which means there are abundant resources, tutorials, and tools available for learning and problem-solving. Additionally, there are numerous libraries and frameworks, such as React, Angular, and Vue.js, that make development faster and more efficient.

Regular updates and improvements: JavaScript is continuously evolving, with new features being added to the language regularly through the ECMAScript standard. This ensures that JavaScript stays up-to-date with modern programming practices and techniques.

Asynchronous programming: JavaScript supports asynchronous programming, which is essential for handling multiple tasks simultaneously, such as handling user input or fetching data from a server without blocking the main thread.

--------------------------------------------------------------------------------------------------------------------------------------------------------------

JavaScript Engine

Each web browser has its own JavaScript engine that supports JavaScript scripts so that they can function properly. The main task of a JavaScript engine is to take JavaScript code and convert it into optimized code, fast that can be interpreted by a browser. Here are the names of the JavaScript engines used in some of the most popular web browsers:
Chrome: V8
Firefox: SpiderMonkey
Safari: JavaScript Core
Microsoft Edge/Internet Explorer: Chakra/ChakraCore.

--------------------------------------------------------------------------------------------------------------------------------------------------------------

Interaction: alert, prompt, confirm

In JavaScript, alert, prompt, and confirm are three built-in functions that allow for simple interaction with users through dialog boxes in the web browser. These dialog boxes are modal, meaning they halt the execution of the script until the user interacts with them.

Example:-

```alert("Hello World");```

prompt: The prompt function displays a dialog box that allows the user to enter input. It takes two arguments: the message to be displayed as a prompt and an optional default value for the input field. The function returns the text entered by the user as a string or null if the user cancels the dialog.

Example:-
```
const name = prompt("Please enter your name:", "John Doe");
if (name !== null) {
  console.log("Hello, " + name + "!");
}
```

confirm: The confirm function displays a dialog box with a message and two buttons: OK and Cancel. It is typically used to prompt the user for a yes-or-no decision. The function returns true if the user clicks OK and false if the user clicks Cancel.

Example:

```
const result = confirm("Are you sure you want to delete this item?");
console.log(result);
```

--------------------------------------------------------------------------------------------------------------------------------------------------------------

What is a Variable?

It is a name given (assigned) to a memory location that serves as a temporary data container. Variables are reserved memory locations used to store values.

JavaScript Variable Scope

It refers to where it is visible and can be used in your code.

Global Variables: A global variable can be defined anywhere in your JavaScript code and has a global scope.

Local Variables: The scope of a local variable is limited to the function in which it is defined, meaning it is not visible outside of that function. Similarly, function parameters are always local to that specific function.

--------------------------------------------------------------------------------------------------------------------------------------------------------------

How to declare variables in JavaScript?

JavaScript has three ways to declare variables:

let (declares mutable variables)
var (declares mutable variables used before ES6)
const (declares immutable variables)

let has block scope and can be reassigned but not redeclared.


var has function scope and can be redeclared and reassigned.
const has block scope and cannot be redeclared or reassigned.

--------------------------------------------------------------------------------------------------------------------------------------------------------------

Data Types

JavaScript has six primitive data types: string, number, boolean, null, undefined, and symbol. None primitive data types : object, Array, function

Array: An Array is a collection of values or elements, which can be of any data type that is stored in a contiguous memory location and accessed using an index.

```
var names = [ “Mayank”, “Shubham”, “Amrita”]; // Array of strings
```

```
var ages = [ 30, 29, 33 ] ; // Array of numbers
```

Objects: An object refers to a set of properties consisting of a key and a corresponding value. These values can include primitive data types, functions, or even other objects.

```
var student = {
  roll_no: 34,
  name: "Mayank",
  age: 27,
  city: "Delhi"
};
```

Functions: A function is a block of code used to perform a specific task or action and can be reused in different parts of a program.

```
function sum(a, b) {
  return a + b
}

console.log(sum(3, 4)); // 7
console.log(sum(5, 6)); //11

```
--------------------------------------------------------------------------------------------------------------------------------------------------------------


Understanding Special Types in JavaScript

JavaScript Type Conversions

JavaScript Type Conversion is the process of converting one data type to another.

In JavaScript, there are two types of conversions: Implicit and Explicit.

Implicit Type Conversion in JavaScript 

Implicit Type Conversion is the automatic conversion of data types done by JavaScript during expressions evaluation. This type of conversion occurs when JavaScript expects one data type but gets another. For example, when a string is concatenated with a number, JavaScript implicitly converts the number to a string.

Example 1: Numeric string used with + gives string type

```
let numStr = "10";
let result = numStr + 5;
console.log(typeof result); // string
```

Example 2: Implicit Conversion to Number

```
let numStr = "10";
let result1 = numStr - 5;
let result2 = numStr / 2;
let result3 = numStr * 3;
console.log(typeof result1); // number
console.log(typeof result2); // number
console.log(typeof result3); // number
```

Example 3: If a Boolean is used, true is 1, false is 0

```
let bool = true;
let result = bool + 5;
console.log(typeof result); // number
console.log(result); // 6
```

Note that JavaScript considers 0 as false and all non-zero numbers as true. If true is converted to a number, then the result is always 1.

Example 4: null is zero when used with the number

```
let nullVal = null;
let result = nullVal + 5;
console.log(typeof result); // number
console.log(result); // 5
```

Explicit Conversion in JavaScript

Explicit Type Conversion is the developer's manual conversion of one data type to another using built-in conversion functions. It is also known as typecasting.

Convert to Number Explicitly

In JavaScript, you can utilize Number() to convert numeric strings and Boolean values into numbers.
let result;

```
// string to number

result = Number('324');
console.log(result); // 324

result = Number('324^(e-1)')
console.log(result); // 32.4
```

```
// boolean to number

result = Number(true);
console.log(result); // 1

result = Number(false);
console.log(result); // 0
```

NaN will be the result if a string is not a valid number. 
let result;

```
result = Number('hello');
console.log(result); // NaN
```

```
result = Number(undefined);
console.log(result); // NaN
```

```
result = Number(NaN);
console.log(result); // NaN
```

You can also generate numbers from strings using parseInt(), parseFloat(), unary operator +, and Math.floor().

```
let result;

result = parseInt('20.01');
console.log(result); // 20

result = parseFloat('20.01');
console.log(result); // 20.01

result = +'20.01';
console.log(result); // 20.01

result = Math.floor('20.01');
console.log(result); // 20
```

Convert to String Explicitly

In JavaScript, you can convert non-string data types to strings using either String() or toString().

```
//number to string

let result;
result = String(325);
console.log(result);  // "325"

result = String(2 + 5);
console.log(result); // "7"
```

```
//other data types to string

result = String(undefined);
console.log(result); // "undefined"

result = String(null);
console.log(result); // "null"

result = String(true);
console.log(result); // "true"

result = String(NaN);
console.log(result); // "NaN"
```

```
//using toString()

result = (324).toString();
console.log(result); // "324"

result = true.toString();
console.log(result); // "true"
```

```
result = String(false);
console.log(result); // "false"
```

Note: String() takes null and undefined and converts them to string. However, toString() gives errors when null is passed.

Convert to Boolean Explicitly

You can use Boolean() to convert other data types to a Boolean in JavaScript. The conversion rules state that undefined, null, 0, NaN, and '' will convert to false.

```
let result;
result = Boolean('');
console.log(result); // false

result = Boolean(0);
console.log(result); // false

result = Boolean(undefined);
console.log(result); // false

result = Boolean(null);
console.log(result); // false

result = Boolean(NaN);
console.log(result); // false

All other values give true.

result = Boolean(324);
console.log(result); // true

result = Boolean('hello');
console.log(result); // true

result = Boolean(' ');
console.log(result); // true
```

--------------------------------------------------------------------------------------------------------------------------------------------------------------

Summary

What did we learn?

JavaScript is a programming language that is interpreted, high-level, and dynamic and is utilized to develop interactive and dynamic web pages and applications.

It is essential for adding interactivity and dynamic elements to websites, allowing developers to create complex and responsive user interfaces, validate user input, and communicate with back-end systems.

JavaScript is popular due to its versatility, ability to run on various platforms, large and active community, and rich library and tools ecosystem.

It powers the internet by enabling dynamic, interactive, and engaging website user experiences, allowing for real-time updates and communication with back-end systems, and making it possible to create complex and responsive web applications.

Cross-browser compatibility and standards compliance are crucial aspects of web development. JavaScript developers must be aware of compatibility issues and write code that follows web standards to ensure their websites are accessible and functional for all users.

Variables in JavaScript are containers that hold a value and can be referenced by a name. They can be declared using the "var", "let", or "const" keywords and store different data types.

Variables can have different scopes, including global, local, and block-level scopes, depending on where they are defined in the code.