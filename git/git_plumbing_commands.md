## Git Plumbing commands

Updating a reference. Creating a branch using update-ref. Git branch uses update-ref using the SHA1 of the last commit (known by using the HEAD file).

```bash
$ git update-ref refs/heads/branchName SHA1
```

View what HEAD is currently pointing at symbolic-ref.

```bash
$ git symbolic-ref head
```

Switching branch using symbolic-ref. (this will not update the working directory).

```bash
$ git symbolic-ref HEAD refs/heads/existingBranch
```

View dangling objects by running an integrity check.

```bash
$ git fsck —full
```
