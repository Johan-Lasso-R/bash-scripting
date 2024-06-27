# Variables
Variables are like boxes where we can store data to use it later. 

## Declaring variables in our script
Let's create a variable that stores our name:
```bash
#!/bin/bash

myName="this is a variable" 
# Change johan with whatever you like
```
Here, I created a variable called `myName` and its content is a string of text. 

If you run the script (remember to add [execute permission](..//first_script/file_permissions.md) to the script) nothing will happen because you just created the variable but didn't print it.

### Calling a variable
If you want to use a variable you need to call it:
```bash
#!/bin/bash

myText="this is a variable" 
# Change text as you please

echo $myText 
```
As you can see, when I used the `$` symbol to access `myText`'s content, why? Because the `s` symbol is used to **dereference** a variable (access its content).

## Asking for input
You can create scripts that can ask the user to write stuff. Let's star by creating a new script and giving it execute permissions 
```bash
touch interactive.sh && chmod u+x interactive.sh
```
`&&` is like the word "and" in the English language. What I'm doing here is telling the console to create a file **AND** also giving it execute permissions.

Now, let's write some commands inside our script:
```bash
#!/bin/bash

echo "Tell me your first name"
read firstName
echo "Tell me how old are you"
read age

echo "Hello" $firstName". You are "$age
```