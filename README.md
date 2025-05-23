# ls-clone-in-C

A custom implementation of the Unix `ls -l` command using C. This project replicates key functionalities of the original `ls` utility found in Linux systems, including support for various flags like `-a`, `-l`, `-i`, and `-s`.

## 🔧 Features

- Lists directory contents using `opendir()` and `readdir()`
- Supports the following flags:
  - `-a`: Show all files, including hidden ones
  - `-l`: Long format output with detailed metadata
  - `-i`: Display inode numbers
  - `-s`: Display file size in blocks
- Displays:
  - File permissions, owner/group names, file size, modification time
  - Correct file type symbols (e.g., `d` for directories, `-` for regular files)
- Uses POSIX system calls and structures:
  - `stat()`, `getpwuid()`, `getgrgid()`, `ctime()`, `strchr()`, etc.

## 🖥️ Sample Output

```bash
$ ./a.out -l
drwxr-xr-x 2 user1 group1 4096 Apr 23 14:03 Documents
-rw-r--r-- 1 user1 group1  356 Apr 21 09:13 README.md
