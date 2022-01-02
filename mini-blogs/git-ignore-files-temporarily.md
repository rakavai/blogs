```shell
$ git status
```
```text
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   file-to-be-ignored-temporarily.txt
	modified:   file-want-to-see-change.txt

no changes added to commit (use "git add" and/or "git commit -a")
```

```shell
$ git update-index --assume-unchanged file-to-be-ignored-temporarily.txt
```

```shell
$ git status
```
```text
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   file-want-to-see-change.txt

no changes added to commit (use "git add" and/or "git commit -a")
```

```shell
$ git update-index --no-assume-unchanged file-to-be-ignored-temporarily.txt
```

```shell
$ git status
```
```text
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   file-to-be-ignored-temporarily.txt
	modified:   file-want-to-see-change.txt

no changes added to commit (use "git add" and/or "git commit -a")
```