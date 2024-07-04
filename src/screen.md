# Screen Session Manual

Screen is a terminal multiplexer that allows you to manage multiple terminal sessions within a single window or remotely, detach and reattach sessions, and more. This manual provides an overview of basic commands and operations for using `screen`.

## Starting and Managing Screen Sessions

### Start a New Screen Session
To start a new screen session, simply type:
```bash
screen
```

### List Existing Screen Sessions
To list all existing screen sessions:

```bash
screen -ls
```

### Attach to an Existing Session
To attach to a running screen session:

```bash
screen -r [session_id]
```
Replace [session_id] with the ID of the session listed by screen -ls.

### Detach from a Screen Session
To detach from a screen session (without terminating it):
- Press Ctrl + A, then d

#### Working with Screen Windows
Create a New Window
Press Ctrl + A, then c

Navigate Between Windows
- Press Ctrl + A, then n (next window)
- Press Ctrl + A, then p (previous window)
- Press Ctrl + A, then [window_number] (switch to a specific window)

### Close a Window
- Exit the shell in the window (exit command) or press Ctrl + D.

### Screen Session Management
#### Rename a Screen Session
- To rename the current screen session:
- Press Ctrl + A, then :
Type sessionname [new_name] and press Enter

### Terminate a Screen Session
To terminate (kill) the current screen session:
- Exit all windows within the session, or
- Type exit in the shell for each window, or
-   Press Ctrl + A, then :quit or :exit


### Exiting Screen
To terminate screen and all its sessions:

- Press Ctrl + A, then :quit or :exit
- Or simply type exit in all open windows

# Summary
Screen is a powerful tool for managing terminal sessions, allowing users to multiplex and manipulate multiple sessions from a single terminal window, detach and reattach sessions, and more. Mastering screen can enhance productivity, especially in remote or long-running tasks where session persistence is crucial.
