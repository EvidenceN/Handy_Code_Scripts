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
