# Essential Linux Commands
## Objective
This documentation manual aims to offer a step by step guide on basic Linux commands for Linux users to master a skillset for an effective and productive use of Linux environment on file management, navigation, text editing, and system administration tasks. It introduces the basic to intermediate commands on the Linux command line with explanations, syntax examples, and use cases to enhance your competence of system management using the Linux command-line.
# 1. Basic Commands
## 1.1  Navigation and File Operations
Navigation and file operations in Linux involve a set of essential commands that allow users to interact with the filesystem
## i. 'pwd' Command - Print Working Directory
pwd, an acronym for "present working directory," displays the current directory's full path.

pwd command syntax:`pwd`
![pwd command](./img/01.png)
## ii. 'ls' Command - List directory contents
The ls command lists files and directories in the current directory. 

ls command syntax:`ls`
![ls command](./img/02.png)

For example, ls -a displays all files, including hidden ones.

command syntax:`ls -a`
![ls -a command](./img/03.png) 
## iii. 'cd' Command - Change directory
The cd command, short for "change directory," allows users to switch directories. If no directory is specified, it defaults to the user's home directory.

cd command syntax:`cd [directory]`
![cd command](./img/04.png)
## iv. 'cp' Command - Copy files or directories
The cp command copies files or directories to a specified location, useful for creating backups or duplicating data.

cp command syntax:`cp [option] source destination`

`cp filename.txt /path/to/destination/`

![cp command](./img/05.png) 

To confirm the file was copied to the Downloads directory, use the cd command to navigate to the destination (Downloads) directory and list the contents with the ls command.
![cp confirmation](./img/06.png)
## v. 'mv' Command - Move/rename files or directories
The mv command moves or renames files and directories. If the destination exists, it will be overwritten.

mv command syntax: `mv [options] source destination`
![mv command](./img/07.png) 

Use the ls command to verify the mv command operation. 
![mv confirmation](./img/08.png)
## vi. 'rm' Command - Remove files or directories
The rm command deletes files or directories. Multiple files can be removed simultaneously. ls command used to verify the rm command.

rm command syntax: `rm [options] file(s)`

to remove a single file syntax: `rm filename.txt`
![rm command](./img/9.png)

to remove multiple file syntax: `rm file1.txt file2.txt file3.txt`
![rm multiple files command](./img/10a.png)

to remove directory syntax: `rm -r directoryname`
![rm director files command](./img/10b.png)

to force remove a file or directory without prompting for confirmation: `rm -f filename.txt`
![rm files/director command](./img/10c.png)

to force remove a directory and its contents without prompting for confirmation: `rm -rf directoryname`
![rm director with content command](./img/10d.png)

## vii. 'mkdir' Command - Create a new directory
The mkdir command creates new directories. Multiple directories an be created simultaneously.

mkdir command syntax: `mkdir directory.name`
![mkdir command](./img/11.png) 

Use the ls command to verify the mkdir command operation.
![mkdir confirmation](./img/12.png)

## viii. 'touch' Command - Create an empty file or update the timestamp
The touch command creates an empty file or updates the timestamp of an existing file.

touch command syntax: `touch file.name`
![touch command](./img/13.png)

Use the ls command to verify the touch command operation.
![touch confirmation](./img/14.png)
## 1.2 Viewing and Editing Files
There are bunch of Linux commands and text editors that come in handy when you need to check out or make changes, to files. Tools like cat, more, less, head and tail help you peek into file contents in ways. When it comes to editing nano is an user friendly text editor option while vi caters to those looking for advanced functionalities. These tools are crucial for navigating through files, in a Linux setup.
## i. 'cat' command - Concatenate and display file content
cat, short for "concatenate," reads, combines, and displays file contents. Use cat followed by the file name to execute.

cat command syntax:`cat filename.txt`
![cat command](./img/15.png)

