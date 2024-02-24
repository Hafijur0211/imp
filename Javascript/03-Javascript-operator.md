What are JavaScript Operators?

An operator is a special symbol that performs operations on operands (values and variables).

For example,

```
console.log(2 + 3); // 5
```

`+` is what we call an operator that does the adding, and 2 and 3 are the numbers we're adding together.

Operators are used to performing various operations.

Operators can be used to assign values, compare values, and perform arithmetic operations.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

JavaScript Operator Types

- Assignment Operators
- Arithmetic Operators
- Comparison Operators
- Logical Operators
- Bitwise Operators
- String Operators
- Other JavaScript Operators

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Assignment Operators

Values can be assigned to variables by making use of assignment operators. For example,
const x = 5;

To assign value 5 to variable x, you can use the = operator.

Below is a list of commonly used assignment operators:

```
Operator
`=`
Name
Assignment operator.
Example
a = 7;        // 7

Operator
`+=`
Name
Addition assignment
Example
a += 5;     // a = a + 5

Operator
`-=`
Name
Subtraction Assignment
Example
a -= 2;      // a = a - 2

Operator
`*=`
Name
Multiplication Assignment
Example
a *= 3;      // a = a * 3

Operator
`/=`
Name
Division Assignment
Example
a /= 2;      // a = a / 2

Operator
`%=`
Name
Remainder Assignment
Example
a %= 2;    // a = a % 2

Operator
`**=`
Name
Exponentiation Assignment
Example
a **= 2;    // a = square of a
```

Important: The most commonly used assignment operator is =. You will easily understand other assignment operators, such as +=, -=, and *=, once you study arithmetic operators in JavaScript.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Arithmetic Operators

Operators used for performing arithmetic calculations are known as Arithmetic Operators, which include the following:

```
const number = 3 + 5; // 8
```

When using the + operator in your code, you're basically adding two values together.

Below is a list of commonly used arithmetic operators:

```
Operator
+
Name
Addition
Example
a + b

Operator
-
Name
Subtraction
Example
a - b

Operator
*
Name
Multiplication
Example
a * b

Operator
/
Name
Division
Example
a / b

Operator
%
Name
Remainder
Example
a % b

Operator
++
Name
Increment (increment by 1)
Example
x++ or ++x

Operator
--
Name
Decrement (decrement by 1)
Example
--x or x-- 

Operator
**
Name
Exponentiation (Power)
Example
a ** b
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Example: Arithmetic operators in JavaScript

```
let num1 = 5;
let num2 = 3;

// addition
console.log('num1 + num2 = ', num1 + num2);  // 8

// subtraction
console.log('num1 - num2 = ', num1 - num2);  // 2

// multiplication
console.log('num1 * num2 = ', num1 * num2);  // 15

// division
console.log('num1 / num2 = ', num1 / num2);  // 1.6666666666666667

// remainder
console.log('num1 % num2 = ', num1 % num2);   // 2

// increment
console.log('++num1 = ', ++num1); // num1 is now 6
console.log('num1++ = ', num1++); // prints 6 and then increased to 7
console.log('num1 = ', num1);     // 7

// decrement
console.log('--num1 = ', --num1); // num1 is now 6
console.log('num1-- = ', num1--); // prints 6 and then decreased to 5
console.log('num1 = ', num1);     // 5

//exponentiation
console.log('num1 ** num2 =', num1 ** num2);
Increment(++) and Decrement(--) Operator

```

In JavaScript, the increment operator ++ adds 1 to a variable's value, while the decrement operator -- subtracts 1 from a variable's value.

```
let num = 5

console.log(++num);          // num becomes 6 and prints 6
console.log(num++);          // Prints 6 and num becomes 7
console.log(num);            // Prints 7
console.log(--num);          // num becomes 6 and prints 6
console.log(num--);          // Prints 6 and num becomes 5
console.log(num);            // Prints 5

