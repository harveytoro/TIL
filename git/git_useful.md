##GIT Useful commands


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

- Reset to remote master. e.g removing locally committed changes

```bash
$ git reset --hard origin/master
```
