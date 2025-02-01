
## 🗄️ Setting up Git 🐙

- **Git** is a popular version control system.
- **GitHub** is a service for hosting and managing your code using Git.
- Git and GitHub are not the same.
- You will install Git, configure it, and create a GitHub account.

### Steps to setup Git:

*   Install Git for your OS.
*   Create a GitHub account and enable private email settings.
*   Setup Git using the `git config` command with your name and email (private email address from GitHub if you choose to keep your email private).
*   Set the default branch to main using `git config --global init.defaultBranch main`.
*   Set the default branch reconciliation behavior to merging using `git config --global pull.rebase false`.
*   Verify that things are working properly by entering `git config --get user.name` and `git config --get user.email`.
*   For macOS users, ignore `.DS_Store` files.
*   Create an **SSH key** which is a cryptographically secure identifier that allows you to upload code to your repository without entering your password each time.
    *   Check if you have an Ed25519 algorithm SSH key using `ls ~/.ssh/id_ed25519.pub`.
    *   If not, create one using `ssh-keygen -t ed25519`.
*   Link your SSH key with GitHub by navigating to Settings > SSH and GPG keys > New SSH Key.
*   Copy your public SSH key using `cat ~/.ssh/id_ed25519.pub` and paste it into GitHub.
*   Test your key by following the directions provided by GitHub.

- Once you've completed the installations, you should let The Odin Project know how it went.
- The module acknowledges that you may not understand much of what you are doing, and that it is normal.
- Additional resources include explanations of SSH key pairs and Asymmetric Encryption.

## 📜 Introduction to Git 💾

- **Git is a version control system** that acts like an "epic save button" for your files and directories.
- Unlike a text editor that only saves a single record of a file, **Git records differences in files and folders** and keeps a historical record of each save.
- Git enables you to:
    - Review how your project grows.
    - Easily look at or restore file states from the past.
- Once connected to a network, Git allows you to push your project to **GitHub** (or alternatives) for sharing and collaborating with other developers.
- The Odin Project **only supports GitHub**.
- **GitHub** is a remote storage facility on the web for all your coding projects.
- Learning Git allows you to showcase your portfolio on GitHub, an **essential skill for modern web developers**.
- This module covers:
    - The history of Git.
    - What Git is and its uses.
    - The basic workflow for using Git.
    - Setting up a project with Git as a template for future projects.

### Key Concepts

- **Git** is a version control system.
- **GitHub** is a service that allows you to upload, host, and manage your code using Git with a web interface.
- **Git works on your local machine**.
- **GitHub is a remote storage facility** on the web.

### Assignment

- Read chapters 1.1 through 1.4 from the Getting Started section of Pro Git to learn the differences between local, centralized, and distributed version control systems.
- Watch “What is Git?” explained in 2 minutes.
- Read “About GitHub and Git” for a brief introduction of what GitHub is and how Git and GitHub work together.
- Visit the Setting Up Git lesson if you have not installed Git.
- Look at The Odin Project's GitHub repository to see how Git records all collaborative efforts.

### Knowledge Check

- What kind of program is Git?
- What are the differences between Git and a text editor in terms of what they save and their record keeping?
- Does Git work at a local or remote level?
- Does GitHub work at a local or remote level?
- Why is Git useful for developers?
- Why are Git and GitHub useful for a team of developers?

## ⚙️ Basic Git Workflow 🚀

- This section covers common Git commands to manage projects and upload work onto GitHub.
- These commands are used about 70-80% of the time when using Git.

### Setting up a Repository

- Ensure you have a recent version of Git (2.28 or later) by running `git --version`.
- Set your local default Git branch to main by running `git config --global init.defaultBranch main`.
- Create a new repository on GitHub by clicking the "+" button and selecting "New repository".
- Name your repository "git_test" and check "Add a README file".
- Copy the SSH clone URL by clicking the green "Code" button, selecting the SSH option.
- Create a directory called "repos" in your home folder with `mkdir repos` and move into it with `cd repos/`.
- Clone your repository from GitHub with `git clone git@github.com:USER-NAME/REPOSITORY-NAME.git`.
- Verify that you have connected to the repository by navigating into the new git_test folder, and typing `git remote -v`.

### Using the Git Workflow

- Create a new file called "hello_world.txt" with the command `touch hello_world.txt`.
- Check the status of your repository with `git status`; the new file will be shown in red as an "Untracked file".
- Add the file to the staging area with `git add hello_world.txt`; it will now be shown in green.
- Commit your changes with `git commit -m "Add hello_world.txt"`.
- View the commit history with `git log`.
- Modify the README.md file by adding "Hello Odin!" on a new line and saving it.
- Use `git status` to see the modified file which is listed in a section titled "Changes not staged for commit".
- Add the modified file to the staging area with `git add README.md`.
- Open and modify `hello_world.txt`, then stage all files with `git add .`.
- Commit all staged files with `git commit -m "Edit README.md and hello_world.txt"`.

### Pushing to GitHub

- Push your work to GitHub with `git push` or `git push origin main`.
- If you receive an error message about password authentication, you have incorrectly cloned with HTTPS instead of SSH.
- Verify your changes are pushed with `git status`. The output should say "Your branch is up to date with 'origin/main'. nothing to commit, working tree clean".
- Refresh your repository page on GitHub to see the changes you pushed.
- Avoid editing directly on GitHub, make changes to local files and push them.

### Git Commands Cheatsheet 📝

- **Remote Repository Commands**:
    - `git clone git@github.com:USER-NAME/REPOSITORY-NAME.git`
    - `git push` or `git push origin main`
- **Workflow Commands**:
    - `git add .`
    - `git commit -m "A message describing what you have done to make this snapshot different"`
- **Status and Log Commands**:
    - `git status`
    - `git log`
- Git syntax is `program | action | destination`.

### Git Best Practices 🏆

- Use **atomic commits**: commits that include changes related to only one feature or task of your program.
    - Makes it easy to revert a specific change without losing other changes.
    - Enables you to write better commit messages.
- Change the default message editor by typing the command `git config --global core.editor "code --wait"` to be able to write commit messages in Visual Studio Code.
    - To make a commit with VS Code, use `git commit`.

### Knowledge Check

- How do you create a new repository on GitHub?
- How do you copy a repository onto your local machine from GitHub?
- What is the default name of your remote connection?
- Explain what origin is in `git push origin main`.
- Explain what main is in `git push origin main`.
- Explain the two-stage system that Git uses to save files.
- How do you check the status of your current repository?
- How do you add files to the staging area in Git?
- How do you commit the files in the staging area and add a descriptive message?
- How do you push your changes to your repository on GitHub?
- How do you look at the history of your previous commits?
