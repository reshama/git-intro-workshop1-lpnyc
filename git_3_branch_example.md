# Git:  Sample Branch Flow

##Check your current directory location
```bash
ds/metis/metisgh  master ✗                                                            ◒  
▶ ls
total 0
drwxr-xr-x  3   102 Aug  6 15:49 prework
```

##Clone the forked repo
```bash
ds/metis/metisgh  master ✗                                                            ◒  
▶ git clone https://github.com/reshama/nyc16_ds9.git
Cloning into 'nyc16_ds9'...
remote: Counting objects: 671, done.
remote: Total 671 (delta 0), reused 0 (delta 0), pack-reused 671
Receiving objects: 100% (671/671), 2.13 MiB | 1.98 MiB/s, done.
Resolving deltas: 100% (350/350), done.
Checking connectivity... done.

ds/metis/metisgh  master ✗                                                            ◒  
▶ ls
total 0
drwxr-xr-x  14   476 Sep 19 10:23 nyc16_ds9
drwxr-xr-x   3   102 Aug  6 15:49 prework

ds/metis/metisgh  master ✗                                                            ◒  
▶ cd nyc16_ds9 

metis/metisgh/nyc16_ds9  master ✔                                                    3d  
▶ ls
total 16
-rw-r--r--  1   8078 Sep 19 10:23 README.md
drwxr-xr-x  4    136 Sep 19 10:23 administrative
drwxr-xr-x  7    238 Sep 19 10:23 challenges
drwxr-xr-x  3    102 Sep 19 10:23 class_lectures
drwxr-xr-x  4    136 Sep 19 10:23 images
drwxr-xr-x  4    136 Sep 19 10:23 investigations
drwxr-xr-x  3    102 Sep 19 10:23 links
drwxr-xr-x  4    136 Sep 19 10:23 pair_programming
drwxr-xr-x  8    272 Sep 19 10:23 projects
drwxr-xr-x  4    136 Sep 19 10:23 resources
```
##List Remotes
```bash
metis/metisgh/nyc16_ds9  master ✔                                                    3d  
▶ git remote -v
origin	https://github.com/reshama/nyc16_ds9.git (fetch)
origin	https://github.com/reshama/nyc16_ds9.git (push)
```
##Add a Remote
```bash
metis/metisgh/nyc16_ds9  master ✔                                                    3d  
▶ git remote add upstream https://github.com/thisismetis/nyc16_ds9.git

metis/metisgh/nyc16_ds9  master ✔                                                    3d  
▶ git remote -v                                                       
origin	https://github.com/reshama/nyc16_ds9.git (fetch)
origin	https://github.com/reshama/nyc16_ds9.git (push)
upstream	https://github.com/thisismetis/nyc16_ds9.git (fetch)
upstream	https://github.com/thisismetis/nyc16_ds9.git (push)
```
##List Branch
```bash
metis/metisgh/nyc16_ds9  master ✔                                                    3d  
▶ git branch
* master
```
##Create a Branch
```bash
metis/metisgh/nyc16_ds9  master ✔                                                    3d  
▶ #create a branch

metis/metisgh/nyc16_ds9  master ✔                                                    3d  
▶ git branch reshama_wip
```
##Navigate to Branch
```bash
metis/metisgh/nyc16_ds9  master ✔                                                    3d  
▶ git checkout reshama_wip
Switched to branch 'reshama_wip'

metis/metisgh/nyc16_ds9  reshama_wip ✔                                               3d  
▶ ls
total 16
-rw-r--r--  1   8078 Sep 19 10:23 README.md
drwxr-xr-x  4    136 Sep 19 10:23 administrative
drwxr-xr-x  7    238 Sep 19 10:23 challenges
drwxr-xr-x  3    102 Sep 19 10:23 class_lectures
drwxr-xr-x  4    136 Sep 19 10:23 images
drwxr-xr-x  4    136 Sep 19 10:23 investigations
drwxr-xr-x  3    102 Sep 19 10:23 links
drwxr-xr-x  4    136 Sep 19 10:23 pair_programming
drwxr-xr-x  8    272 Sep 19 10:23 projects
drwxr-xr-x  4    136 Sep 19 10:23 resources
```

##Create a Test File
```bash
metis/metisgh/nyc16_ds9  reshama_wip ✔                                               3d  
▶ cd challenges/submissions/00-practice1

challenges/submissions/00-practice1  reshama_wip ✔                                   3d  
▶ mkdir reshama

challenges/submissions/00-practice1  reshama_wip ✔                                   3d  
▶ emacs reshama/test.py
```

##Check Status
```bash
challenges/submissions/00-practice1  reshama_wip ✗                                 3d ◒  
▶ git status
On branch reshama_wip
Untracked files:
  (use "git add <file>..." to include in what will be committed)

	reshama/

nothing added to commit but untracked files present (use "git add" to track)

challenges/submissions/00-practice1  reshama_wip ✗                                 3d ◒  
```
##Switch to `master` Branch
```bash
▶ git checkout master
Switched to branch 'master'
Your branch is up-to-date with 'origin/master'.

challenges/submissions/00-practice1  master ✗                                      3d ◒  
▶ git status
On branch master
Your branch is up-to-date with 'origin/master'.
Untracked files:
  (use "git add <file>..." to include in what will be committed)

	reshama/

nothing added to commit but untracked files present (use "git add" to track)
```

##`git add folder/file`
```bash
challenges/submissions/00-practice1  master ✗                                      3d ◒  
▶ git add reshama/

challenges/submissions/00-practice1  master ✗                                      3d ✚  
▶ git status
On branch master
Your branch is up-to-date with 'origin/master'.
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	new file:   reshama/test.py
```

##`git commmit -m 'commit message'`
```bash
challenges/submissions/00-practice1  master ✗                                      3d ✚  
▶ git commit -m 'adding reshama folder and test python file'
[master 16e6aea] adding reshama folder and test python file
 1 file changed, 1 insertion(+)
 create mode 100644 challenges/submissions/00-practice1/reshama/test.py

challenges/submissions/00-practice1  master ✔                                        0m  
▶ git push origin master
Counting objects: 7, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (5/5), done.
Writing objects: 100% (7/7), 544 bytes | 0 bytes/s, done.
Total 7 (delta 4), reused 0 (delta 0)
remote: Resolving deltas: 100% (4/4), completed with 4 local objects.
To https://github.com/reshama/nyc16_ds9.git
   f1528aa..16e6aea  master -> master

challenges/submissions/00-practice1  master ✔                                        0m  
▶ # next, submit pull request from GitHub (on browser) (green pull request button)   0m  

challenges/submissions/00-practice1  master ✔                                        0m  
▶ 
```
