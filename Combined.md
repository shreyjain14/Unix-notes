# Unix-notes

# MODULE V

### 1. What is Unix and what are some of its key features?
Unix is a powerful operating system initially developed by Ken Thompson and Dennis Ritchie at AT&T Bell laboratories in 1970. Some of its key features include:
- **Multitasking capability**
- **Flexibility and modularity**
- **Hierarchical file system for storing and retrieving information**
- **Written in the C programming language**

### 2. What are the main differences between Unix and Windows operating systems?
- Unix is command-based while Windows is menu-based with a GUI
- Unix is open-source under GPL while Windows is proprietary 
- Unix supports multiprocessing while Windows supports multithreading
- **Unix is generally more secure than Windows**
- Hardware support is more limited in Unix compared to Windows

### 3. What are the roles and responsibilities of a Unix System Administrator?
A Unix System Administrator has various duties including:
- **Installing and maintaining the Unix system**
- **Scripting and programming to resolve system issues**
- Ensuring peripherals are working properly
- **Creating and managing user accounts and passwords**
- Analyzing system performance 
- **Implementing backup and recovery procedures**
- Updating the OS and setting security policies

### 4. What are the steps involved in partitioning disks in Unix?
To partition a disk in Unix, follow these steps:
1. Attach the disk to the proper port
2. Create partitions on the disk (maximum of 4, either all primary or 3 primary + 1 extended)
3. Create a file system on the partition 
4. Mount the file system to make it accessible

### 5. How can you monitor and manage system resource usage in Unix?
Unix provides various tools to monitor and tune major system resources like CPU, memory, disk, I/O, network, etc. Some useful commands are:
- `nice/renice` to modify process scheduling priority
- `netstat` to view network statistics
- `vmstat` for virtual memory statistics
- `top` to view running system tasks and resource usage
- `ps` to report a snapshot of current processes

# Redirection

### 1. What is the file descriptor of the Standard Input File?
The file descriptor **0** is assigned to the standard input file.

### 2. What is the file descriptor of the Standard Error File?
The file descriptor **2** is assigned to the standard error file.

### 3. What are the three types of redirection in UNIX?
The three types of redirection in UNIX are:
- Input redirection (<)
- Output redirection (>)
- Error redirection (2>)

### 4. What is the output of the following command: `$ cat file1 > file2`?
The command `cat file1 > file2` redirects the contents of **file1** to **file2**. If file2 already exists, its contents will be overwritten. If file2 doesn't exist, it will be created.

### 5. What is the output of the following command: `$ cat`?
The `cat` command without any arguments will wait for input from the **keyboard** (standard input) and display the entered text on the **screen** (standard output).

### 6. What is the output of the following command: `$ cat < newfile`?
The command `cat < newfile` takes the contents of **newfile** as input and displays it on the screen (standard output).

### 7. What is the output of the following command: `$ cat para3 para4 para5 >> report`?
The command `cat para3 para4 para5 >> report` appends the contents of files **para3**, **para4**, and **para5** to the end of the file named **report**. If the file report doesn't exist, it will be created.

### 8. What is the output of the following command: `$ date > aaa`?
The command `date > aaa` redirects the output of the `date` command to a file named **aaa**. If the file aaa already exists, its contents will be overwritten. If aaa doesn't exist, it will be created.

### 9. What is the output of the following command: `$ (date;who;ls) > report`?
The command `(date;who;ls) > report` executes the commands `date`, `who`, and `ls` sequentially and redirects their combined output to a file named **report**. If the file report already exists, its contents will be overwritten. If report doesn't exist, it will be created.

### 10. What is the output of the following command: `$ cat aaa > bbb 2 > ccc`?
The command `cat aaa > bbb 2 > ccc` redirects the contents of file **aaa** to file **bbb** and redirects any error messages (file descriptor 2) to file **ccc**. If the files bbb and ccc already exist, their contents will be overwritten. If they don't exist, they will be created.

# UNIX  Environment Variables

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

# UNIX COMMANDSNEW

