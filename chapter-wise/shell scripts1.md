### 1. What is a shell script?
A shell script is a **text file that contains a sequence of Unix commands**. It allows you to execute multiple commands at a single moment of time and automate repetitive tasks.

### 2. How can you execute a shell script?
To execute a shell script, you can:
- Make the script executable using `chmod a+x script.sh` and then run it directly: `./script.sh`
- Use the `sh` command: `sh script.sh`

### 3. What is the purpose of the `echo` command in shell scripting?
The `echo` command is used to **display messages or values of variables on the screen**. For example:
```
echo "Hello, World!"
name="John"
echo "My name is $name"
```

### 4. What are the different types of variables in shell scripting?
The three main types of variables in shell scripting are:
- **Local Variables**: Present within the current instance of the shell and not available to programs started by the shell.
- **Environment Variables**: Available to any child process of the shell. They are set for the current shell and any spawned processes.
- **Shell Variables**: Special variables used by the shell itself, such as `$HOME`, `$PATH`, `$PS1`, etc.

### 5. How do you define and access variables in shell scripting?
To define a variable, use the syntax: `variable_name=value`. For example:
```
name="John"
age=25
```

To access the value of a variable, prefix its name with the `$` symbol. For example:
```
echo $name
echo "My age is $age"
```

### 6. What is the purpose of the `read` command in shell scripting?
The `read` command is used to **read user input from the keyboard** and store it in a variable. It allows you to make your shell scripts interactive. For example:
```
echo "Enter your name: "
read name
echo "Hello, $name!"
```

### 7. How do you perform arithmetic operations in shell scripting?
In shell scripting, you can use the `expr` command to perform arithmetic operations. For example:
```
a=10
b=5
sum=`expr $a + $b`
echo "The sum is: $sum"
```

Note that there should be spaces around the arithmetic operators when using `expr`.

These questions cover some of the key concepts mentioned in your notes, such as shell scripting basics, variables, the `echo` and `read` commands, and arithmetic operations using `expr`.