#Git Best Practices

##Git Workflow
1.  Fork repo, clone repo, `git remote add upstream` 
2.  Create a branch:  `reshama_wip`
3.  Work in `reshama_wip` branch, launch Jupyter notebooks for course repo from `reshama_wip` branch
4.  Submitting Pull Requests:
  - copy file from `reshama_wip` to `master` branch; in `master` branch:  `git checkout branch_wip myfile.txt`
  - do `git add filename`, `git commit -m 'message'`, `git push origin master`
  - in GitHub (browser), create a pull request


###Copy file from one branch to current branch
Run this from the branch where you want the file to end up:  
```
git checkout branch_wip myfile.txt
```

###Copy directory from one branch to current branch
```
git checkout branch_wip myfolder/** 
```

###More Commands
```
git diff --stat "$branch"
git checkout --merge "$branch" "$file"
git diff --stat "$branch"
```

--

##Tips for Working Cleanly

###Launch your Jupyter notebook from your working branch (not `master` branch)

###Adding, committing files
* Do this:  `git add filename`
* DON'T do this:  `git add . `

---

####Reference

[How do I copy a version of a single file from one git branch to another?](http://stackoverflow.com/questions/307579/how-do-i-copy-a-version-of-a-single-file-from-one-git-branch-to-another)  
