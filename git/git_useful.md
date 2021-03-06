## GIT Useful commands


- Git log graph

```bash
$  git log --graph --oneline --all
```

- Git checkout branch

```bash
$ git checkout -b feature/<branchName> --track origin/feature/<branchname>
```

- Set upstream branch

```bash
# use of feature/ is optional
$ git push --set-upstream origin feature/<branch name>
```

- Diff against a remote branch

```bash
$ git diff origin/master
```

- Remove changes, not committed

```bash
$ git clean -f
```

- Remove file from staging area

```bash
$ git reset <file>
```

- Reset to remote master. e.g removing locally committed changes

```bash
$ git reset --hard origin/master
```

- Deleted files staging

```bash
$ git rm <file>
```

- Rename a branch

```bash
$ git branch -m <current name> <new name> # if not on branch to rename

$ git branch -m <new name> # if on branch to rename

$ git push origin :<current name> <new name> # to rename upstream branch
```

- Update branch without switching to it

```bash

$  git update-ref refs/heads/master origin/master # need to fetch prior to this

```

- Revert to previous commit and push

```bash
# Recommend creating a branch at the current commit before doing this

$ git reset --hard <COMMIT SHA>

$ git push --force
```

- Delete local and remote 

```bash

$ git push origin --delete <branch nane>

```

- Cherry pick commit

```bash

$ git fetch

$ git cherry-pick <SHA>

```

- Print current SHA-1

```bash

$ git rev-parse HEAD

```
