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
