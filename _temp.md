## get rid of uncessary files
You should add a line with:

```
*.pyc 

```

to the `.gitignore` file in the root folder of your git repository tree right after repository initialization.

As _ralphtheninja_ said, if you forgot to to do it beforehand, if you just add the line to the `.gitignore` file, all previously committed `.pyc` files will still be tracked, so you'll need to remove them from the repository.

If you are on a Linux system (or "parents&sons" like a MacOSX), you can quickly do it with just this one line command that you need to execute from the root of the repository:

```
find . -name "*.pyc" -exec git rm -f "{}" \;

```

This just means:

> _starting from the directory i'm currently in, find all files whose name ends with extension `.pyc`, and pass file name to the command `git rm -f`_

After `*.pyc` files deletion from git as tracked files, commit this change to the repository, and then you can finally add the `*.pyc` line to the `.gitignore` file.
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTk5NjE5Nzg5MF19
-->