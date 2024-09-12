tags:: [[git]]

- After performing a **squash and merge** on a branch (e.g., merging `dev` into `main` with squashed commits), your **local branch history** (`dev`) will no longer match the **remote history** (`main`) because the history has been rewritten.
  
  To continue working locally after a squash and merge, you need to sync your `dev` branch with the updated `main` branch. Here's the step-by-step process:
- ### 1. **Switch to `dev` Branch**:
  First, ensure you are on your `dev` branch:
  ```bash
  git checkout dev
  ```
- ### 2. **Rebase Your `dev` Branch onto `main`**:
  Since you’ve squashed the commits in `main`, you should rebase your `dev` branch to sync with the new history of `main`.
  
  ```bash
  git fetch origin
  git rebase origin/main
  ```
  
  This command takes your current commits from `dev` and replays them on top of the latest `main` branch, updating your `dev` branch to follow the squashed commit.
- ### 3. **Resolve Any Conflicts**:
  If there are any conflicts during the rebase, Git will notify you. You’ll need to resolve them manually, and then continue the rebase:
  
  ```bash
  # After resolving conflicts
  git add <conflicted-files>
  git rebase --continue
  ```
- ### 4. **Push the Updated `dev` Branch**:
  Once the rebase is complete, you need to push the changes back to the remote `dev` branch. Since the history has changed due to the rebase, you'll need to force-push:
  
  ```bash
  git push --force-with-lease origin dev
  ```
  
  > **Note**: Using `--force-with-lease` is a safer version of `--force`, as it ensures you're not accidentally overwriting someone else's work on the remote.
- ### 5. **Continue Working on the `dev` Branch**:
  Now that your `dev` branch is synced with the latest `main`, you can continue making changes and commit them as usual.
- ### **Summary of Steps**:
  1. Switch to the `dev` branch: `git checkout dev`.
  2. Rebase `dev` onto `main`: `git rebase origin/main`.
  3. Resolve any conflicts, if necessary.
  4. Push the updated `dev` branch: `git push --force-with-lease origin dev`.
  5. Continue working on your `dev` branch as normal.
  
  This will ensure your `dev` branch is in sync with the squashed history of `main`, and you can continue working from there.