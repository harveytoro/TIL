# Git Interactive Rebase

- Using git rebase interative to change author of a commit.

```bash
$ git rebase -i HEAD~3

// opens last three commits, change pick to edit
// then 

$ git commit --amend --author "harveytoro <email@email.com>"
$ git rebase --continue
```
