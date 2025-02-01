This chapter focuses on collaborating with Git, especially using platforms like **GitHub**, Bitbucket, or private servers. It covers scenarios with multiple collaborators having commit rights and explores different workflows, including forking and pull requests.

## 🧑‍🤝‍🧑 Setting Up Collaboration

- **Invite collaborators** to a repository via the settings page on GitHub.
- Collaborators receive a notification and can **clone the repository** using the provided URL.
    - `git clone <URL>` copies the repository, including its history.
- For the tutorial, the text editors for the original website and the cloned copy should be side by side.

## ✍️ Making and Merging Changes

- A collaborator (Bob) can make changes to the website.
- Use `git diff` to see changes, like a wrapped line of text.
- Bob commits and pushes changes using:
    - `git commit -am "Add link to tutorial title"`
    - `git push`
- The original owner (Alice) can then get the changes by running `git pull`.
    - This command retrieves changes from the remote repository and merges them into the local branch.
- Alice's local copy is then identical to Bob's commit.
- Use `git log` and `git log -p` to verify the changes.

## 🚧 Handling Non-Conflicting Changes

- When collaborators edit different parts of the same file, Git can merge the changes automatically.
    - For example, Alice changes a heading while Bob adds an image.
- Bob downloads an image using `curl`:
    - `curl -o images/polar_bear.jpg -L https://cdn.learnenough.com/polar_bear.jpg`.
- Bob adds the image to the page using the `<img>` tag.
- Bob's changes are committed and pushed.
- Alice then runs `git pull`. Git automatically merges her change and Bob's change.
    - The default editor, Vim, may appear to complete the merge.
- Use `git log` to verify the merge commit.
- Alice can also verify the changes in her browser.

## 💥 Resolving Conflicting Changes

- Conflicts occur when collaborators edit the same lines of the same file.
- For example, Alice and Bob both add an `alt` attribute to an image.
- Alice commits and pushes her change first.
- When Bob tries to push, GitHub rejects it, and Bob must `pull`.
- After pulling, the file shows a **merge conflict**, marked by `<<<<<<<`, `=======`, and `>>>>>>>`.
- To resolve the conflict, Bob must manually edit the file, removing the conflict markers and making sure the correct code is there.
- Bob then saves the file, commits the merge and pushes again.

## 📌 Pushing Branches

- Collaboration can also occur on branches other than `main`.
- Alice creates a `fix-trademark` branch to address a bug.
    - `git checkout -b fix-trademark`.
- She adds HTML comments to the files as placeholders for the fix.
- Alice commits and pushes the branch:
    - `git commit -am "Add placeholders for the TM fix"`.
    - `git push -u origin fix-trademark`.
- Bob can pull the new branch.
- Bob checks out the new branch and can use `git diff main` to see what's changed.
- Bob adds the necessary `<meta charset="utf-8">` tag to address the trademark bug.
- Bob commits and pushes the fix.
- Bob merges the fix into `main`:
    - `git checkout main`.
    - `git merge fix-trademark`.
    - `git push`.

## 🚀 GitHub Pages

- **GitHub Pages** allows hosting static websites directly from a GitHub repository.
- Enable GitHub Pages in the repository settings.
- Configure it to use the `main` branch.
- The website will be available at `https://<username>.github.io/<repository>`.
- `index.html` is the default page, and other pages can be accessed by adding the filename.
- GitHub Pages caches static HTML pages for fast loading.

## 🔑 Important Commands

|Command|Description|Example|
|---|---|---|
|`git clone <URL>`|Copy a repo (including full history) to the local disk|`git clone https://ex.co/repo.git`|
|`git pull`|Pull in changes from the remote repository|`git pull`|
|`git branch -a`|List all branches|`git branch -a`|
|`git checkout <br>`|Check out a remote branch and configure for|`git checkout fix-trademark`|

## ⚙️ Advanced Setup

- Create an alias for `git checkout`: `git config --global alias.co checkout`.
    - Now you can use `git co main` instead of `git checkout main`.
- Customize the command-line prompt to include the current branch.
- Add tab completion for branch names.
- Download the scripts, make them executable, and configure your `~/.bashrc` file:
    - `curl -o ~/.git-prompt.sh -L https://cdn.learnenough.com/git-prompt.sh`
    - `curl -o ~/.git-completion.bash -L https://cdn.learnenough.com/git-completion.bash`
    - `chmod +x ~/.git-prompt.sh ~/.git-completion.bash`
- After editing `.bashrc`, you must `source ~/.bashrc` to apply the changes.

## ✅ Conclusion

This chapter covered key aspects of collaborating with Git, including inviting collaborators, managing branches, resolving merge conflicts, and using GitHub Pages. These skills are crucial for working effectively in teams and deploying websites.. The chapter also introduces more advanced setup options like aliases and prompt customizations.