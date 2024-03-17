DOM Basics

Introduction to DOM Basics

The Document Object Model (DOM) is a programming interface for HTML and XML documents. It represents the structure, content, and style of a web page as a tree-like structure of objects. The DOM provides a way for programs or scripts to access and manipulate the elements, attributes, and text within a document.
When a web page is loaded into a web browser, the browser creates a DOM tree based on the HTML or XML code of the page. The DOM tree consists of various types of nodes, including element nodes, attribute nodes, and text nodes.

Here's a simple example of an HTML document structure with its DOM tree:

```
<!DOCTYPE html>
<html>
<head>
  <title>My Title</title>
</head>
<body>
	<a href="https://www.example.com">My Link</a>
  <h1>My header</h1>
</body>
</html>
```

Element nodes represent HTML or XML elements, such as `<div>`, `<p>`, or `<h1>`. Each element node can have child nodes, which can be other elements, attributes, or text nodes.
Attribute nodes represent attributes of an element, such as id, class, or src. They provide additional information about the elements.

Text nodes contain the actual text content within an element. For example, the text between `<p>` and `</p>` tags would be represented as a text node.

The DOM tree allows developers to access and manipulate these nodes using programming languages like JavaScript. By accessing the DOM, developers can dynamically modify the content, style, and structure of a web page.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Targeting Nodes with Selectors

In DOM programming, selectors are used to target and select specific nodes within the DOM tree. Selectors allow you to identify elements based on their attributes, tag names, or relationships with other elements. There are various methods and syntaxes available to target nodes using selectors in the DOM. Here are some commonly used ones:

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

1. getElementById()

Syntax: `document.getElementById(id)`

The method takes a single parameter, id, which is a string representing the unique identifier assigned to an HTML element.

The method searches the entire DOM tree starting from the document object, looking for an element with a matching id.

If a matching element is found, the method returns the element object, allowing you to access and manipulate its properties, attributes, and contents using JavaScript.

If no element with the specified id is found, the method returns null.

It's important to note that the id attribute of an element should be unique within the HTML document. If multiple elements have the same id, the method will only return the first element it encounters during the search.

Example usage:
```
<!-- HTML -->
<div id="myElement">Hello, World!</div>

// JavaScript
var element = document.getElementById('myElement');
element.innerHTML = 'Updated content';
```

In the example above, getElementById('myElement') is used to retrieve a reference to the `<div>` element with the id attribute of "myElement". The returned element object is stored in the element variable. Subsequently, the innerHTML property of the element is modified, updating the content of the `<div>` to "Updated content".

Overall, getElementById() is a fundamental method that provides a convenient way to access and manipulate specific elements in the DOM based on their unique identifiers.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

2. getElementsByTagName()

The method is invoked on a DOM element or the document object and takes a single parameter, which is the tag name of the elements you want to select. The tag name is specified as a string. The method returns a live HTMLCollection or NodeList containing all the elements in the document that match the specified tag name. The returned collection is ordered in the same sequence as they appear in the document.

```
var elements = document.getElementsByTagName(tagName);
```

You can use getElementsByTagName() to access and manipulate specific elements on a web page. For example, to select all the `<p>` (paragraph) elements in the document:

```
var paragraphs = document.getElementsByTagName('p');
```

Iterating through the Collection: Since the returned value is a collection, you can iterate through it using a loop, such as a for loop or a forEach() method, to perform operations on each selected element.

```
var paragraphs = document.getElementsByTagName('p');
for (var i = 0; i < paragraphs.length; i++) {
  // Perform operations on each paragraph element
  console.log(paragraphs[i].textContent);
}
```

Live Collection: The returned collection is live, meaning if the DOM changes (e.g., new elements are added or existing elements are removed), the collection will automatically reflect those changes without requiring manual updates.

Tag Name Case Sensitivity: The getElementsByTagName() method is case-insensitive, meaning it matches elements regardless of whether the tag name is specified in uppercase or lowercase.


```
// Selects all <P> and <p> elements
var elements = document.getElementsByTagName('P');
```

