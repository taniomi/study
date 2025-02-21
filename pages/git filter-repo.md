tags:: [[git]]

- [stack overflow](https://stackoverflow.com/questions/43762338/how-to-remove-file-from-git-history/64563565#64563565)
- This command removes the file from all commits in all branches:
  logseq.order-list-type:: number
	- ```bash
	  git filter-repo --invert-paths --path <path to the file or directory>
	  ```
	- Multiple paths can be specified by using multiple `--path` parameters. You can find detailed documentation here: [https://www.mankier.com/1/git-filter-repo](https://www.mankier.com/1/git-filter-repo)
- Add the remote origin again
  logseq.order-list-type:: number
	- ```bash
	  git remote add origin <repo SSH>
	  ```
- Now force push the repo: `git push origin --force --all`
  logseq.order-list-type:: number
- Tell your collaborators to rebase `git pull --rebase`.
  logseq.order-list-type:: number
- logseq.order-list-type:: number