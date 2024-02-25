Palindrome Strings

Sarah is a web developer who wants to create a JavaScript function to check if a given string is a palindrome. She wants to use this function to build a feature that validates whether user input is a palindrome.
Help Sarah by writing a JavaScript function named isPalindrome that takes a string as input and returns true if the string is a palindrome and false otherwise.

```
Example 1:
Input: "racecar"
Output: true

Example 2:
Input: "hello"
Output: false
```

```
function isPalindrome(str) {
    const reversedStr = str.split('').reverse().join('');
    return str === reversedStr;
}

// Example usage:
console.log(isPalindrome("racecar")); // Output: true
console.log(isPalindrome("hello"));   // Output: false
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------


The Sign of Product

In a faraway land of mathematical wonders, a group of curious mathematicians found themselves pondering over the signs of products. They decided to embark on a coding journey to build a function that would determine the sign of the product of three given numbers.
The mathematicians laid down the rules for the function called productSign:
If the product is positive (greater than 0), the function should return 1. If the product is negative (less than 0), the function should return -1. If the product is zero, the function should return 0. The mathematicians were eager to see their function come to life and started coding in JavaScript. However, they faced some challenges in handling different scenarios.
Can you use your coding prowess to assist the mathematicians in creating the function productSign and unraveling the mysteries of the signs of products?

```
Example 1:
Input:
2, 3, 5

Output:
1
Example 2:
Input:
-4, 6, 0

Output:
0
Example 3:
Input:
-1, -2, -3

Output:
-1
```

```
function productSign(num1, num2, num3) {
    // Calculate the product of the three numbers
    let product = num1 * num2 * num3;

    // Determine the sign of the product and return the corresponding result
    if (product > 0) {
        return 1; // Positive
    } else if (product < 0) {
        return -1; // Negative
    } else {
        return 0; // Zero
    }
}

// Examples
console.log(productSign(2, 3, 5));     // Output: 1
console.log(productSign(-4, 6, 0));    // Output: 0
console.log(productSign(-1, -2, -3));  // Output: -1
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------


The Sign Checker

In a land where mathematical wizards roamed, the people needed a function that could determine the signs of three given numbers and return the result as a string. They sought a JavaScript function to aid them in their quest.
Write a JavaScript function called checkSign that takes three numbers as input and returns a string representing the signs of the numbers.
If all three numbers are positive, return "+++" If two numbers are positive and one is negative, return "++-" If one number is positive and two are negative, return "+--" If all three numbers are negative, return "---"

```
Example 1:
Input:
1, 2, 3

Output:
"+++"
Example 2:
Input:
-1, 2, 3

Output:
"++-"
Example 3:
Input:
-1, -2, 3

Output:
"+--"
Example 4:
Input:
-1, -2, -3

Output:
"---"
```

```
function checkSign(num1, num2, num3) {
    if (num1 > 0 && num2 > 0 && num3 > 0) {
        return "+++";
    } else if (num1 > 0 || num2 > 0 || num3 > 0) {
        return "++-";
    } else if (num1 < 0 && num2 < 0 && num3 < 0) {
        return "---";
    } else {
        return "+--";
    }
}

// Example usage:
console.log(checkSign(1, 2, 3));     // Output: "+++"
console.log(checkSign(-1, 2, 3));    // Output: "++-"
console.log(checkSign(-1, -2, 3));   // Output: "+--"
console.log(checkSign(-1, -2, -3));  // Output: "---"
```