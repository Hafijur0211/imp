Take Home Assignment

Task 1: DOM Manipulation

Create an HTML file with a button and a div element. Use JavaScript to implement the following tasks:

1. When the button is clicked, change the background color of the div element to a random color.

2. Append a new paragraph (`<p>`) element inside the div element with some sample text.

Task 2: Event Listeners and Event Object

Create an HTML file with a button and a paragraph element. Use JavaScript to implement the following tasks:

1. Attach a click event listener to the button element.

2. When the button is clicked, update the paragraph's text content to display the number of times the button has been clicked. For example, "Button clicked 3 times."

Task 3: Event Propagation and Event Delegation

Create an HTML file with a parent `<div>` containing several child `<button>` elements. Use JavaScript to implement the following tasks:

1. Attach a click event listener to each button element.

2. When a button is clicked, display an alert with the text "Button {button number} clicked," where `{button number}` corresponds to the button's order in the parent `<div>` (e.g., "Button 1 clicked" for the first button).

3. Implement event delegation by attaching a single click event listener to the parent `<div>`. When clicking any button, display an alert with the same message as in the previous task.

---

Solution

```
<!DOCTYPE html>
<html>
<head>
    <title>DOM and Events Assignment</title>
</head>
<body>
    <!-- Task 1: DOM Manipulation -->
    <h2>Task 1: DOM Manipulation</h2>
    <button id="changeColorBtn">Change Color</button>
    <div id="colorDiv" style="width: 200px; height: 100px; margin-top: 10px; border: solid 0.2rem"></div>
    <button id="appendParagraphBtn">Append Paragraph</button>

    <!-- Task 2: Event Listeners and Event Object -->
    <h2>Task 2: Event Listeners and Event Object</h2>
    <button id="clickBtn">Click Me</button>
    <p id="clickCount">Button clicked 0 times.</p>

    <!-- Task 3: Event Propagation and Event Delegation -->
    <h2>Task 3: Event Propagation and Event Delegation</h2>
    <div id="parentDiv">
        <button>Button 1</button>
        <button>Button 2</button>
    </div>
    
    <script>
        // Task 1: DOM Manipulation
        const changeColorBtn = document.getElementById('changeColorBtn');
        const colorDiv = document.getElementById('colorDiv');
        const appendParagraphBtn = document.getElementById('appendParagraphBtn');

        function getRandomColor() {
            const letters = '0123456789ABCDEF';
            let color = '#';
            for (let i = 0; i < 6; i++) {
                color += letters[Math.floor(Math.random() * 16)];
            }
            return color;
        }

        changeColorBtn.addEventListener('click', function() {
            colorDiv.style.backgroundColor = getRandomColor();
        });

        appendParagraphBtn.addEventListener('click', function() {
            const newParagraph = document.createElement('p');
            newParagraph.textContent = 'Sample text for the new paragraph.';
            colorDiv.appendChild(newParagraph);
        });


        // Task 2: Event Listeners and Event Object
        const clickBtn = document.getElementById('clickBtn');
        const clickCount = document.getElementById('clickCount');
        let count = 0;

        clickBtn.addEventListener('click', function(event) {
            count++;
            clickCount.textContent = `Button clicked ${count} times.`;
        });

        // Task 3: Event Propagation and Event Delegation
        const parentDiv = document.getElementById('parentDiv');

        function handleClick(event) {
            alert(`${event.target.textContent} clicked.`);
        }

        // Attach event listener to each button
        const buttons = parentDiv.querySelectorAll('button');
        buttons.forEach(button => button.addEventListener('click', handleClick));

        // Event Delegation - Attach a single event listener to the parent div
        parentDiv.addEventListener('click', function(event) {
            if (event.target.tagName === 'BUTTON') {
                alert(`${event.target.textContent} clicked (Event Delegation).`);
            }
        });
    </script>
</body>
</html>
```

----

