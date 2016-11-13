# Fork, Clone & Sync a repo

### Step 1:  Go to repo on GitHub
In my personal account on GitHub, go to repo to be cloned.

In this example, it is:  https://github.com/thisismetis/nyc16_ds9   (**bookmark this!**)

### Step 2:  Fork repo
Upper right of github page:  "Fork" the repo

Go to my forked repo: https://github.com/reshama/nyc16_ds9  (**bookmark this!**)

 
### Step 3:  Clone repo
Clone that forked repo (which is now under my name)

In right column, find the link to **HTTPS clone URL** and copy that URL to be cloned.

In terminal: 
* `cd` in to directory where repo will be cloned
* clone repo:   `git clone <url goes here>`
* `cd` into cloned repo
```
$ metisgh
$ pwd
/Users/reshamashaikh/ds/metis/metisgh

$ cd metisgh/
$ ls

$ git clone https://github.com/reshama/nyc16_ds9.git
$ cd nyc16_ds9
```
--

### Step 4:  Add remote upstream 
`$ git remote add upstream <url goes here>`

If there are changes to the original repo, how do you get them?  You need to tell your local repo that it can also get updates from the original.

Origin:  reshama/nyc16_ds9


**Note:  Need to be in that directory on Unix to update repo**
```
$ git remote -v
origin	https://github.com/reshama/nyc16_ds9.git (fetch)
origin	https://github.com/reshama/nyc16_ds9.git (push)
```

Want to add reference to metis repo (which is master repo)
Note:  can call it “upstream” or “root” or any other name
```
$ git remote add upstream https://github.com/thisismetis/nyc16_ds9.git
```

Now we see we have two remotes: 
* origin
* upstream
```
$ git remote -v
origin	https://github.com/reshama/nyc16_ds9.git (fetch)
origin	https://github.com/reshama/nyc16_ds9.git (push)
upstream	https://github.com/thisismetis/nyc16_ds9.git (fetch)
upstream	https://github.com/thisismetis/nyc16_ds9.git (push)
```
--
### Step 5:  Sync repos
#### Workflow:  get files from metis (master) down to local (my computer) and up to origin (me/nyc16_ds9)

**Always "git pull" before sending up any changes**

`$ git pull`  (by default, it pulls from remote origin)

`$ git pull upstream master`  (we want to pull from branch master)

```
$ git pull upstream master
remote: Counting objects: 55, done.
remote: Compressing objects: 100% (31/31), done.
remote: Total 55 (delta 9), reused 0 (delta 0), pack-reused 24
Unpacking objects: 100% (55/55), done.
From https://github.com/thisismetis/nyc16_ds9
 * branch            master     -> FETCH_HEAD
 * [new branch]      master     -> upstream/master
Updating 73c9b7f..e2fa70b
Fast-forward
...
```

### Step [anytime]: Check status of your git repo
```
$ git status
```

`$ git push` or `$ git push origin master` (we want to push to our forked repo, changes will show up when we go to browser)  

**Do this one time only**

`$ git config --global push.default simple`




