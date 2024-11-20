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
 Save Changes with git stash
```bash
git stash
```
View Stashed Changes
```bash
git stash list
```
Apply the Stash
```bash
git stash apply
```
If you want to apply a specific stash (e.g., stash@{1}):
```bash
git stash apply stash@{1}
```
Apply and Drop Stash
```bash
git stash pop
```
 Remove a Stash
```bash
git stash drop stash@{0}
```
To drop or clear all stashes:
```bash
git stash clear
```
 Stash with a Message
```bash
git stash save "Work on feature X"
```
Stash Only Unstaged Changes
If you only want to stash changes that haven't been staged (i.e., files that haven't been added using git add)
```bash
git stash --keep-index
```
Stash Untracked or Ignored Files
```bash
git stash -u
```
To stash untracked and ignored files:
```bash
git stash -a
```
Stash Branch
If you're in the middle of working on a feature and want to quickly switch to a new branch but don’t want to lose progress, you can use:
```bash
git stash branch <branch-name>
```
## To delete a branch in Git, use the following commands based on your needs:
The below command checks if the branch being deleted has been fully merged into the current branch or another branch. **(safe delete)**
```bash
git branch -d branch-name
```
The below command forcefully deletes a branch, ignoring whether it has been merged or not. **(force delete)**
```bash
git branch -D branch-name
```
Delete a Remote Branch
```bash
git push origin --delete branch-name
```

