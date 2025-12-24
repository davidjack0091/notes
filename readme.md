# version control

## git/github

linux commands

`this is` 

**git** - version control system. track changes in code.
**git bash** - cli for windows that provides a unix like environment to use git and run linux commands.
**commit** - saved change with a message.
**version history** - list of all commits.
**head** - points to current branch or commit.

github - platform for hosting and collaborating git repositories.
fork - you make copy of someone else's repository on github.
pull request - ask to merge your changes into someone else's repository on github.
without ssh - when you push for the first time - github asks to authenticate - it redirects you to browser to verify github account - after verification git stores a credential/token in your pc so that next pushes don't ask again to authenticate.
ssh - after setting up ssh - you can push without redirecting to browser to authenticate.

1. configure git
```bash
# set a config option globally
git config --global user.name 'Your Name' # set name for all repo
git config --global user.email 'youremail@example.com' # set email for all repo
git config --global init.defaultBranch main # main will be default branch whenever you init
```
2. getting started

```bash
git init # create a new local repo
git clone [url] # clone an existing remote repo
```
3. add a remote
```bash
git remote add origin [url] # connect local repo to remote repo
```
4. prepare to commit
```bash
git add [file]  # stage file
git add .  # stage all files
git rm [file] # remove file from repo and pc
git rm --cached [file] # remove file from repo but keep it in pc
git reset [file] # unstage file
git reset # unstage all files
git status # show what is staged/unstaged/untracked
```
5. make commits
```bash
git commit -m 'message' # commit staged changes
```
code archaeology
git log [file] # all commit of file
git log # commit history

move between branches
git switch [branch] # switch branch
git checkout [branch] # same
git switch -c [branch] # create and switch branch
git checkout -b [branch] # same
git branch # list branches
git branch -m [branch] # rename branch
git branch -d [branch] # delete branch
git branch -D [branch] # force delete branch
git merge [branch] # merge branch

discard your changes
git restore [file] # remove unstaged changes in file
git checkout [file] # same
git restore --staged --worktree [file] # remove staged and unstaged changes in file
or git checkout HEAD [file]
git reset --hard # delete all staged and unstaged changes

restore an old file
git checkout [commit] [file] # restore file from a commit
git restore [file] --source [commit] # same

push your changes
git push -u origin [branch] # push branch that never pushed before
git push origin [branch] # push branch
git push # push current branch

pull changes
git fetch origin [branch] # fetch changes but don't merge
git pull origin [branch] # fetch changes and then merge
git pull # fetch changes and then merge into current branch

important files
.gitignore




