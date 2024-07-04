# Text Editing (nano, vim)

In this section, we'll cover basic text editing using two popular command-line text editors in Linux: `nano` and `vim`.

## `nano`

`nano` is a simple and user-friendly text editor for Unix-like systems. It's ideal for beginners and those who prefer straightforward editing capabilities.

### Opening a File:
```bash
nano filename
```

### Keybindings:
Ctrl + O: Write out (save) the current file
Ctrl + X: Exit the editor

### Basic Navigation:
Use arrow keys to move around
Page Up/Page Down to navigate larger files
### Example:
```bash
nano example.txt
```

## `vim`
`vim` (Vi IMproved) is a powerful and highly configurable text editor built to enable efficient text editing. It's popular among more advanced users and programmers.
```
### Opening a File:
```bash
vim filename
```

### Modes:
- Normal Mode: For navigation and executing commands
- Insert Mode: For inserting and editing text
- Command-Line Mode: For entering commands
### Keybindings:
- i: Switch to Insert mode
- Esc: Return to Normal mode
- : Write (save) the current file
- : Quit the editor
- : Write and quit (save and exit)

### Example:
```bash
vim example.txt
```

# Summary
Both nano and vim are powerful text editors in Linux, catering to different levels of expertise and preferences. Learning to use at least one of these editors is essential for efficient text editing and programming on Linux systems.

For more information and advanced features, refer to the respective manual pages using the man command (e.g., man nano, man vim).
