This chapter introduces **Git**, a powerful version control system (VCS) that is essential for modern software development. The chapter focuses on practical skills, teaching you how to use Git through the command line. This chapter is part of the "Learn Enough Git to Be Dangerous" tutorial, which itself is part of the larger "Learn Enough Developer Tools to Be Dangerous" series.

## 📦 What is Version Control?

- Version control systems (VCS) allow you to track changes to files and directories over time.
- They provide an automatic way to view previous versions of files, which allows for experimentation without disrupting the main project.
- VCS enables secure backups, collaboration, and easy restoration to previous states.
- Using a VCS is an essential component of **technical sophistication** for developers, designers, and project managers alike.
- The tutorial focuses on **Git** because it has emerged as the dominant open-source VCS.
- Git is a command-line program designed in the Unix tradition.

## 💻 Installation and Setup

### Checking Git Installation

- The most common way to use Git is via a command-line program called `git`.
- You can check if Git is installed by opening a terminal window and typing `which git`.
- If the result is empty or says the command is not found, you'll need to install Git manually.
- The tutorial strongly recommends using macOS or Linux.
- Windows users are encouraged to set up a Linux-compatible development environment.
- It is important to ensure that you have a sufficiently recent version of Git, which you can check with the command `git --version`. The version should be at least 2.28.0.
- You can upgrade Git using the instructions provided in the tutorial.
- For cloud IDE: `source <(curl -sL https://cdn.learnenough.com/upgrade_git)`
- For macOS: `brew upgrade git`

### Global Configuration

- After installing Git, you need to perform a few one-time global setups.
- These setups include your name and email address.
- The command `git config --global user.name "Your Name"` sets your name.
- The command `git config --global user.email your.email@example.com` sets your email.
- The command `git config --global init.defaultBranch main` sets the default branch name to `main`.
- It's important to note that the default branch name for the first 15+ years of Git’s existence was `master`, but the tutorial recommends using `main` as the default.
- Git stores global configuration settings in a hidden text file located in your home directory, `~/.gitconfig`.

## 🗂️ Initializing a Repository

- Git is used to track changes to files inside a **repository** (or repo for short).
- To create a new Git repository, you need to first create a directory.
- The command `mkdir -p repos/website` creates a directory called `website` inside a directory called `repos`.
- The command `cd repos/website` changes the directory to `repos/website`.
- To convert the directory into a Git repository, use the command `git init`.
- This command creates a hidden directory called `.git`, which stores the information Git needs to track your project's changes.
- All Git commands consist of the command-line program `git` followed by the name of the command.

## 📝 Our First Commit

- A **commit** represents a snapshot of your project at a given point in time.
- Git won't let you complete the initialization of the repository while it's empty, so you need to create at least one file to make a commit.
- To create an empty file, use the command `touch index.html`.
- The command `git status` shows the status of the repository.
- The command `git add -A` adds all untracked files to the **staging area**.
- The staging area is an intermediate step before changes are committed.
- After adding files to the staging area, you need to use the command `git commit` to commit the changes.
- Most uses of `git commit` use the `-m` option to include a **commit message**, indicating the purpose of the commit.
- The convention used in the tutorial is to write commit messages in the **present tense** using the **imperative mood**, as in "Initialize repository".
- The command `git commit -m "Initialize repository"` creates a commit with the message "Initialize repository".
- Each commit has a unique identifier called a **hash**, which lets Git retrieve the commit's changes.
- You can view a record of all your commits using the command `git log`.

## 📊 Viewing the Diff

- The command `git diff` shows the differences between the last commit and unstaged changes in the current project.
- By default, the `git diff` command shows the changes in a format that highlights the additions and subtractions.
- The command `git commit -a -m "Add content to index.html"` commits all changes to files that have already been added to the repository, along with the message "Add content to index.html".
- The command `git diff --staged` shows the difference between staged changes and the previous version of the repository.
- It's important to use `git add -A` to make sure new files are tracked properly.

## ✍️ Adding an HTML Tag

- You can use the `echo` command to add content to a file.
- The command `echo "hello, world" > index.html` adds the line "hello, world" to the file `index.html`.
- The command `git commit -am "Add an h1 tag"` combines the staging and commit steps into a single command.
- HTML uses **tags** to mark up text.
- Tags are made using angle brackets, where for example `<h1>` is an opening tag, and `</h1>` is a closing tag.
- The `h1` tag is a top-level (Level 1) heading.
- You can add a `p` tag for a paragraph of text.
- You can view the HTML file in a browser by double-clicking the file in a file explorer.
- The command `atom index.html` opens the `index.html` file in the Atom text editor.
- A properly formatted HTML page should include `<html>`, `<head>`, and `<body>` tags.
- It should also include a `<!DOCTYPE html>` declaration and a `<title>` tag within the `head` tag.
- The command `git diff` can be used to view the changes made to the `index.html` file.
- The command `git commit -am "Add some HTML structure"` adds the new HTML structure to the repository.
- The command `git log -p` displays the full diffs represented by each commit.

## 📝 Key Commands Summary

|Command|Description|
|---|---|
|`git help`|Get help on a command|
|`git config`|Configure Git|
|`mkdir -p`|Make intermediate directories as necessary|
|`git status`|Show the status of the repository|
|`touch <filename>`|Create an empty file|
|`git add -A`|Add all files/directories to staging area|
|`git add <filename>`|Add a file to the staging area|
|`git commit -m <message>`|Commit staged changes with a message|
|`git commit -am <message>`|Stage and commit changes with a message|
|`git diff`|Show diffs between commits, branches, etc.|
|`git commit --amend`|Amend the last commit|
|`git show <SHA>`|Show diff vs. the SHA|

## 🎯 Conclusion

This chapter has covered the basics of getting started with Git, including installation, setup, initializing a repository, making commits, and viewing diffs. This knowledge will help you track changes in your projects and allow you to collaborate with other developers.