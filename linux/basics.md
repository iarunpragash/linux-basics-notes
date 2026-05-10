Terminal Basics
Terminal = command-line interface to control system
Commands = instructions given to the system

Why it matters:
DevOps engineers manage:
- servers
- cloud systems
- automation
mainly through terminal instead of GUI.

--------------------------------------------------

Core Navigation Commands

pwd → show current location
ls → list files/folders
ls -a → show hidden files
ls -l → detailed info
ls -la → all + detailed
cd → move into folder
cd .. → move up
cd ~ → go home

Why it matters:
Before doing anything, you must know:
- where you are
- what exists

Prevents mistakes like:
- editing wrong files
- deleting wrong folders
- running commands in wrong locations

--------------------------------------------------

File & Folder Operations

mkdir → create folder
touch → create file
cp → copy
mv → move/rename
rm → delete (permanent)

Why it matters:
DevOps work involves managing:
- configs
- scripts
- logs
- application files

Everything in Linux is file-based.

--------------------------------------------------

Paths

Path = location of file/folder

Absolute Path:
Full path from root

Example:
/Users/name/Desktop/project

Relative Path:
Based on current location

Example:
cd project

Why it matters:
Wrong path can cause:
- broken scripts
- failed deployments
- missing files
- system errors

--------------------------------------------------

Special Symbols

~ → home directory
. → current directory
.. → parent directory

Why it matters:
Used heavily in:
- navigation
- scripting
- automation
- deployment workflows

--------------------------------------------------

Hidden Files

Hidden files start with dot (.)

Examples:
.env
.git
.zshrc

Not visible using:
ls

Use:
ls -a

Why it matters:
Hidden files store:
- environment variables
- secrets/configuration
- Git data
- shell settings

Ignoring them can cause:
- missing configurations
- deployment failures
- unexpected system behavior

--------------------------------------------------

File Details & Permissions

Command:
ls -l

Shows:
- permissions
- owner
- group
- size
- modified date
- filename

Permissions:
r = read
w = write
x = execute

--------------------------------------------------

Permission Output Example

-rw-r--r--  1 yourname  staff  25 Apr  2 10:00 hello.sh

Breakdown:

First Character:
- = regular file

Owner Permissions:
rw-
r = read
w = write
- = no execute permission

Group Permissions:
r--
r = read only

Others Permissions:
r--
r = read only

Meaning:
The owner can:
- read
- modify

Others can:
- only read

Script cannot execute because x is missing.

--------------------------------------------------

After chmod +x

Command:
chmod +x hello.sh

Output:
-rwxr-xr-x  1 yourname  staff  25 Apr  2 10:01 hello.sh

Breakdown:

First Character:
- = regular file

Owner Permissions:
rwx
r = read
w = write
x = execute

Group Permissions:
r-x
r = read
x = execute

Others Permissions:
r-x
r = read
x = execute

Meaning:
The script is now executable.

--------------------------------------------------

Why Permissions Matter

Incorrect permissions can:
- break scripts
- stop applications
- block deployments
- create security issues

Permissions are very important in:
- cloud servers
- Docker containers
- CI/CD pipelines
- deployment scripts

--------------------------------------------------

Key Workflow Habit

pwd → where am I
ls → what is here
cd → navigate
perform action

--------------------------------------------------

File Handling

cat
Reads file content

Example:
cat file.txt

Why it matters:
Used to read:
- configs
- logs
- scripts

--------------------------------------------------

less

Opens file page-by-page

Example:
less file.txt

Useful for:
- large logs
- long configuration files

Controls:
q → quit

--------------------------------------------------

head

Shows first lines of file

Example:
head file.txt

Useful for:
- checking beginning of logs/files

--------------------------------------------------

tail

Shows last lines of file

Example:
tail file.txt

Useful for:
- checking latest logs
- monitoring application output

--------------------------------------------------

echo

Prints text or writes into file

Example:
echo "Hello"

--------------------------------------------------

Output Redirection

> (overwrite)
Writes content into file and replaces old content

Example:
echo "text" > file.txt

--------------------------------------------------

>> (append)

Adds content without removing old data

Example:
echo "text" >> file.txt

--------------------------------------------------

Searching Files & Content

find
Search files/folders

Example:
find . -name "config.txt"

Why it matters:
Used to locate:
- logs
- configs
- scripts
- deployment files

--------------------------------------------------

grep

Search inside file contents

Example:
grep "port" config.txt

Why it matters:
Used for:
- searching logs
- finding errors
- checking configuration values
- filtering outputs

--------------------------------------------------

Pipes

| = pipe

Sends output of one command into another command

Example:
cat config.txt | grep "port"

Meaning:
- cat reads file
- pipe transfers output
- grep filters matching result

Why it matters:
Pipes are heavily used in:
- automation
- monitoring
- deployment scripting
- log analysis

--------------------------------------------------

Basic Process Understanding

Process = running program

Examples:
- terminal
- browser
- server
- database

Command:
ps

Shows running processes.

Why it matters:
Applications depend on processes.
If process fails:
- application crashes
- deployment fails
- services stop working

