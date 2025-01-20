# Linux Commands Guide

A detailed guide to essential Linux commands, including their purposes and example outputs. Perfect for learning or quick reference.

---

## What You'll Learn

### 🙋 Help! (and WTF)
1. [man](#man) - Show help (the manual)  
2. [which](#which) - Find out where a command is  
3. [--help](#--help) - Find help on any command  
4. [Ctrl+C](#ctrlc) - Stop the current program  
5. [:q!](#q) - Quit the `vi` text editor without saving  

### 👤 Logging In and Out
6. [logout](#logout) - Exit the current login shell  
7. [passwd](#passwd) - Change your password  
8. [sudo](#sudo) - Execute a command as a superuser  
9. [ssh](#ssh) - Create an SSH connection to a server  

### 🗂️ Move Around the File System
10. [cd](#cd) - Change the current directory  
11. [ls](#ls) - List files in a directory  
12. [mkdir](#mkdir) - Create a new directory  
13. [pwd](#pwd) - Print the current directory  
14. [cp](#cp) - Copy files and directories  
15. [rm](#rm) - Delete files and directories  

### 📝 Find, View, and Edit Files
16. [cat](#cat) - Print the contents of a file  
17. [chmod](#chmod) - Change file permissions  
18. [chown](#chown) - Change file owner and group  
19. [diff](#diff) - Show the difference between two files  
20. [file](#file) - Show the type of a file  
21. [less](#less) - Browse file contents interactively  
22. [locate](#locate) - Find files with matching names  
23. [tail](#tail) - Print the last lines of a file  
24. [touch](#touch) - Create or update a file  
25. [nano](#nano) - Edit files interactively  
26. [vim](#vim) - An advanced text editor  

### 📦 Install Programs
27. [dnf](#dnf) - Install and manage packages (RHEL/Fedora)  
28. [apt](#apt) - Install and manage packages (Ubuntu)  

### 📯 Networking
29. [curl](#curl) - Get a web page or API  
30. [dig](#dig) - Look up DNS information  
31. [ip addr](#ip-addr) - Show network configuration  
32. [ping](#ping) - Check if a server is alive  

### ⌚ Manage Processes
33. [kill](#kill) - Terminate a process  
34. [top](#top) - Show the top processes  
35. [ps](#ps) - List running processes  
36. [Ctrl+Z](#ctrlz) - Suspend a process  
37. [fg](#fg) - Resume a process  
38. [jobs](#jobs) - List all active jobs  

### ⚙️ System Management
39. [cat /etc/redhat-release](#cat-etchosts-release) - Show Linux distribution name and version  
40. [date](#date) - Show the current date and time  
41. [df](#df) - Show free disk space  
42. [du](#du) - Show disk usage  
43. [shutdown](#shutdown) - Halt or reboot the system  
44. [uname](#uname) - Print system information  
45. [uptime](#uptime) - Show how long the system has been running  

---

## Commands and Examples

### 🙋 Help! (and WTF)

#### `man`
- **Description**: Displays the manual or help file for a command, providing detailed information on its options and usage.
- **Why the name?**: "man" stands for manual, reflecting its purpose of providing detailed documentation.
- **Example**:  
  ```bash
  $ man ls
  ```

#### `which`
- **Description**: Finds the location of a command or executable in the system’s PATH.
- **Why the name?**: "which" helps you find out "which" location a command is executed from.
- **Example**:  
  ```bash
  $ which python
  /usr/bin/python
  ```

#### `--help`
- **Description**: Displays brief usage information and options for a command.
- **Why the name?**: Simply appending `--help` gives you a quick reference guide for any command.
- **Example**:  
  ```bash
  $ ls --help
  ```

#### `Ctrl+C`
- **Description**: Interrupts and stops the currently running process in the terminal.
- **Why the name?**: "Ctrl+C" is the common keyboard shortcut for "canceling" a running process.
- **Example**:  
  Simply press `Ctrl+C` while a process is running.

#### `:q!`
- **Description**: Force quits the `vi` text editor without saving any changes.
- **Why the name?**: ":q" stands for "quit," and "!" forces the action without saving.
- **Example**:  
  In `vi`, type `:q!` and press Enter to quit without saving.

---

### 👤 Logging In and Out

#### `logout`
- **Description**: Exits the current login shell.
- **Why the name?**: "logout" indicates that the user is logging out of the session.
- **Example**:  
  ```bash
  $ logout
  ```

#### `passwd`
- **Description**: Changes your password.
- **Why the name?**: "passwd" stands for password, the purpose of this command is to manage user passwords.
- **Example**:  
  ```bash
  $ passwd
  ```

#### `sudo`
- **Description**: Executes a command as a superuser.
- **Why the name?**: "sudo" stands for "superuser do," which allows a user to perform tasks that require administrator privileges.
- **Example**:  
  ```bash
  $ sudo apt update
  ```

#### `ssh`
- **Description**: Creates a secure terminal connection to a remote server.
- **Why the name?**: "ssh" stands for "secure shell," indicating a secure communication channel.
- **Example**:  
  ```bash
  $ ssh user@hostname
  ```

---

### 🗂️ Move Around the File System

#### `cd`
- **Description**: Changes the current directory.
- **Why the name?**: "cd" stands for "change directory."
- **Example**:  
  ```bash
  $ cd /path/to/directory
  ```

#### `ls`
- **Description**: Lists files and directories in the current directory.
- **Why the name?**: "ls" stands for "list," which is exactly what it does—lists directory contents.
- **Example**:  
  ```bash
  $ ls
  ```

#### `mkdir`
- **Description**: Creates a new directory.
- **Why the name?**: "mkdir" stands for "make directory."
- **Example**:  
  ```bash
  $ mkdir new_directory
  ```

#### `pwd`
- **Description**: Prints the full path of the current directory.
- **Why the name?**: "pwd" stands for "print working directory."
- **Example**:  
  ```bash
  $ pwd
  /home/user/Documents
  ```

#### `cp`
- **Description**: Copies files or directories.
- **Why the name?**: "cp" stands for "copy."
- **Example**:  
  ```bash
  $ cp file.txt backup/
  ```

#### `rm`
- **Description**: Removes files or directories.
- **Why the name?**: "rm" stands for "remove."
- **Example**:  
  ```bash
  $ rm file.txt
  ```

---

### 📝 Find, View, and Edit Files

#### `cat`
- **Description**: Prints the contents of a file.
- **Why the name?**: "cat" stands for "concatenate," as it can also concatenate multiple files.
- **Example**:  
  ```bash
  $ cat file.txt
  ```

#### `chmod`
- **Description**: Changes the permissions of a file or directory.
- **Why the name?**: "chmod" stands for "change mode," referring to the file permissions (read, write, execute).
- **Example**:  
  ```bash
  $ chmod 755 file.txt
  ```

#### `chown`
- **Description**: Changes the owner and group of a file or directory.
- **Why the name?**: "chown" stands for "change owner."
- **Example**:  
  ```bash
  $ chown user:group file.txt
  ```

#### `diff`
- **Description**: Displays the differences between two files.
- **Why the name?**: "diff" stands for "difference," indicating that the command shows what differs between files.
- **Example**:  
  ```bash
  $ diff file1.txt file2.txt
  ```

#### `file`
- **Description**: Determines and displays the type of a file.
- **Why the name?**: "file" refers to identifying the type of file, whether it's text, binary, etc.
- **Example**:  
  ```bash
  $ file example.txt
  ```

#### `less`
- **Description**: Allows you to browse the contents of a file interactively, one screen at a time.
- **Why the name?**: "less" is the opposite of "more," allowing forward and backward movement in files.
- **Example**:  
  ```bash
  $ less file.txt
  ```

#### `locate`
- **Description**: Searches for files by name.
- **Why the name?**: "locate" helps locate a file in the system.
- **Example**:  
  ```bash
  $ locate file.txt
  ```

#### `tail`
- **Description**: Displays the last few lines of a file.
- **Why the name?**: "tail" refers to the end of something (like the tail of an animal).
- **Example**:  
  ```bash
  $ tail -n 10 file.txt
  ```

#### `touch`
- **Description**: Creates a new empty file or updates the timestamp of an existing file.
- **Why the name?**: "touch" refers to modifying a file without changing its contents.
- **Example**:  
  ```bash
  $ touch newfile.txt
  ```

#### `nano`
- **Description**: A simple interactive text editor.
- **Why the name?**: "nano" is named after a small, user-friendly text editor.
- **Example**:  
  ```bash
  $ nano file.txt
  ```

#### `vim`
- **Description**: A more advanced interactive text editor.
- **Why the name?**: "vim" stands for "Vi IMproved," an enhanced version of the `vi` editor.
- **Example**:  
  ```bash
  $ vim file.txt
  ```

---

### 📦 Install Programs

#### `dnf`
- **Description**: A package manager for managing software on RHEL/Fedora-based systems.
- **Why the name?**: "dnf" stands for "Dandified YUM," which is the successor of the older `yum` package manager.
- **Example**:  
  ```bash
  $ sudo dnf install package_name
  ```

#### `apt`
- **Description**: A package manager for managing software on Debian/Ubuntu-based systems.
- **Why the name?**: "apt" stands for "Advanced Package Tool," which is used for handling package installations and updates.
- **Example**:  
  ```bash
  $ sudo apt install package_name
  ```

---

### 📯 Networking

#### `curl`
- **Description**: A tool to transfer data from or to a server, using various protocols (HTTP, FTP, etc.).
- **Why the name?**: "curl" stands for "client URL," as it can interact with various URLs (web pages or APIs).
- **Example**:  
  ```bash
  $ curl https://www.example.com
  ```

#### `dig`
- **Description**: A tool to query DNS records and get domain name system information.
- **Why the name?**: "dig" stands for "domain information gather," which reflects its purpose of gathering DNS data.
- **Example**:  
  ```bash
  $ dig example.com
  ```

#### `ip addr`
- **Description**: Displays network interface and IP address information for the system.
- **Why the name?**: "ip addr" stands for "IP address," showing the system’s IP configuration.
- **Example**:  
  ```bash
  $ ip addr
  ```

#### `ping`
- **Description**: Tests network connectivity to a host and checks if a server is reachable.
- **Why the name?**: "ping" refers to the sonar ping used in submarines to detect objects underwater, metaphorically used for testing connections.
- **Example**:  
  ```bash
  $ ping google.com
  ```

---

### ⌚ Manage Processes

#### `kill`
- **Description**: Terminates a running process by sending a signal to it.
- **Why the name?**: "kill" refers to ending a process or terminating it forcefully.
- **Example**:  
  ```bash
  $ kill 1234
  ```

#### `top`
- **Description**: Displays a dynamic, real-time view of system processes and resource usage.
- **Why the name?**: "top" refers to showing the top processes consuming system resources.
- **Example**:  
  ```bash
  $ top
  ```

#### `ps`
- **Description**: Lists

 running processes.
- **Why the name?**: "ps" stands for "process status," showing detailed information about active processes.
- **Example**:  
  ```bash
  $ ps aux
  ```

#### `Ctrl+Z`
- **Description**: Suspends the current process.
- **Why the name?**: "Ctrl+Z" is a shortcut used to pause or stop a running command.
- **Example**:  
  Simply press `Ctrl+Z` during a running process.

#### `fg`
- **Description**: Resumes a suspended process.
- **Why the name?**: "fg" stands for "foreground," bringing a process back to the active state.
- **Example**:  
  ```bash
  $ fg
  ```

#### `jobs`
- **Description**: Lists the active jobs in the current shell session.
- **Why the name?**: "jobs" refers to the background processes or tasks in the current session.
- **Example**:  
  ```bash
  $ jobs
  ```

---

### ⚙️ System Management

#### `cat /etc/redhat-release`
- **Description**: Displays the version of the Red Hat-based distribution.
- **Why the name?**: "redhat-release" is the file that contains version information for Red Hat-based systems.
- **Example**:  
  ```bash
  $ cat /etc/redhat-release
  ```

#### `date`
- **Description**: Displays the current system date and time.
- **Why the name?**: "date" reflects its function to display and set the system’s date and time.
- **Example**:  
  ```bash
  $ date
  ```

#### `df`
- **Description**: Displays disk space usage for mounted file systems.
- **Why the name?**: "df" stands for "disk free," which shows the available disk space.
- **Example**:  
  ```bash
  $ df -h
  ```

#### `du`
- **Description**: Displays disk usage for directories and files.
- **Why the name?**: "du" stands for "disk usage," showing how much space a file or directory is consuming.
- **Example**:  
  ```bash
  $ du -sh *
  ```

#### `shutdown`
- **Description**: Powers off or reboots the system.
- **Why the name?**: "shutdown" clearly indicates its purpose: shutting down the system.
- **Example**:  
  ```bash
  $ sudo shutdown -h now
  ```

#### `uname`
- **Description**: Displays system information such as kernel version.
- **Why the name?**: "uname" stands for "Unix name," providing details about the system.
- **Example**:  
  ```bash
  $ uname -a
  ```

#### `uptime`
- **Description**: Shows the duration for which the system has been running.
- **Why the name?**: "uptime" reflects how long the system has been active since the last boot.
- **Example**:  
  ```bash
  $ uptime
  ```

---

## Additionally

Thank you for going through this guide! If you're looking for more detailed explanations and examples, visit [TutorialWorks - Linux Commands](https://www.tutorialworks.com/linux-commands), implement these commands.

Happy learning!