Task 1: Conquer these DOM coding questions effortlessly using the VS Code IDE, and become a DOM manipulation expert!

Problem

Task 1: DOM Manipulation

Create an HTML file with a button and a div element. Use JavaScript to implement the following tasks:

1. When the button is clicked, change the background color of the div element to a random color.

2. Append a new paragraph (`<p>`) element inside the div element with some sample text.

Task 2: Event Listeners and Event Object

Create an HTML file with a button and a paragraph element. Use JavaScript to implement the following tasks:

1. Attach a click event listener to the button element.

2. When the button is clicked, update the paragraph's text content to display the number of times the button has been clicked. For example, "Button clicked 3 times."

Task 3: Event Propagation and Event Delegation

Create an HTML file with a parent `<div>` containing several child `<button>` elements. Use JavaScript to implement the following tasks:

1. Attach a click event listener to each button element.

2. When a button is clicked, display an alert with the text "Button `{button number}` clicked," where {button number} corresponds to the button's order in the parent `<div>` (e.g., "Button 1 clicked" for the first button).

3. Implement event delegation by attaching a single click event listener to the parent `<div>`. When clicking any button, display an alert with the same message as in the previous task.

---

Solution

```
<!DOCTYPE html>
<html>
<head>
    <title>DOM and Events Assignment</title>
</head>
<body>
    <!-- Task 1: DOM Manipulation -->
    <h2>Task 1: DOM Manipulation</h2>
    <button id="changeColorBtn">Change Color</button>
    <div id="colorDiv" style="width: 200px; height: 100px; margin-top: 10px; border: solid 0.2rem"></div>
    <button id="appendParagraphBtn">Append Paragraph</button>

    <!-- Task 2: Event Listeners and Event Object -->
    <h2>Task 2: Event Listeners and Event Object</h2>
    <button id="clickBtn">Click Me</button>
    <p id="clickCount">Button clicked 0 times.</p>

    <!-- Task 3: Event Propagation and Event Delegation -->
    <h2>Task 3: Event Propagation and Event Delegation</h2>
    <div id="parentDiv">
        <button>Button 1</button>
        <button>Button 2</button>
    </div>
    
    <script>
        // Task 1: DOM Manipulation
        const changeColorBtn = document.getElementById('changeColorBtn');
        const colorDiv = document.getElementById('colorDiv');
        const appendParagraphBtn = document.getElementById('appendParagraphBtn');

        function getRandomColor() {
            const letters = '0123456789ABCDEF';
            let color = '#';
            for (let i = 0; i < 6; i++) {
                color += letters[Math.floor(Math.random() * 16)];
            }
            return color;
        }

        changeColorBtn.addEventListener('click', function() {
            colorDiv.style.backgroundColor = getRandomColor();
        });

        appendParagraphBtn.addEventListener('click', function() {
            const newParagraph = document.createElement('p');
            newParagraph.textContent = 'Sample text for the new paragraph.';
            colorDiv.appendChild(newParagraph);
        });


        // Task 2: Event Listeners and Event Object
        const clickBtn = document.getElementById('clickBtn');
        const clickCount = document.getElementById('clickCount');
        let count = 0;

        clickBtn.addEventListener('click', function(event) {
            count++;
            clickCount.textContent = `Button clicked ${count} times.`;
        });

        // Task 3: Event Propagation and Event Delegation
        const parentDiv = document.getElementById('parentDiv');

        function handleClick(event) {
            alert(`${event.target.textContent} clicked.`);
        }

        // Attach event listener to each button
        const buttons = parentDiv.querySelectorAll('button');
        buttons.forEach(button => button.addEventListener('click', handleClick));

        // Event Delegation - Attach a single event listener to the parent div
        parentDiv.addEventListener('click', function(event) {
            if (event.target.tagName === 'BUTTON') {
                alert(`${event.target.textContent} clicked (Event Delegation).`);
            }
        });
    </script>
</body>
</html>
```