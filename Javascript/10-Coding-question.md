The Word Reverser

In a realm of linguistic marvels, a task has been bestowed upon you to create a JavaScript function that can reverse the order of words in a given string. The people of the realm are eager to explore the magic of word reversal to unlock hidden meanings within their sentences.
Write a JavaScript function called reverseWords that takes a sentence (a string containing multiple words separated by spaces) as input and returns the sentence with the order of words reversed.

```
Example 1:
Input:
"Hello, world!"

Output:
"world! Hello,"
Example 2:
Input:
"The quick brown fox"

Output:
"fox brown quick The"
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Solution:

```
function reverseWords(sentence) {
  // Split the sentence into an array of words
  const wordsArray = sentence.split(' ');

  // Reverse the order of words in the array
  const reversedArray = wordsArray.reverse();

  // Join the reversed array back into a string
  const reversedSentence = reversedArray.join(' ');

  return reversedSentence;
}

// Example usage:
const example1 = "Hello, world!";
const example2 = "The quick brown fox";

console.log(reverseWords(example1)); // Output: "world! Hello,"
console.log(reverseWords(example2)); // Output: "fox brown quick The"
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Palindrome Detector

In the mystical land of characters and strings, a group of adventurers seeks to identify palindromes—words or phrases that read the same forwards and backwards. To aid them in their quest, they need a JavaScript function that can determine whether a given string is a palindrome.
Write a JavaScript function called isPalindrome that takes a string as input and returns true if it is a palindrome, and false otherwise.
A palindrome is case-sensitive and should be read from left to right and right to left in the same way.

```
Example 1:
Input:
"racecar"

Output:
true+
Example 2:
Input:
"hello"

Output:
false
Example 3:
Input:
"Madam In Eden, I'm Adam"
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Solution:

```
function isPalindrome(str) {
  // Remove non-alphanumeric characters and convert to lowercase
  const cleanStr = str.replace(/[^a-zA-Z0-9]/g, '').toLowerCase();

  // Compare the original string with its reverse
  return cleanStr === cleanStr.split('').reverse().join('');
}

// Test cases
console.log(isPalindrome("racecar")); // Output: true
console.log(isPalindrome("hello"));   // Output: false
console.log(isPalindrome("Madam In Eden, I'm Adam")); // Output: true
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

The Array Rotator

In the land of cyclical arrays, the people need a JavaScript function that can rotate an array by a given number of positions to the right. They seek to shift their array elements in a circular manner, enabling them to explore new possibilities with their data.
Write a JavaScript function called rotateArray that takes an array of integers and a positive integer k as inputs. The function should rotate the array k positions to the right.
Note: The value of k can be greater than the length of the array, so multiple rotations might be needed.

```
Example 1:
Input:
[1, 2, 3, 4, 5]

2

Output:
[4, 5, 1, 2, 3]
Example 2:
[7, 8, 9]

5

Output:
[ 8, 9, 7 ]
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Solution:

```
function rotateArray(arr, k) {
  // Ensure k is within the length of the array
  k = k % arr.length;

  // Perform rotation using array slicing
  const rotatedPart = arr.slice(-k);
  const remainingPart = arr.slice(0, arr.length - k);

  // Concatenate the rotated and remaining parts
  const rotatedArray = rotatedPart.concat(remainingPart);

  return rotatedArray;
}

// Example usage:
const example1 = rotateArray([1, 2, 3, 4, 5], 2);
console.log(example1); // Output: [4, 5, 1, 2, 3)

const example2 = rotateArray([7, 8, 9], 5);
console.log(example2); // Output: [8, 9, 7]

```

