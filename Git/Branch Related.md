# List Local Git Branches by Last Commit Date
List all local branches, sorted by their most recent commit date, showing the branch name and the timestamp of the last update.
```
 git for-each-ref --sort=-committerdate --format='%(refname:short) %(committerdate:iso8601)' refs/heads/
```

---
# Renaming a GitHub Branch (Add Jira Ticket Reference)

Forgot to add a Jira ticket reference to your GitHub branch name?  
Follow these steps to rename it both locally and on GitHub.

```bash
# Rename the branch you're currently on
git branch -m new-name

# OR rename a branch you're NOT on
git branch -m old-name new-name

# Push the renamed branch to GitHub
git push origin new-name

# Delete the old branch on GitHub
git push origin --delete old-name

# Set upstream (so git push works normally)
git push --set-upstream origin new-name

# Verify remote branches
git ls-remote --heads origin



