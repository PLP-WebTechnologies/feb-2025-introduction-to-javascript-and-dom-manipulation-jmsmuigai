# Introduction to JavaScript and DOM Manipulation

## Objectives

Write basic JavaScript functions.
Manipulate the DOM dynamically.
Respond to user interactions.

## Instructions

- Create a script.js file and link it to a HTML.
- Structure the document using DOCTYPE, html, head, and body.

>[!NOTE]
>  - Write JavaScript that:
>  - Changes text content dynamically.
>  - Modifies CSS styles via JavaScript.
>  - Adds or removes an element when a button is clicked.


# Tasks
- Create a well-structured HTML5 document.
- Use at least 5 different HTML elements.
- Ensure semantic correctness.

Happy Coding! 💻✨

index.html

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>JavaScript DOM Demo</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <header>
    <h1 id="mainTitle">Welcome to DOM Manipulation 🚀</h1>
  </header>

  <main>
    <p id="introText">Click the button below to change this text and style.</p>
    <button onclick="changeText()">Change Text & Style</button>

    <section>
      <h2>Dynamic List</h2>
      <ul id="dynamicList">
        <li>Item 1</li>
        <li>Item 2</li>
      </ul>
      <button onclick="addItem()">Add Item</button>
      <button onclick="removeItem()">Remove Item</button>
    </section>
  </main>

  <footer>
    <p>&copy; 2025 - JavaScript DOM Fun 🎉</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>




script.js

function changeText() {
  const intro = document.getElementById("introText");
  intro.textContent = "The text has changed! ✨";
  intro.style.color = "blue";
  intro.style.fontWeight = "bold";
}

function addItem() {
  const ul = document.getElementById("dynamicList");
  const newItem = document.createElement("li");
  newItem.textContent = "New Item " + (ul.children.length + 1);
  ul.appendChild(newItem);
}

function removeItem() {
  const ul = document.getElementById("dynamicList");
  if (ul.children.length > 0) {
    ul.removeChild(ul.lastChild);
  }
}



style.css
body {
  font-family: Arial, sans-serif;
  margin: 2rem;
  background-color: #f0f4f8;
}

button {
  margin-top: 10px;
  margin-right: 5px;
  padding: 0.5rem 1rem;
  cursor: pointer;
}

