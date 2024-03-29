JavaScript Objects and JSON

JavaScript Object

JavaScript's Object type is a data type that can be used to store collections of key-value pairs and more complex entities. Keys are also called properties of an object.

In JavaScript, most objects are derived from Object, meaning they inherit properties, including methods, from Object.prototype. However, it's possible for these properties to be shadowed, or overridden, by properties with the same name in a derived object.

Here's an example of an object in JavaScript:

In this example, person is an object with three properties: 

firstName, lastName, and age.

```
let person = {
  firstName: "John",
  lastName: "Doe",
  age: 30,
};
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Object Declaration

In JavaScript, you can declare an object in two ways:

1. Object literal method

```
let person = {
  firstName: "John",
  lastName: "Doe",
  age: 30,
};

console.log(person.firstName);
console.log(person.age);

// Output
"John"
30
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

2. Object constructor method

```
let person = new Object();

person.firstName = "John";
person.lastName = "Doe";
person.age = 30;

console.log(person.firstName);
console.log(person.age);

// Output
"John"
30
```

Both of these methods will create an object with the same properties and values. However, using the object literal syntax is generally preferred because it is more concise and easier to read.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Accessing Object Properties

Two main ways to access object properties are dot notation and bracket notation.

1. Using dot Notation: Dot notation is used to access properties of an object using the dot (.) operator, followed by the property name. Syntax for Dot Notation is objectName.key.

Example:

```
let person = {
  name: 'John',
  age: 30,
  occupation: 'Developer'
};

console.log(person.name);
console.log(person.age);
console.log(person.occupation);

// Output
"John"
30
"Developer"
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

2. Using bracket Notation: Bracket notation is used to access object properties using square brackets ([ ]), with the property name as a string inside the brackets. Syntax for Bracket Notation is objectName```["propertyName"]```.

Example:

```
let person = {
  name: 'John',
  age: 30,
  occupation: 'Developer'
};

console.log(person['name']);
console.log(person['age']);
console.log(person['occupation']);

// Output
"John"
30
"Developer"
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

JavaScript Nested Objects

Objects can contain other objects as properties, known as Nested Objects.

```
let person = {
  name: 'John',
  age: 30,
  address: {
    street: '123 Main St',
    city: 'Anytown',
    state: 'CA',
    zip: '12345'
  }
};
```

In this example, the person object has a property called address, which is itself an object with properties street, city, state, and zip.

We can access these properties using either dot notation or bracket notation:

```
console.log(person.address.street); 
console.log(person['address']['city']);

// Output
"123 Main St"
"Anytown"
```

We can also modify, add and remove (using delete keyword) properties of nested objects using dot notation or bracket notation:

// Modify existing properties in an object

```
person.address.city = 'Othertown';
person['address']['zip'] = '54321';

// Add new properties to an object
person.address.country = 'USA';
person['address']['phone'] = '555-1234';

// Remove properties from an object
delete person.age;
delete person['address']['phone'];
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

JavaScript Object Methods

JavaScript objects are collections of properties, and properties can be either values or functions. Functions that are attached to objects are called object methods.

Here are some commonly used object methods in JavaScript:

1. Object.keys(): This method returns an array of all the keys (property names) of an object.

```
const myObj = { name: "John", age: 30 };
const keys = Object.keys(myObj);

console.log(keys);

// Output
["name", "age"]
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------


2. Object.values(): This method returns an array of all the values of an object.

```
const myObj = { name: "John", age: 30 };
const values = Object.values(myObj);

console.log(values);

// Output
["John", 30]
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------


3. Object.entries(): This method returns an array of arrays, where each sub-array contains a key-value pair of the object.

```
const myObj = { name: "John", age: 30 };
const entries = Object.entries(myObj);

console.log(entries);

// Output
[["name", "John"], ["age", 30]]
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------


4. Object.assign(): This method is used to copy the values of all enumerable own properties from one or more source objects to a target object.

