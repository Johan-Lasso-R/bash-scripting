## Positional arguments
For the `cp` command to work, you need to specify both the source file or folder and the destination path. These are called arguments and must be written in a specific order: first, the file or folder you want to copy, and then the path where you want to copy it.
```bash
cp variables.sh ../some_dir
```
These are known as positional arguments because their position in the command line is crucial for the command to execute correctly.

If you write the path firs, you'll get an error:
```bash
cp ../some_dir/ ./variables.sh 
cp: -r not specified; omitting directory '../some_dir/'
```

### How positional arguments work
As always let's create a new script with the `touch` command and change its permissions with `chmod`.

`positional_ag.sh`:
```bash
#!/bin/bash

num1=$1
num2=$2

# adding two numbers
result=$((num1 + num2))

echo "The sum of $num1 and $num2 is: $result"
```

#### Explanation:
- `$1` and `$2`: refer to the first and second positional arguments passed to the script.
- `num1` and `num2`: are assigned the values of these positional arguments.
- `result`: calculates the sum of `num1` and `num2`.
Usage example:
```bash
$ bash add_numbers.sh 3 5
The sum of 3 and 5 is: 8
```

### Why is this useful?
In this example, the order you pass the arguments does not matter, but in other cases it does matter. For example, as I mentioned in the `cp` example:
> These are known as positional arguments because their position in the command line is crucial for the command to execute correctly.
