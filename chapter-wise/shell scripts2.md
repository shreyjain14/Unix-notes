### 1. What are the basic arithmetic operators supported in shell scripting?
The basic arithmetic operators supported in shell scripting are:
- Addition (`+`)
- Subtraction (`-`) 
- Multiplication (`*`)
- Division (`/`)
- Modulus (`%`)

### 2. How can you perform arithmetic operations in shell scripts?
There are a few ways to perform arithmetic operations in shell scripts:
- Using the `expr` command: 
  ```
  val=`expr $a + $b`
  ```
- Using double parentheses:
  ```
  echo "a + b = $((a + b))"
  ```
- Using the `let` command:
  ```
  let "result = a + b"
  ```

### 3. What are the relational operators used in shell scripting?
The relational operators used in shell scripting include:
- `-eq`: Checks if the values are equal
- `-ne`: Checks if the values are not equal
- `-gt`: Checks if the left operand is greater than the right operand
- `-lt`: Checks if the left operand is less than the right operand
- `-ge`: Checks if the left operand is greater than or equal to the right operand
- `-le`: Checks if the left operand is less than or equal to the right operand

### 4. How can you compare strings in shell scripting?
Strings can be compared using the following operators:
- `=`: Checks if the strings are equal
- `!=`: Checks if the strings are not equal
- `-z`: Checks if the string is empty (zero length)
- `-n`: Checks if the string is not empty

Example:
```sh
if [ "$str1" = "$str2" ]
then
  echo "Strings are equal"
else
  echo "Strings are not equal"
fi
```

### 5. What are the file test operators in shell scripting?
Some commonly used file test operators in shell scripting are:
- `-e file`: Checks if the file exists
- `-f file`: Checks if the file exists and is a regular file
- `-d file`: Checks if the file exists and is a directory
- `-r file`: Checks if the file exists and is readable
- `-w file`: Checks if the file exists and is writable
- `-x file`: Checks if the file exists and is executable
- `-s file`: Checks if the file exists and has a size greater than zero

### 6. What is the syntax of the `if-else` statement in shell scripting?
The basic syntax of the `if-else` statement in shell scripting is:
```sh
if [ condition ]
then
  # commands to execute if condition is true
else
  # commands to execute if condition is false
fi
```

You can also use `elif` for multiple conditions:
```sh
if [ condition1 ]
then
  # commands to execute if condition1 is true
elif [ condition2 ]
then
  # commands to execute if condition2 is true
else
  # commands to execute if all conditions are false
fi
```