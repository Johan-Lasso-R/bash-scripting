# Basics

## Creating a script
We use the `touch` command to create an empty file:
```bash
touch helloWorld.sh
```
The `.sh` is the file extension used for bash scripts.

### Let's run our script
To run an script we need to write this in the console and hit enter:
```bash
bash helloWorld.sh
```
The `bash` command is used to tell the system which interpreter will execute our script.

When you executed the file nothing happened, right? Of course not, because it was empty. So, let's write the instruction to print "Hello world!" message to the console.

## `echo` command
Let's open our script (I'll use nano, but you can use whichever text editor you like):
```bash
nano helloWorld.sh
```
Inside the script write this:
```bash
echo Hello world!
# Change the message as you please
```
The `echo` command is used to display a message on the console.

## `#!` (shebang)
Instead of writing `bash` every time we want to run a script, we can add this line at the top of our scripts: 
```bash
#!/bin/bash
# Your commands
```
The `#!` sequence is called "shebang" and it's used to tell the OS which interpreter we want to use to run our script.
Now, run it again:
```bash
./helloWorld.sh 
# You don't have call bash anymore
```
Wait, does it throw an error? Because of the [file permissions](file_permissions.md).

### Giving the script permissions
To add execute permissions to our script we need to use this command:
```bash
chmod u+w file.sh 
```