### 1. What is the purpose of the 'date' command in Unix?
The 'date' command is used to **display the current date and time** in Unix. It can also be used to **format the date and time output** using various options like %H for hour, %M for minute, %d for day of the month, etc.

### 2. How can you display a calendar for a specific year using the 'cal' command?
To display a calendar for a specific year using the 'cal' command, use the syntax:
```
cal <year>
```
For example, to display the calendar for the year 2000, the command would be:
```
cal 2000
```

### 3. What does the 'echo' command do in Unix?
The 'echo' command is used to **print the specified arguments or text to the screen**. For example:
```
echo "Hello World" 
```
This will print "Hello World" on the terminal.

### 4. How can you create a new directory using the command line in Unix?
To create a new directory, use the `mkdir` command followed by the name of the directory you want to create. For example:
```
mkdir mynewdirectory
```
This will create a new directory called "mynewdirectory" in the current working directory.

### 5. What is the difference between the 'cp' and 'mv' commands?
- The `cp` command is used to **copy files or directories from a source to a destination**. The original file remains unchanged.
- The `mv` command is used to **move or rename files and directories**. The original file is removed from the source location.

### 6. How can you search for specific patterns in a file using the 'grep' command?
The `grep` command is used to search for specified patterns in a file. The basic syntax is:
```
grep [options] "pattern" filename
```
For example, to search for the word "error" in a log file named "app.log", the command would be:
```
grep "error" app.log
```

### 7. What is the purpose of the pipe operator (|) in Unix?
The pipe operator `|` is used to **pass the output of one command as the input to another command**. It allows you to chain multiple commands together. For example:
```
cat file.txt | grep "pattern" | wc -l
```
This command will display the contents of "file.txt", search for the specified pattern using `grep`, and then count the number of matching lines using `wc -l`.

### 8. How can you change the file permissions using the 'chmod' command?
The `chmod` command is used to change the permissions of files and directories. The basic syntax is:
```
chmod [options] mode filename
```
For example, to give read, write, and execute permissions to the owner, and read permissions to group and others for a file named "script.sh", the command would be:
```
chmod 744 script.sh
```

### 9. What is the purpose of the 'cat' command in Unix?
The `cat` command is used to **display the contents of a file** on the terminal. It can also be used to **concatenate multiple files** into a single file. For example:
```
cat file1.txt file2.txt > combined.txt
```
This command will concatenate the contents of "file1.txt" and "file2.txt" and redirect the output to a new file named "combined.txt".

### 10. How can you display the top or bottom lines of a file using the 'head' and 'tail' commands?
- The `head` command is used to display the **first few lines** (by default, 10 lines) of a file. For example:
  ```
  head filename.txt
  ```
- The `tail` command is used to display the **last few lines** (by default, 10 lines) of a file. For example:
  ```
  tail filename.txt
  ```
You can also specify the number of lines to display using the `-n` option. For example, `head -n 5 filename.txt` will display the first 5 lines of the file.

# UNIX Process

### 1. What is the difference between a process and a program in Unix?
A **program is a passive entity**, such as contents of a file stored on disk, whereas a **process is an active entity with a program counter specifying the next instruction to execute and a set of associated resources**. A program is elevated to the status of a process when it starts executing.

### 2. What are the different states a process can be in?
A process in Unix can be in the following states:
- NEW: The process is being created
- RUNNING: Instructions are being executed
- WAITING: The process is waiting for some event to occur (such as I/O completion or reception of a signal)
- READY: The process is waiting to be assigned to a processor
- TERMINATED: The process has finished execution

### 3. How are processes created in Unix?
The only way for a user to create a new process in Unix is to invoke the `fork` system call. The process that invokes `fork` is called the **parent process**, and the newly created process is called the **child process**. The `fork` system call creates an exact copy of the parent process.

### 4. What are zombie and orphan processes?
- **Orphan Process**: When a parent process is killed before its child process, the child process becomes an orphan. The `init` process becomes the new parent (PPID) of the orphan process.
- **Zombie Process**: When a child process is killed, the parent process is updated via a SIGCHLD signal. If the parent process does not handle this signal and clean up the child process, the child process becomes a zombie process, which continues to exist in the process table even after termination.

