## Git reset and reflow

Putting master back to a specific commit.

```bash
$ git reset --hard SHA1
```

Commits after this SHA1 will be lost, to recover need to create a branch for those commits. Can see HEAD references using reflow.

```bash
$ git reflog
```

Then create a branch using the SHA1.

```bash
$ git branch someBranch SHA1
```
