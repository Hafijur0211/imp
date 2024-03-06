1. The JSON Parser

In a world of data exchange, the people need a JavaScript function that can parse JSON strings and convert them into JavaScript objects. They seek the power to transform their data structures seamlessly, enabling communication and understanding between systems.

Write a JavaScript function called parseJSON that takes a JSON string as input and returns the corresponding JavaScript object. Assume that the input JSON string will always be valid.

```
Example 1:
Input:
{"name": "John", "age": 30, "isStudent": true}

Output:
{ name: 'John', age: 30, isStudent: true }

Example 2:
Input:
{"colors": ["red", "green", "blue"], "length": 3}

Output:
{ colors: ['red', 'green', 'blue'], length: 3 }

Example 3:
Input:
{"colors": ["red", "green", "blue"], "length": 3}

Output:
{ colors: ['red', 'green', 'blue'], length: 3 }
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Solution

```
function parseJSON(jsonString) {
  return JSON.parse(jsonString);
}

// Example 1
const example1Input = '{"name": "John", "age": 30, "isStudent": true}';
const example1Output = parseJSON(example1Input);
console.log(example1Output);

// Example 2
const example2Input = '{"colors": ["red", "green", "blue"], "length": 3}';
const example2Output = parseJSON(example2Input);
console.log(example2Output);

// Example 3
const example3Input = '{"colors": ["red", "green", "blue"], "length": 3}';
const example3Output = parseJSON(example3Input);
console.log(example3Output);
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

2. The Object Merger

In a world of data amalgamation, the people need a JavaScript function that can merge two objects into a single, unified object. They seek to combine the strengths of multiple objects to create a comprehensive data structure.

Write a JavaScript function called mergeObjects that takes two objects as inputs and returns a new object that combines the properties of both objects. If there are overlapping properties, the value from the second object should take precedence. 

```
Example 1:
Input:
{ "name": "John", "age": 30 }

{ "isStudent": true, "age": 25 }

Output:
{ name: "John", age: 25, isStudent: true }
Example 2:
Input:
{ "a": 1, "b": 2 } { "c": 3 }

Output:
{ a: 1, b: 2, c: 3 }
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

```
function mergeObjects(obj1, obj2) {
  // Use the spread operator to create a new object with properties from both objects
  return { ...obj1, ...obj2 };
}

// Example 1
const example1Obj1 = { "name": "John", "age": 30 };
const example1Obj2 = { "isStudent": true, "age": 25 };
const example1Output = mergeObjects(example1Obj1, example1Obj2);
console.log(example1Output);

// Example 2
const example2Obj1 = { "a": 1, "b": 2 };
const example2Obj2 = { "c": 3 };
const example2Output = mergeObjects(example2Obj1, example2Obj2);
console.log(example2Output);
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

3. The Nested Object Finder

In a world of complex data structures, the people need a JavaScript function that can find the value of a given property within a nested object. They seek to explore the depths of their data and retrieve valuable information.
Write a JavaScript function called findNestedValue that takes an object and a string representing the property path as inputs. The property path will be a dot-separated string, representing the hierarchy of nested properties.
The function should return the value of the property if found within the nested object. If the property is not found or any intermediate property is not an object, the function should return null.

```
Example 1:
Input:
{"person":{"name": "John","age": 30,"address": {"city": "New York","country":"USA"}}}

person.name

Output:
John
Example 2:
Input:
{"person":{"name": "John","age": 30,"address": {"city": "New York","country":"USA"}}}

person.address.city

Output:
New York
Example 3:
Input:
{"person":{"name": "John","age": 30,"address": {"city": "New York","country":"USA"}}}

person.address.postalCode

Output:
null
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

```
function findNestedValue(obj, path) {
  // Split the property path into an array
  const properties = path.split('.');

  // Iterate through the properties to navigate the nested object
  let currentObj = obj;
  for (const property of properties) {
    // Check if the current property exists in the current object
    if (currentObj && typeof currentObj === 'object' && property in currentObj) {
      currentObj = currentObj[property];
    } else {
      // Return null if the property is not found or any intermediate property is not an object
      return null;
    }
  }

  // Return the final value if found
  return currentObj;
}

// Example 1
const example1Input = {"person":{"name": "John","age": 30,"address": {"city": "New York","country":"USA"}}};
const example1Output = findNestedValue(example1Input, 'person.name');
console.log(example1Output);

// Example 2
const example2Input = {"person":{"name": "John","age": 30,"address": {"city": "New York","country":"USA"}}};
const example2Output = findNestedValue(example2Input, 'person.address.city');
console.log(example2Output);

// Example 3
const example3Input = {"person":{"name": "John","age": 30,"address": {"city": "New York","country":"USA"}}};
const example3Output = findNestedValue(example3Input, 'person.address.postalCode');
console.log(example3Output);
```
