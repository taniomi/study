tags:: [[git]]

- # What's the difference between the 3 modes of performing a PR in github?
- The three main modes of performing a Pull Request (PR) in GitHub are **Merge**, **Rebase**, and **Squash**. Here's the difference between them:
- ## Merge
	- **Operation**: Combines all commits from the source branch into the target branch with a merge commit.
	- **Effect**: Preserves the full commit history of the source branch. A new merge commit is created.
	- **Best for**: When you want to keep a detailed history of the changes, including all commits made during the feature development.
- ## Rebase
	- **Operation**: Reapplies the source branch commits on top of the target branch.
	- **Effect**: Rewrites the commit history as if the source branch was based on the latest commit of the target branch. No merge commit is created.
	- **Best for**: Keeping a linear commit history without merge commits. More commonly used in private repositories.
- ## Squash
	- **Operation**: Combines all commits from the source branch into a single commit.
	- **Effect**: Collapses the entire feature branch into one commit, making the commit history more compact.
	- **Best for**: When you want to condense multiple small or intermediary commits into a single commit before merging into the target branch.
- Each mode has its own use case depending on whether you prioritize maintaining full commit history (Merge), having a clean linear history (Rebase), or simplifying the commit history (Squash).