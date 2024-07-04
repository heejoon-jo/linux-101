# Process Management (ps, top, kill)

In this section, we'll cover essential commands for managing processes in Linux.

## `ps` (Process Status)

The `ps` command is used to display information about currently running processes.

### Syntax:
```bash
ps [options]
```

### Examples:
```bash
ps         # Display processes owned by the current user
ps aux     # Display all processes in a detailed listing format
ps -ef     # Display all processes in a full listing format
```

### Common Options:
- a: Show processes for all users.
- u: Display more detailed information, including the user that owns the process.
- x: Include processes not attached to a terminal.

## `top`
The `top` command provides a dynamic real-time view of running processes and system resource usage.

### Syntax:
```bash
top
```

### Keybindings:
- q: Quit top.
- k: Kill a process.
- r: Renice a process.

### Example:
```bash
top
```
Note: Press q to exit top.

## `kill`
The `kill` command is used to terminate or send signals to processes.

### Syntax:
```bash
kill [options] pid
```

### Examples:
```bash
kill 1234     # Terminate the process with PID 1234
kill -9 1234  # Forcefully terminate the process with PID 1234
killall firefox   # Terminate all processes named 'firefox'
```

### Common Signals:
- -15 (SIGTERM): Default signal, terminates the process gracefully.
- -9 (SIGKILL): Forces termination of the process.

# Summary
These process management commands (ps, top, kill) are crucial for monitoring system activity, identifying resource-intensive processes, and managing processes effectively in Linux. Understanding how to use these commands is essential for system administrators and advanced users.

For more information and options, refer to the respective manual pages using the man command (e.g., man ps, man top, man kill).
