## GIT Useful commands


- Git log graph

```bash
$  git log --graph --oneline --all
```

- Git checkout branch

```bash
$ git checkout -b feature/<branchName> --track origin/feature/<branchname>
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
```

- Update branch without switching to it

```bash

$  git update-ref refs/heads/master origin/master # need to fetch prior to this

```
