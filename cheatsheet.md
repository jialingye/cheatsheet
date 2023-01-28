# Set Up

- Set the name and email that will be attached to your commits and tags
```
git config --global user.name "Danny Adams"
git config --global user.email "my-email@gmail.com"
```
# Start a Project
- Create a local repo (omit<directory> to initialise the current directory as a git repo)
`git init <directory>`
- Download a remote repo
`git clone <url>`

# Make a Change

- Add a file to staging
` git add <file> `
- Stage all files
` git add . `
- Commit all staged files to git
` git commit -m "commit message"`
- Add all changes made to tracked files & commit
` git commit -am "commit message"`

# Basic Concepts

+ **main:** default development
+ **origin:** default upstream repo
+ **HEAD:** current branch
+ **HEAD^:** parent of HEAD
+ **HEAD~4:** great great parent of HEAD

# Branches

- list all local branches.  `git branch`
- show all remote branches  `git branch -r`
- show all branches `git branch -a`
- create a new branch `git branch <new-branch>`
- switch to a branch & update the working directory **`git checkout <branch>`**
- add a tag to current commit `git tag <tag-name>`
* delete a merged branch `git branch -d <branch>`
+ delete a branch, whether merged or not `git branch -D <branch>`

# Merging

-merge branch A into branch B. Add no-ff option for no-fast-forward merge
```
git checkout b
git merge a
```
-merge & squash all commits into one new commit
```
git merge --squash a
```
# Rebasing

- rebase feature branch onto main (to incorporate new changes made to main). Prevents unnecessary merge commits into feature, keeping history clean
```
git checkout feature
git rebase main
```
- interatively clean up a branches commits before rebasing onto main
```
git rebase -i main
```

# Review your Repo

- list new or modified files not yet committed `git status`
- list commit history, with respective IDs `git log --oneline`
- show changes to unstaged files. For changes to staged file, add --cached `git diff`

# Synchronizing

- add a remote repo `git remote add <alias> <url>`
- fetch the remote repo's copy of the current branch, then merge `git pull`
- upload local content to remote repo `git push <alias>`
- fetch a specific branch `git fetch <alias> <branch>`

# Undoing

- move (&/or rename) a file & stage move `git mv <existing_path> <new_path>`
- remove a file from working directory & stageing area, then stage the remove `git rm <file>`
- view a previous commit (READ Only) `git checkout <commit_ID>`
- creat a new commit, reverting the changes from a specified commit `git revert <commit_ID>`
- go back to previous commit & delete all commits ahead of it `git reset <commit_ID>`


