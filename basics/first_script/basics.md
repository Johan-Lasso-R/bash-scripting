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