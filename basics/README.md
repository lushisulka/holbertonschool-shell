# Shell Basics – Learning Guide

## 1. Introduction

This project introduces the fundamentals of Shell scripting and Linux command-line operations.

It focuses on understanding how to interact with the operating system, navigate directories, manage files, execute commands, and automate basic tasks using Bash.

## 2. Essential Concepts

**Shell:** A command-line interpreter that allows users to communicate with the operating system.

**Bash:** A widely used Shell that allows users to execute commands and create scripts.

**Terminal:** The application where users type and execute commands.

**Shell Script:** A text file containing commands that are executed sequentially by a Shell interpreter.

**Shebang (`#!/bin/bash`):** The first line of a script, specifying which interpreter should execute it.

**Filesystem:** The structure used by an operating system to organize files and directories.

**Directory:** A location used to organize files and other directories.

**Path:** The location of a file or directory in the filesystem.

- Absolute path: Starts from the root directory (`/`).
- Relative path: Starts from the current working directory.

## 3. Important Shell Commands

| Command | Explanation |
|---|---|
| `pwd` | Displays the current working directory. |
| `ls` | Lists files and directories. |
| `cd` | Changes the current directory. |
| `mkdir` | Creates directories. |
| `touch` | Creates empty files. |
| `mv` | Moves or renames files. |
| `cp` | Copies files. |
| `rm` | Removes files. |
| `rmdir` | Removes empty directories. |
| `ln -s` | Creates symbolic links. |
| `file` | Identifies file types. |
| `cat` | Displays file contents. |
| `chmod` | Changes file permissions. |

## 4. Important Shell Operators and Symbols

- `~` – Represents the user's home directory.
- `.` – Represents the current directory.
- `..` – Represents the parent directory.
- `/` – Separates directory names and represents the root directory.
- `*` – Wildcard matching multiple characters.
- `|` – Pipe operator; sends the output of one command to another.
- `>` – Redirects output to a file, replacing its contents.
- `>>` – Appends output to a file.
- `&&` – Executes the next command only if the previous command succeeds.
- `;` – Separates commands.
- `#` – Introduces a comment in a Shell script.

## 5. File Permissions

Linux uses permissions to control access to files and directories.

There are three main permission types:

- `r` (Read): Allows reading a file.
- `w` (Write): Allows modifying a file.
- `x` (Execute): Allows executing a file.

Permissions are assigned to three categories:

- User: The file owner.
- Group: Users belonging to the file's group.
- Others: All other users.

### Understanding chmod

`chmod` means Change Mode. It changes file permissions.

Example:

```bash
chmod +x filename
```

Adds executable permission to a file.

```bash
chmod 755 filename
```

Sets read, write, and execute permissions for the owner, and read and execute permissions for the group and others.

### Checking permissions

```bash
ls -l
```

Displays file permissions and additional file information.

## 6. Wildcards and Pattern Matching

Wildcards allow commands to match multiple files based on their names.

Examples:

- `*.txt` – Matches all files ending in `.txt`.
- `*~` – Matches files ending in `~`.
- `[[:upper:]]*` – Matches names beginning with an uppercase letter.
- `.*` – Matches hidden filenames beginning with a dot.

These patterns make it easier to perform operations on multiple files.

## 7. Symbolic Links

A symbolic link is a special file that points to another file or directory.

Example:

```bash
ln -s /bin/ls my_link
```

This creates a symbolic link named `my_link` pointing to `/bin/ls`.

Symbolic links are similar to shortcuts and help access files from different locations.

## 8. Pipes and Redirection

Pipes and redirection allow commands to work together and control where their output goes.

**Pipe (`|`):** Sends the output of one command as input to another.

Example:

```bash
ls | sort
```

**Output redirection (`>`):** Writes command output into a file, replacing existing content.

**Append redirection (`>>`):** Adds command output to the end of a file.

These techniques help build more powerful Shell commands.

## 9. Executing Shell Scripts

To execute a Bash script:

1. Create the script.
2. Add the Bash shebang.
3. Write the required commands.
4. Give the script executable permission.
5. Execute it.

Example:

```bash
chmod +x script_name
./script_name
```

Alternatively:

```bash
bash script_name
```

**Important difference:**

- `./script_name` executes the script in a separate process.
- `source script_name` executes it in the current Shell session.

This distinction is important when a script needs to change the current terminal directory.

## 10. Git and Version Control

Git is a version control system used to track changes in files and projects.

Important Git commands:

| Command | Purpose |
|---|---|
| `git status` | Checks the current repository status. |
| `git add` | Stages changes. |
| `git commit` | Saves staged changes locally. |
| `git push` | Uploads commits to a remote repository. |
| `git pull` | Downloads and integrates remote changes. |
| `git log` | Displays commit history. |

### Typical Git Workflow

```bash
chmod +x filename
git add filename
git update-index --chmod=+x filename
git commit -m "Add descriptive commit message"
git push
```

This workflow prepares a script, stages it, records its executable permission, creates a commit, and uploads the changes to GitHub.

## 11. Useful Linux Concepts

**Root (`/`):** The starting point of the Linux filesystem.

**Home directory (`~`):** The personal directory of a user.

**Hidden files:** Files whose names begin with a dot (`.`).

**Environment:** The configuration and variables available to Shell processes.

**Process:** A running instance of a program or command.

**Exit status:** A numerical value indicating whether a command succeeded or failed. Usually, `0` means success and a non-zero value indicates an error.

**Manual (`man`):** Documentation that explains how Linux commands work.

Example:

```bash
man ls
```

## 12. Key Takeaways

Through Shell Basics, I developed foundational knowledge of:

- Linux command-line navigation.
- File and directory management.
- Bash scripting fundamentals.
- File permissions and execution.
- Wildcards and pattern matching.
- Symbolic links.
- Pipes and output redirection.
- Git and version control.

These concepts provide an important foundation for working with Linux systems, writing scripts, automating tasks, and developing software.