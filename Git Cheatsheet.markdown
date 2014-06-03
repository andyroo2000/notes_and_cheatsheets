# Git Workflows

This is a personal list of Git tasks that I commonly perform.

These are broken down by situations that commonly occur, rather than a list of commands and what they do.



# Cloning a GitHub repository

- Find the repo on GitHub

- Copy the **HTTPS clone URL** (located near the bottom right of the web page for the repo)

In this case, I will use my [notes_and_cheatsheets](https://github.com/andyroo2000/notes_and_cheatsheets) repo as an example:

`git clone https://github.com/andyroo2000/notes_and_cheatsheets.git`

The git repo will now be created in your current directory.

To only clone the contents and not the containing folder add a space and a `.` at the end, like so:

`git clone https://github.com/andyroo2000/notes_and_cheatsheets.git .`





## Rebase my branch, because changes have been made to **master**

In this case, I'm working on a feature branch and the **master** branch has changed. Those changes need to be be added to my branch before I can merge it back onto **master**. This can happen when you start several features and merge one of them into **master**. The remaining feature branches will need to **rebase** before being merged into **master**.

While my feature branch is checked out...

`git rebase master`



## Rebase my branch (including my local copy of master) because changes have been made to master on GitHub

In this case, someone has pushed changes to GitHub (aka origin master) and I need to add those changes to my local working copy before I can push to **master**. And before you can do that, you need to fetch the most recent copy of **master** from GitHub.

`git fetch origin`

`git rebase origin/master`



## Trash my local changes

In this case, I've made a bunch of changes to my working copy... whether it's a branch or **master** and things are screwed up and I just want to revert to the last commit.

`git reset --hard`

However, I may have added files since my last commit and I not only want to revert changes to my files, but also delete the files and directories I added since the last commit.

`git clean -f -d`



## Feature Branch Workflow (local only)

I would recommend doing all work on a feature branch. This way, if what you are working on temporarily makes things function incorrectly and you need to bang out some other feature quickly and push it to GitHub, you can just switch branches, complete that feature, push to GitHub and then switch back to your complicated feature.

- Create and switch to a new branch

`git branch myNewBranchName`

- Work on your feature

`git add .`

`git commit -am "your commit message"`

- When you feature is 100% complete

`git checkout master`

`git merge myNewBranchName`

`git push`

`git branch -d myNewBranchName`




## Feature Branch Workflow (using GitHub collaboratively)

- Create and switch to a new branch

`git branch myNewBranchName`

- Work on your feature

`git add .`

`git commit -am "your commit message"`

`git push origin -u myNewBranchName`

- Code can be reviewed on GitHub website by someone else

- Make suggested changes to the code on your branch

`git push`

- If code is acceptable it can be merged onto master by you or a coworker on the GitHub website (point-and-click style).

- Delete your local branch (which has been merged into Master)

`git branch -d myNewBranchName`

- Delete your remote branch on GitHub (point-and-click style).






## Add files to staging, commit, and push to GitHub (whether you're on a branch or not)

- Add files in the current directory to the **staging** area

`git add .`

- Commit and create a **commit message**

`git commit -am "my message describing what is being done - Fixes #24"

The last part, `Fixes #24` is not required. However, if you use the **Issues** feature on GitHub and you use the **Issue** number in your commit message, the code you commit will be automatically linked to the **Issue** on GitHub. And if you use the word `Fixes` before the **Issue** number it will automatically close the **issue** in Github when it's merged with `origin/master`.

- Push your **commit** to GitHub

`git push`













# General Git Commands


* `git status` - shows the status of files (whether there have been changes to files since the last commit, etc.)

* `git reset` - upstage all files you might have staged with `git add`
* `git checkout .` - revert all local uncommitted changes (should be executed in repo root)
* `git clean -fdx` - remove all local untracked files, so only git tracked files remain
* `git add -u` - stage files that have changed without adding new files to staging area


* `git branch -a` - shows remote and local branches
* `git fetch origin` - fetches remote branches so that you can check them out locally

* `git checkout -b nameOfBranch` - checkout and switch to new branch



## Commands for navigating git-diff

* Next line:  `return`
* Next page:  `space bar`
* Previous page:  `w`
* Quit viewing the diff:  `q`
* Help:  `h`



# General things to be aware of

If you want to switch branches, you have to commit an changes on your current files first... Actually there is a way to **stash** your changes, switch branches, switch back, and apply your stashed changes... If you're interested in doing that, you can hit up Google and add to this little Git cheatsheet.

If you're using Sublime Text as your text editor, there is an excellent plugin called [SublimeGit](https://sublimegit.net), which makes many tasks in Git much quicker and simpler. This is a tremendous time-saver if you interact with Git a lot and I use it constantly.

There are also various GUIs for Git, but I'm not too crazy about any of them. For me, the hardest part about git isn't learning (or Googling) the relevant commands, but understanding how Git works... And with a GUI, you end up having to learn Git, while also learning how to use the GUI... Also, most of the help online via [Stack Overflow](http://stackoverflow.com/questions/tagged/git) is geared toward the command-line interface and it can be tricky to translate command-line advice to whatever GUI application you may be using. 

## Andrew's edits

Here are some edits made my Andrew
