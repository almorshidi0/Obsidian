This chapter builds on the basic workflow introduced in the previous sections to add more complex tools and techniques, focusing on adding images, ignoring files, branching, merging, and recovering from errors. It emphasizes practical techniques used by software developers using Git.

## 🖼️ Adding an Image

- The first step is to make a new directory, called `images`, using the command `mkdir images`.
- Next, download an image using the command `curl -o images/breaching_whale.jpg -L https://cdn.learnenough.com/breaching_whale.jpg`.
- To include the image in your website, use the `img` tag, which is a **void element** or **self-closing tag**.
- The `img` tag uses the `src` attribute to specify the image source, and the `alt` attribute to give a description of the image.
- The image path `images/breaching_whale.jpg` should appear in the `index.html` file.
- After adding the `img` tag to your `index.html`, the image should appear when you refresh the browser.
- Use `git diff` to confirm the changes are ready to go.
- Use `git status` to see that the images directory is untracked.
- Use `git add -A` to add the untracked directory and image file.
- You can commit and push the changes as usual with `git commit -m "Add an image"` and `git push`.
- Confirm the new image directory and file on GitHub.

## 🔕 Ignoring Files

- A common issue when working with Git is dealing with files that you don't want to include in your repository.
- These include files containing secret credentials, configuration files, temporary files, log files, etc.
- For example, macOS creates a hidden file called `.DS_Store`.
- To ignore such files, you can use a special configuration file called `.gitignore`.
- Create a file called `.gitignore` using your text editor, and add the names of the files you want to ignore, for example, `.unwanted_DS_Store`.
- You can also use wildcards, such as `*` to represent anything.
- For example, `*~` will ignore all files ending with a tilde, such as temporary Vim files, and `tmp/` will ignore all files in the `tmp` directory.
- Many systems generate a starting `.gitignore` file for you.
- Use `git status` to see the effect of `.gitignore`.
- Commit the `.gitignore` file and push the changes to GitHub.

## 🌿 Branching and Merging

- Git allows you to make branches, which are effectively complete copies of the project source.
- You can use branches to make changes in isolation, and then merge those changes into the original branch.
- Create a new branch called `about-page` using `git checkout -b about-page`.
- The prompt will change to show the name of the current branch.
- Use the command `git branch` to view the current branches on the local machine.
- The asterisk indicates the currently checked-out branch.
- To make a new page called `about.html`, you can copy the contents of the `index.html` file using the command `cp index.html about.html`.
- Open `about.html` in your editor and make the necessary changes.
- The `about.html` file includes two new tags: `<strong>` which renders as boldface, and `<em>` which renders as italicized text.
- Commit the changes using `git add -A && git commit -m "Add About page"`.
- The `about-page` branch has now diverged from `main`.
- Before merging the `about-page` branch back into the `main` branch, add a link to the About page to the `index.html` file.
- Use the anchor tag `<a>` to create the link, which contains both the content ("About this project") and a _hypertext reference_, or `href` (which is `about.html` in this case).
- You can use `git diff` to see the difference between the two branches. The command `git diff main` shows the difference between the current branch (`about-page`) and the `main` branch.
- To incorporate the changes on `about-page` into `main`, checkout the `main` branch using `git checkout main`.
- Next, use the command `git merge about-page`.
- In this case, the `main` branch didn't change while working on the `about-page` branch, so Git can automatically merge the changes.
- You can sync the local `main` branch with GitHub using `git push`.
- You can also delete the `about-page` branch using `git branch -d about-page`.
- The most common way to combine branches is using `git merge`, but another method called `git rebase` is also available. It is recommended to only use `git rebase` when working on a team where an advanced Git user tells you to.

## ⛑️ Recovering from Errors

- Git has features that allow you to recover from errors.
- For example, if you accidentally overwrite a file, you can use `git checkout -f` to revert to the most recent commit, also called `HEAD`.
- The command `git reset --hard HEAD` is equivalent, but `git checkout -f` is easier to remember.
- Another way to recover from errors is by using branches, because changes made on one branch are isolated from other branches.
- You can also use `git log` to see the history of commits and checkout an earlier version of the repository.
- To go to the last line of the log, type `G` when using the `less` interface.
- To check out a specific commit, copy the commit's SHA and use the command `git checkout <SHA>`.
- If you want to create a new branch with that commit, use `git checkout -b new_branch_name`.
- After inspecting the state of the project, you can check out the `main` branch again with `git checkout main`.
- The `git checkout -f` trick only works with files that are staged or already part of the repository, but you can get rid of new files using `touch`, `git add`, and `git checkout -f`.
- Git accepts both "short form" and "long form" options, so `-f` is equivalent to `--force`.

## ⌨️ Key Commands Summary

|Command|Description|Example|
|---|---|---|
|`.gitignore`|Tell Git which things to ignore|`$ echo .DS_Store >> .gitignore`|
|`git checkout <br>`|Check out a branch|`git checkout main`|
|`git checkout -b <br>`|Check out and create a branch|`git checkout -b about-page`|
|`git branch`|Display local branches|`git branch`|
|`git merge <br>`|Merge in a branch|`git merge about-page`|
|`git rebase`|Do something possibly weird and confusing|See "Git Commit" ([https://m.xkcd.com/1296/](https://m.xkcd.com/1296/))|
|`git branch -d <br>`|Delete branch (if merged)|`git branch -d about-page`|
|`git branch -D <br>`|Delete branch (even if un-merged) (dangerous)|`git branch -D other-branch`|
|`git checkout -f`|Force checkout, discarding changes (dangerous)|`git add -A && git checkout -f`|

## ✅ Conclusion

This chapter has covered more advanced Git workflows, including how to add images, ignore files, create and merge branches, and recover from errors. It has introduced concepts that will be valuable for both solo work and collaboration with other developers.