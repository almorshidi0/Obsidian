This chapter introduces text editors as essential tools for anyone working with computers. Unlike word processors, text editors are designed to work with plain text, which is ubiquitous in modern computing. The chapter emphasizes the importance of understanding text editors as a category and introduces the basic principles of using them, specifically focusing on the Vim editor. It also touches on modern editors like Atom, Sublime Text, Visual Studio Code, and Cloud9. This chapter equips you with the skills to use a text editor to modify plain text, which is essential for coding, configuration files, and more. It is a core skill for anyone aiming for technical sophistication.

**Core Concepts**:

*   **Plain Text**: Understanding the concept of plain text and how it differs from formatted text produced by word processors.
*   **Text Editor**: The general category of application used to edit plain text.
*   **Technical Sophistication**: Developing the general ability to use computers and acquire new technical knowledge.
*   **Modal Editing**: Understanding the concept of modal editing in Vim, which separates normal mode and insertion mode.
*   **Minimum Viable Vim**: Learning just enough Vim to perform basic edits.
*   **Command Line**: Integrating text editing with the command line.

#### 5.1 Introduction to Text Editors 💻

*   A text editor is a crucial tool for technical work.
*   Unlike word processors, text editors work with plain text, which is used for code, markup, and configuration files.
*   Plain text has no formatting, only content.
*   Word processors use "What You See Is What You Get" (WYSIWYG) and save files in proprietary formats. Text editors save files in a universal and durable format.
*   Text editors have features for technical users, including syntax highlighting and regular expressions.
*   The chapter focuses on general principles of text editors and introduces the Vim editor, before moving to more modern editors.
*   Even if you use an IDE, the lessons in this tutorial still apply.
*   The tutorial emphasizes technical sophistication, including the ability to use help menus, learn keyboard shortcuts, and tolerate ambiguity.

#### 5.2 Minimum Viable Vim ⌨️

*   **Vim** is a powerful text editor that can be run in the terminal window.
*   Vim is ubiquitous in Unix-like systems.
*   Vim is a **modal editor**, having a normal mode for moving around and editing text and an insertion mode for entering text.
*   Vim starts in normal mode.
*   The **Most Important Vim Command™** is `ESC:q!` which quits Vim without saving any changes.
*   The command means pressing the `Escape` key, then typing `:q!` and then pressing the `return` key.
*   The `ESC` key is used to exit insertion mode and enter normal mode.

#### 5.3 Editing Small Files 📄

*   To start Vim with a file, you can use `vim filename`.
*   Vim can create a file if it doesn't exist.
*   The `i` key switches to insertion mode.
*   The `ESC` key switches back to normal mode.
*   The arrow keys can be used for basic navigation within the file.
*   The `0` key moves to the beginning of the line.
*   The `$` key moves to the end of the line.

#### 5.4 Saving and Quitting Files 💾

*   The command `:q` quits Vim, but only if there are no changes to save.
*   The command `:q!` force quits Vim without saving changes.
*   The command `:w` saves the file.
*   The command `:wq` saves and quits the file.
*   The `u` key undoes previous steps.
*   An alias is a synonym for a command or set of commands.
*   Aliases are added to `.bashrc` (or `.zshrc`) to create shortcuts.
*   The `source .bashrc` command activates the changes in the `.bashrc` file.
*   The `.bashrc` file is automatically sourced when a new terminal tab or window is opened.

#### 5.5 Deleting Content 🗑️

*   The `x` key deletes the character under the cursor.
*   The `dd` key deletes the current line.
*   The `p` key "puts" or pastes deleted text.

#### 5.6 Editing Large Files 📚

*   The **Ctrl-F** command moves forward one screen.
*   The **Ctrl-B** command moves backward one screen.
*   The **G** command moves to the end of the file.
*  The **1G** command moves to the beginning of the file.
*  The **`/`** command followed by a search string and return initiates a search.
*  The **`n`** key moves to the next search result.
*   This navigation is similar to the `less` program.

#### 5.7 Summary 📒

*   **Important Vim Commands:**
    *   `ESC:q!` - The Most Important Vim Command™.
    *   `i` - Enter insertion mode.
    *   `ESC` - Exit insertion mode.
    *   Arrow keys - Move around.
    *   `0` - Go to the beginning of the line.
    *   `$` - Go to the end of the line.
    *   `:w` - Save (write) a file.
    *   `:q` - Quit a file (must be saved).
    *   `:wq` - Write and quit a file.
    *   `:q!` - Force-quit a file, discarding any changes.
    *   `u` - Undo.
    *   `x` - Delete the character under the cursor.
    *   `dd` - Delete a line.
    *   `p` - Put (paste) deleted text.
    *   `Ctrl-F` - Go forward one screen.
    *   `Ctrl-B` - Go backward one screen.
    *   `G` - Go to the last line.
     *   `1G` - Go to the first line.
    *   `/` - Search for a string.
    *  `n` - Go to the next match in search.
*   Technical sophistication includes using help menus, learning keyboard shortcuts, and tolerating ambiguity.

**Key Takeaway:**

This chapter introduces the basic principles of using a text editor, particularly focusing on Vim. You've learned how to navigate, edit, save, and quit files using Vim. You also learned the difference between plain text and formatted text, and the importance of text editors for technical tasks. By understanding modal editing in Vim and learning the essential commands, you've gained the fundamental knowledge needed to use any text editor effectively. You have also expanded your technical sophistication. 🚀 You are now ready to use text editors for various technical tasks. 🧙‍♂️
