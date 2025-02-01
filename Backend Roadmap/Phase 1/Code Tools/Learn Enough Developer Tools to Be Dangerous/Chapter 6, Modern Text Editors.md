This chapter dives into the world of modern text editors, highlighting their power and ease of use compared to basic editors like Vim. It covers essential text editing skills, moving around, selecting text, cut/copy/paste, and more.

## 📝 Modern Text Editors: The Big Three

The chapter introduces three main contenders for modern text editors:

- **Sublime Text**:
    - 👍 **Advantages**: Powerful, hackable, easy to use, fast, robust, cross-platform, and backed by a profitable company.
    - 👎 **Disadvantages**: Not free, has a mildly annoying popup, costs $70, setting up command-line tools takes some fiddling.
- **Visual Studio Code (VSCode)**:
    - 👍 **Advantages**: Powerful with lots of packages, free, fast, robust, cross-platform, backed by Microsoft.
    - 👎 **Disadvantages**: Not open-source and backed by Microsoft.
- **Atom**:
    - 👍 **Advantages**: Powerful, hackable, easy to use, free, open-source, cross-platform, easy to set up command-line tools, backed by GitHub.
    - 👎 **Disadvantages**: Slower than Sublime or VSCode, archived by GitHub.

> ⚠️ **Note**: While Atom was once recommended for its simplicity and being 100% free, it has been archived by GitHub, making **VSCode** or **Sublime Text** better alternatives. Skills learned in one editor generally translate to others.

## ⚙️ Essential Editing Skills

The chapter covers the following core editing skills:

### 📂 Opening Files

- Use the command line tool, `atom` (or `subl` or `code` respectively), to open files. Example: `$ atom README.md`.
- Cloud IDEs like Cloud9 can open files through a filesystem navigator.
- Word wrap (soft wrap) is useful for long lines of text.
- Syntax highlighting makes text formatting visually easier to identify.

### 🖱️ Moving Around

- Use the mouse or trackpad for basic navigation.
- Use arrow keys for movement, often in combination with `Command`, `Control`, or `Function` keys.
- **Important key combinations** include:
    - `←` and `→` to move to the beginning and end of lines.
    - `↑` and `↓` to move to the top and bottom of the file.

### ✍️ Selecting Text

- **Mouse**: Click and drag or click then `Shift`-click.
- **Double-click** a word to select it.
- **Selecting lines**:
    - Click and drag over the lines.
    - Use `Shift` key with `↑` and `↓` arrow keys.
    - `←` and `→` to select single lines.
- **Selecting the entire document**: Use a menu item ("Select All") or press `A`.

### ✂️ Cut, Copy, Paste

- Use the keyboard shortcuts `X` (cut), `C` (copy), and `V` (paste).
- Cut removes text from the document; copy places the text in a buffer without removing it.
- **Jumpcut** on Mac: A free program that expands the copy-and-paste buffer for multiple entries, using the shortcuts `^ V` and `^ V`.

### 🗑️ Deleting and Undoing

- Use the `Delete` key to remove selected text.
- On a Mac, deletes one word at a time.
- **Undo** reverses actions (typically `Z` or `^Z`), and **Redo** reverses the undo (typically `Z` or `Y`).
- `Cut` instead of `Delete` provides an extra layer of redundancy.
- `Undo/Redo` is a trick to find the cursor position.

### 💾 Saving

- Save files using the menu or with `S`.
- Editors often have a visual indicator of unsaved changes.

### 🔍 Finding and Replacing

- Find text with the "Find" menu or `F` shortcut, replace using the modal window.
- Use `G` to find the next match.
- Find and Replace can be done case sensitive or insensitive.

## ⌨️ Key Commands Summary

Here is a table of important commands from the chapter:

|Command|Description|
|---|---|
|Move to beginning of line|Stops on whitespace|
|Move to end of line||
|Move to beginning of file||
|Move to end of file||
|Select Text|Use mouse drag or `Shift` + arrow keys|
|Select Current Word|Double-click, etc.|
|Select All|`A` or menu item|
|Cut/Copy/Paste|`X`/`C`/`V`|
|Undo|`Z` or `^Z`|
|Redo|`Z` or `Y`|
|Save|`S`|
|Find|`F`|
|Find next|`G`|

## 🎯 Conclusion

Mastering a modern text editor is crucial for any aspiring developer. This chapter offers practical techniques for efficient text manipulation, which, when combined with a solid understanding of the underlying principles, provides a strong foundation for more advanced topics in the following chapters.