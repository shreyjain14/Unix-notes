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