Performance Considerations: While getElementsByTagName() is a convenient method, repeatedly invoking it for the same tag name can be inefficient. If you need to work with the same set of elements multiple times, it's recommended to store the result in a variable to avoid redundant DOM queries.

The getElementsByTagName() method is a straightforward way to select elements based on their tag names and is widely used for basic DOM manipulation and traversal. However, it should be noted that newer methods like querySelectorAll() offer more powerful and flexible options for element selection based on various CSS-like selectors.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

3. getElementsByClassName()

Used to retrieve a collection of elements that have a specific class name. It allows you to select multiple elements based on the class attribute. The method is called on an element (such as document or another DOM element) and takes a single argument, className, which is a string representing the CSS class name to search for. It returns a live HTMLCollection (a collection of elements) or a static NodeList (a non-live collection) that matches the specified class name.

Syntax: `element.getElementsByClassName(className)`

If multiple elements have the same class name, all matching elements are returned.

The returned collection is live, meaning it is automatically updated when the DOM changes. If elements with the specified class name are added or removed, the collection is dynamically updated to reflect the changes.

The method searches for the class name in the element's descendants, including nested elements, but does not search within shadow roots or other DocumentFragments.

If no elements match the specified class name, an empty collection (HTMLCollection or NodeList) is returned.

Example usage:

```
// Get all elements with the class name "myClass" in the entire document
var elements = document.getElementsByClassName('myClass');

// Loop through the returned collection and perform operations on each element
for (var i = 0; i < elements.length; i++) {
  // Access each element using the index and manipulate it
  elements[i].textContent = 'Updated content';
}
```

Note that getElementsByClassName() returns a collection, not an array. If you want to perform array-like operations on the returned elements, you can convert the collection to an array using methods like Array.from() or the spread syntax [...collection].

In summary, getElementsByClassName() is a convenient method for selecting and manipulating elements based on their CSS class name, allowing you to target specific elements within a document or a specific portion of the DOM.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

4. querySelector()

The querySelector() method is a built-in function that allows you to select elements from the DOM (Document Object Model) using CSS selectors. It is part of the Document object and is commonly used to retrieve or manipulate specific elements on a web page. The querySelector() method takes a CSS selector as a parameter and returns the first element that matches the selector. The selector can be a class, an ID, an element type, or any other valid CSS selector. Syntax for querySelector() is document.querySelector(selector)

Here are a few examples of how querySelector() can be used:

```
Selecting an element by its ID:
const myElement = document.querySelector("#myId");
```

This will select the element with the ID "myId" and assign it to the myElement variable.

```
Selecting an element by its class:
const myElement = document.querySelector(".myClass");
```

This will select the first element with the class "myClass" and assign it to the myElement variable.

```
Selecting an element by its tag name:
const myElement = document.querySelector("div");
```

This will select the first `<div>` element on the page and assign it to the myElement variable. If no element matches the specified selector, querySelector() will return null.

It's important to note that querySelector() only returns the first matching element. If you want to select multiple elements that match a given selector, you can use querySelectorAll() instead, which returns a collection of elements.

This will select all elements with the class "myClass" and assign them to the elements variable as a NodeList (a collection of nodes).

Example usage:
```
const elements = document.querySelectorAll(".myClass");
```

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

5. querySelectorAll()

The querySelectorAll() method in JavaScript is a powerful DOM method that allows you to select multiple elements from the DOM using a CSS selector. It returns a static NodeList representing a collection of elements that match the specified selector.

The syntax for querySelectorAll() is as follows:
```
var elementList = document.querySelectorAll(selector);
```

Here, document refers to the global document object, which represents the current HTML document. The querySelectorAll() method is called on the document object, but it can also be called on any DOM element to search for elements within that specific element.
 
The selector parameter is a string representing the CSS selector used to match the elements. It can be any valid CSS selector, such as an element name, class name, ID, attribute, or a combination of selectors.

For example, to select all `<p>` elements in the document, you can use:

