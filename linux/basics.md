# Linux Basics – Quick Revision (with Concepts)
---

## Terminal Basics

* Terminal = command-line interface to control system
* Commands = instructions given to the system

Why it matters:
DevOps engineers manage servers, cloud systems, and automation mainly through terminal, not GUI.

---

## Core Navigation Commands

* pwd → show current location
* ls → list files/folders
* ls -a → show hidden files
* ls -l → detailed info
* ls -la → all + detailed
* cd <folder> → move into folder
* cd .. → move up
* cd ~ → go home

Why it matters:
Before doing anything, you must know:

* where you are
* what exists

Prevents mistakes like editing or deleting wrong files.

---

## File & Folder Operations

* mkdir <name> → create folder
* touch <file> → create file
* cp <src> <dest> → copy
* mv <src> <dest> → move/rename
* rm <file> → delete (permanent)

Why it matters:
DevOps work involves managing:

* configs
* scripts
* logs
* application files

Everything is file-based.

---

## Paths

* Path = location of file/folder

Absolute Path:

* Full path from root
* Example: /Users/name/Desktop/project

Relative Path:

* Based on current location
* Example: cd project

Why it matters:
Wrong path = broken scripts, failed deployments, system errors.

---

## Special Symbols

* ~ → home directory
* . → current directory
* .. → parent directory

Why it matters:
Used in navigation, scripting, and automation.

---

## Hidden Files

* Start with dot (.)
* Examples: .env, .git
* Not visible with ls
* Use ls -a

Why it matters:
Hidden files store:

* environment variables
* secrets/config
* version control data

Ignoring them = missing critical system behavior.

---

## File Details & Permissions

* ls -l shows:

  * permissions
  * owner
  * size
  * date

Permissions:

* r = read
* w = write
* x = execute

Why it matters:
Incorrect permissions can:

* break scripts
* stop applications
* cause security issues

---

## Key Workflow Habit

1. pwd → where am I
2. ls → what is here
3. cd → navigate
4. perform action

# File Handling

## cat
Reads file content

Example:
cat file.txt

Why it matters:
Used to read configs, logs, and scripts.

---

## echo
Prints text or writes to file

Example:
echo "Hello"

---

## > (overwrite)
Writes content into file (replaces existing content)

Example:
echo "text" > file.txt

---

## >> (append)
Adds content to file without removing existing content

Example:
echo "text" >> file.txt

---

## Key Understanding
Files are not just created—they store and transfer data.
This is important for logs, configs, and automation in DevOps.