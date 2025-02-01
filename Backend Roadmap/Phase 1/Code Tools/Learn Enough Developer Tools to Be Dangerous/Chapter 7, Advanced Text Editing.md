This chapter builds upon the basics of modern text editors covered in Chapter 6, diving into advanced features that boost productivity and efficiency. These advanced features can be used in any professional-grade editor.

## ⚡ Autocomplete and Tab Triggers

These two features allow users to type less and accomplish more.

### ✨ Autocomplete

- The most common form of autocomplete allows you to type the first few letters of a word, then presents you with options for completion.
- You can usually accept the completion using the `tab` key.
- Autocomplete is especially helpful in longer documents with many potential completions.
- For example, when writing in LaTeX, you can use autocomplete to avoid typing out long cross-reference labels.
- Some text editors allow you to configure a specific key, such as `ESC`, for autocompletion.

### ⌨️ Tab Triggers

- Tab triggers are similar to autocomplete but are activated by pressing the `tab` key after typing a few letters.
- The specific triggers available will depend on the text editor and file type.
- For example, in Markdown, typing `lorem` then `tab` will generate sample `lorem ipsum` text.
- In HTML, typing `html` then `tab` will create an HTML skeleton.
- In Ruby, typing `def` then `tab` will create a Ruby function definition.
- You can also define your own custom tab triggers.

## ✍️ Writing Source Code

Text editors provide many special functions for writing computer programs.

### 🌈 Syntax Highlighting

- Syntax highlighting makes code easier to read by using different colors for different elements (e.g., keywords, strings, comments).
- The editor often infers the language from the file extension (e.g., `.rb` for Ruby).
- Syntax highlighting helps to catch errors, for example if a quote is missing in a string the highlighting can make it apparent.

### 💬 Commenting Out

- Commenting out code allows you to temporarily disable it without deleting it.
- Most programming and markup languages support comment lines.
- In Ruby, a line beginning with `#` is a comment.
- Text editors allow you to select multiple lines of code and comment them out with a menu item or keyboard shortcut (usually `⌘/`).
- The commenting out feature is a toggle that allows you to easily re-enable the code.

### 📏 Indenting and Dedenting

- Indentation is the use of leading spaces at the beginning of lines.
- Many programmers use a set number of spaces (typically two or four) to represent a tab.
- Text editors typically insert new lines at the same indentation level as the previous line.
- You can also indent or dedent entire blocks of code using a keyboard shortcut or menu option.
- The default key bindings in Atom are `⌘[` for dedenting, and `⌘]` for indenting.

### 📍 Goto Line Number

- Text editors allow you to quickly jump to a specific line number using a shortcut.
- In many editors, the relevant shortcut is `^G`.

### ↔️ 80 Columns

- Many text editors help you enforce a line limit of 80 characters for readability.
- Some editors show a subtle vertical line at the 80-column mark.
- The 80-column limit is a good coding discipline, as exceeding it may indicate a variable or function name is too long.

## 📝 Writing an Executable Script

- You can use a text editor to create a shell script (a program to automate common tasks).
- The first line of a shell script is often a "shebang" (e.g., `#!/bin/bash`) which tells the system how to execute the script.
- A shell script can be used to send a sequence of codes to kill a misbehaving process.
- It's important to add the directory where the script is located to the system path.
- To add `~/bin` to the system path, you can edit the `~/.bash_profile` file by adding the line `export PATH="$HOME/bin:$PATH"` and then use the `source` command.
- The `chmod +x <filename>` command makes the script executable.
- You can use the `which <filename>` command to verify that the script is ready to use.
- It's also important to make sure that your script has helpful usage messages.

## 📁 Editing Projects

- Text editors can be used to open and edit entire projects, not just single files.
- You can use the command line to open an entire directory with `atom .`.
- A project is displayed in a "tree view".
- **Fuzzy opening** allows you to quickly open a file by typing a few letters of its name (usually `⌘P` in Atom).

### 📑 Multiple Tabs and Panes

- You can open multiple files in different tabs.
- You can also split the editor into multiple panes to view different files side by side.
- This is useful for viewing test code and application code in separate panes.
- Opening the same file in two panes can be helpful for navigating around a document.

### 🔍 Global Find and Replace

- Text editors support a global find and replace feature for editing multiple files at once.
- You can use regular expressions to perform more advanced replacements, such as adding an annotation to every function definition.
- Global find and replace can be powerful but dangerous, so use it with caution.

## ⚙️ Customization

- All good text editors are highly customizable.
- You can customize things like syntax highlighting themes, font sizes, and tab sizes.
- Most text editors have a package system to extend their functionality.

## 📝 Key Commands Summary

|Command|Description|
|---|---|
|`Select + ⌘/`|Toggle commenting out|
|`Select + tab`|Indent|
|`Select + ⇧tab`|Dedent|
|`^G`|Goto line number|
|`⌘W`|Close a tab|
|`$ echo $PATH`|Show the current path variable|
|`$ chmod +x <filename>`|Make executable|
|`$ unzip <filename>.zip`|Unzip a ZIP archive|
|`⌘P`|Fuzzy opening|
|`⌘1`, `⌘2`|Switch focus to tab #1, #2, etc.|
|`⇧⌘F`|Global find and replace|

## 🎯 Conclusion

This chapter has covered some of the most useful advanced features of modern text editors. These skills will allow you to be more productive when programming or working with text in general. You should apply your technical sophistication to customize the text editor to your liking. You can continue your journey by exploring further resources for your text editor.
