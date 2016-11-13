## Git Branch  
[Helpful Tutorial:  Using Branches on Git](https://www.atlassian.com/git/tutorials/using-branches)  

Why use branches?
 * independent line of development
 * think of them as a way to request a brand new working directory, staging area, and project history
 * in Git, branches are a part of your everyday development process. 
    * when you want to add a new feature or fix a bug—no matter how big or how small,  spawn a new branch to encapsulate your changes
    * this makes sure that unstable code is never committed to the main code base
    * it gives you the chance to clean up your feature’s history before merging it into the main branch

**Note:  'wip' = 'work in progress'**    

---

##Branch Commands
 * **List branches**  
    `$ git branch`
 * **Create a new branch**  
    `$ git branch reshama_wip`
 * **Navigate between branches**  
    `$ git checkout branchname`
 * **Create and switch to branch** (2 steps in 1 line)  
    `$ git checkout -b testbranch`

 * **Delete a branch** (safe delete; won't delete if there are unmerged changes)  
    `$ git branch -d reshama_wip`
 * **Delete a branch** (force delete; will delete even if branch has unmerged changes)  
    `$ git branch -D reshama_wip`


 * **Rename a branch** (whichever is the current one, be careful)  
    `$ git branch -m newone_wip`
 * **Rename a branch** (can specify oldname and newname)  
    `$ git branch -m <oldname> <newname>`


 * **Back to main branch**  
    `$ git checkout master`
 * **Merge branches** (will merge specified <branchname> into current branch)  
    `$ git merge <branchname>`

###Copy file/folder from one branch to current branch (`master`)

####Copy file from one branch to current branch (`master`)
Run this from the branch where you want the file to end up:  
on:  `master` branch
```
git checkout branch_wip myfile.txt
```

####Copy directory from one branch to current branch (`master`)
on:  `master` branch
```
git checkout branch_wip myfolder/** 
```

--- 

###An Example  

```
reshama$ #print working directory
reshama$ pwd
/Users/reshamashaikh/ds/metisgh/nyc16_ds9

reshama$ #list the branches in this repo
reshama$ git branch
* master

reshama$ #create a test branch
reshama$ git branch test

reshama$ #list branches in this repo
reshama$ git branch
* master
  test
  
reshama$ #delete the 'test' branch
reshama$ git branch -d test
Deleted branch test (was f320504).

reshama$ #check to see the branch 'test' was deleted
reshama$ git branch
* master

reshama$ #create a branch
reshama$ git branch reshama
reshama$ git branch
* master
  reshama
  
reshama$ #rename the branch
reshama$ git branch -m reshama reshama_wip
reshama$ git branch
* master
  reshama_wip
  
reshama$ #switch to another branch
reshama$ git checkout reshama_wip
Switched to branch 'reshama_wip'
reshama$ git branch
  master
* reshama_wip

reshama$ #back to master branch
reshama$ git checkout master
Switched to branch 'master'
Your branch is up-to-date with 'origin/master'.

reshama$ git branch
* master
  reshama_wip
reshama$ 

```
---

###Notes
 * You can create multiple branches, but stick with just one for now; makes it easier to manage until you're more of an expert Git user 

####Push (by Qualifying Remote Name and Branch Name)
```
$ # Work on your branch as usual, and then push to your `origin`
$ # git push <remotename> <branchname>
$ git push origin reshama_wip
```

####Pull Request on GitHub 
 * When you sync up, sync up your branchname to metis `master`!

---

####Back to your 'master' branch and syncing repos
```
$ git checkout master
$ git pull upstream master
```

It's possible to do pull requests from your `master` branch, but this puts you in an awkward position where you're waiting for the pull request to get merged before it's safe for you to sync up again. Topic branches are highly recommended.
