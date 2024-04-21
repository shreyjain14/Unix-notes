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