```
const targetObj = { name: "John" };
const sourceObj = { age: 30 };
Object.assign(targetObj, sourceObj);

console.log(targetObj);

// Output
{
  name: "John",
  age: 30
}
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------


5. Object.freeze(): This method is used to prevent an object from being modifying.

```
const myObj = { name: "John", age: 30 };
Object.freeze(myObj);
myObj.age = 40; // This will not modify the object

console.log(myObj)

// Output
{
  name: "John",
  age: 30
}
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------


6. Custom method: An object can contain a function as one of its properties. These functions are called methods when they are attached to an object.

```
const car = {
  make: "Toyota",
  model: "Corolla",
  year: 2022,
  startEngine: function() {
    console.log("Engine started!");
  }
};

car.startEngine();

// Output
"Engine started!"
```

In this example, we define an object car with properties for its make, model, and year. We also define a method startEngine that simply logs a message to the console when invoked.
To invoke the method, we use the object's name (car) followed by the method name (startEngine) and parentheses ().

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Accessing Object Methods

You can access an object's methods using dot notation or bracket notation.

```
objectName.methodKey();     // Dot Notation
objectName["methodKey"]();  // Bracket Notation
```

1. Accessing Object Property: You can access property by calling an objectName and a key.

2. Accessing Object Method: You can access a method by calling an objectName and a key for that method along with ().

Example:

```
const person = {
  name: "John",
  age: 30,
  greet: function() {
    console.log(`Hello, my name is ${this.name} and I am ${this.age} years old.`);
  }
};

// Accessing Object Property
console.log(person.name);

// Accessing Object Method
person.greet();

// Output
"John"
"Hello, my name is John and I am 30 years old."
```

Here, the greet method is accessed as person.greet() instead of person.greet.
If you try to access the method with only person.greet, it will give you a function definition.

```
console.log(person.greet); 

// Output
function() {
  console.log(`Hello, my name is ${this.name} and I am ${this.age} years old.`);
}
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Adding Object Methods

You can also add a method in an object.

For example:

```
// creating an object
let student = { };

// adding a property
student.name = 'John';

// adding a method
student.greet = function() {
    console.log('hello');
}

// accessing a method
student.greet(); // hello
```

In the above example, an empty student object is created. Then, the name property is added. Similarly, the greet method is also added. In this way, you can add a method as well as a property to an object.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

“this” keyword

To access a property of an object from within a method of the same object, you need to use the this keyword.

For example:

```
// Define an object called "person"
let person = {
  name: "Rocky",
  age: 30,
  sayHello: function() {
    console.log("Hello, my name is " + this.name + "."); // Accessing the "name" property using "this"
  }
};

person.sayHello(); // Calling the "sayHello" method on the "person" object

// Output
"The name is Rocky"
```

Explanation:

We have an object called person that has properties name and age, and a method called sayHello.
Inside the sayHello method, we use the this keyword to access the name property of the current object.
When we call the sayHello method on the person object using person.sayHello(), it will log the message Hello, my name is Rocky. to the console, referencing the value of the name property specified in the person object.
In order to access the properties of an object, this keyword is used following by . and key. However, the function inside of an object can access its variable in a similar way as a normal function would.

For example:

```
const person = {
  name: 'John',
  age: 30,
  greet: function() {
    let surname = 'Doe';
    console.log('The name is' + ' ' + this.name + ' ' + surname);
  }
};

person.greet();

// Output
"The name is John Doe"
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

JavaScript Sets

In JavaScript, a Set is a built-in object that allows you to store unique values of any type. This means that a Set can contain only distinct values, and any duplicate values are automatically ignored.

Sets are often used when you need to work with collections of unique elements and perform set operations like union, intersection, and difference.

In JavaScript, you can create a Set using three different approaches:

1. Using the new keyword with the Set() constructor:

```
const mySet = new Set();
```

2. Initializing a Set with an array containing initial values using the new keyword and the Set() constructor:

```
const fruitsArray = ['apple', 'banana', 'orange'];
const fruitsSet = new Set(fruitsArray);
```

3. Using the Set Literal (Available from ECMAScript 6):

```
const mySet = new Set(['a', 'b', 'c']);
```