### 5. How can you manage processes using job control in Unix?
The Unix shell provides job control commands to manage processes:
- `&`: Runs a command in the background
- `ctrl-z`: Suspends the current foreground process
- `bg`: Resumes a suspended process and runs it in the background
- `fg`: Brings a background process to the foreground
- `jobs`: Lists the current jobs (processes)
- `kill %<job-id>`: Terminates a specific job based on its job ID

# UNIX1 (1)

### 1. What is the primary goal of an operating system?
The **primary goal of an operating system is to make the computer system convenient to use** for the user. The secondary goal is to use the computer hardware efficiently.

### 2. What are the three broad categories of activities that an operating system is responsible for?
An operating system is responsible for:
- **Essential Functions**: Ensures optimum and effective utilization of resources
- **Monitoring Functions**: Monitors and collects information related to system performance
- **Service Functions**: Provides services to users

### 3. What is the difference between a single-user and multi-user operating system?
- A **single-user operating system**, like DOS, is designed for use by one person at a time on a personal computer.
- A **multi-user operating system** allows more than one user to access the system simultaneously. It is required when multiple programs need to run concurrently or when resources like printers and disks need to be shared by multiple users.

### 4. What are the two types of user interfaces available in Unix operating systems?
Unix operating systems provide two types of user interfaces:
1. **Command User Interface (CUI)**: A simple command-line shell where commands are typed in and executed. Examples include MS-DOS and traditional Unix shells.
2. **Graphical User Interface (GUI)**: A graphical interface similar to Microsoft Windows, called X Window or simply X, is available on modern Unix systems like Linux.

### 5. What is the role of the command interpreter in an operating system?
The command interpreter, also known as the command processor or command line interpreter, is a user interface to the file system, process management system, and protection system. Its role is to:
`Translate the commands keyed in by the user into a language that the CPU can understand, since the CPU cannot directly understand user commands.`

# UNIX2 (1)

### 1. Who developed the UNIX operating system and where was it first created?
The **UNIX operating system was first developed in the 1960s at AT&T Bell Labs by Ken Thompson and Dennis Ritchie**. Thompson and Ritchie rewrote the UNIX kernel in C in 1973, which was a significant step in making the system more portable.

### 2. What are some key features of the UNIX operating system?
Some of the key features of UNIX include:
- Multi-user and multi-tasking capabilities
- Portability across different hardware platforms
- Hierarchical file system
- Pipes and filters for creating complex programs from simple ones
- Powerful shell for user interaction
- Background processing
- Security features like user authentication and file permissions

### 3. Describe the architecture of the UNIX operating system.
The architecture of UNIX is divided into three main levels:
1. The outer layer contains `application programs and utilities` that interact with the user
2. The middle layer is the `shell`, which acts as an interpreter between the user and the kernel
3. The inner layer is the `kernel`, which directly interacts with the hardware and controls system resources

There is only one kernel per system, but each user has their own shell program running.

### 4. What is the role of the shell in the UNIX system?
The shell in UNIX acts as a **command line interpreter (CLI) that mediates between the user and the kernel**. When a user logs in, the shell program is started and presents a prompt to the user. The user types commands which are interpreted by the shell and passed to the kernel for execution. The shell also provides features like I/O redirection, piping, and scripting.

### 5. Name some of the different types of shells available in UNIX.
Some of the common types of shells in UNIX include:
- **Bourne Shell (sh)**: The original shell developed by Stephen Bourne, distributed with UNIX
- **C Shell (csh)**: Developed by Bill Joy, with a syntax resembling the C programming language
- **Korn Shell (ksh)**: Developed by David Korn, combining features of Bourne and C shells
- **Restricted Shell (rsh)**: A restricted version of the Bourne shell, used for guest logins with limited permissions

# UNIX3 

### 1. What is a file in UNIX?
In UNIX, **everything is considered as a file**, including physical devices such as DVD ROMs, USB devices, floppy drives, input/output devices, programs, services, text, images, etc. If something is not a file, it is a process.

