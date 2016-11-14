# Git Reference Notes

## Add, commit, push a file

### 1. See what’s changed since the last commit
`git status` shows files that have changed or are untracked  
`git diff [optional: filename]` shows the changes themselves

### 2. “Stage” the things you want to include in your commit
This includes both files that have changed and new files you want to add.

`git add <file or directory>`

### 3. Commit your changes and add a useful message

`git commit -m ‘message goes here’`

### 4. Push to the origin repo
syntax:  `git push <remote> <branch>`  
`git push origin master`

### Adding, committing a file
>my example 
```
$ git status
$ git add test.txt                     # sets working copy to staged copy
$ git status
$ git commit -m "add a simple file"    # staged copy to revision history
$ git push origin master               # send it to (my forked) repo (branch = master)
```

--

## Git commands (deleting & copying files with Git)

###Important:  To Remove a File from the Repo
`$ git rm filename`  

###Important:  To Rename or Move a File in the Repo
`$ git mv filename` 

###List of Git commands
`$ git`

###Git log
`$ git log`
