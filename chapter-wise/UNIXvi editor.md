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