### 2. What is the difference between a directory and a file in UNIX?
Some key differences between directories and files in UNIX are:
- A directory can contain other files and sub-directories, while a file cannot contain a directory
- A directory is also considered a special type of file that contains names of other files
- Files contain the actual data/information, while directories are used to organize files in a hierarchical structure

### 3. What is the root directory in UNIX and how is it represented?
The root directory is the top-most directory in the UNIX file system hierarchy. **No directory exists above the root directory**. It serves as the reference/starting point for all files, directories and sub-directories. The root directory is represented by a forward slash (`/`) symbol.

### 4. What are the different types of files in UNIX?
The main types of files in UNIX are:
1. Ordinary/Regular Files - used to store user data, programs, text, etc. Users can modify these files.
2. Directory Files - contain information about files and sub-directories within them. Modified automatically by the system.
3. Device/Special Files - represent physical devices like printers, terminals. Found in `/dev` directory. Cannot be altered by users.

### 5. How are file permissions represented and modified in UNIX?
File permissions in UNIX are represented in the following format: `rwxrwxrwx`
- `r` is for read, `w` is for write, `x` is for execute 
- The first triplet is for user, second for group, third for others
- Permissions can be modified using the `chmod` command in either symbolic or absolute/octal mode
For example: 
```
chmod u=rwx,g=rx,o=r myfile
chmod 754 myfile
```

# UNIX5INODE

