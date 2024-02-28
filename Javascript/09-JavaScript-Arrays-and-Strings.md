JavaScript Arrays and Strings

JavaScript Array

A JavaScript array is an object that can store multiple values. Arrays are zero-indexed, meaning that the first element in the array is at index 0, the second element is at index 1, and so on.

For example:
Here, words is an array. The array stores three values.
const words = ['hello', 'world', 'Hafijur'];

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

JavaScript Array indexing

In JavaScript, arrays are zero-indexed, which means that the initial element is positioned at index 0, followed by the second element at index 1, and this pattern continues sequentially. In order to access an element in an array, you can use the array name followed by square brackets enclosing the index of the desired element.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Array Operations

Creating an Array

In JavaScript, there are two ways to create an array:

Array literal

This is the most common way to create an array, using square brackets [] and placing the array elements inside the brackets, separated by commas. 

```
let fruits = ['apple', 'banana', 'orange'];
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Array Constructor

An alternative method to create an array involves using the Array() constructor with the new keyword. With this approach, the length of the array needs to be specified as an argument.

```
let numbers = new Array(3); // creates an empty array with a length of 3
```

Note: It is recommended to create arrays using array literals instead of other methods.
 
An array in JavaScript can contain not only simple data types but also more complex ones, such as arrays, functions, and other objects. 

```
For example:

let myArray = [
  1, "Hello", true, [2, 4, 6],
  {
    name: "John",
    age: 30
  },
  function() {
    console.log("This is a function inside an array");
  }
];

console.log(myArray[3][1]); // Output: 4

myArray[5](); // Output: This is a function inside an array
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Accessing Array Elements

Accessing array elements is possible using indices starting from 0 and incrementing by 1 for each subsequent element.

```
For example:

const fruits = ['apple', 'banana', 'orange'];

console.log(fruits[0]); // output: "apple"
console.log(fruits[1]); // output: "banana"
console.log(fruits[2]); // output: "orange"
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Adding Element to an Array

The push() method inserts an element to the array's last index.

For example:

```
let myArray = [1, 2, 3];

// adds an element to the array end
myArray.push(4);

console.log(myArray); // output is: [1, 2, 3, 4]
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

The unshift() method inserts an element at the beginning of the array.

For example:

```
const fruits = ['banana', 'apple', 'orange'];
console.log(fruits); // ['banana', 'apple', 'orange']

fruits.unshift('grape');
console.log(fruits); // ['grape', 'banana', 'apple', 'orange']
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Changing Array Elements

You can also modify elements or add new ones by accessing them through their index value in the array.

```
let fruits = ['apple', 'banana', 'cherry'];
console.log(fruits); // output: ['apple', 'banana', 'cherry']

fruits[1] = 'pear';
console.log(fruits); // output: ['apple', 'pear', 'cherry']

fruits[3] = 'orange';
console.log(fruits); // output: ['apple', 'pear', 'cherry', 'orange']
```

For example:

Suppose an array has three elements. If you try to insert an element at index 4 (fifth element), the fourth element will be undefined.

```
let dailyActivities = [ 'eat', 'sleep', 'play'];

// this will add the new element 'running' at the 4 index

dailyActivities[4] = 'running';

console.log(dailyActivities); // ["eat", "sleep", "play", undefined, "running"]
```

If you attempt to add elements to higher indices, the indices in between will have an undefined value.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Removing Array Element 

By using the pop() method, you can remove the final element from the array while also receiving its returned value.

For example:

```
let fruits = ['apple', 'banana', 'orange'];
let removedFruit = fruits.pop();  // removes 'orange' from the array and returns it

console.log(fruits);              // prints ['apple', 'banana']
console.log(removedFruit);        // prints 'orange'
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

The shift() method will remove the first element and returns the removed element as its returned value.

For example:

```
let fruits = ['apple', 'banana', 'orange'];
let removedFruit = fruits.shift();

console.log(fruits);         // Output: ['banana', 'orange']
console.log(removedFruit);   // Output: 'apple'
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Length of an Array

The length of an array can be obtained using the length property of the array.

For example:

```
let myArray = ["apple", "banana", "orange"];

console.log(myArray.length); // Output: 3
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Array Methods

JavaScript has several array methods that can be used to perform calculations and data manipulation.

Some of the commonly used methods include:

