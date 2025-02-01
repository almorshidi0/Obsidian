This module dives into the core concepts of CSS, focusing on syntax, selectors, the cascade, the box model, and element display properties. This knowledge is fundamental to styling webpages and controlling their layout.

## ✍️ Intro to CSS 💻

### Core Concepts 💡

- **CSS (Cascading Style Sheets)** is used to add style to HTML elements. It controls the visual presentation of a web page, including colors, fonts, layout, and responsiveness.
- **CSS rules** consist of a selector and a declaration block. The declaration block includes properties and values.
- A **selector** indicates the HTML element(s) that a rule will be applied to.
- A **declaration** is composed of a property and a value, separated by a colon, e.g., `color: blue;`. Multiple declarations within a block are separated by semicolons.

### Selectors 🎯

- **Universal Selector (`*`)**: Selects all elements on the page.
- **Type Selectors**: Select all elements of a given type, using the element name e.g., `div`.
- **Class Selectors**: Select all elements with a specific class, denoted by a period (`.`) followed by the class name, e.g., `.alert-text`.
- **ID Selectors**: Select a single element with a specific ID, denoted by a hashtag (`#`) followed by the ID, e.g., `#title`. IDs should be unique on a single page.
- **Grouping Selectors**: Apply the same rules to multiple selectors using a comma-separated list, e.g., `.read, .unread`.
- **Chaining Selectors**: Combine multiple selectors without spaces to target elements with multiple classes or a class and ID, e.g., `.subsection.header` or `.subsection#preview`.
- **Descendant Combinator**: Selects an element that is a descendant of another element, using a space between the selectors, e.g., `.ancestor .child`.
- **Combinators** show a relationship between selectors. The descendant combinator is represented by a space between selectors.
- Descendant combinators can be nested to select elements with multiple levels of nesting, e.g., `.one .two .three .four`.

### Properties ⚙️

- **`color`**: Sets the text color of an element.
- **`background-color`**: Sets the background color of an element.
    - Both `color` and `background-color` can take keyword values (e.g. `red`, `transparent`), HEX values, RGB values, or HSL values.
- **`font-family`**: Sets the font of the text, takes a comma-separated list of font names (with generic fallbacks).
- **`font-size`**: Sets the size of the font.
- **`font-weight`**: Sets the boldness of the font.
- **`text-align`**: Sets the horizontal alignment of the text.
- **`height`**: Sets the height of an element. Using `auto` for height while setting `width` will maintain proportions.
- **`width`**: Sets the width of an element. Setting explicit heights and widths for images prevents content shift while loading.

### Adding CSS to HTML 🔗

- **External CSS**: Links a separate `.css` file in the `<head>` of an HTML document using a `<link>` tag. This is the most common and recommended method.
- **Internal CSS**: Adds CSS rules inside `<style>` tags in the `<head>` of an HTML document. Useful for unique styles on a single page.
- **Inline CSS**: Adds CSS directly to an HTML element using the `style` attribute. Not recommended for most situations due to maintainability issues.
- External CSS keeps HTML and CSS separate for cleaner code and easier maintenance.
- Inline CSS will override other methods, which can cause unexpected results.

### 🤔 Knowledge Check:

- **What is the syntax for class and ID selectors?** Class selectors use a `.` (period) followed by the class name. ID selectors use a `#` (hashtag) followed by the ID name.
- **How would you apply a single rule to two different selectors?** Use a comma-separated list e.g. `.read, .unread { ... }`.
- **Given an element that has an id of `title` and a class of `primary`, how would you use both attributes for a single rule?** Chain the selectors together e.g. `#title.primary`.
- **What does the descendant combinator do?** It selects elements that are descendants of a specified ancestor.
- **What are the names of the three ways to add CSS to HTML?** External, internal, and inline.
- **What are the main differences between the three ways of adding CSS to HTML?** External CSS is in a separate file and linked to the HTML, internal CSS is within `<style>` tags in the HTML, and inline CSS is added directly to HTML elements.

## 🌊 The Cascade ⚖️

### Core Concepts 💡

- The **cascade** determines which CSS rules are applied when there are conflicting styles.
- CSS does not act against our wishes, any unexpected behavior is due to default browser styles, a misunderstanding of how a property works or a misunderstanding of the cascade.
- The cascade uses **specificity**, **inheritance**, and **rule order** to determine which styles are applied.

### Specificity 🎯

