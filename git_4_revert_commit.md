#Git: Revert Commits

Where you are:  
 * you've committed some files, pushed to your local repo, and want to delete the commit

##View the commit log
```console
reshama$ git log -2
commit a3334f177bed83528f5ab3883d87f1336f599f49
Author: reshama <rs2715@gmail.com>
Date:   Tue May 24 11:04:52 2016 -0400

    adding test file 4

commit 12dc41f2620118977c17ad21dfc4b504191e170e
Author: reshama <rs2715@gmail.com>
Date:   Tue May 24 11:04:06 2016 -0400

    adding test3 file
reshama$ 
```
##How to undo a commit
```console
git reset --soft HEAD^     # use --soft if you want to keep your changes
git reset --hard HEAD^     # use --hard if you don't care about keeping the changes you made
```
```
reshama$ git reset --soft HEAD~1    # use --soft to preserve changes that were made and undo last commit (~1 = back 1 commit)
```

##Unstage a file
```
$ git reset HEAD <file>       
````
 
---

###References

[Stack Overflow:  How do you undo the last commit](http://stackoverflow.com/questions/927358/how-do-you-undo-the-last-commit)  
[Stack Overflow:  Remove files from last commit](http://stackoverflow.com/questions/12481639/remove-files-from-git-commit)  


