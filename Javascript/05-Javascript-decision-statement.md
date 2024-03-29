If Statement

In JavaScript, an if statement is used to execute a code block based on a Boolean expression conditionally. An if statement follows the syntax as shown below:

```
if (expression) {
  // code to execute if expression is true
}
```

Here, expression is a Boolean expression evaluated as either true or false. The code block within the curly braces is executed if the expression is true. If the expression is false, the code block is skipped over, and the program moves over to the next statement after the if block.
Here's an example:

```
const num = 10;
if (num > 0) {
  console.log("The number is positive");
}
```

In this example, the if statement evaluates the expression num > 0. Since num is indeed greater than 0, the code block within the curly braces is executed, and the message "The number is positive" is printed to the console.

---

If...else Statement

In JavaScript, there are two forms of the if...else statement:

if-else statement: This statement executes a block of code if the if condition is true and another block of code if the condition is false.

The if-else statement has the following syntax:

```
if (condition) {
  // this code will execute if condition is true
} else {
  // code to execute if condition is false
}
```

Here's an example:

```
const num = 10;
if (num > 0) {
  console.log("The number is positive");
} else {
  console.log("The number is not positive");
}
```

In this example, if the num variable exceeds 0, the first code block is executed, and the message "The number is positive" is printed to the console. Otherwise, the second code block is executed, and the message "The number is not positive" is printed to the console.
if-else if statement: This statement executes different blocks of code based on multiple conditions.

The syntax of the if-else if statement is as follows:

```
if (condition1) {
  // code to execute if condition1 is true
} else if (condition2) {
  // code to execute if condition2 is true
} else {
  // code to execute if both condition1 and condition2 are false
}
```

Here's an example:

```
const num = 10;
if (num > 0) {
  console.log("The number is positive");
} else if (num < 0) {
  console.log("The number is negative");
} else {
  console.log("The number is zero");
}
```

Explanation
In this example, if the num variable is greater than 0, the first block of code is executed and the message "The number is positive" is printed to the console. If num is less than 0, the second block of code is executed and the message "The number is negative" is printed to the console. If neither condition is true, the third block of code is executed and the message "The number is zero" is printed to the console.

---

Activity: Code Practice

Write a JavaScript program that takes a temperature as input and outputs a message about the weather.
Declare a variable temperature and assign any value to it. This will represent the current temperature.
Write an if statement that checks if the temperature is below 0. If it is, log a message to the console saying "It's freezing outside."
Write an else if statement that checks if the temperature is between 0 and 20. If it is, log a message to the console saying "The weather is cool."

Write another else if statement that checks if the temperature is between 21 and 30. If it is, log a message to the console saying "The weather is warm."
Write an else statement that logs a message to the console saying "It's hot outside."

Solution

```
let temperature = 25; // You can change this value to test different conditions

if (temperature < 0) {
    console.log("It's freezing outside.");
} else if (temperature >= 0 && temperature <= 20) {
    console.log("The weather is cool.");
} else if (temperature >= 21 && temperature <= 30) {
    console.log("The weather is warm.");
} else {
    console.log("It's hot outside.");
}
```

---

Nested if...else Statement

In JavaScript, a nested if-else statement is used to test for multiple conditions and execute different blocks of code based on those conditions. The basic structure of a nested if-else statement is as follows:

```
if (condition1) {
  // code to execute if condition1 is true

  if (condition2) {
    // code to execute if both condition1 and condition2 are true
  } else {
    // code to execute if condition1 is true but condition2 is false
  }

} else {
  // code to execute if condition1 is false
}
```

Let's take a look at an example:

```
// Checks if Number is Positive or not. Also checks it the number is even or odd.

const num = 10;
if (num > 0) {
  console.log("The number is positive");
  if (num % 2 === 0) {
    console.log("The number is even");
  } else {
    console.log("The number is odd");
  }
} else {
  console.log("The number is not positive");
}
```

Explanation

