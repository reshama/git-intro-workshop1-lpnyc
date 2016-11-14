#Create a Repository on GitHub


##Step 1: Create a repo using GitHub (on web browser)
- Click on "+" next to your profile picture
- Select `New Repository`
- Repository name:  `starting_git`
- Description (optional):  `test project for git`
- `Public` repos are free
- Check box for `Initialize this repository with a README`
- Select green button `Initialize this repository with a README`

##Step 2:  Let's add a couple of files
- Add a Markdown file:  `holiday.md`
  - add a line with an emoji
- Add a Python file:  `hello.py`
  - add a line, the ubiquitous "Hello World!"
  
**Note:  add a meaningful commit message**  

##Step 3:  Add collaborators (if you would like to share)


##Step 4:  Clone repo

### Go to directory on local computer  
For me, it is: 
`/Users/reshamashaikh/git_work`  

>my example
```bash
~/git_work  master ✗                                                                  ◒  
▶ pwd
/Users/reshamashaikh/git_work
```

### Clone repo
`git clone https://github.com/reshama/starting_git.git`  

>my example  
```bash
~/git_work  master ✗                                                                  ◒  
▶ git clone https://github.com/reshama/starting_git.git
Cloning into 'starting_git'...
remote: Counting objects: 15, done.
remote: Compressing objects: 100% (10/10), done.
remote: Total 15 (delta 1), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (15/15), done.
Checking connectivity... done.
```

### `cd` into cloned repo

```bash
▶ pwd
/Users/reshamashaikh/git_work/starting_git

▶ ls
total 0
drwxr-xr-x  7   238 Nov 14 11:29 data-science-from-scratch
drwxr-xr-x  6   204 Nov 14 11:48 starting_git

~/git_work  master ✗                                                                  ◒  
▶ cd starting_git 

~/git_work/starting_git  master ✔                                                    6m  
▶ 
```

### Check out the remote
Note:  
- a 'remote' is a copy of a repository
- notice you have push and pull access  

>my example  
```bash
▶ git remote -v
origin	https://github.com/reshama/starting_git.git (fetch)
origin	https://github.com/reshama/starting_git.git (push)
```

### We can 'pull' updates from GitHub version
```bash
▶ git pull
Already up-to-date.
```

### Let's make a change on local computer and push changes up to GitHub
Use an editor of your choice to create a python file which will print your name.  
My file `print_name.py` contains the following line of code:  
```python
print("My name is Reshama")
```

```bash
~/git_work/starting_git  master ✔                                                   11m  
▶ emacs print_name.py

~/git_work/starting_git  master ✗                                                 11m ◒  
▶ python print_name.py 
Hello, my name is Reshama

~/git_work/starting_git  master ✗                                                 12m ◒  
▶ 
```

### We made a change!  How does git track it?
To see what changes have been made since last `git pull`, type `git status`  
```bash
▶ git status
On branch master
Your branch is up-to-date with 'origin/master'.
Untracked files:
  (use "git add <file>..." to include in what will be committed)

	print_name.py
	print_name.py~

nothing added to commit but untracked files present (use "git add" to track)

~/git_work/starting_git  master ✗                                                 14m ◒  
▶ 
```

## Git:  add, commit and push a file

### `add` a file
This sets a file for staging:  
`git add print_name.py`  

>my example  
```
~/git_work/starting_git  master ✗                                                 14m ◒  
▶ git add print_name.py
```



```git
▶ git status
On branch master
Your branch is up-to-date with 'origin/master'.
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	new file:   print_name.py

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	print_name.py~


~/git_work/starting_git  master ✗                                               17m ✚ ◒  
▶ 
```

### `git commit -m 'message'`

```bash
▶ git commit -m 'adding file that prints my name'
[master bfefcd3] adding file that prints my name
 1 file changed, 1 insertion(+)
 create mode 100644 print_name.py

~/git_work/starting_git  master ✗                                                  0m ◒  
▶ git status
On branch master
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)
Untracked files:
  (use "git add <file>..." to include in what will be committed)

	print_name.py~

nothing added to commit but untracked files present (use "git add" to track)

~/git_work/starting_git  master ✗                                                  0m ◒  
▶ 
```

