This chapter focuses on using **GitHub** to back up your project and collaborate with others using **remote repositories**. The chapter builds on the previous chapter by teaching how to push local Git repositories to GitHub.

## 🤝 Why use Remote Repositories?

- A remote repository, such as on **GitHub**, serves as a backup of your project and its history.
- It also makes it easier for collaborators to work with you on your project.
- Using a platform like GitHub allows you to build up a portfolio, which can be a great way to show off your work.
- In the context of this tutorial, using a public repo is an efficient way to demonstrate the principles being taught.
- It's also useful to backup your data on a remote repository for security.

## 📝 Signing Up for GitHub

- To get started, you need a **GitHub account**.
- You can sign up at [github.com/join](https://github.com/join).
- The signup page is shown in **Figure 9.1**.
- Use your technical sophistication skills if you encounter any issues during the sign up process.

## ☁️ Creating a Remote Repo

- After signing up, you need to create a **remote repository**.
- Start by selecting the menu item for adding a new repository, as shown in **Figure 9.2**.
- Fill in the repository name and description. For this tutorial, name the repository `website` and use the description "A sample website for Learn Enough Git to Be Dangerous".
- The GitHub interface is actively developed, so the screenshots in the book may not match your results, but this should not be a problem.
- **Figure 9.3** shows the screen for creating a new repository.

## ⬆️ Pushing to GitHub

- After creating the repository, GitHub will display instructions for how to **push** your local repository to GitHub.
- Make sure you select the **HTTPS** option.
- **Figure 9.4** shows the instructions for pushing up to GitHub.
- The exact commands will be tailored to your account name and default branch name.
- The first command sets up GitHub as the `remote origin`.
- The second command ensures that the default branch is named `main`.
- The third command arranges to **push** the full repository to GitHub. The `-u` option sets GitHub as the `upstream repository`, which will allow you to download any changes automatically.
- The command `git remote add origin https://github.com/<name>/website.git` adds a remote repository called `origin` to your git configuration.
- The command `git push -u origin main` pushes the commits in your local `main` branch to the remote `origin`.
- You will be prompted to enter your GitHub username and **personal access token**.
- The username is your GitHub username, but the password is not your GitHub password.
- Instead, you must create a personal access token by following the instructions in the GitHub article "Creating a personal access token".
- It's suggested that you select "No expiration" for the token, and make sure to select "repo" as the scope of the token.
- After creating the token, copy and paste it in the command line when prompted.
- It is possible to configure your system to remember your GitHub credentials, so you don't have to enter your personal access token every time you push changes to the remote repository.

## 🔄 Refresh and View

- After executing the first `git push` you should reload the current page.
- The page should look like **Figure 9.6**, if so, you have successfully shipped your first Git repository.

## 📝 Adding a README file

- Now that your repository is on Github, you can add a README file.
- You cannot use `git commit -am` because the README file isn't yet in your repository.
- First, add the file to the staging area with `git add -A`.
- Then, commit the file with the command `git commit -m "Add README file"`.
- You can use the command `git add README.md`, but the tutorial recommends the habit of using `git add -A` unless there is a reason not to.
- Now you can push the new README to the remote repository with `git push`.
- GitHub uses the `.md` extension to identify the file as **Markdown**.
- It is then converted to HTML for easy viewing, as shown in **Figure 9.12**.
- The `#` symbol in **Listing 9.2** is converted into a top level heading and the Markdown link format `[content](address)` is converted into an HTML anchor tag `<a>`.

## ⚙️ Using Markdown

- The text editor, **Atom**, has a built-in Markdown previewer.
- You can preview the markdown with the Packages menu shown in **Figure 9.10**.
- The preview window is shown in **Figure 9.11**.
- If you get an error message, try running the "Toggle Preview" keyboard shortcut a few times.

## ⌨️ Key Commands Summary

|Command|Description|Example|
|---|---|---|
|`git remote add`|Add remote repo|`git remote add origin https://github.com/...`|
|`git push -u <loc> <br>`|Push branch to remote|`git push -u origin main`|
|`git push`|Push to default remote|`git push`|

## ✅ Conclusion

This chapter has covered the basics of backing up and sharing your code using GitHub. It has shown you how to create a remote repository and push your local repository to GitHub. You've also learned how to add a README file using Markdown and view it in the browser.