```
var paragraphs = document.querySelectorAll('p');
```

The method returns a NodeList, which is a collection of nodes similar to an array but with a few differences. The NodeList represents a snapshot of the selected elements at the time querySelectorAll() was called. It doesn't dynamically update as the DOM changes.
 
You can iterate over the NodeList using a for loop, forEach(), or other array iteration methods. Each item in the NodeList corresponds to a matched element, and you can access their properties and perform operations on them.

Here's an example that adds a CSS class to all `<p>` elements selected using querySelectorAll():

```
var paragraphs = document.querySelectorAll('p');
paragraphs.forEach(function(paragraph) {
  paragraph.classList.add('highlight');
});
```

In the above code, the classList.add() method is used to add the CSS class 'highlight' to each `<p>` element in the NodeList.

Overall, querySelectorAll() provides a flexible and convenient way to select multiple elements from the DOM using CSS selectors, allowing you to perform various operations or apply changes to the selected elements.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

DOM Methods

DOM (Document Object Model) methods are a set of JavaScript methods that allow you to interact with HTML and XML documents. They provide a way to access, manipulate, and modify elements within a web page. Here are some commonly used DOM methods:

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

1. createElement()

The createElement() method is a built-in function in JavaScript that allows you to dynamically create a new DOM element. It is part of the Document Object Model (DOM) API and is available on the document object.

The syntax for using createElement() is as follows:

```
document.createElement(tagName)
```

Here, tagName specifies the HTML tag name of the element you want to create, such as `"div"`, `"p"`, `"span"`, `"img"`, or any other valid HTML tag.

When createElement() is called, it returns a new DOM element of the specified tag name. This element is initially empty, without any content or attributes.

You can then manipulate the newly created element by modifying its properties, adding child elements, setting attributes, or applying styles before appending it to the document.

Here's an example that demonstrates how to use createElement() to create a new div element and add it to the document:

```
// Create a new div element
var newDiv = document.createElement("div");
```
```
// Modify the properties of the new div
newDiv.textContent = "This is a dynamically created div.";
newDiv.style.backgroundColor = "blue";
```
```
// Append the new div to the document
document.body.appendChild(newDiv);
```

In the above example, createElement("div") creates a new div element. Subsequently, properties like textContent and style.backgroundColor are modified to set the text content and background color of the new div, respectively. Finally, appendChild() is used to append the new div as a child of the body element in the document.

The createElement() method is commonly used when you need to dynamically generate and insert elements into the DOM, allowing for flexible and dynamic web page construction and manipulation using JavaScript.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

2. appendChild()

The appendChild() method in JavaScript is used to add a new child node to an existing parent node in the DOM (Document Object Model). It appends the specified node as the last child of the target parent node.

The syntax for using appendChild() is as follows:

```
parentNode.appendChild(childNode);
```

Here, parentNode is the existing node to which you want to append the childNode, which is the new node you want to add.

When appendChild() is called, the following happens:

The childNode is detached from its current position in the DOM, if it exists elsewhere.

The childNode is then added as the last child of the parentNode.

The DOM structure is updated to reflect the new relationship between the parent and child nodes.

It's important to note that if the childNode already exists in the DOM, it will be moved to the new position as the last child of the parentNode.

Here's an example that demonstrates the usage of appendChild():

```
// Create a new paragraph element
var paragraph = document.createElement('p');
paragraph.textContent = 'This is a new paragraph.';

// Find the parent element
var parentElement = document.getElementById('myDiv');

// Append the paragraph as the last child of the parent element
parentElement.appendChild(paragraph);
```

In the example above, a new `<p>` (paragraph) element is created and assigned some text content. Then, using getElementById(), the parent element with the ID 'myDiv' is accessed. Finally, appendChild() is used to append the newly created `<p>` element as the last child of the parent element.

The appendChild() method is a fundamental DOM operation that allows you to dynamically add new content to an existing document structure, enabling dynamic updates and manipulations in web applications.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

2. removeChild()

