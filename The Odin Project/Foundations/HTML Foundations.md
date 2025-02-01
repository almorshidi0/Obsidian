This module covers the essential building blocks of web development: HTML and CSS, along with a brief introduction to JavaScript and how it relates to these two foundational languages. Let's dive in!

## 🧱 HTML & CSS Basics 🎨

### Core Concepts 💡

- **HTML (HyperText Markup Language)** is the **raw data** that forms the structure of a webpage. It's responsible for the content: text, links, lists, and buttons. Think of it as the skeleton 🦴 of a webpage.
- **CSS (Cascading Style Sheets)** adds style to the plain HTML elements. It handles positioning, colors, fonts, and overall appearance, making webpages visually appealing. It's the skin and clothing 👕 of the webpage.
- **JavaScript** is a programming language that makes webpages interactive. It is not covered in the module but important to understand its relationship to HTML and CSS.
- **HTML and CSS are not programming languages** because they are only used for presentation and not for programming logic.

### HTML & CSS Working Together 🤝

- HTML puts information on the page, and CSS positions that information and makes it look great.
- You need both HTML and CSS to build functional and visually appealing websites.

### 🤔 Knowledge Check:

- **What do HTML and CSS stand for?** HyperText Markup Language and Cascading Style Sheets
- **Which would you use for putting paragraphs of text on a webpage?** HTML
- **Which would you use for changing the font and background color of a button?** CSS

## 🏷️ Elements and Tags 📦

### Key Concepts 🔑

- **HTML elements** create the structure of a web page: paragraphs, headings, lists, images and links.
- **HTML tags** are used to define elements. Most elements are made of opening and closing tags.
- Opening tags use angle brackets `< >` to mark the start of an element, e.g. `<p>`.
- Closing tags look like opening tags, but with a forward slash `/` before the keyword, e.g. `</p>`.
- Elements are like containers for content. Tags indicate what kind of content the element contains and how the browser should display it.
- **Semantic HTML** is using the correct tags for the correct content. This impacts search engine rankings and accessibility.

### Structure of an Element

- **Opening tag:** `<p>`
- **Content:** "some text content"
- **Closing tag:** `</p>`
- Example: `<p>some text content</p>`

### Void Elements 🚫

- Some elements don't have closing tags, such as `<img>` or `<br>`. They are called void elements because they do not contain any content.
- Void elements might also be seen as self-closing tags with a forward slash `/` at the end: `<img />`, but this is discouraged in the latest HTML specification.

### 🤔 Knowledge Check:

- **What is an HTML tag?** A keyword enclosed in angle brackets that defines an HTML element.
- **What are the three parts of an HTML element?** Opening tag, content, and closing tag.

## 📃 HTML Boilerplate ⚙️

### What is a Boilerplate?

- All HTML documents need a basic structure, or "boilerplate," to function correctly.

### Creating an HTML File 📁

- Create a new folder, e.g., `html-boilerplate`, and within it create `index.html` file.
- The `.html` extension tells the computer that it's an HTML file.
- The file containing the homepage of the website should be called `index.html`.

### Key Elements of the Boilerplate 🧱

- **`<!DOCTYPE html>`** - This declaration specifies the HTML version (HTML5) to the browser. It should be the very first line of an HTML document.
- **`<html>`** - The root element that contains all other elements.
    - The **`lang` attribute** specifies the language of the text, enhancing accessibility. e.g., `<html lang="en">`.
- **`<head>`** - Contains meta-information (not displayed content) required for the page to render properly.
    - **`<meta charset="UTF-8">`** - Specifies the character encoding for the page, which helps to display different characters and symbols correctly.
    - **`<title>My First Webpage</title>`** - Sets the title of the webpage that appears in the browser tab.
- **`<body>`** - Contains all content that is displayed on the webpage. This is where all the text, images and other visible elements go.

### Viewing HTML Files in the Browser 🌐

- Use Google Chrome 🌐 as a primary browser during this course.
- **Methods to Open HTML Files**:
    - Drag and drop the HTML file into the browser address bar.
    - Double-click the HTML file to open it in your system's default browser.
    - Use the terminal: `google-chrome index.html` (Ubuntu), `open ./index.html` (macOS), or `explorer.exe index.html` (WSL).

### VSCode Shortcut ⚡

- Typing `!` in a `.html` file and pressing `Enter` will generate the boilerplate.
- It's important to understand how to write boilerplate from scratch, not just use the shortcut, to build muscle memory.

### 🤔 Knowledge Check:

- **What is the purpose of the doctype declaration?** To tell the browser which version of HTML is being used.
- **What is the HTML element?** The root element of the document that contains all other elements.
- **What is the purpose of the head element?** To contain meta-information about the webpage.
- **What is the purpose of the body element?** To contain all the content that is displayed to the user.

## ✍️ Working with Text 📃

### Paragraphs `<p>`

- Browsers compress new lines of text in HTML into single spaces.
- Use the `<p>` element to create paragraphs, which will add a new line after each paragraph.

### Headings `<h1>` to `<h6>`

- Headings are displayed larger and bolder than other text.
- There are six heading levels from `<h1>` (largest, most important) to `<h6>` (smallest, least important).
- The correct level of heading provides hierarchy to content.
    - `<h1>` should be used for the main heading of the page.
    - Lower-level headings (`<h2>`, `<h3>`, etc.) should be used for headings within smaller sections.

### Strong `<strong>` and Emphasis `<em>`

- The `<strong>` element is used to make text bold and indicate importance.
- The `<em>` element is used to emphasize text, typically rendered in italics .

### Nesting Elements 🪆

- HTML elements can be nested inside one another, creating a hierarchical structure .
- For example, text can be emphasized inside a paragraph .

### HTML Comments `<!-- -->`

- Comments are used to add notes within the HTML code that are not displayed in the browser .
- They can be used to explain the code or temporarily hide parts of it .

### 🤔 Knowledge Check:

- **What is the HTML element to make text bold?** `<strong>`.
- **What is the HTML element to make text italicized?** `<em>` .
