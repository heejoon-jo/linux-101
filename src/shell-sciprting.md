# Introduction to Shell Scripting

## What is Shell Scripting?

Shell scripting is a way to automate tasks in Unix-like operating systems using the command-line interface. It involves writing a series of commands in a file that can be executed as a program.

## Why Learn Shell Scripting?

- Automate repetitive tasks
- Perform system administration
- Create powerful command-line tools
- Enhance productivity

## Basic Concepts

### Shebang

The shebang (`#!`) is used at the beginning of a script to specify which interpreter should run the script.

Example:
```bash
#!/bin/bash
```

Comments
Use # for single-line comments:
```bash
# This is a comment
```

Variables
Declare and use variables:
```bash
name="John"
echo "Hello, $name!"
```

Command Substitution
Use command output as a value:
```bash
current_date=$(date +%Y-%m-%d)
echo "Today is $current_date"
```

Control Structures
If-Else Statements
```bash
if [ "$1" -gt 10 ]; then
    echo "Number is greater than 10"
elif [ "$1" -eq 10 ]; then
    echo "Number is equal to 10"
else
    echo "Number is less than 10"
fi
```

Loops
For Loop
```bash
for i in {1..5}
do
    echo "Iteration $i"
done
```

While Loop
```bash
count=1
while [ $count -le 5 ]
do
    echo "Count: $count"
    ((count++))
done
```

Functions
Define and use functions:
```bash
greet() {
    echo "Hello, $1!"
}

greet "Alice"
```

Input and Output
Command-line Arguments
Access command-line arguments:
```bash
echo "Script name: $0"
echo "First argument: $1"
echo "Second argument: $2"
```

Reading User Input
```bash
echo "Enter your name:"
read name
echo "Hello, $name!"
```

File Operations
Reading Files
```bash
while IFS= read -r line
do
    echo "$line"
done < "input.txt"
```

Writing to Files
```bash
echo "This is a new line" >> output.txt
```

Practical Examples
Example 1: Backup Script
```bash
#!/bin/bash

source_dir="/path/to/source"
backup_dir="/path/to/backup"
date=$(date +%Y%m%d)

tar -czf "$backup_dir/backup_$date.tar.gz" "$source_dir"

echo "Backup created: backup_$date.tar.gz"
```

Example 2: System Information Script
```bash
#!/bin/bash

echo "System Information:"
echo "==================="
echo "Hostname: $(hostname)"
echo "OS: $(uname -s)"
echo "Kernel Version: $(uname -r)"
echo "CPU: $(lscpu | grep 'Model name' | cut -f 2 -d ":")"
echo "Memory: $(free -h | awk '/^Mem:/ {print $2}')"
echo "Disk Usage: $(df -h / | awk '/\// {print $5}')"
```

Best Practices
- Use meaningful variable names
- Comment your code
- Use proper indentation
- Test your scripts thoroughly
- Use shellcheck for linting

Conclusion
- Recap of key concepts
- Encourage further exploration and practice
- Provide resources for advanced topics
