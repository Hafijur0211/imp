JavaScript Loops & Control Statements

For loop

A for-loop is a control flow statement that allows you to execute a block of code repeatedly. It's typically used when you need to perform a specific task a certain number of times or when you need to iterate over an array or object. 

The basic syntax for a for-loop in JavaScript is as follows:

```
for (initialization; condition; increment/decrement) {
  // code to be executed
}
```

Let's break down each part of the syntax:

Initialization: This is where you declare and assign an initial value to a counter variable. This is usually a variable that will be used to track the current iteration of the loop. For example, you might initialize a variable called i to a value of 0.

Condition: This Boolean expression serves as a decision-making factor to either continue or terminate the loop. The loop will keep executing if the condition evaluates to true, but it will terminate if it evaluates to false. This expression is evaluated at the beginning of each iteration of the loop. As an instance, you could employ the condition i < 10 to signify that the loop must persist until i is no longer less than 10.

Increment/decrement: This is where you update the counter variable at the end of each iteration of the loop. This is usually done using an increment or decrement operator. For example, you might use the expression i++ to increment i by 1 at the end of each iteration.

Code to be executed: This is the block of code that will be executed each time the loop iterates. This can be any valid JavaScript code, including other control flow statements, function calls, or variable assignments.

Here's an example of a for-loop that iterates over an array of numbers and logs each one to the console:

```
const numbers = [1, 2, 3, 4, 5];

for (let i = 0; i < numbers.length; i++) {
  console.log(numbers[i]);
}
```

Explanation

In this example, the loop initializes a variable called i to a value of 0, sets the condition to i < numbers.length (which is true as long as i is less than the number of elements in the numbers array), and increments i by 1 at the end of each iteration. The block of code that is executed simply logs the current element of the array to the console. The loop continues to iterate until i is equal to the length of the array, at which point the condition is false and the loop terminates.

Example 1: Display a Text Five Times

```
// program to display text 5 times
for (let i = 0; i < 5; i++) {
  console.log("Hello, world!");
}

// Output
Hello, world!
Hello, world!
Hello, world!
Hello, world!
Hello, world!
```

Example 2: To Display Numbers from 1 to 5

```
// write a program to display numbers from 1 to 5
for (let i = 1; i <= 5; i++) {
  console.log(i);
}

// Output
1
2
3
4
5
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Infinite for loop

An infinite loop in JavaScript is a loop that runs indefinitely and it never breaks unless the browser is closed or the program is manually stopped.
Here's an example of an infinite loop using a for loop:

```
// infinite for loop
for (;;) {
  console.log("This loop will run indefinitely!");
}
```

In this example, the for-loop is initialized with an empty initialization, condition, and final expression, which means that there are no conditions to stop the loop. Therefore, the loop will run indefinitely and keep logging the message "This loop will run indefinitely!" to the console.

Infinite loops can cause your program to become unresponsive and can potentially crash the browser or the environment in which they're running. They should be avoided in most cases. If you're testing an infinite loop in your browser, be prepared to kill the page or even the browser itself.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

For...in loop

The for...in loop in JavaScript is a control flow statement that is used to iterate over the enumerable properties of an object, such as its own properties or those inherited through its prototype chain. It provides a convenient way to loop through the properties of an object without needing to know the property names in advance. 

Here's the syntax for the for...in loop:

```
for (let variable in object) {
  // code to be executed for each value in iterable
}
```

In this syntax, variable is a variable that is assigned to each property name of the object as the loop iterates, and object is the object that is being looped over. For each property of the object, the code block inside the loop is executed once, with the variable denoting the current property name during each iteration.
Here’s the basic introduction for Objects in JavaScript. You’ll be learning more about Objects in JavaScript in further lessons. 

In JavaScript, an object is a collection of key-value pairs. Each key-value pair in an object is known as a property.

The key (also known as "name" or "identifier") is always a string. The value can be any data type, including numbers, strings, Booleans, arrays, functions, and even other objects.

Here's an example of a for...in loop:

```
let person = {
  name: 'Alice',
  age: 25,
  city: 'New York'
};

for (let key in person) {
  console.log(`${key}: ${person[key]}`);
}

// Output
name: Alice
age: 25
city: New York
```

In this example, the for...in loop is used to iterate over the properties of the person object. For each iteration, the variable key is assigned the name of a property, and person[key] is used to access the value of the property.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

For...of loop

The for...of loop is a modern loop in JavaScript that is used to iterate over iterable objects, such as Arrays, Strings, Maps, Sets, and so on. It's a more concise and readable syntax compared to traditional for loops and for...in loops.

Here's the syntax for the for...of loop:

```
for (let variable of iterable) {
  // code to be executed for each value in iterable
}
```

The variable variable will be assigned the value of the next element in the iterable object. The loop will continue to execute until the iterator has no more values to return.

Here's an example of a for...of loop:

```
const array = [1, 2, 3, 4, 5];

for (let number of array) {
  console.log(number);
}

// Output
1
2
3
4
5
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

For...in vs For...of

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

While loop

The while loop in JavaScript is a statement for controlling the flow of code that enables the repeated execution of a code block while a certain condition remains true.

The syntax for a while loop in JavaScript is as follows:

```
while (condition) {
  // code to be executed while the condition is true
}
```

The conditionis an expression that is evaluated before each iteration of the loop. 

If the condition is true, the code enclosed within the loop will be executed. 

When the condition is false, the loop will terminate, and the program will proceed to execute from the location immediately following the loop.

Example 1: To display Numbers from 1 to 5