The removeChild() method in JavaScript is used to remove a specified child node from its parent node in the DOM (Document Object Model). It allows you to dynamically remove elements from the HTML structure. The removeChild() method is called on the parent node to which the child node belongs. It takes the child node as an argument and removes it from the parent node, effectively removing it from the DOM tree. The removed child node is no longer accessible or part of the DOM structure.

Example 1:

```
parentNode.removeChild(childNode);
```

parentNode is the parent node from which the child node will be removed. childNode is the specific child node that needs to be removed from the parent node.

Example 2:

```
// HTML: <div id="parent"><p id="child">This is a child element.</p></div>

var parent = document.getElementById('parent');
var child = document.getElementById('child');

parent.removeChild(child);
```

In the above example, the removeChild() method is used to remove the `<p>` element with the id of "child" from its parent `<div>` element with the id of "parent".

It's important to note that when using removeChild(), you need a reference to both the parent and the child node to perform the removal. Additionally, removing a child node with removeChild() permanently deletes it from the DOM.

These are just a few examples of the many DOM methods available. DOM methods provide powerful functionality for manipulating and interacting with web pages dynamically using JavaScript.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Adding Text and HTML Content

The textContent property allows you to set or retrieve the text content of an element. To add or update text content, simply assign the desired text to the textContent property of the element.

Example:

```
var element = document.getElementById("myElement");
element.textContent = "Hello, world!";
```

In this example, the text content of the element with the ID "myElement" is set to "Hello, world!".
 
The innerHTML property allows you to set or retrieve the HTML content of an element. To add or update HTML content, assign the desired HTML string to the innerHTML property of the element.

Example:

```
var element = document.getElementById("myElement");
element.innerHTML = "<strong>Hello, world!</strong>";
```

In this example, the HTML content of the element with the ID "myElement" is set to `<strong>Hello, world!</strong>`, which will render the text "Hello, world!" in bold.

It's important to note that when using the innerHTML property, you should be cautious with untrusted or user-generated content to avoid potential security risks such as cross-site scripting (XSS) attacks. If you need to insert dynamic content that includes user input or content from an external source, consider using other methods like textContent or sanitizing the HTML before adding it to the DOM.

By utilizing the textContent and innerHTML properties, you can easily add and update text and HTML content within DOM elements.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Practical Implementation Step 1:

```
<!DOCTYPE html>
<html>
<head>
  <title>DOM Selectors and Methods</title>
</head>
<body>
  <div id="myElement">Hello, World!</div>

  <div class="myClass">This is a div with the class "myClass".</div>
  <div class="myClass">Another div with the class "myClass".</div>

  <script>
    // getElementById()
    var elementById = document.getElementById("myElement");
    console.log(elementById);

    // getElementsByTagName()
    var elementsByTagName = document.getElementsByTagName("div");
    console.log(elementsByTagName);

    // getElementsByClassName()
    var elementsByClassName = document.getElementsByClassName("myClass");
    console.log(elementsByClassName);

    // querySelector()
    var elementSelector = document.querySelector("#myElement");
    console.log(elementSelector);

    // querySelectorAll()
    var elementsSelectorAll = document.querySelectorAll(".myClass");
    console.log(elementsSelectorAll);

    // createElement() and appendChild()
    var newElement = document.createElement("p");
    newElement.textContent = "This is a new paragraph.";
    document.body.appendChild(newElement);

    // removeChild()
    var elementToRemove = elementsByTagName[0];
    elementToRemove.parentNode.removeChild(elementToRemove);
  </script>
</body>
</html>
```

In this example, we have a simple HTML document with a few elements. The JavaScript code demonstrates the usage of DOM selectors (getElementById(), getElementsByTagName(), getElementsByClassName(), querySelector(), and querySelectorAll()) to select specific elements. It also showcases the usage of DOM methods (createElement(), appendChild(), and removeChild()) to create, append, and remove elements dynamically.

When you run this code in a web browser and inspect the browser's console, you will see the selected elements logged as output. Additionally, a new paragraph element is created and appended to the <body>, and the first <div> element is removed from its parent.

