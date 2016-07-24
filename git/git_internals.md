##GIT Internals

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