```
Operation
push()

Description
Appends one or multiple elements to the end of an array.

Example
arr.push(4);

Operation
pop()

Description 
Eliminates the final element from an array, returning it.   

Example 
const last = arr.pop();

Operation
shift()

Description 
Takes out the initial element from an array and gives it back.

Example 
const first = arr.shift();

Operation 
unshift()

Description 
Inserts one or several elements at the start of an array.

Example 
arr.unshift(1);

Operation
slice()

Description 
Provides a shallow duplicate of a part of an array.

Example
const subArr = arr.slice(1, 3);

Operation
splice()

Description
Inserts and/or deletes elements within an array.

Example
arr.splice(1, 0, 2, 3);

Operation
indexOf()

Description
Gives back the first index where a specified element is located.

Example
const index = arr.indexOf(3);

Operation
lastIndexOf()

Description
Supplies the final index where a particular element is situated.

Example
const lastIndex = arr.lastIndexOf(3);

Operation
includes()

Description
Establishes if an array contains a specific element.

Example
const isIncluded = arr.includes(2);


Operation
find()

Description
Offers the initial element in the array that meets a certain criterion.

Example
const found = arr.find(num => num > 2);

Operation
filter()

Description
Forms a new array containing elements that pass a certain test.

Example
const filtered = arr.filter(num => num > 2);

Operation
map()

Description
Produces a new array by applying a function to each array element.

Example
const doubled = arr.map(num => num * 2);

Operation
reduce()

Description
Condenses an array into a single value using a function.

Example
const sum = arr.reduce((acc, num) => acc + num, 0);

Operation
concat()

Description
Unites two or more arrays into a fresh array.

Example
const merged = arr1.concat(arr2);

Operation
join()

Description
Combines all elements of an array into a single string.

Example
const str = arr.join(', ');

Operation
reverse()

Description
Inverts the sequence of the elements within an array.

Example
arr.reverse();
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Array Methods Examples

```
let numbers = [3, 5, 1, 8, 2];

// sort the array in ascending order
numbers.sort();
console.log(numbers);             // [1, 2, 3, 5, 8]
```

// find the index of the element with value 5

```
let index = numbers.indexOf(5);
console.log(index);               // 3

// adding elements to array's end
numbers.push(4, 7);
console.log(numbers);             // [1, 2, 3, 5, 8, 4, 7]

// concatenate two arrays
let moreNumbers = [6, 9];
let allNumbers = numbers.concat(moreNumbers);
console.log(allNumbers);          // [1, 2, 3, 5, 8, 4, 7, 6, 9]

// check if the array includes a certain element
let hasFive = allNumbers.includes(5);
console.log(hasFive);             // true

// find the first element that is satisfying a condition
let greaterThanFour = allNumbers.find(number => number > 4);
console.log(greaterThanFour);     // 5
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Working of JavaScript Array

Arrays in JavaScript are implemented as objects and their indices are treated as object keys.

As arrays are objects, their elements are stored as references, so when an array is copied, any modification to it will also be reflected in an original array.

For example:

```
let arr = [{name: 'John'}, {name: 'Jane'}];
let arr1 = arr;
arr1.push({name: 'Bob'});

console.log(arr); // [{name: 'John'}, {name: 'Jane'}, {name: 'Bob'}]
console.log(arr1); // [{name: 'John'}, {name: 'Jane'}, {name: 'Bob'}]

arr[0].name = 'Mike';
console.log(arr); // [{name: 'Mike'}, {name: 'Jane'}, {name: 'Bob'}]
console.log(arr1); // [{name: 'Mike'}, {name: 'Jane'}, {name: 'Bob'}]
```

You can also store values by passing a named key in an array.

For example:

```
let arr = ['h', 'e'];
arr.name = 'John';

console.log(arr); // ["h", "e"]
console.log(arr.name); // "John"
console.log(arr['name']); // "John"
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Activity: Code Practice

Use the appropriate Array methods on the given array according to the instructions and print each of step in console.

Use the push() method to add a new element, grape to the end of the fruits array.

The pop() method removes the last element from the fruit array.
Use the shift() method to remove the first element from the fruits array.

```
const fruits = ['apple', 'banana', 'orange', 'kiwi', 'pear'];
Solution
const fruits = ['apple', 'banana', 'orange', 'kiwi', 'pear'];
```

```
// 1. Use the push() method to add a new element, 'grape', to the end of the fruits array.

fruits.push('grape');

console.log(fruits); // Output: ['apple', 'banana', 'orange', 'kiwi', 'pear', 'grape']
```

```
// 2. The pop() method removes the last element from the fruit array.

fruits.pop();

console.log(fruits); // Output: ['apple', 'banana', 'orange', 'kiwi', 'pear']
```

```
// 3. Use the shift() method to remove the first element from the fruits array.

fruits.shift();
console.log(fruits); // Output: ['banana', 'orange', 'kiwi', 'pear']
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Multidimensional Array