---

Adding Inline Style

To add inline styles to elements in the DOM (Document Object Model), you can use the style property of an element. The style property allows you to directly manipulate the inline CSS styles of an element. Here's how you can add inline styles using the DOM:
```
var element = document.getElementById("myElement");
element.style.property = "value";
```
In the above code snippet, replace "myElement" with the ID of the element you want to modify. Then, set the desired CSS property and value using the style property. For example, if you want to set the background color of the element to red:
```
var element = document.getElementById("myElement");
element.style.backgroundColor = "red";
```
You can add multiple inline styles by chaining the property assignments:
```
var element = document.getElementById("myElement");
element.style.backgroundColor = "red";
element.style.fontSize = "20px";
element.style.marginTop = "10px";
```
In this example, we set the background color, font size, and margin top properties of the element.

Note that when setting the property name using the style property, you should use camel-case notation for CSS properties that have hyphens. For example, background-color becomes backgroundColor.

Additionally, keep in mind that using inline styles should be done sparingly and for specific cases. It is generally recommended to use CSS classes or modify styles through CSS rules whenever possible, as it helps separate the presentation from the JavaScript logic and makes the code more maintainable.

---

Practical Implementation Step 2:
```
<!DOCTYPE html>
<html>
<head>
  <title>Inline Styling Example</title>
</head>
<body>
  <div id="myElement" style="color: red; font-size: 24px; background-color: yellow;">Hello, World!</div>

  <script>
    var elementById = document.getElementById("myElement");

    // Changing inline styles
    elementById.style.color = "blue";
    elementById.style.fontSize = "18px";
    elementById.style.backgroundColor = "green";

    // Adding multiple inline styles
    elementById.style.cssText = "color: purple; font-weight: bold; text-align: center;";

    // Removing an inline style
    elementById.style.removeProperty("background-color");
  </script>
</body>
</html>
```

Initially, the element has inline styles defined in the HTML using the `style` attribute.

The JavaScript code accesses the element using `getElementById`.

Inline styles are modified using the `style` property by directly assigning values to specific style properties like `color`, `fontSize`, and `backgroundColor`.

Multiple inline styles can be added using the `cssText` property by providing a string containing the desired CSS rules.

An inline style can be removed using the `removeProperty` method by specifying the style property to be removed.

By manipulating the `style` property, you can easily apply and modify inline styles on DOM elements.

---

Editing Attributes

To edit attributes in the DOM (Document Object Model), you can use the setAttribute(), getAttribute(), and removeAttribute() methods. These methods allow you to modify, retrieve, and remove attributes of HTML elements. Here's how you can use them:

setAttribute()
The setAttribute() method in JavaScript is used to add or modify an attribute of an HTML element. It allows you to set the value of a specified attribute on an element dynamically.

The syntax for using `setAttribute()` is as follows:

```
element.setAttribute(attributeName, attributeValue);
```

`element`: The HTML element to which the attribute will be added or modified.

`attributeName`: The name of the attribute to be set.

`attributeValue`: The value to be assigned to the attribute.

Here's an example that demonstrates the usage of setAttribute():

```
<button id="myButton">Click me</button>

var button = document.getElementById('myButton');
button.setAttribute('disabled', 'true');
```

In the above example, the `setAttribute()` method is used to set the `disabled` attribute of the button element to `'true'`. This effectively disables the button, making it unclickable.

If the specified attribute already exists on the element, `setAttribute()` will update its value. If the attribute doesn't exist, `setAttribute()` will create a new attribute with the specified name and value.

It's important to note that when using `setAttribute()`, the attribute value is treated as a string. If you need to set a boolean attribute, such as `disabled` or `checked`, you should pass the string `'true'` or `'false'` as the attribute value.

Overall, `setAttribute()` provides a convenient way to modify attributes of HTML elements using JavaScript dynamically. It allows for flexible manipulation of element properties, enabling you to adapt the behavior and appearance of elements based on application logic or user interactions.

---