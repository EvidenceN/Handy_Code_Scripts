delete branch locally

    git branch -d localBranchName

delete branch remotely

    git push origin --delete remoteBranchName

Create new git branch

    git checkout -b branchName

  This is shorthand for:
  
    git branch branchName
    git checkout branchName
    
Make an empty commit for pushing to production. 

    git commit --allow-empty -m "Commit message"
    git push -u origin branch_name 

Scenario

* Has a pre-existing remote repo with code
* Has a local folder that is not a git repo but I want to turn it into a git repo and sync it with my pre-existing remote repo

How to get it done. 
* Go to local repo
* `git init`
* `git remote add origin <ssh link to remote repo>`
* `git fetch` - this will bring upstream code down to local repo
* `git checkout -b "new branch name"` - this will move the new code changes to the new branch
* `git add` on the new branch
* `git commit -m "message"` on the new branch
* `git push -u origin new_branch_name` 
* On github, merge the new branch back into master branch
* On terminal (local computer). Do a `git pull` to merge online master branch to local master branch
* Proceed to make the necessary changes like deleting some files, moving things around, e.t.c from master branch. Could also do this step before merging to master branch. 


**How to resolve a merge conflict where master branch has changed resulting in your own code being out of sync with master**

From the commandline
1. `git checkout master`
2. `git fetch`
3. `Git checkout the branch you were using to do your work`
4. `git merge master`
6. If the code merges automatically, GREAT. If not, it will show you things that couldn't be merged automatically. To resolve this, Go to VSCode or your IDE. Click `"Accept both changes"`
7. Push your changes back to github and merge conflict should be resolved. 


After setting up SSH, how to add email and username

```
git config --global user.email "email@example.com"
git config --global user.email (To confirm setting) 
git config --global user.name "Mona Lisa"
git config --global user.name (To confirm setting)```