All three methods create a new Set, but they offer different ways to initialize the Set with initial values. The first method creates an empty Set, and you can later add elements using the .add() method. The second and third methods allow you to create a Set with initial values provided in an array, which is convenient when you have a collection of unique elements.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Set Operations

Here's an overview of how to work with JavaScript Sets:

1. Adding and Removing Elements:

```
const mySet = new Set();

mySet.add('apple');
mySet.add('banana');
mySet.add('orange');
mySet.add('apple');     // Ignored, as 'apple' is already in the Set
console.log(mySet);

mySet.delete('banana'); // Removes 'banana' from the Set
console.log(mySet);

mySet.clear();          // Removes all elements from a Set
console.log(mySet);

// Output
Set(3) { 'apple', 'banana', 'orange' }
Set(2) { 'apple', 'orange' }
Set(0) {}
```

2. Checking if an Element is in the Set:

```
const mySet = new Set(['apple', 'banana', 'orange']);

console.log(mySet.has('banana'));
console.log(mySet.has('grape'));

// Output
true
false
```

3. Getting the Size of the Set:

```
const mySet = new Set(['apple', 'banana', 'orange']);

console.log(mySet.size);

// Output
3
```

4. Iterating through a Set:

```
const mySet = new Set(['apple', 'banana', 'orange']);

// Using forEach
mySet.forEach((value) => {
  console.log(value);
});

// Using for...of loop
for (const fruit of mySet) {
  console.log(fruit);
}

// Output
apple
banana
orange

apple
banana
orange
```

5. Converting Set to Array:

```
const mySet = new Set(['apple', 'banana', 'orange']);

const fruitsArray = Array.from(mySet);
console.log(fruitsArray);

Output
[ 'apple', 'banana', 'orange' ]
```

Remember that Sets store elements based on their value's uniqueness, not the reference. So, objects with the same contents but different references will be considered unique in a Set.

For example:

```
const obj1 = { name: "John", age: 30 };
const obj2 = { name: "John", age: 30 };

const mySet = new Set();

mySet.add(obj1);
mySet.add(obj2);

console.log(mySet.size);

// Output
2    // Even though obj1 and obj2 have the same contents, they are considered unique in the Set
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------


JavaScript Maps

In JavaScript, a Map is a built-in object that allows you to store key-value pairs, where each key can be of any data type, and each value can also be of any data type. Maps are useful for associating data and performing lookups based on specific keys.

Map Operations

Here's an overview of how to work with JavaScript Sets:

1. Creating a Map: You can create a Map in JavaScript using the new keyword with the Map() constructor.

```
const myMap = new Map();
```

2. Adding and Removing Entries: To add key-value pairs to a Map, you can use the .set() method, and to remove entries, you can use the .delete() method.

```
const myMap = new Map();

myMap.set('name', 'John');
myMap.set('age', 30);
console.log(myMap);

myMap.delete('age');
console.log(myMap);

myMap.clear();
console.log(myMap);

// Output
Map(2) { 'name' => 'John', 'age' => 30 }
Map(1) { 'name' => 'John' }
Map(0) {}
```

3. Getting the Size of the Map: You can use the .size property to get the number of entries in the Map.

```
const myMap = new Map([
  ['name', 'John'],
  ['age', 30]
]);

console.log(myMap.size);

// Output
2
```

4. Checking if a Key Exists: To check if a specific key exists in the Map, you can use the .has() method.

```
const myMap = new Map([
  ['name', 'John'],
  ['age', 30]
]);

console.log(myMap.has('name'));
console.log(myMap.has('gender'));

// Output
true
false
```

Getting the Value for a Key: To retrieve the value associated with a specific key, you can use the .get() method.

```
const myMap = new Map([
  ['name', 'John'],
  ['age', 30]
]);

console.log(myMap.get('name'));
console.log(myMap.get('age'));

// Output
"John"
30
```

6. Iterating through a Map: You can use various methods to iterate through the entries of a Map, such as forEach() and for...of loop.

```
const myMap = new Map([
  ['name', 'John'],
  ['age', 30]
]);