```
let i = 1;
while (i <= 5) {
  console.log(i);
  i++;
}

// Output
1
2
3
4
5
```

Explanation

In this example, the condition is i <= z. The loop will continue to execute as long as the value of i remains less than or equal to 5. Inside the loop, the current value of i is printed to the console, and then i is incremented by 1 using the i++ shorthand for i = i + 1.

Example 2: Sum of Positive Numbers Only

```
// array of numbers
const numbers = [5, -2, 10, 0, -3, 8, -1];

// variable to store the sum
let sum = 0;

// index variable for the while loop
let i = 0;

// Using a while loop, iterate through the array and add any positive numbers to the sum
while (i < numbers.length) {
  if (numbers[i] > 0) {
    sum += numbers[i];
  }
  i++;
}

// print the sum of positive numbers
console.log(`The sum of positive numbers is ${sum}`);

// Output
23
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

do...while loop

The do...while loop in JavaScript shares similarities with the while loop, except that it runs the loop body at least once, regardless of whether the condition is false or not. The loop condition is checked after each iteration, and the loop continues to execute until the condition becomes false.

Here's the syntax for the do...while loop in JavaScript:

```
do {
  // loop body
} while (condition);
```

The do...while loop consists of the following parts:

The do keyword: This keyword starts the loop and indicates the beginning of the loop body.

The loop body: This is the code that gets executed repeatedly as long as the condition is true. This part of the loop must be enclosed in curly braces { }.

The while keyword: This keyword is followed by a condition enclosed in parentheses ( ). The condition is checked after each iteration of the loop, and the loop continues to execute as long as the condition is true.

Example: To display Numbers from 1 to 5

```
let i = 1;

do {
  console.log(i);
  i++;
} while (i <= 5);

// Output
1
2
3
4
5
```

Explanation

In this program, we initialize the variable ito 1 outside the loop. Within the loop, we initially output the value of i to the console, and then use the ++ operator to increase it by 1.

The loop will continue executing as long as the condition i <= 5is true. 

Due to the utilization of a do...while loop, the loop body gets executed at least once prior to the condition being checked. 

Once the value of i reaches 6, the condition becomes false and the loop exits. Therefore, this program will log the numbers from 1 to 5 to the console.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

break Statement

The break statement in JavaScript is employed to prematurely terminate a loop prior to the loop condition being fulfilled. It can be used with for, while, and do-while loops.

Once the break statement is encountered within a loop, the loop terminates immediately, and control is transferred to the statement succeeding the loop. This allows you to exit a loop prematurely based on a certain condition without having to wait for the loop to run its course.

Working of JavaScript break Statement:

Example 1: break with for Loop

```
for (let i = 1; i <= 10; i++) {
  if (i === 5) {
    break;
  }
  console.log(i);
}

// Output
1
2
3
4
```

In this example, the loop will print out the numbers 1 through 4, but when i becomes 5, the break statement is executed, and the loop terminates early.

Example 2: break with while Loop

```
let i = 1;
while (i <= 10) {
  if (i === 5) {
    break;
  }
  console.log(i);
  i++;
}

// Output
1
2
3
4
```

In this case, the loop will also print out the numbers 1 through 4 before terminating early when i becomes 5.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

continue Statement

The continue statement in JavaScript is employed within loops to bypass the current iteration and proceed to the subsequent iteration of the loop. 

Example: 

```
// Example of using continue statement

for (var i = 1; i <= 5; i++) {
  // Skip iteration if i is odd
  if (i % 2 !== 0) {
    continue; // continue statement used here
  }

  console.log("Iteration: " + i);
}

console.log("Exited the loop.");

// Output
Iteration: 2
Iteration: 4

```

Exited the loop. 

In this example, there is a for loop that iterates five times, from 1 to 5. Inside the loop, there is an if statement that checks if i is odd. If i is odd, the continue statement is executed, which skips the rest of the code in the loop for that iteration and moves on to the next iteration.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

continue with for Loop

In JavaScript, the continue statement is used within a loop to skip the current iteration and move on to the next iteration. It is commonly used when you want to skip certain values or operations within a loop and move on to the next one. The continue statement works with all types of loops, including the for loop.

Here is an example of using continue with a for loop in JavaScript:

```
for (let i = 1; i <= 5; i++) {
  if (i === 3) {
    // skip iteration if i equals 3
    continue;
  }
  console.log(i);
}

// Output
1
2
4
5
```

In the above example, the loop will iterate through the values of i from 1 to 5. In the event that i is equal to 3, the continue statement will be executed, causing the loop to disregard the present iteration and proceed to the subsequent one. This means that the number 3 will not be printed to the console.

It's important to note that the continue statement only skips the current iteration and moves on to the next one. It does not stop the loop entirely. If you want to stop the loop based on a condition, you should use the break statement instead.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Summary

What did we learn?

JavaScript Loops and Control Statements are fundamental building blocks of JavaScript programming that allow developers to control the flow of their code. 

Loops are used to repeat blocks of code, while control statements are used to make decisions and direct the flow of code execution based on conditions. 

The main types of loops in JavaScript are for loops and while loops, and the main types of control statements are if statements, switch statements, and ternary operators. 

The break statement in JavaScript is used to exit a loop prematurely before the loop's condition is met.

Shortcomings & Challenges

if-else loops are that they can become slow and inefficient when used to handle many conditions.

if-else loops can be error-prone, as it is easy to forget to include a condition or to include a condition that is never met.

One of the biggest risks with while and do-while loops is the possibility of creating an infinite loop where the loop never ends.

Using break statements can cause performance overhead, especially in large loops where the code must evaluate the break condition repeatedly.