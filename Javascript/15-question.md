Problem

Create an HTML document with the following structure:

```
<!DOCTYPE html>
<html>
<head>
    <title>DOM Manipulation Assignment</title>
</head>
<body>
    <div id="main-container">
        <h1>Hello, DOM Manipulation!</h1>
        <p class="intro">Welcome to this assignment. This is a simple demonstration of DOM manipulation.</p>
        <div class="box"></div>
        <button id="btn">Click Me!</button>
    </div>
</body>
</html>
```

Task 1: DOM Selection and Text Manipulation

- Use JavaScript to target the `<h1>` element with the ID "main-container" and change its text content to "DOM Manipulation Assignment."

- Target the paragraph with the class "intro" and append the following text to it: "In this assignment, you will practice DOM manipulation techniques."

Task 2: Adding HTML Content and Inline Styles

- Target the `<div>` with the class "box" and add the following HTML content inside it:

```
<h2>Box Content</h2> <p>This box is being dynamically generated and styled using JavaScript.</p>
```

Apply inline styles to the box (the `<div>` with class "box") with the following properties:

- Background color: "#f2f2f2"
- Border: "1px solid #333"
- Padding: "10px"

Task 3: Working with Classes

- Create a new CSS class called "highlight" with the following properties:
- Background color: "yellow"
- Font-weight: "bold"
- When the button with the ID "btn" is clicked, add the "highlight" class to the paragraph with the class "intro".

solution

index.html

```
<!DOCTYPE html>
<html>
<head>
    <title>DOM Manipulation Assignment</title>
    <style>
        .box {
            background-color: #f2f2f2;
            border: 1px solid #333;
            padding: 10px;
        }

        .highlight {
            background-color: yellow;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <div id="main-container">
        <h1>Hello, DOM Manipulation!</h1>
        <p class="intro">Welcome to this assignment. This is a simple demonstration of DOM manipulation.</p>
        <div class="box"></div>
        <button id="btn">Click Me!</button>
        <button id="btn-remove">Remove Highlight</button>
    </div>

    <script src="script.js"></script>
</body>
</html>
```

script.js

```
// DOM Selection and Text Manipulation
document.getElementById("main-container").querySelector("h1").textContent = "DOM Manipulation Assignment";

const introParagraph = document.querySelector(".intro");
introParagraph.textContent += " In this assignment, you will practice DOM manipulation techniques.";

// Adding HTML Content and Inline Styles
const boxDiv = document.querySelector(".box");
boxDiv.innerHTML = `
    <h2>Box Content</h2>
    <p>This box is being dynamically generated and styled using JavaScript.</p>
`;

// Inline styles
boxDiv.style.backgroundColor = "#f2f2f2";
boxDiv.style.border = "1px solid #333";
boxDiv.style.padding = "10px";


// Working with Classes
const btn = document.getElementById("btn");
const btnRemove = document.getElementById("btn-remove");

btn.addEventListener("click", () => {
    introParagraph.classList.add("highlight");
});

btnRemove.addEventListener("click", () => {
    introParagraph.classList.remove("highlight");
});
```