In this example, the outer if statement tests whether num is greater than 0.
If it is, the program moves into the first block of code and prints the message "The number is positive" to the console.
Then, there's an inner if statement that tests whether num is even or odd using the modulo operator (%).
If num is even, the program moves into the first block of code within the inner if statement and prints the message "The number is even" to the console.
If num is odd, the program moves into the else block within the inner if statement and prints the message "The number is odd" to the console.
If num is not greater than 0, the program moves into the else block within the outer if statement and prints the message "The number is not positive" to the console.
Nested if-else statements can be nested even further to create more complex conditions. However, it's essential to remember that excessive nesting can probably make your code hard to read and maintain.
Body of if...else With Only One Statement
In JavaScript, you can use a single statement as the body of an if-else statement without using curly braces {}. This can be useful for writing shorter and more concise code.

Here's an example:

```
const num = 10;

if (num > 0)
  console.log("The number is positive");
else
  console.log("The number is not positive");
```

In this example, we're using a single console.log statement as the body of each branch of the if-else statement. Since there's only one statement in each branch, we don't need to use curly braces. The if statement tests whether num is greater than 0, and if it is, it executes the first console.log statement. If num is not greater than 0, it executes the second console.log statement.

It's important to note that while using a single statement without curly braces can make your code shorter and more concise, it can also make it harder to read and maintain. If your if-else statement requires more than one statement in each branch, it's generally recommended to use curly braces to improve readability and avoid errors.

---

Switch Statement

In JavaScript, the switch statement is a type of control structure that allows you to execute different code blocks based on different conditions. It is a convenient alternative to using multiple if-else statements when you need to check the value of a single variable or expression against multiple possible values.
The basic syntax of a switch statement is as follows:

```
switch(expression) {
case value1:
// Executes this code block if the expression matches value1
break;
case value2:
// Executes this code block if the expression matches value1
break;
case value3:
// Executes this code block if the expression matches value1
break;
default:
// Executes this code block if none of the previous cases match
}
```

Here, the expression is evaluated and its value is compared to each of the value cases. If a match is found, the corresponding code block is executed until a break statement is encountered, which exits the switch statement. If none of the cases match, the code block associated with the default case is executed.

Let's look at an example to better understand how the switch statement works:

```
let dayOfWeek = 5;
let dayName;

switch (dayOfWeek) {
case 1:
dayName = 'Monday';
break;
case 2:
dayName = 'Tuesday';
break;
case 3:
dayName = 'Wednesday';
break;
case 4:
dayName = 'Thursday';
break;
case 5:
dayName = 'Friday';
break;
case 6:
dayName = 'Saturday';
break;
case 7:
dayName = 'Sunday';
break;
default:
dayName = 'Invalid day';
break;
}

console.log(dayName); // Output: "Friday"
```

Explanation

In this example, we have a variable dayOfWeek that stores the value 5, representing Friday. We use a switch statement to evaluate dayOfWeek against different case values. When the value of dayOfWeek matches the case value of 5, the code block following that case is executed, which sets the value of dayName to 'Friday'. Finally, we log the value of dayName to the console.

You can have multiple case statements that share the same code block by omitting the break statement after each case statement. This can be useful when executing the same code for multiple cases.

Here's an example:

```
let fruit = 'orange';
let color;

switch (fruit) {
case 'banana':
case 'lemon':
color = 'yellow';
break;
case 'apple':
case 'cherry':
case 'strawberry':
color = 'red';
break;
case 'grape':
case 'blueberry':
color = 'purple';
break;
default:
color = 'unknown';
break;
}

console.log(color); // Output: "unknown"
```

Explanation

In this example, we have a variable fruit that stores the value 'orange'. We use a switch statement to evaluate fruit against different case values. In this case, there are no matching cases, so the default block is executed, which sets the value of color to 'unknown'. Finally, we log the value of color to the console.

---

Switch Statement Use Case Examples

