# Git:  Add, Commit a File & Pull Request

--

## Sync repos (pull from the origin repo)
**Always do this before sending up any changes:**  
`git pull upstream master`

If any other changes were made since you last pulled, this will attempt to merge them with yours. If you don’t do this and you need to, the remote repo will tell you.

>my example

```
$ pwd
/Users/reshamashaikh/_ds/metis/metisgh/nyc16_ds9

$ git pull  (by default, it pulls from origin, SO DON'T DO THIS)

$ git pull upstream master #we want to pull from master

remote: Counting objects: 55, done.
remote: Compressing objects: 100% (31/31), done.
remote: Total 55 (delta 9), reused 0 (delta 0), pack-reused 24
Unpacking objects: 100% (55/55), done.
From https://github.com/thisismetis/nyc16_ds9
 * branch            master     -> FETCH_HEAD
 * [new branch]      master     -> upstream/master
Updating 73c9b7f..e2fa70b
Fast-forward
```

## Practice - let's add a file
>my example
```
$ cd nyc16_ds9/challenges/submissions/00-practice1
$ mkdir reshama
$ cd reshama
```

**Note: in the `00-practice1` folder, directories have been made for each student, as an example.  Going forward, you will need to make a folder with your name.**  
**Naming Convention:  first name, lower case, under scores (add last name if needed)**

Make a small file  
Redirect standard output to a file called “text.txt”
>my example

```
$ echo "Hello! Nice to meet you!" > test.txt
echo "Hello! Nice to meet you" > test.txt

$ cat test.txt 
Hello! Nice to meet you
```

---
## When you’re ready to push code

### 1. See what’s changed since the last commit
`git status` shows files that have changed or are untracked  
`git diff [optional: filename]` shows the changes themselves

### 2. “Stage” the things you want to include in your commit
This includes both files that have changed and new files you want to add.

`git add <file or directory>`

### 3. Commit your changes and add a useful message

`git commit -m ‘message goes here’`

### 4. Push to the origin repo

`git push origin master`

---

### Adding, committing a file
>my example 
```
$ git status
$ git add test.txt                     # sets working copy to staged copy
$ git status
$ git commit -m "add a simple file"    # staged copy to revision history
$ git push origin master               # send it to (my forked) repo (branch = master)
```

### Adding, committing multiple (all) files in a directory (AVOID DOING THIS!!!!!)
```
$ git add .     # DON'T DO THIS!
$ git status
$ git commit -m "adding all files in this repo"
$ git push
```

### Sync repos
```
$ git pull upstream master
$ git push origin master
```

## Pull Request

Go to your forked version
https://github.com/reshama/nyc16_ds9

Right column, go to **"New pull request"**

Click on green **"Create pull request"**

Fill in info at **"Leave a comment"**

Click on green **"Create pull request"**

Look in this repo and see that file has been updated.

--

## Git Commands

###Important:  To Remove a File from the Repo
`$ git rm filename`  

###Important:  To Rename or Move a File in the Repo
`$ git mv filename` 

###List of Git commands
`$ git`

###Git log
`$ git log`

**Note:**  
GitHub:  commit every day, green dots show up on user home page; looks good for potential employers.  
This is what my GitHub activity graph looks like:  
https://github.com/reshama