## ii. 'more' command - View file content interactively
more command displays the contents of a file, one screen at a time in the terminal. It’s useful if you have a large ﬁle. For instance, cat displays the entire contents of a file all at once. Using more, you navigate through the ﬁle, page by page. It’s quite handy for large ﬁles.

more command syntax:`more filename.txt`
![more command](./img/16.png)

Excuting more command with large file
![more command with large file](./img/17.png)
### Key Navigation for more command
    - Press 'Space' to move to the next page.
    - Press 'Enter' to move to the next line.
    - Press 'b' to move back one page.
    - Press 'q' to quit the more viewer.
## iii. 'less' command - View file content interactively with more options
The less command works similar to the more command in the terminal, but with more advanced features. It allows not just forward but backward navigation through the file as well.

less command syntax:`less filename.txt`
![less command](./img/18.png)
![less command view](./img/19.png)
### Key Navigation for less command
    - 'Space' or 'f' to move forward one page.
    - 'b' to move backward one page.
    - 'Enter' to move forward one line.
    - 'y' to move backward one line.
    - 'n' to repeat the last search forward.
    - 'N' to repeat the last search backward.
    - 'q' to quit the viewer.
## iv. 'head' command - View the first few lines of a file
The head command shows the first few lines of a file. You can specify the number of lines from the command line with an option.

head command syntax: `head [Option] filename.txt`
![head command](./img/20.png)

## v. 'tail' command - View the last few lines of a file
The tail command prints the last 10 lines of a file, useful for reviewing newly-written data or to check error messages.

tail command syntax: `tail [Option] filename.txt`
![tail command](./img/21.png)

## vi. 'Nano' & 'vi' - Simple text editor
Two of the most widely used Linux text editors are nano and vi, each with advantages and disadvantages of their own. Nano is incredibly user-friendly and basic. Nano is great for binners who just wants to open a text file, make a few quick changes, and close it, this is ideal. With its very clear screen and commands that can be executed on it for simple editing and navigation, Nano doesn't require any prior knowledge to begin using. On the other hand, vi is incredibly configurable and powerful. Power users discover that it becomes incredibly simple to use because it has so many power features and shortcuts. Thus, vi can be used to make intricate changes to a file.
#### To execute 'nano' command
nano command syntax: `filename.txt`
![nano command](./img/22.png)
![tail command1](./img/23.png)
#### Key Commands
    - ^G (Ctrl + G): Display help
    - ^O (Ctrl + O): Write out (save) the file
    - ^X (Ctrl + X): Exit Nano
    - ^W (Ctrl + W): Search within the file
    - ^K (Ctrl + K): Cut text
    - ^U (Ctrl + U): Paste text
    - ^C (Ctrl + C): Show the current cursor position
    - ^\ (Ctrl + ): Replace text
 To save the changes, press Ctrl + O, then press enter to exit. To close Nano, press Ctrl + X. If you have unsaved changes, you’ll be prompted to save them before Nano exits.
#### To execute 'vi' command
Basic Vi Modes:
Normal Mode: For navigation and text manipulation (default mode when Vim starts).
Insert Mode: For text entry (press i to enter this mode from Normal Mode).
Command-Line Mode: For executing commands (press : to enter this mode from Normal Mode).

vi command syntax: `vi filename.txt`
![vi command](./img/24.png)

vi Key Commands:
#### In Normal Mode:
    - i: Switch to Insert Mode at cursor position.
    - Esc: Switch back to Normal Mode.
    - :w: Save the file.
    - :q: Quit Vim.
    - :wq: Save and quit Vim.
    - :q!: Quit without saving changes.
#### In Insert Mode:
    - Esc: Switch back to Normal Mode.
#### Command-Line Mode:
    - :w: Save the file.
    - :q: Quit Vim.
    - :wq: Save and quit Vim.
    - :q!: Quit without saving changes.