```
Type Checking in Switch Statement
// program using switch statement
let value = '123';

switch (typeof value) {
case 'string':
console.log('The value is a string');
break;
case 'number':
console.log('The value is a number');
break;
case 'boolean':
console.log('The value is a boolean');
break;
default:
console.log('The value is not a string, number, or boolean');
break;
}

// Output
"The value is a string"
```

Explanation

In this example, we have a variable value that stores the value '123'.
We use the typeof operator to determine the type of value and then use a switch statement to evaluate the type against different case values.
In this case, the typeof operator returns 'string', so the first case block is executed, which logs the message 'The value is a string' to the console.

If value had been a different type, the appropriate case block would be executed. For example, if value had been true, the third case block would be executed, logging the message 'The value is a boolean' to the console.

---

Simple Calculator

Use the parseFloat() function to convert the user input from a string to a number. This is important to ensure that the calculations are performed correctly.

```
// program for a simple calculator
let num1 = parseFloat(prompt('Enter the first number:'));
let num2 = parseFloat(prompt('Enter the second number:'));
let operator = prompt('Enter the operator (+, -, \*, /):');
let result;

switch (operator) {
case '+':
result = num1 + num2;
break;
case '-':
result = num1 - num2;
break;
case '_':
result = num1 _ num2;
break;
case '/':
result = num1 / num2;
break;
default:
console.log('Invalid operator');
}

console.log(`The result of ${num1} ${operator} ${num2} is ${result}`);

// Output
Enter the first number: 4
Enter the second number: 5
Enter operator: +
The result of 4 + 5 is 9
```

Explanation

In this program, we prompt the user to enter two numbers and an operator (+, -, \*, or /).

We then use a switch statement to evaluate the operator and perform the appropriate calculation.

If an invalid operator is entered, the default block is executed, and an error message is logged to the console.
Finally, we log the calculation result to the console using a template literal.

---

Switch with Multiple Case

```
let dayOfWeek = 'Tuesday';

switch (dayOfWeek) {
case 'Monday':
case 'Tuesday':
case 'Wednesday':
case 'Thursday':
case 'Friday':
console.log('It is a weekday');
break;
case 'Saturday':
case 'Sunday':
console.log('It is a weekend');
break;
default:
console.log('Invalid day of the week');
}
```

Explanation

In this example, we have a variable dayOfWeek that stores the value 'Tuesday'.

We use a switch statement to evaluate dayOfWeek against multiple case values for each day of the week.

If dayOfWeek matches any of the weekday case values, the first case block is executed, which logs the message 'It is a weekday' to the console.

If dayOfWeek matches either of the weekend case values, the second case block is executed, logging the message 'It is a weekend' to the console.

In JavaScript, if the break statement is not added in a switch statement case, the program will continue executing the code for all the subsequent cases until it reaches a break statement or the end of the switch statement. This is known as "falling through" the cases.

---

Summary

What did we learn?

JavaScript provides conditional statements to perform different actions based on different conditions. These include if, if...else, if...else if...else, and switch statements.

The if statement is used to execute a block of code only if a specified condition is true.

The if...else statement is used to execute one block of code if a specified condition is true, and another block of code if the condition is false.

The if...else if...else statement is used to execute one of many blocks of code, based on multiple conditions.

The switch statement is used to perform different actions based on different conditions. It's often used when you have many conditions to check.

The ternary operator is a shorthand way of writing an if...else statement. It's written as condition ? exprIfTrue : exprIfFalse.

In JavaScript, all values have an inherent Boolean value, generally known as either truthy or falsy. Most values are truthy unless they are defined as falsy. Falsy values in JavaScript are false, 0, '' (empty string), null, undefined, and NaN.

JavaScript has both strict comparison (===, !==) and type-converting comparison (==, !=). It's generally recommended to use strict comparison to avoid unexpected type coercion.

JavaScript includes logical operators (&&, ||, !) that can be used to combine or invert conditions.
Logical operators (&& and ||) use short-circuit evaluation, meaning they only evaluate what is necessary and then stop. This can be used to your advantage in your code.
