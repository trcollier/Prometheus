List all local branches, sorted by their most recent commit date, showing the branch name and the timestamp of the last update.
```
 git for-each-ref --sort=-committerdate --format='%(refname:short) %(committerdate:iso8601)' refs/heads/
```
