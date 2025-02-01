This module dives deep into Flexbox, a powerful CSS layout tool that has become a cornerstone of modern web development. Forget old methods; Flexbox is here to revolutionize how you position elements!.

## 🚀 Introduction to Flexbox

- Flexbox is a CSS layout model that arranges items in rows or columns. It allows items to "flex"—grow or shrink based on defined rules.
- It might seem complex at first, but with practice, it'll become your go-to for layouts.
- **Key Concept**: Flexbox is not just one property, but a toolbox of properties.
- Use your browser's developer tools to inspect and debug your Flexbox layouts.

### 📦 Flex Containers and Items

- A **flex container** is any element with `display: flex`.
- A **flex item** is an element that lives directly inside a flex container.
- **Important**: Any element can be both a flex container and a flex item, allowing for nesting. This enables complex layouts.
- `display: flex` makes the element a flex container and its direct children become flex items.

### 🔨 Getting Started with Flexbox

- Start by experimenting with interactive examples in the course.
- Uncomment the flex-related CSS declarations to see Flexbox in action.
- You'll see that divs arrange horizontally and "flex" (grow/shrink) to fit the available space.

## 📏 Flexbox Properties

### ↔️ The Flex Shorthand

- The `flex` property is a shorthand for `flex-grow`, `flex-shrink`, and `flex-basis`.
- `flex: 1` is equivalent to `flex-grow: 1, flex-shrink: 1, flex-basis: 0`.
- If only one value is specified, it applies to `flex-grow`.
- **Example:** `flex: 1` is shorthand for `flex: 1 1 0;`.
- `flex: auto` is equivalent to `flex-grow: 1`, `flex-shrink: 1` and `flex-basis: auto`.
- `flex: auto` is equivalent to `flex: 1 1 auto`.

#### 🪴 Flex-grow

- Determines a flex item's "growth factor".
- `flex-grow: 1` makes all items grow equally.
- `flex-grow: 2` makes an item grow twice as much as others.

#### 📉 Flex-shrink

- Sets the "shrink factor" of a flex item.
- Applied when the size of flex items exceeds their container.
- `flex-shrink: 1` (default) makes all items shrink evenly.
- `flex-shrink: 0` prevents an item from shrinking.

#### 📐 Flex-basis

- Sets the initial size of a flex item.
- Default is `0%` in the flex shorthand.
- `flex-basis: auto` tells the item to check for a width declaration.
- **Important**: Flex items might not respect given width values when flex-grow or flex-shrink are specified.

### 🧭 Flexbox Axes

- Flex containers have two axes: the **main axis** and the **cross axis**.
- The **main axis** direction is changed with the `flex-direction` property.
- `flex-direction: row` (default): main axis is horizontal.
- `flex-direction: column`: main axis is vertical.
- When `flex-direction` is column, `flex-basis` refers to height instead of width.
- The default behavior is `flex-direction: row`, which works well because block-level elements default to the full width of their parent.

## 🧮 Alignment

### ↔️ justify-content

- Aligns items across the **main axis**.
- Values include `space-between`, `center`, and others.
- Changes alignment behavior when you change the `flex-direction` of a container.

### ↕️ align-items

- Aligns items across the **cross axis**.
- `align-items: center` centers items along the cross axis.
- Changes alignment behavior when you change the `flex-direction` of a container.

### ↔️ Gap

- Adds space between flex items, similar to margin.
- `gap: 8px` sets a space of 8 pixels between items.

## 📝 Practical Tips

- Use `flex: 1` to make divs grow evenly.
- Use `flex-shrink: 0` to prevent certain divs from shrinking.
- Start with HTML content, then style using CSS.

## 💻 Project: Landing Page

- Create a full web page from a given design.
- Use images for the complete website and for the fonts and colors used.
- Focus on getting elements in the right relative positions, not pixel-perfect.
- Divide your work into sections for easier management.
- Use free-to-use images and give proper credit.

### 📚 Setting up your Project

- Set up a Git repository for your project.
- Avoid looking at others' solutions prematurely.
- Commit early and often!.
- Publish your project via GitHub pages.

## 🤔 Knowledge Checks

- **Flex Container vs. Flex Item:** A flex container has `display: flex`, and flex items are its direct children.
- **Flex Shorthand:** `flex: 1` is shorthand for `flex-grow: 1`, `flex-shrink: 1`, `flex-basis: 0`.
- **Axes:** Main axis is horizontal (row) or vertical (column) based on `flex-direction`.
- **Alignment:** `justify-content` aligns items along the main axis, and `align-items` aligns them along the cross axis.

## 🔗 Additional Resources

- [Interneting Is Hard](https://www.internetingishard.com/html-and-css/flexbox/)
- [Flexbox in 8 minutes](https://www.youtube.com/watch?v=k32voqQhXl8)
- [MDN’s flex documentation](https://developer.mozilla.org/en-US/docs/Web/CSS/flex)
- [CSS Tricks "Guide to Flexbox"](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
- [Interactive Guide to Flexbox](https://www.joshwcomeau.com/css/interactive-guide-to-flexbox/)
- [Flexbox Froggy](https://flexboxfroggy.com/)
- [Flexbox Zombies](https://mastery.games/p/flexbox-zombies)
