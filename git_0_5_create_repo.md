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