```

Explanation


let num = 5; - Initializes the variable num with the value 5.

console.log(++num); - Pre-increment: The value of num is incremented by 1 first, making num equal to 6, and then the new value is printed. Output: 6.

console.log(num++); - Post-increment: The original value of num (which is now 6) is printed first, and then the value of num is incremented by 1, making num equal to 7. Output: 6.

console.log(num); - The current value of num is printed. Since num was incremented to 7 in the previous step, the output is 7.
console.log(--num); - Pre-decrement: The value of num is decremented by 1 first, making num equal to 6, and then the new value is printed. Output: 6.

console.log(num--); - Post-decrement: The original value of num (which is now 6) is printed first, and then the value of num is decremented by 1, making num equal to 5. Output: 6.
console.log(num); - The current value of num is printed. Since num was decremented to 5 in the previous step, the output is 5.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Comparison Operators

Comparison operators are used to comparing 2 values and then return a Boolean value, either true or false. For example,

```
const a = 3, b = 2;

console.log(a > b); // true
```

When using the comparison operator >, we confidently compare whether a is greater than b.

Below is a list of commonly used comparison operators:

```

Operator
==
Description
Equal to
Example
5 == "5" returns true

Operator
===
Description
Equal value and type
Example
5 === "5" returns false

Operator
!=
Description
Not equal to
Example
5 != 6 returns true

Operator
!==
Description
Not equal value or not equal type
Example
5 !== "5" returns true

Operator
>
Description
Greater than
Example
6 > 5 returns true

Operator
>=
Description
Greater than or equal to
Example
5 >= 5 returns true

Operator
<
Description
Less than
Example
5 < 6 returns true

Operator
<=
Description
Less than or equal to
Example
7 <= 5 returns false
```

Example: Comparison operators in JavaScript

```
// equal operator
console.log(2 == 2); // true
console.log(2 == '2'); // true

// not equal operator
console.log(3 != 2); // true
console.log('hello' != 'Hello'); // true

// strict equal operator
console.log(2 === 2); // true
console.log(2 === '2'); // false

// strict not equal operator
console.log(2 !== '2'); // true
console.log(2 !== 2); // false
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------


Logical Operators

Logical operators are used for performing logical operations and return either true or false. Logical operators are used in decision-making and loops.

Example: Logical operators in JavaScript

```
const x = 5, y = 3;
(x < 6) && (y < 5); // true
```

The logical operator && is utilized in this code. With both x < 6 and y < 5 being true, the result of the operation is confidently true.

Below is a list of commonly used Logical operators:

```
Operators
&&
Description
Logical AND: true if both the operands are true , else returns false
Examples
x && y

Operators
||
Description
Logical OR: true if either of the operands is true ; returns false if both are false
Examples
x || y

Operators
!
Description
Logical NOT: true if the operand is false and vice-versa.
Examples
!x

Example: Logical Operators in JavaScript
// logical AND
console.log(true && true); // true
console.log(true && false); // false

// logical OR
console.log(true || false); // true

// logical NOT
console.log(!true); // false
```
---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Bitwise Operators

Bitwise operators are employed to carry out operations on binary representations of numbers. Everyday programming rarely involves the use of bitwise operators.

Below is a list of commonly used Bitwise operators:

```
Operators
&
Description
AND
Examples
5 & 6 returns 4

Operators
|
Description
OR
Examples
5 | 6 returns 7

Operators
^
Description
XOR
Examples
5 ^ 6 returns 3

Operators
~
Description
NOT
Examples
~5 returns -6

Operators
<<
Description
Left shift
Example
5 << 2 returns 20

Operators
>>
Description
Right shift
Example
5 >> 1 returns 2

Operators
>>>
Description
Zero-fill right shift
Example
5 >>> 1 returns 2

Example: Bitwise Operators in JavaScript

const a = 5; // 0101 in binary
const b = 3; // 0011 in binary

// Bitwise AND
console.log(a & b); // 1 (0001 in binary)

// Bitwise OR
console.log(a | b); // 7 (0111 in binary)

// Bitwise XOR
console.log(a ^ b); // 6 (0110 in binary)

// Bitwise NOT
console.log(~a); // -6 (1010 in binary)

// Left shift
console.log(a << 1); // 10 (1010 in binary)

// Right shift
console.log(a >> 1); // 2 (0010 in binary)
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

String Operators

In JavaScript, + operator is used to concatenate (join) two or more strings.

Example: String Operators in JavaScript

```
let str1 = "Hello";
let str2 = "world!";
let result = str1 + " " + str2; // concatenation using the + operator
console.log(result);            // Output: "Hello world!"
```

It's important to note that the + operator performs concatenation when used with strings but performs addition when used with numbers.

Other JavaScript Operators

Below is a list of additional operators that are available in JavaScript.
 
```
Operators
(condition) ? (if_true) : (else_false);
Description
Ternary operator
Example
x > 0 ? "positive" : "non-positive"