- Specificity determines which rule takes precedence when multiple rules target the same element.
- **Inline styles** have the highest specificity.
- **ID selectors** are more specific than class selectors.
- **Class selectors** are more specific than type selectors.
- When there is no selector with higher specificity, a rule with more selectors of the same type will take precedence.
- The **universal selector (`*`) and combinators** (e.g., , `>`, `+`, `~`) do not add specificity.
- Chaining selectors increases specificity only when the chain includes different types of selectors, such as a class and an ID selector.
    - When comparing rules with the same specificity, the number of selectors is taken into account, with rules that have more selectors taking precedence.

### Inheritance 🧬

- Some CSS properties are inherited by descendant elements.
- **Typography-based properties** such as `color`, `font-size`, and `font-family` are usually inherited.
- Directly targeting an element always beats inheritance.

### Rule Order 📃

- If specificity and inheritance do not resolve conflicts, the rule declared **last** in the CSS file is applied.

### 🤔 Knowledge Check:

- **Between a rule that uses one class selector and a rule that uses three type selectors, which rule has the higher specificity?** The rule with the class selector has a higher specificity.

## 🔎 Inspecting HTML and CSS ⚙️

### Core Concepts 💡

- **Browser developer tools** are essential for inspecting and debugging HTML and CSS.
- The **Elements** panel displays the HTML structure of the page.
- The **Styles** panel displays all the currently applied CSS styles of the selected element.

### Using the Inspector 💻

- Open the inspector by right-clicking on an element and selecting "Inspect" or by pressing F12.
- In the Elements panel, click on an element or use the inspector icon to select a specific element.
- The Styles panel will show the element's styles, including any that are being overridden by more specific rules (indicated by a strikethrough).
- Styles can be edited directly in the Styles panel in real-time. Changes made are temporary and do not modify the source files.

### 🤔 Knowledge Check:

- **How do you select a specific element on your page with your browser’s developer tools?** Use the inspector tool, or click on elements directly in the Elements tab.
- **What does a strikethrough in a CSS declaration mean in your browser’s developer tools?** It means the style has been overwritten by another style with higher specificity.
- **How do you change CSS in real-time on specific elements of a web page with your browser’s developer tools?** Click inside a CSS rule in the Styles panel, and make changes.

## 📦 The Box Model 📐

### Core Concepts 💡

- Every element on a webpage is a **rectangular box**.
- The **box model** defines how the size of an element is calculated, including content, padding, border, and margin.
- **Padding** creates space between the content and the border.
- **Border** adds space between padding and margin.
- **Margin** creates space between the border of one element and the border of adjacent elements.

### Key Properties ⚙️

- **`padding`**: Increases the space between the content and the border of an element.
- **`border`**: Adds a border around an element, also creating space.
- **`margin`**: Creates space around an element, between its border and the border of other elements.
- **`box-sizing`**: Alters how the width and height of an element is calculated.
    - The default `content-box` adds padding and border to the width and height.
    - `border-box` includes padding and border in the width and height.

### 🤔 Knowledge Check:

- **From inside to outside, what is the order of box-model properties?** Content, padding, border, margin.
- **What does the box-sizing CSS property do?** It changes how an element’s total width and height are calculated by including or excluding padding and border.
- **What is the difference between the standard and alternative box model?** The standard box model (`content-box`) does not include padding and border in the element's width and height; the alternative model (`border-box`) does.
- **Would you use margin or padding to create more space between 2 elements?** Margin.
- **Would you use margin or padding to create more space between the contents of an element and its border?** Padding.
- **Would you use margin or padding if you wanted two elements to overlap each other?** You would use a negative margin.
- **How do you set the alternative box model for all of your elements?** Using the universal selector and `box-sizing: border-box;`.
- **How do you center an element horizontally?** You can use `margin: 0 auto;` on block-level elements.

## 🧱 Block and Inline ↔️

### Core Concepts 💡

- **Normal flow** refers to how elements are laid out on a page by default.
- Elements are either **block** or **inline**. The `display` property controls this.
- **Block elements** start on a new line and take up the full width available. They stack on top of each other by default.
- **Inline elements** do not start on a new line and only take up as much width as necessary.
- **Inline-block elements** are like inline elements but with block-style padding and margin capabilities.

### Key Elements ⚙️

- `<div>` elements are block-level elements, often used as containers. They can be used to divide the page into blocks and apply styling.
- `<span>` elements are inline-level elements, often used for styling text. They can be used for grouping inline content.

### 🤔 Knowledge Check:

- **What is the difference between a block element and an inline element?** Block elements start on a new line and take up full width; inline elements do not start on a new line and only take up the necessary width.
- **What is the difference between an inline element and an inline-block element?** Inline elements do not respect padding and margin; inline-block elements do.
- **Is an `h1` block or inline?** Block.
- **Is `button` block or inline?** Inline.
- **Is `div` block or inline?** Block.
- **Is `span` block or inline?** Inline.
