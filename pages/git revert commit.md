tags:: [[git]]

- To revert your repository to a previous commit, you can use the following Git commands depending on whether you want to reset or revert the changes:
- ### Option 1: **Reset to a previous commit (destructive, history rewrite)**
  
  If you want to discard the commit and all subsequent changes (hard reset):
  
  ```bash
  git reset --hard <commit_hash>
  ```
  
  Replace `<commit_hash>` with the hash of the commit you want to revert to. This will reset the repository to that commit, discarding all changes made after it.
  
  To keep the changes but reset the commit history (soft reset):
  
  ```bash
  git reset --soft <commit_hash>
  ```
- ### Option 2: **Revert the commit (non-destructive, keeps history)**
  
  If you want to create a new commit that undoes the changes from the specific commit:
  
  ```bash
  git revert <commit_hash>
  ```
  
  This will generate a new commit that undoes the changes from the commit you specify. You’ll need to replace `<commit_hash>` with the hash of the commit where you renamed the column.
- ### After running either of these commands, remember to push the changes if you’re working on a remote branch:  
  
  ```bash
  git push origin <branch_name> --force # use --force for reset
  git push origin <branch_name>          # for revert
  ```