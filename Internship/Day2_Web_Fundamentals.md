# Day 2 - Web Fundamentals

## 1. How the Web Works

### Client-Server Model
* **Client (Web Browser):** The device/application (like Chrome, Safari, Firefox) that requests information from a server.
* **Server:** A computer hosting website files (HTML, CSS, JS, images) that receives requests from clients and sends back the requested data.

### HTTP vs. HTTPS
* **HTTP (HyperText Transfer Protocol):** The standard protocol used to transmit web pages over the internet.
* **HTTPS (HTTP Secure):** The encrypted version of HTTP. It ensures all data transferred between browser and server is private and secure.

---

## 2. Introduction to HTML (Structure)
HTML stands for **HyperText Markup Language**. It provides the structure of a webpage.

### Basic HTML Page Structure
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My First Webpage</title>
</head>
<body>
    <h1>Welcome to Web Development!</h1>
    <p>This is a paragraph structured with HTML tags.</p>
</body>
</html>
```

### Key Elements & Tags
* **Headings:** `<h1>` to `<h6>`
* **Text Formatting:** `<p>` (paragraph), `<strong>` (bold), `<em>` (italic), `<a>` (links with `href` attribute)
* **Media:** `<img src="profile.jpg" alt="Profile Picture">`
* **Lists:** Ordered `<ol>` and Unordered `<ul>` with list items `<li>`
* **Forms & Input:** `<form>`, `<input>`, `<button>`, `<textarea>`

---

## 3. Introduction to CSS (Styling)
CSS stands for **Cascading Style Sheets**. It defines the layout and styling of HTML elements.

### Adding CSS to HTML
1. **Inline CSS:** Applied directly on elements using the `style` attribute.
   ```html
   <p style="color: blue;">Blue text</p>
   ```
2. **Internal CSS:** Defined inside a `<style>` block in the `<head>` section.
   ```html
   <style>
       body { background-color: #f0f0f0; }
       h1 { color: darkblue; }
   </style>
   ```
3. **External CSS (Recommended):** Linked from an external `.css` file using the `<link>` tag.
   ```html
   <link rel="stylesheet" href="style.css">
   ```

### Selectors & the Box Model
* **Selectors:** Target elements by Tag name (`h1`), Class name (`.card`), or ID (`#submitBtn`).
* **Box Model:** Every HTML element is represented as a box.
  * **Content:** The actual text or image.
  * **Padding:** Space between the content and the border.
  * **Border:** The edge surrounding the padding and content.
  * **Margin:** Outer space separating this element from others.

<div style="text-align: center;">
  <img src="https://github.com/so-sc/HackHarbor-3.0/blob/main/Tech/assets/pyramid-html-css-js.png" alt="HTML CSS JS Relationship" width="350">
</div>

---

## 4. JavaScript Basics (Interactivity)
JavaScript (JS) is a high-level programming language that adds interactivity and dynamic behavior to webpages.

### Variables (`let` and `const`)
* Use `let` for variables that can change.
* Use `const` for variables that remain constant.
```javascript
let score = 10;
score = 15; // valid

const name = "Alice";
// name = "Bob"; // Error: Assignment to constant variable.
```

### DOM Manipulation & Events
The **DOM (Document Object Model)** is the browser's representation of the HTML document structure as a tree. JavaScript can manipulate the DOM dynamically.

#### Example: Changing text content and styles
```javascript
// Selecting elements
const titleElement = document.getElementById("main-title");
const toggleButton = document.getElementById("toggle-btn");

// Modifying attributes/styles
titleElement.innerText = "Hello, DOM!";
titleElement.style.color = "purple";
```

### Event Listeners
We can wait for user actions (like clicks) and run code in response:
```javascript
toggleButton.addEventListener("click", function() {
    alert("Button was clicked!");
});
```

---

## 5. Hands-on Project: Dark Mode Toggle
Let's build a simple page containing a header, some paragraph text, and a button that toggles between Dark Mode and Light Mode.

### Step 1: Create `index.html`
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dark Mode Toggle</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
        <h1 id="theme-title">Light Mode</h1>
        <p>This is a simple demo showing how JavaScript interacts with HTML and CSS.</p>
        <button id="toggle-btn">Toggle Mode</button>
    </div>

    <script src="script.js"></script>
</body>
</html>
```

### Step 2: Create `style.css`
```css
body {
    font-family: Arial, sans-serif;
    background-color: #ffffff;
    color: #333333;
    transition: background-color 0.3s, color 0.3s;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
}

.container {
    text-align: center;
    border: 1px solid #ccc;
    padding: 30px;
    border-radius: 8px;
    box-shadow: 0 4px 6px rgba(0,0,0,0.1);
}

/* Dark Mode Styles */
body.dark-mode {
    background-color: #1e1e1e;
    color: #f5f5f5;
}

button {
    padding: 10px 20px;
    font-size: 16px;
    cursor: pointer;
    border: none;
    border-radius: 4px;
    background-color: #007bff;
    color: white;
    margin-top: 15px;
}

button:hover {
    background-color: #0056b3;
}
```

### Step 3: Create `script.js`
```javascript
const toggleButton = document.getElementById("toggle-btn");
const themeTitle = document.getElementById("theme-title");

toggleButton.addEventListener("click", () => {
    // Toggle the dark-mode class on the body
    document.body.classList.toggle("dark-mode");
    
    // Update the header text accordingly
    if (document.body.classList.contains("dark-mode")) {
        themeTitle.innerText = "Dark Mode";
    } else {
        themeTitle.innerText = "Light Mode";
    }
});
```
