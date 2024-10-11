# Git World
Issue: To go back in previous commit and update to remote
## Steps:
1. First, find the commit ID of the third commit back by using:
      ```bash
      git log --oneline
2. Then, use the checkout command with the commit ID:
      ```bash
      git checkout <commit-id>
3. This will check out the repository at the state of the specified commit (detached HEAD state). To return to the       latest commit later, run:
      ```bash
      git checkout master
4.  Hard Reset to a Specific Commit (Permanently Revert to an Older Commit):
If you want to permanently reset your repository to that specific commit and discard all commits made after it:
      ```bash
      git reset --hard <commit-id>
5. Push the updated master branch to the remote repository:
      ```bash
      git push origin master
6. Force Push if You've Rewritten History (Optional but Risky):
      ```bash
      git push origin master --force
Then the remote Master will be updated in specifie previous commit!
-------------------------------------------------------------------------------------------------------------------------
## Alternative way
Suppose you want to go back in previous commit point ID 778ea21. Here branch3 is a branch name
```bash
git checkout 778ea21
git checkout -b branch3 
git add . && git commit -m"update to specificcommit"
git checkout master
git merge branch3
git add . && git commit -m"update to specificcommit master"
git push
```
--------------------------------------------------------------------------------------------------------------

## Temporary Commit