Operators
delete
Description
Delete a property from an object
Example
delete obj.prop

Operators
typeof
Description
Returns the type of a value
Example
typeof x

Operators
void
Description
Evaluates an expression and returns undefined
Example
void(0)

Operators
in
Description
Checks if a property exists in an object
Example
"prop" in obj

Operators
instanceof
```
Description
Checks if an object is an instance of a particular class or constructor function
Example
x instanceof MyClass


---------------------------------------------------------------------------------------------------------------------------------------------------------------------


Example: Ternary Operator

```
let age = 18;
let canVote = age >= 18 ? "Yes" : "No";
console.log(canVote); // Output: Yes
```

In this example, we check if the age variable is greater than or equal to 18. If the statement's condition is true, the ternary operator returns "Yes"; otherwise, it returns "No". The result is then stored in the canVote variable.

The same logic can be written using an if-else statement:

```
let age = 18;
let canVote;

if (age >= 18) {
  canVote = "Yes";
} else {
  canVote = "No";
}

console.log(canVote); // Output: Yes
```
Example: typeof Operator

```
const num = 42;
const str = "Hello, World!";
const bool = true;
const obj = { key: "value" };
const arr = [1, 2, 3];
const func = function () {};
const und = undefined;
const nul = null;

console.log(typeof num);  // Output: "number"
console.log(typeof str);  // Output: "string"
console.log(typeof bool); // Output: "boolean"
console.log(typeof obj);  // Output: "object"
console.log(typeof arr);  // Output: "object" (arrays are objects in JavaScript)
console.log(typeof func); // Output: "function"
console.log(typeof und);  // Output: "undefined"
console.log(typeof nul);  // Output: "object" (this is considered a historical bug in JavaScript)
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Activity: Code Practice

Open any JavaScript IDE or VS Code IDE.

Enter the following code:
```
let a=10;

console.log(a++ + ++a)
console.log(a++ - ++a)

console.log("0" == 0)
console.log("0" === 0)

console.log((5 > 2) && (7 < 11))
console.log((7 > 9) || (9 < 5))


if(a > 6) {
	console.log("Pass")
} else {
	console.log("Fail")
}

console.log(a > 6 ? "Pass" : "Fail")
Press Enter or Return to see the output of each operation in the console.
Answers
22
-2

true
false

true
false

"Pass"

"Pass"
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Summary

What did we learn?

JavaScript operators are symbols that perform actions on values and return a result. 

They are a fundamental aspect of the language and allow developers to perform operations such as arithmetic, comparison, and assignment.

Arithmetic operators perform basic mathematical operations such as addition (+), subtraction (-), multiplication (*), and division (/).

Comparison operators are used for comparing two values and return a Boolean result (true or false). Examples include equality (==), inequality (!=), greater than (>), and less than (<).

Assignment operators serve the purpose of assigning a value to a variable. The most common assignment operator is the equal sign (=).

Logical operators: These operators perform logical operations such as AND (&&), OR (||), and NOT (!).

Ternary operator: This operator is a shorthand for an if-else statement and returns one of two values based on a condition.

JavaScript provides a range of methods for working with strings. 

Some common methods include .length(to find the length of a string), .substring()(to extract a portion of a string), .indexOf()(to find the position of a substring), .toLowerCase()(to convert a string to lowercase), and .toUpperCase()(to convert a string to uppercase).

In JavaScript, there is a variety of built-in functions available to manipulate strings, including parseInt() for converting strings to integers, split() for dividing a string into an array of substrings, and replace() for substituting a substring within a string.