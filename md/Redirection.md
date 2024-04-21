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