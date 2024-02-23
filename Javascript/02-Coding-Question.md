Problem 1: The Data Detective
In the charming village of JavaScriptville, a young detective named Max was known for solving mysterious data cases. One day, the villagers approached Max with an intriguing challenge. They had a magical box that could contain anything - numbers, strings, arrays, or even objects. However, the villagers were unsure about the contents inside the box.
Max's task was to determine the type of the input inside the magical box and report back with the result.
Example 1:

Input:
"4"
Output:
string

Example 2:
Input:
Hello, JavaScriptville!
Output:
string

// Solution

```
function dataTypeDetect(magicalBox) {
    return typeof magicalBox;
}

// Example 1
var result1 = dataTypeDetect("4");
console.log(result1); // Output: string

// Example 2
var result2 = dataTypeDetect("Hello, JavaScriptville!");
console.log(result2); // Output: string
```

--------------------------------------------------------------------------------------------------------------------------------------------------------------

Problem 2: Sum two numbers

In the serene countryside of Mathland, there were two young friends, Lily and Ethan, who loved exploring the beauty of numbers. One sunny afternoon, they stumbled upon an ancient mathematical scroll with a mysterious challenge.
The scroll contained a mystical function named calculateSum, which took two numbers as input and returned their harmonious sum. With excitement in their eyes, Lily and Ethan set out to solve the riddle and uncover the magic hidden within the function.
Can you help Lily and Ethan complete the calculateSum function to unveil the harmonious sum of the two numbers?

Example 1:
Input:
2, 3
Output:
5

// Solution

```
function calculateSum(num1, num2) {
  // Add the two numbers to get their harmonious sum
  const sum = num1 + num2;
  
  // Return the result
  return sum;
}

// Example usage:
const result = calculateSum(2, 3);
console.log(result); // Output: 5
```

--------------------------------------------------------------------------------------------------------------------------------------------------------------

Problem 3: The Truth Detector

In the technologically advanced city of Codeville, there was a clever programmer named Ava who created a truth-detecting algorithm. To test its powers, she embarked on a mission to determine the truthfulness of a statement.
The statement was represented by a variable named isTrue, which contained a boolean value. Ava's task was to log the data type of this variable to the console, unlocking the key to the statement's truth.
Can you assist Ava in this important mission by writing a code snippet to reveal the data type of isTrue and uncover the mystery?
Example 1:
Input:
true

Output:
boolean
Example 2:
Input:
false

Output:
boolean

// Solution

```
function detectTruthType(isTrue) {
  // Logging the data type to the console
  console.log(typeof isTrue);
}

// Example usage:
detectTruthType(true);  // Output: boolean
detectTruthType(false); // Output: boolean
```

--------------------------------------------------------------------------------------------------------------------------------------------------------------
