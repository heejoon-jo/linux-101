# Basic Commands - Navigation (cd, ls, pwd)

In this section, we'll cover some fundamental commands for navigating the Linux filesystem.

## `cd` (Change Directory)

The `cd` command is used to change the current working directory.

### Syntax:
```bash
cd [directory]
```
Examples:

```bash
cd /           # Change to the root directory
cd ~           # Change to the user's home directory
cd ~/Desktop   # Change to the Desktop directory within the home directory
cd ..          # Move up one directory level
cd Documents   # Change to the Documents directory (assuming it exists in the current directory)
```

## `ls` (List Directory Contents)
The ls command is used to list information about files and directories in the current directory.


### Syntax:
ls [options] [files or directories]


Examples:
```bash
ls           # List files and directories in the current directory
ls -l        # List files in long format (detailed listing)
ls -a        # List all files, including hidden files
ls -lh       # List files in long format with human-readable file sizes
ls /usr/bin  # List files and directories in the /usr/bin directory
```

## `pwd` (Print Working Directory)
The pwd command prints the full path of the current working directory.

### Syntax:
pwd (Print Working Directory)
The pwd command prints the full path of the current working directory.

Syntax:
```bash
pwd
```

Example:
pwd   # Output: /home/user/Documents (if you are currently in the Documents directory)

## Summary
Mastering these basic navigation commands (cd, ls, pwd) is essential for efficient navigation and management of files and directories in Linux.

For more information, refer to the respective manual pages using man command (e.g., man cd, man ls, man pwd).
