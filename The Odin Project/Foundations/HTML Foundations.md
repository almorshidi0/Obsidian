Okay, here's a comprehensive summary of the HTML Foundations section from the Odin Project, formatted for Obsidian notes with markdown, emojis, and icons, as requested. This summary aims to be thorough, covering all the key aspects of the lessons so you shouldn't need to refer back to the original source.

# 🌐 HTML Foundations: The Core of Web Development

This section introduces the basics of how web pages are constructed, focusing on **HTML** and its role in structuring content. You will also learn about **CSS** and its relationship to HTML as well as other supporting concepts such as file structure, commit messages, and more.

## 🧱 HTML, CSS, and JavaScript: The Trio of Web Development

- **HTML (HyperText Markup Language):** Think of HTML as the **foundation** of a website. It provides the **raw data** and structure for all the content you see on the internet, including text, links, lists and more. HTML uses elements to create all the paragraphs, headings, lists, images, and links that make up a typical webpage.
- **CSS (Cascading Style Sheets):** CSS is what adds **style** to the plain HTML elements. It handles positioning, colors, fonts, and other visual aspects to make the page look good. It is also concerned with the presentation of the information on the web page.
- **JavaScript:** Is a **programming language** that is used to make webpages dynamic. It enables interactive elements, and other functions not found in HTML or CSS.

> ⚠️ **Important**: HTML and CSS are **not** considered programming languages because they are focused on presentation and structure rather than logic.

## 🏷️ HTML Elements and Tags: The Building Blocks

- **HTML Elements:** These are the basic components of a web page, such as paragraphs, headings, and images.
- **HTML Tags:** These are keywords enclosed in angle brackets `< >` that define the start and end of an element.
    - **Opening Tags:** Mark the beginning of an element. For example, `<p>` is an opening paragraph tag.
    - **Closing Tags:** Indicate the end of an element. They are similar to opening tags but include a forward slash. For example, `</p>`.
    - **Full Element**: An HTML element consists of the content wrapped within an opening and closing tag. For example `<p>This is a paragraph.</p>`.
- **Elements as Containers**: HTML elements can be thought of as containers for content, which the browser uses to determine how to interpret and format that content.
- **Semantic HTML:** Is when the correct HTML tags are used for the appropriate content to improve accessibility and search engine rankings.
- **Void Elements**: Some HTML elements do not have a closing tag such as `<br>` or `<img>`. They are also sometimes referred to as self-closing tags, like `<br />` or `<img />`, but this is discouraged in the latest HTML specifications.

## ⚙️ The HTML Boilerplate: The Basic Structure

Every HTML document needs a basic structure or boilerplate before you can start adding content.

- **Creating an HTML file**:
    - Start by creating a new folder, for example, `html-boilerplate`.
    - Then, create a new file in that folder and name it `index.html`. The `.html` extension tells the computer it's an HTML file.
    - Always name the homepage `index.html` because web servers will look for this file by default.
- **`<!DOCTYPE html>` Declaration:** This is the first line of an HTML document and tells the browser what version of HTML to use. For HTML5, it's simply `<!DOCTYPE html>`.
- **`<html>` Element:** This is the root element of the document. All other elements are descendants of this one.
    - The `lang` attribute inside the `<html>` tag specifies the language of the text content, which is important for accessibility.
- **`<head>` Element:** This contains meta-information about the webpage. It should not contain elements that display content on the page.
    - **`<meta charset="utf-8">`:** Sets the character encoding to UTF-8 which helps ensure special characters from various languages display correctly.
    - **`<title>`:** Sets the title that appears in the browser tab. For example, `<title>My First Webpage</title>`.
- **`<body>` Element:** This contains all the content that is displayed to the user, such as text, images, and lists.
- **Viewing HTML Files:** You can open HTML files in a browser by dragging and dropping, double-clicking, or using the terminal.
- **VSCode shortcut**: Typing `!` in the first line of an HTML file in VSCode and pressing enter generates the basic HTML boilerplate.
    - The boilerplate produced by this shortcut includes a viewport meta tag, which is for responsive design and is discussed later in the curriculum.
- **Validators**: Use an HTML validator like the [W3 HTML validator](https://validator.w3.org/) to check if your HTML is correct, and to help identify errors such as missing closing tags or extra spaces.

## 📝 Working with Text Elements

- **Paragraphs**: Use the `<p>` tags to create paragraphs. Browsers will compress new lines into single spaces, so the `<p>` tag is necessary to create paragraphs.
- **Headings**: There are six levels of headings, from `<h1>` (most important) to `<h6>` (least important).
    - `<h1>` should be used for the main heading of the page.
    - Lower level headings should be used for content in smaller sections of the page.
- **Bold Text:** The `<strong>` element makes text bold and also semantically marks it as important.
- **Italicized Text:** The `<em>` element makes text italic and adds emphasis to it.
- **Nesting Elements:** Elements can be placed inside other elements. This creates a parent and child relationship. Elements at the same level are considered siblings. Indentation is used to make the nesting level clear.
- **HTML Comments:** These are not visible in the browser. They are used to comment on your code using `<!--` and `-->` tags.

## 📃 Lists: Ordered and Unordered

- **Unordered Lists:** These are used for lists where the order doesn't matter. They are created using the `<ul>` element. Each list item is created with the `<li>` element.
- **Ordered Lists:** Use these for lists where the order is important, using the `<ol>` element. List items are again created using `<li>` tags.

## 🔗 Links and Images

- **Links:** Use the anchor element `<a>` to create links to other pages.
    - The `href` attribute specifies the destination of the link.
    - The `target` attribute specifies where the link will open. `target="_blank"` will open the link in a new tab or window.
    - The `rel="noopener"` attribute ensures the link opened in a new tab can’t access the original page. The `rel="noreferrer"` attribute provides both privacy and security, it prevents the new page from knowing where the user came from, and also includes the behavior of `noopener`. It's recommended to always pair a `target="_blank"` with a `rel="noopener noreferrer"`.
- **Types of Links**:
    - **Absolute Links**: Links to pages on other websites, including the scheme, domain, and path.
        - Example `https://www.theodinproject.com/about`
    - **Relative Links**: Links to other pages within your own website and they don't include the domain name. They include the path relative to the page you are creating the link on.
        - For example, if the current page is `index.html` and you want to link to `about.html` that is located in the same directory, you would use `about.html`. If about.html was in a subdirectory called `pages`, the link would be `pages/about.html`.
        - To specify a file/directory relative to the current directory you should prepend `./` before the link: `./pages/about.html`.
        - To go to a parent directory, use `../` in the relative filepath.
- **Images:** Use the `<img>` element to display an image on a web page.
    - The `src` attribute is used to tell the browser the location of the image file. This can be an absolute or relative path.
    - The `alt` attribute is used to describe an image for accessibility purposes and will be shown if the image can't be loaded.
    - It is a good habit to also include the `height` and `width` attributes to prevent the page from jumping and flashing while it loads.

## 📝 Commit Messages: Documenting Your Code

- **Importance**: Good commit messages are crucial for job applications, for other developers, and for yourself when you return to a project.
- **Structure:** Effective commits should consist of two parts:
    - **Subject:** A brief summary of the change, kept within 50 characters.
    - **Body:** A concise yet clear description of why the change was made, kept within 50 characters.
- Always separate the subject from the body with a new/blank line.
- Use the command `git commit` without the `-m` flag to write a commit with a subject and body in VSCode.
- **Committing**: Commit your code every time you have a meaningful change, such as when a piece of code functions as expected, or when you have fixed a bug.
- **Additional Resources:** [[How to Write a Git Commit Message]]