// Using forEach
myMap.forEach((value, key) => {
  console.log(`${key}: ${value}`);
});

// Using for...of loop
for (const [key, value] of myMap) {
  console.log(`${key}: ${value}`);
}

// Output
name: John
age: 30

name: John
age: 30
```

7. Converting Map to Array: To convert a Map into an array of key-value pairs, you can use the Array.from() method.

```
const myMap = new Map([
  ['name', 'John'],
  ['age', 30]
]);

const entriesArray = Array.from(myMap);
console.log(entriesArray);

// Output
[ [ 'name', 'John' ], [ 'age', 30 ] ]
```

Remember that unlike objects, Maps maintain the insertion order of elements, making them suitable for scenarios where order matters. Additionally, Maps allow you to use any data type as keys, making them more versatile than objects for certain use cases.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

JavaScript Object Notation (JSON)

JavaScript Object Notation (JSON) is a lightweight data interchange format that is easy for both humans and machines to read and write. It is primarily used to transmit data between a server and a web application as an alternative to XML.

It is language-independent and widely supported in various programming languages, making it an ideal choice for data exchange over the web.

JSON data is represented as key-value pairs similar to JavaScript objects, and it follows a specific syntax:

Data is enclosed in curly braces {}.

Each data item is represented as a key-value pair separated by a colon :.

Keys (also known as properties) must be strings enclosed in double quotes ".

Values can be strings, numbers, booleans, null, arrays, or other JSON objects.

Data items are separated by commas ,.

Here's a simple example of JSON data representing information about a person:

```
{
  "name": "John Doe",
  "age": 30,
  "email": "john@example.com",
  "isMarried": false,
  "hobbies": ["reading", "painting", "traveling"],
  "address": {
    "street": "123 Main St",
    "city": "Anytown",
    "country": "USA"
  }
}
```

JavaScript provides built-in methods to work with JSON: JSON is a native part of the language, so parsing and serialization are straightforward tasks using JSON.parse() and JSON.stringify() methods, respectively.

1. JSON.stringify(): This method is used to convert a JavaScript object or value to a JSON-formatted string.

2. JSON.parse(): This method is used to parse a JSON-formatted string and convert it back into a JavaScript object or value.

For example:

To convert a JavaScript object to a JSON string

```
const person = {
  name: "John Doe",
  age: 30,
  email: "john@example.com",
};

const jsonStr = JSON.stringify(person);
console.log(jsonStr);

// Output
'{"name":"John Doe","age":30,"email":"john@example.com"}'
```

And to parse a JSON string back into a JavaScript object

```
const jsonString = '{"name":"John Doe","age":30,"email":"john@example.com"}';


const parsedObject = JSON.parse(jsonString);
console.log(parsedObject.name);
console.log(parsedObject.age);
console.log(parsedObject.email); 

// Output
"John Doe"
30
"john@example.com"
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Summary

What did we learn?

JavaScript objects are fundamental data type in the language and allow you to represent complex data structures, including arrays, functions, and even other objects. 

Objects can be created using the object literal syntax {key1: value1, key2: value2, ...} or using the Object constructor. 

They provide a flexible and versatile way to organize and store data in JavaScript and are widely used for tasks such as storing collections of data, organizing code into modules, and more.

You can access properties of an object using either dot notation object.property or bracket notation object["property"].

Object methods are functions that are associated with an object and can be invoked using the dot notation or bracket notation.

They can access the object properties and other methods within the same object using the this keyword.

Sets in JavaScript are a collection of unique values. They are similar to arrays, but each value in a set must be unique.

Maps in JavaScript are collections of key-value pairs. Unlike sets, maps allow you to store values with a specific key and retrieve values by that key.

The JavaScript Object Notation (JSON) is a lightweight format utilized for the exchange of data that can be effortlessly comprehended and produced by both human beings and machines.

JSON objects could be converted to JavaScript objects using the JSON.parse() method, and JavaScript objects can be converted to JSON using the JSON.stringify() method.