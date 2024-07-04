# Filesystem Hierarchy

The filesystem hierarchy in Linux defines the structure of directories and the organization of files on a Linux system. Understanding this hierarchy is crucial for navigating the filesystem and locating important system files and user data.

## / (Root Directory)

The root directory is the top-level directory in the filesystem hierarchy. It contains all other directories and files on the system.

### Important Directories:

- **/bin**: Essential command binaries required for system boot and repair.
- **/boot**: Files required for booting the operating system.
- **/etc**: System-wide configuration files and scripts.
- **/home**: Home directories for user accounts.
- **/lib** and **/lib64**: Essential shared libraries and kernel modules.
- **/opt**: Optional software packages.
- **/sbin**: Essential system binaries.
- **/usr**: User-related programs and data.
- **/var**: Variable data files (e.g., logs, databases).

## Common Files and Directories:

- **/etc/passwd**: User account information.
- **/etc/fstab**: Filesystem table.
- **/var/log**: Log files.
- **/tmp**: Temporary files.

## Symbolic Links:

Linux uses symbolic links (symlinks) to create shortcuts or references to files and directories. They appear similar to shortcuts in Windows.

### Example:

$ ls -l /bin/sh
lrwxrwxrwx 1 root root 4 Jan 1 00:00 /bin/sh -> bash

In this example, `/bin/sh` is a symbolic link pointing to `/bin/bash`.

## Understanding Permissions:

Permissions on files and directories control who can read, write, or execute them. They are represented by a combination of letters and symbols.

### Example:

$ ls -l /etc/passwd
-rw-r--r-- 1 root root 1000 Jan 1 00:00 /etc/passwd


In this example, `-rw-r--r--` indicates the file permissions.

## Summary:

Understanding the Linux filesystem hierarchy is essential for Linux users and administrators. It facilitates efficient navigation, maintenance, and troubleshooting of Linux systems.

For more details, refer to the [Filesystem Hierarchy Standard (FHS)](https://refspecs.linuxfoundation.org/FHS_3.0/fhs/index.html).