# 2. Intermediate Commands
## 2.1 File Permissions and Ownership
## i. 'chmod' command - Change file modes or Access Control Lists
The chmod command changes file or directory permissions, such as read, write, and execute.
chmod command syntax: `chmod [who][operator][permission] file`
### who: Specifies the user classes whose permissions you are modifying. It can be:
    - u for the file owner (user)
    - g for the group
    - o for others (everyone else)
    - a for all (user, group, and others)
### operator: Specifies how the permission should be changed. It can be:
    - + to add permissions
    - - to remove permissions
    - = to set exact permissions
### permission: Specifies the permission to be changed. It can be:
    - r for read
    - w for write
    - x for execute
Example: `chmod u+x file.txt` [This command adds execute permission for the file owner]
Set permissions to read, write, and execute for owner, and read and execute for group and others:
![set permission](./img/26.png)

## ii. 'chown' command - Change file owner and group
The chown command changes the ownership of a file, directory, or symbolic link to a specified user.

chown command syntax: `chown [OPTIONS] USER[:GROUP] FILE...`

    - USER: The username or user ID (UID) of the new owner.
    - GROUP: The group name or group ID (GID) of the new group. This is
      optional
    - FILE...: One or more files or directories to change ownership.

Change the owner of a file syntax: `chown newowner filename`

Change the owner and group of a file syntax: `chown newowner:newgroup filename`

Change the owner of a directory and its contents recursively syntax: `chown -R newowner directory`

Change only the group of a file: `chown :newgroup filename`

## iii. 'chgrp' command - Change group ownership
The chgrp command in Linux is used to change the group ownership of files and directories
chgrp syntax command: `chgrp [OPTION] GROUP FILE...`
### Options
    - -c, --changes: Report when a change is made.
    - -f, --silent, --quiet: Suppress most error messages.
    - -R, --recursive: Operate on files and directories recursively.
    - and so on.
Change the group of a single file syntax: `chgrp newgroup filename`

Change the group of multiple files syntax: `Change the group of multiple files`

Change the group of a directory syntax: `chgrp newgroup directoryname`

Change the group recursively syntax: `chgrp -R newgroup directoryname`

## 2.2 Searching and Finding Files
## i. 'find' command - Search for files in a directory hierarchy
The find command searches for files within a specified directory and can perform subsequent operations on them.
find command syntax" `find [path] [expression]`
![find command](./img/27.png)

## ii. 'grep' command - Search text using patterns
The grep command searches for specific text within files, returning lines that match the search criteria.

The basic syntax for grep is: `grep [options] pattern [file...]`

    - pattern: The text pattern to search for.
    - file...: One or more files to search. 
## Commonly Used Options
Here are some commonly used options with grep:

     -i: Ignore case distinctions in both the pattern and the input
         files
     -v: Invert the match, showing lines that do not match the
         pattern
     -r or -R: Recursively search directories.
     -l: List filenames containing the match.
     -c: Count the number of matching lines.

Example of grep syntax: `grep "hello" file.txt`

Case-Insensitive Search syntax: `grep -i "hello" file.txt`

## iii. 'locate' command - Find files by name
The locate command searches for files by name. Adding the -i argument makes the search case-insensitive.

The basic locate syntax: `locate [options] pattern`

Common Examples:
Basic Usage: Find a file by its name: `locate filename`

Case-Insensitive Search: Use the -i option to perform a case-insensitive search: `locate -i filename`

# 3.0 System Administration
## 3.1 'sudo' command- Execute a command as another user
The basic syntax of the sudo command is: `sudo [OPTION] COMMAND [ARGUMENTS...]`

## i. Running a Command as Root
To run a command as the root user: `sudo command`
Example: `sudo apt-get update`

## ii. Running a Command as a Specific User
To run a command as a specific user, use the -u option: `sudo -u username command`
Example: `sudo -u mark ls /home/mark`

## Common Options: 
    - -u: Specify a user to run as. Default is root.
    - -i: Start a shell as the target user.
    - -k or --reset-timestamp: Invalidate the user's sudo timestamp.
    - and many more.