### 1. What is an environment variable in Unix?
An **environment variable** in Unix is a variable that is available to any child process of the shell. It is used to provide information to the programs you use. Environment variables can be either **system-defined** or **user-defined**.

### 2. How can you view and modify shell environment variables?
Shell environment variables can be viewed and modified using the following syntax:
- To view the value of a variable: `echo $VARIABLE`
- To set a new value for a variable: `VARIABLE=value`
- To remove a variable: `unset VARIABLE`

### 3. What are some common environment variables in Unix?
Some common environment variables in Unix include:
- `PATH`: Specifies the directories to search for executable files
- `HOME`: Specifies the user's home directory
- `TERM`: Specifies the terminal type
- `PS1`: Specifies the primary command prompt string
- `LOGNAME`: Specifies the user's login name

### 4. What is the difference between shell variables and environment variables?
The main difference is in their scope:
- **Shell variables** exist only in the shell where they are defined
- **Environment variables** exist in the current shell and all its child processes

### 5. What is the purpose of the `.profile` file?
The `.profile` file is a special shell script that is executed when a user logs in. It is used to set environment variables and other standard settings for the system. For example:
```
HOME=/usr/roger
PATH=:/bin:/usr/bin
LOGNAME=roger
PS1="$"
export HOME PATH LOGNAME PS1
```