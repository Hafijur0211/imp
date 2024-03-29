1.The Odd or Even Sum

In the mystical land of numbers, there lived a talented JavaScript wizard named Alaric. He possessed a unique power to distinguish between odd and even numbers effortlessly. One day, the people of the land came to him with a puzzling request. They wanted a function that could compute the sum of odd and even numbers separately from a given array of integers.
Determined to help, Alaric began crafting a function called oddOrEvenSum. The function would take an array of integers as input and return an object containing the sum of all odd numbers and the sum of all even numbers found in the array.
With a heart full of curiosity and magic at his fingertips, Alaric delved into the task, creating a solution that showcased his mastery over decision statements. Little did he know that this function would prove invaluable to the people of the mystical land, helping them unravel the secrets hidden within their numbers.
Can you assist Alaric in completing his enchanting oddOrEvenSum function to bring balance to the numbers of the land?
Can you rise to the challenge of the String Splitter and impress your teacher with your coding skills? The challenge awaits, and it's up to you to take it on.

```
Example 1:

Input: [1, 2, 3, 4, 5]

Output: { oddSum: 9, evenSum: 6 }

Example 2:

Input: [10, 20, 30, 40, 50]

Output: { oddSum: 0, evenSum: 150 }

Example 3:

Input: [7, 13, 42, 31, 55]

Output: { oddSum: 106, evenSum: 42 }
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

```
function oddOrEvenSum(arr) {
  // Initialize sums for odd and even numbers
  let oddSum = 0;
  let evenSum = 0;

  // Loop through the array
  for (let num of arr) {
    // Check if the number is odd or even
    if (num % 2 === 0) {
      // If even, add to evenSum
      evenSum += num;
    } else {
      // If odd, add to oddSum
      oddSum += num;
    }
  }

  // Return an object with the sums
  return {
    oddSum: oddSum,
    evenSum: evenSum
  };
}

// Test cases
console.log(oddOrEvenSum([1, 2, 3, 4, 5]));    // Output: { oddSum: 9, evenSum: 6 }
console.log(oddOrEvenSum([10, 20, 30, 40, 50])); // Output: { oddSum: 0, evenSum: 150 }
console.log(oddOrEvenSum([7, 13, 42, 31, 55]));  // Output: { oddSum: 106, evenSum: 42 }
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------


2. The Grade Distributor

In a kingdom where knowledge was highly cherished, the wise scholars developed a system to grade students based on their academic performance. They assigned letter grades "A", "B", "C", "D", and "F" to represent different levels of achievement.
The kingdom needed a function that would analyze a set of numerical scores and distribute the corresponding letter grades to each student. They sought a skilled JavaScript sorcerer to create the distributeGrades function.
The distributeGrades function would take an array of numerical scores as input and return an object containing the count of grades distributed as "A", "B", "C", "D", and "F", respectively, based on the following scale:
Scores from 90 to 100 would receive an "A". Scores from 80 to 89 would receive a "B". Scores from 70 to 79 would receive a "C". Scores from 60 to 69 would receive a "D". Scores below 60 would receive an "F". Eager to leave a mark on the kingdom's education system, the JavaScript sorcerer accepted the challenge. Utilizing decision statements, the sorcerer worked tirelessly to craft a solution that would efficiently distribute the grades and empower the kingdom's educators with valuable insights.
Could you lend your coding expertise to assist the JavaScript sorcerer in completing the distributeGrades function and bestow the gift of knowledge upon the kingdom's students?

```
Example 1

Input:

[85, 92, 78, 65, 95]

Output:
{ A: 2, B: 1, C: 1, D: 1, F: 0 }

Example 2

Input:
[76, 81, 60, 55, 88}

Output:
{ A: 0, B: 2, C: 1, D: 1, F: 1 }

Example 3

Input:
[92, 95, 87, 60, 72]

Output:
{ A: 2, B: 1, C: 1, D: 1, F: 0 }
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

```
function distributeGrades(scores) {
  // Initialize grade counters
  let gradeCount = { A: 0, B: 0, C: 0, D: 0, F: 0 };

  // Loop through the scores
  for (let score of scores) {
    // Determine the grade based on the score
    if (score >= 90 && score <= 100) {
      gradeCount.A++;
    } else if (score >= 80 && score < 90) {
      gradeCount.B++;
    } else if (score >= 70 && score < 80) {
      gradeCount.C++;
    } else if (score >= 60 && score < 70) {
      gradeCount.D++;
    } else {
      gradeCount.F++;
    }
  }

  // Return the grade count object
  return gradeCount;
}

// Test cases
console.log(distributeGrades([85, 92, 78, 65, 95]));  // Output: { A: 2, B: 1, C: 1, D: 1, F: 0 }
console.log(distributeGrades([76, 81, 60, 55, 88]));   // Output: { A: 0, B: 2, C: 1, D: 1, F: 1 }
console.log(distributeGrades([92, 95, 87, 60, 72]));   // Output: { A: 2, B: 1, C: 1, D: 1, F: 0 }

```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

3. Simple Calculator

Alice is a math teacher who wants to create a simple calculator using JavaScript. The calculator should be able to perform basic arithmetic operations like addition, subtraction, multiplication, and division.
Help Alice by creating a JavaScript function called simpleCalculator that takes two numbers and an operator (+, -, *, /) as input and returns the arithmetic operation result.

```
// Test cases
console.log(simpleCalculator(5, 2, '+')); // 7
console.log(simpleCalculator(5, 2, '-')); // 3
console.log(simpleCalculator(5, 2, '*')); // 10
console.log(simpleCalculator(5, 2, '/')); // 2.5
console.log(simpleCalculator(5, 0, '/')); // "Cannot divide by zero."
console.log(simpleCalculator('5', 2, '+')); // "Invalid input. Please enter numeric values."
console.log(simpleCalculator(5, 2, '&')); // "Unsupported operator. Please enter a valid operator (+, -, *, /)."
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

```
function simpleCalculator(num1, num2, operator) {
  // Check if input values are numeric
  if (typeof num1 !== 'number' || typeof num2 !== 'number' || isNaN(num1) || isNaN(num2)) {
    return "Invalid input. Please enter numeric values.";
  }

  // Perform arithmetic operation based on the operator
  switch (operator) {
    case '+':
      return num1 + num2;
    case '-':
      return num1 - num2;
    case '*':
      return num1 * num2;
    case '/':
      // Check for division by zero
      if (num2 === 0) {
        return "Cannot divide by zero.";
      }
      return num1 / num2;
    default:
      return "Unsupported operator. Please enter a valid operator (+, -, *, /).";
  }
}

// Test cases
console.log(simpleCalculator(5, 2, '+')); // Output: 7
console.log(simpleCalculator(5, 2, '-')); // Output: 3
console.log(simpleCalculator(5, 2, '*')); // Output: 10
console.log(simpleCalculator(5, 2, '/')); // Output: 2.5
console.log(simpleCalculator(5, 0, '/')); // Output: "Cannot divide by zero."
console.log(simpleCalculator('5', 2, '+')); // Output: "Invalid input. Please enter numeric values."
console.log(simpleCalculator(5, 2, '&')); // Output: "Unsupported operator. Please enter a valid operator (+, -, *, /)."

```
