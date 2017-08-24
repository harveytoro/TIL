## GIT stash

Create a stash.

```bash
$ git stash save “MESSAGE FOR STASH”
```

Show stashes.

```bash
$ git stash list
```

Restore a stash. Without specifying an index this pops the stash at 0 (as expected acts like a stack, new stashes are pushed on to the top and popped off).

```bash
$ git stash pop
```
