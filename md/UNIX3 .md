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