### 1. What is an inode in UNIX?
An inode in UNIX is a **data structure that denotes a file or a directory on the file system**. It contains information about the file such as its **location on the disk, access mode, ownership, and file type** (specifically the file's metadata). Each file in UNIX has a **unique inode number** that can be found using the `ls -i` command.

### 2. How does UNIX access files using inodes?
- Internally, UNIX identifies a file by its **unique inode number** associated with it.
- The inode number can be obtained using the command `ls -li`.
- If several slots are available in the inode table, the slot corresponding to the file's inode number **contains information about that file**.

### 3. What are the components of a typical UNIX file system?
A UNIX file system consists of the following components:
- **Boot Block**: The first block of the file system that contains the "Bootstrap Loader" program executed when booting the machine.
- **Super Block**: Describes the state of the file system, including its size, maximum number of files, and available space.
- **Inode Block**: Contains the inode table, which stores information related to all files (but not their contents).
- **Data Blocks**: Store the actual contents of the files. Each allocated block belongs to only one file in the file system.

# Wild Card Characters

### 1. What are wildcards in UNIX?
Wildcards, also known as meta characters, are **symbols or special characters that represent other characters**. They are used with commands like `ls` or `rm` to list or remove files matching a given criteria. The shell interprets these wildcards and returns the results to the command being run.

### 2. What are the main wildcards in UNIX?
The three main wildcards in UNIX are:
- **Asterisk (*)**: Matches one or more occurrences of any character, including no character.
- **Question mark (?)**: Represents or matches a single occurrence of any character.
- **Bracketed characters ([])**: Matches any occurrence of the characters enclosed in the square brackets. It can include alphanumeric characters, numbers, letters, and other special characters.

### 3. How do regular expressions differ from wildcards in UNIX?
Regular expressions are used when you want to search for specific lines of text containing a particular pattern. They provide more advanced pattern matching capabilities compared to wildcards. Some common regular expression symbols include:
```
^ - matches the beginning of the line
$ - matches the end of the line
. (dot) - matches a single character
[abc] - matches any of the characters included within the square brackets
[^abc] - matches any character not included within the square brackets
[a-e] - matches any character within the specified range (a, b, c, d, or e)
```

# UNIX7Filters

### 1. What is a filter in Unix?
A filter is a program that takes its input from the standard input, processes (or filters) it, and sends the output to the standard output. Unix has a rich set of filters which can be used to work on data in an effective way. Some examples of filters are: cat, grep, sort, paste, pg, more, wc, tr, cut, less, head, tail, tee, sed, and uniq.

### 2. What does the grep filter do and what is its syntax?
The grep filter searches a file for a particular pattern of characters and displays all lines that contain that pattern. The pattern that is searched for in the file is referred to as the regular expression (grep stands for "Global regular expression print"). The syntax of the grep command is:
`grep regular_expression filename`

### 3. Explain the function of the following grep options:
- `-n`: This prints each line matching the pattern along with its line number. The number is printed at the beginning of the line.
- `-c`: This prints only a count of the lines that match a pattern.
- `-v`: This prints out all those lines that do not match the pattern specified by the regular expression.
- `-i`: Matches either upper or lowercase.
- `-l`: Prints only the names of files with matching lines (letter "l").

### 4. What is the difference between grep, fgrep, and egrep?
- `grep`: The standard grep command for searching patterns in files.
- `fgrep`: Faster than grep, but with the same features. Used for searching strings from multiple files.
- `egrep`: Combination of grep and fgrep features.

### 5. What does the wc filter do and what are its options?
The wc filter is used to count the number of lines, words, and characters in a disk file or in the standard input. The options for wc are:
- `wc -l`: Displays the number of lines
- `wc -w`: Displays the number of words
- `wc -c`: Displays the number of characters

### 6. Explain the function of the tr filter with examples.
The tr filter can be used to translate one set of characters to another, convert new lines into spaces, or squeeze multiple occurrences of a character into one. Some examples:
- `tr 'S' 'N' file1`: Wherever capital S is available, it is converted into capital N.
- `tr 'aeiou' 'U'`: Wherever lowercase vowels (a, e, i, o, u) are available, they are converted into capital U.
- `tr -d '0-9' file1`: Wherever numbers are available, they are deleted.
- `tr -s 'l'`: Squeezes multiple occurrences of the letter 'l' into one.

### 7. What is a pipe (|) in Unix and how is it used?
A pipe (|) is used to send the output of one command as input to another command for further processing. It allows filters and commands to be combined so that the standard output of one filter or command can be sent as standard input to another file or command. There is no limit to the number of filters or commands that can be used in a pipe. For example:
`ls -l | grep "Aug" | sort +4n`
This pipe consists of the ls, grep, and sort commands to list files modified in August and sort them by size.

# UNIXvi editor

### 1. What is the default editor that comes with the UNIX operating system?
The default editor that comes with the UNIX operating system is called **vi (Visual editor)**.

### 2. What are the advantages of using the vi editor?
The advantages of using the vi editor are:
- It is available on all flavors of Unix systems
- It requires very few resources
- It is more user-friendly than other editors such as ed and ex
- An improved version called vim is also available

### 3. What are the three modes of operation in the vi editor?
The three modes of operation in the vi editor are:
1. Command mode
2. Insert mode 
3. Last Line mode (also known as Execute or Escape mode)

### 4. How do you enter and exit insert mode in vi?
To enter insert mode in vi, simply type `i` while in command mode. To exit insert mode and return to command mode, press the `Esc` key.

### 5. What are some basic navigation keys used to move the cursor in vi?
Some basic navigation keys to move the cursor in vi are:
- `h` - move one character to the left
- `j` - move down one line 
- `k` - move up one line
- `l` - move one character to the right
- `0` - move to the beginning of the current line
- `$` - move to the end of the current line

### 6. How can you delete characters or lines in vi?
Some commands to delete characters or lines in vi are:
- `x` - delete the character under the cursor
- `dw` - delete from cursor to the end of the current word
- `dd` - delete the entire current line
- `5dd` - delete 5 lines starting from the current line

### 7. What are the commands to copy and paste text in vi?
The basic commands to copy (yank) and paste text in vi are:
- `yy` - yank (copy) the current line
- `5yy` - yank 5 lines starting from the current one
- `p` - put (paste) the copied text after the cursor
- `P` - put (paste) the copied text before the cursor

### 8. How do you save changes and exit vi?
To save changes and exit vi, use the following commands:
- `:w` - write (save) the file
- `:wq` - write and quit 
- `:x` - same as :wq
- `ZZ` - same as :wq
To quit vi without saving changes, use:
- `:q!` - quit and discard any changes

# all seperate.

PK
