## GIT Internals

Git objects:
+ Blobs
+ Trees 
+ Commits
+ Annotated tags

git commits stored in object folder as type commit, with a tree SHA1 reference. Every commit after the first will also have a reference to its parent commit.
So a commit points to a tree which can have SHA1 references to other trees and blobs.
File names and permissions are stored in the tree type object, blobs only store content allowing for blob objects to be references from multiple tree objects for the same content.

Create a git object for text “Hello world” and store it.

```bash
$ echo “Hello world” | git hash-object \-\-stdin -w
```

Show the content of a git object. (-p = pretty print, -t = file type)

```bash
$ git cat-file -p SHA1
```

Count git objects.

```bash
$ git count-objects
```

Create an annotated tag.

```bash
$ git tag -a someTag -m “Some message“
```
git cat-file can be used to see annotated tag.
```bash
$ git cat-file -p someTag
```

References between commits = History

All other references = Content

##### Branches and HEAD
Branch is a reference to a commit.

HEAD is a reference to a branch (pointer to a pointer).

Move between branches. 

```bash
$ git checkout someBranch
```

##### Checking out a specific commit 

```bash
$ git checkout SHA1
```

this will give a detached head. Can carry on committing, then when experimentation is over checkout master or another branch again. Objects will become unreachable and git will garbage collect at some point during another operation, to save the detached head git branch before returning to master.
