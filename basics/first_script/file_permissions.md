# File permissions
There are three types of permissions a file can have:
- Read `r`: watch the file's content.
- Write `w`: edit the file's content.
- Execute `x`: run the file if it's a script or binary.

## View file permissions
You can see which permissions you files have with the `ls -l` command:
```bash
-rw-rw-r-- 1 johan johan   28 Jun 23 13:21 helloWorld.sh
```
What does all of that mean?

### Understanding `ls -l` output
The first character "-" indicates if the file type (file or directory): 
- `-` for files.
- `d` for directories.

`rw-rw-r` are the permissions that the owner, the group and other users have on the file or directory. 

I won't go into detail about about owner and groups, but as you can see `helloWorld.sh` can be read and written, but not executed. How can we change that?

## Changing file permissions
To give execute permissions you write this command:
```bash
chmod u+w file.sh 
```

### What did I just do exactly?
- `chmod`: this command stands for "change mode" and is used to change permissions.
- `u`: represents the file owner.
- `+`: is an operator used to **add** a permission.
- `x`: is the permission we want to add. 