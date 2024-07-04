# Working with Directories (mkdir, rmdir)

In this section, we'll cover basic operations for working with directories in Linux.

## `mkdir` (Make Directory)

The `mkdir` command is used to create directories (folders) in the filesystem.

### Syntax:
```bash
mkdir [options] directory_name
```

### Examples:
```bash
mkdir mydirectory   # Create a directory named mydirectory in the current location
mkdir /path/to/newdirectory   # Create a directory named newdirectory in the specified path
mkdir -p /path/to/parent/child   # Create parent directories if they do not exist (-p option)
```

## `rmdir` (Remove Directory)
The `rmdir` command is used to remove (delete) empty directories from the filesystem.

### Syntax:
```bash
rmdir [options] directory_name
```

### Examples:
```bash
rmdir mydirectory   # Remove (if empty) the directory named mydirectory from the current location
rmdir /path/to/directory   # Remove (if empty) the directory named directory from the specified path
```
Note: The rmdir command only removes directories that are empty. To remove directories and their contents recursively, use the rm -r command.

# Summary
Understanding how to create (mkdir) and remove (rmdir) directories is essential for managing directory structures in Linux efficiently. These commands are straightforward but powerful tools in the Linux filesystem.

For more information and options, refer to the respective manual pages using the man command (e.g., man mkdir, man rmdir).
