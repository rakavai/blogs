---
layout: post
title: How to ignore files temporarily in git
---

To start ignoring files in git:

```shell
git update-index --assume-unchanged <path/to/file1> <path/to/dir2>
```

To track the change of the specific file again:

```shell
git update-index --no-assume-unchanged <path/to/file1> <path/to/dir2>
```

To track all the files that are ignored temporarily:

```shell
git update-index --really-refresh
```

To see the list of temporarily ignored files:

```shell
git ls-files -v | grep "^h"
```

## Example

```text
$ git status

# On branch master
# Changes not staged for commit:
#   (use "git add <file>..." to update what will be committed)
#   (use "git restore <file>..." to discard changes in working directory)
# 	modified:   file-to-be-ignored-temporarily.txt
# 	modified:   file-want-to-see-change.txt
# 
# no changes added to commit (use "git add" and/or "git commit -a")
```

```txt
$ git update-index --assume-unchanged file-to-be-ignored-temporarily.txt
```

```text
$ git status

# On branch master
# Changes not staged for commit:
#   (use "git add <file>..." to update what will be committed)
#   (use "git restore <file>..." to discard changes in working directory)
# 	modified:   file-want-to-see-change.txt
# 
# no changes added to commit (use "git add" and/or "git commit -a")
```

```txt
$ git update-index --no-assume-unchanged file-to-be-ignored-temporarily.txt
```

```txt
$ git status

# On branch master
# Changes not staged for commit:
#   (use "git add <file>..." to update what will be committed)
#   (use "git restore <file>..." to discard changes in working directory)
# 	modified:   file-to-be-ignored-temporarily.txt
# 	modified:   file-want-to-see-change.txt
# 
# no changes added to commit (use "git add" and/or "git commit -a")
```

> **Note:** In case some files need to be ignored all the time, it is better
ignore the file in the `.gitignore`.