A multidimensional array is an array that holds one or more arrays as its elements.

```
For instance:
const matrix = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9]
];
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Create a Multidimensional Array

Example: We have created a 2-dimensional array called myArray with three rows and two columns. Each row is an array containing two strings.

```
const myArray = [];
myArray.push(["apple", "orange"]);
myArray.push(["grape", "pear"]);
myArray.push(["pineapple", "mango"]);

console.log(myArray);   

/* Output
[["apple", "orange"], ["grape", "pear"], ["pineapple", "mango"]]
*/
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Access Elements of Multidimensional Array

The elements belonging to the multidimensional array can be accessed using indices (0, 1, 2, etc.).

For example:
```
let x = [
['Jack', 24],
['Sara', 25],
['Peter', 26]
];

// accessing the first item
console.log(x[0]); // ["Jack", 24]

// accessing the first item of the first inner array
console.log(x[0][0]); // Jack

// accessing the second item of the third inner array
console.log(x[2][1]); // 26
```

One way to conceptualize a multi-dimensional array, such as 'x', is to view it as a table with 3 rows and 2 columns.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Add an Element to Multidimensional Array

Array's push() method or an indexing notation can be used to add elements to a multi-dimensional array.

Adding Element to the Outer Array

```
let studentData = [['Jack', 24], ['Sara', 23],];
studentsData.push(['Mark', 24]);

console.log(studentsData); //[["Jack", 24], ["Sara", 23], ["Mark", 24]
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Adding Element to the Inner Array

```
Using Index Notation

let studentsData = [['Jak', 23], ['Sara', 24],];
studentsData[1][2] = 'hello';

console.log(studentsData); // [["Jack", 23], ["Sara", 24, "hello"]]
```

```
Using push() method

let studentsData = [['Jack', 23], ['Sara', 24],];
studentsData[1].push('hello');

console.log(studentsData); // [["Jack", 23], ["Sara", 24, "hello dear"]]
```

An element can be added at a specific index using the splice() method of an array.

```
let studentsData = [['Sara', 23],['Jack', 24],];

// adding element at index 1
studentsData.splice(1, 0, ['Mark', 24]);

console.log(studentsData); // [['Sara', 23], ["Mark", 24], ['Jack', 24]]
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Remove an Element from a Multidimensional Array

Array's pop() method can be used to remove an element from a multi-dimensional array. 

```
Remove Element from Outer Array

let studentData = [['Jack', 25], ['Sara', 27],];
studentData.pop();

console.log(studentData); // [["Jack", 25]]
```

```
Remove Element from Inner Array

let studentData = [['Jack', 25], ['Sarah', 23]];
studentData[1].pop();

console.log(studentData); // [["Jack", 25], ["Sarah"]]
```

Using the splice() method of an array, it is possible to remove an element at a particular index.

```
let studentsData = [['Jack', 24], ['Mark', 23]];

// removing 1 index array item
studentsData.splice(1,1);

console.log(studentsData); // [["Jack", 24]]
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Iterating over Multidimensional Array

To iterate over a multidimensional array, you can use the forEach() method of the Array object.

For example:

```
let studentsData = [['Ryan', 24], ['Sara', 23],];

// iterating over the studentsData
studentsData.forEach((student) => {
    student.forEach((data) => {
        console.log(data);
    });
});

// Output
Ryan
24
Sara
23
```

The outer array elements are iterated using the first forEach() method, while the inner array elements are iterated using the second forEach() method.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Iterating over a multidimensional array can also be achieved using the for...of loop.

For example:

```
let studentsData = [['Ryan', 24], ['Sara', 23]];

for (let i of studentsData) {
  for (let j of i) {
    console.log(j);
  }
}
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

To iterate over a multidimensional array, you can also use a for() loop.

For example:

```
let studentsData = [['Ryan', 24], ['Sara', 27]];

// looping outer array elements
for(let i = 0; i < studentsData.length; i++){

    // gives the length of the inner array elements
    let innerArrayLength = studentsData[i].length;

    // looping inner array elements
    for(let j = 0; j < innerArrayLength; j++) {
        console.log(studentsData[i][j]);
    }
}
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

String Operations

Create JavaScript Strings

To create a string in JavaScript, surround the text with quotes.

There are three options to choose from:

```
Single quotes: 'Hello, World'

Double quotes: "Hello, World"

Template Literals (Backticks): `Hello, World`
```

For example:

```
//strings example

let singleQuoteString = 'This is a string using single quotes.';
let doubleQuoteString = "This is a string using double quotes.";
let templateLiteralString = `This is a string using a template literal.`;
```

Single or double quotes are preferred, as they have practically the same function.

Backticks are commonly used to incorporate variables or expressions into a string. The ${} syntax is used to interpolate the values of the variables into the string.

```
const name = "Ryan";
const age = 28;

console.log(`My name is ${name} and I am ${age} years old.`);

// Output
My name is Ryan and I am 28 years old.
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Access String Characters

There are two ways to access the characters in a string.

First approach is to treat strings as if they were arrays.

```
const a = 'hello';
console.log(a[1]); // "e"
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Another option is to use the charAt() method. 

```
const a = 'hello';
console.log(a.charAt(1)); // "e"
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

String Properties

JavaScript Strings are immutable

In JavaScript, strings are immutable, meaning their characters cannot be changed. 

```
let a = 'hello';
a[0] = 'H';

console.log(a); // "hello"
```

You can assign a variable name to a new string.

```
let a = 'hello';
a = 'Hello';

console.log(a); // "Hello"
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

JavaScript String is Case-Sensitive

It's important to remember that capitalizing letters matters. Lowercase and uppercase letters are treated as separate values. 

```
const a = 'a';
const b = 'A'

console.log(a === b); // false
```

In JavaScript, remember that a and A are considered distinct values.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

JavaScript Multiline Strings

You have two options to use a multiline string: the + operator or the \\ operator. 

```
// using the + operator

const message1 = 'This is a long message ' +
    'that spans across multiple lines' +
    'in the code.'

// using the \ operator

const message2 = 'This is a long message \
that spans across multiple lines \
in the code.'
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

JavaScript String Length

To determine the length of a string, you can utilize the built-in length property. 

```
const a = 'hello';

console.log(a.length); // 5
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

JavaScript String Methods

Below are some commonly used methods for working with strings in JavaScript:

```
Method
length
Description
Returns the length of the string
Example
"hello".length returns 5

Method
toUpperCase()
Description
Returns the string with all characters converted to uppercase letters.
Example
"hello".toUpperCase() returns "HELLO"

Method
toLowerCase()
Description
Returns the string with all characters converted to lowercase letters.
Example
"HELLO".toLowerCase() returns "hello"

Method
indexOf(substr)
Description
Returns the index of the first occurrence of a substring in the string
Example
"hello".indexOf("e") returns 1

Method
concat()
Description
Joins two or more strings and returns a new string.
Example
'hello'.concat(' ', 'world') returns 'hello world'

Method
slice(start, [end])
Description
Extracts a portion of the string and returns it as a new string
Example
"hello".slice(1, 3) returns "el"

Method
charAt(index)
Description
Returns the character at a specified index in the string
Example
"hello".charAt(1) returns "e"

Method
replace(searchValue, replaceValue)
Description
Replaces a substring in the string with another substring and returns the new string
Example
"hello".replace("e", "a") returns "hallo"

Method
split([separator])
Description
Splits the string into an array of substrings, optionally using a separator
Example
"hello world".split(" ") returns ["hello", "world"]

Method
trim()
Description
Removes whitespace from both ends of the string
Example
" hello ".trim() returns "hello"
```

These methods provide various ways to manipulate strings in JavaScript, such as finding specific characters or substrings, joining multiple strings together, or converting a string to all lowercase or uppercase.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

JavaScript String() Function

The String() function converts different data types to strings. 

```
For instance:

const a = 225; // number
const b = true; // boolean
```

```
//converting to string

const result1 = String(a);
const result2 = String(b);

console.log(result1); // "225"
console.log(result2); // "true"
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Escape Character

To include special characters in a string, you can use the escape character \, also known as a backslash.

For example:

```
const name = 'My name is \'Peter\'.';
console.log(name);   // My name is 'Peter'.
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Summary

What did we learn?

In JavaScript, you can create an array using the Array object or square brackets [].

Array elements are accessed using square brackets [] and the index element you would like to access.

JavaScript provides several built-in array methods, operations, and functions for working with arrays. Some commonly used methods include push, pop, shift, unshift, sort, reverse, splice, concat, slice, and indexOf.

Array operations include using the +operator to concatenate arrays and using the == and === operators to compare arrays.

In-built functions for arrays include Array.isArray(), Array.from(), Array.of(), Array.prototype.forEach(), Array.prototype.map(), Array.prototype.filter(), and Array.prototype.reduce().

A multi-dimensional array is an array that contains other arrays as its elements. You can create a multidimensional array by nesting arrays inside of each other. 

To access elements within a multidimensional array, you can use multiple square brackets representing a different dimension.

In JavaScript, arrays have several properties that provide information about their contents and behavior. Some of the most commonly used properties are length, constructor, prototype.