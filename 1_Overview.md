Kernel
======
The Linux® kernel is the main component of a Linux operating system (OS) and is the core interface between a computer’s hardware and its processes.

The kernel has 4 jobs:
- Memory management: Keep track of how much memory is used to store what, and where
- Process management: Determine which processes can use the CPU, when, and for how long
- Device drivers: Act as mediator/interpreter between the hardware and processes
- System calls and security: Receive requests for service from the processes


Users Groups
============
- Access to Linux is based on users
- Each user has password and belongs to one or more groups
- the adminstrator account is "root"

File System 
============
A popular approach for Linux distributions is to organise the file system this way:
- The top folder is "/" (think of  C:\ on Windows)
- /bin essential user command binaries (for all users)
- /etc host specific system configuration
- /home contains the users' home folders
- /usr second major section of the filesystem
- /var variable data files

If you want to put some logic around some odd concepts in the way the file system is organized: http://landley.net/writing/hackermonthly-issue022-pg33.pdf


Paritions:
- Disk partitioning or disk slicing is the creation of one or more regions on secondary storage, so that each region can be managed separately. Partitions are "mounted"


Basic Navigation commands
=========================
"ls": list the content fo the current directory
"ls -l": same as above, but add more details to the output (ownership, permissions)
"ls -a": list all files, even the hidden ones
"ls -al" or "ls -la": combination of command 3 and 4
"cd blabla" : move to the blabla folder
"pwd": shows the current folder


Files attributes:
=================
Types:
- file
- directory
- symbolink link (shortcut)

Permissions:
============
- read permission settings
- write permission settings
- execution permission settings

Permissions are set accross of the 3 dimenions (read, write, exec) for:
1) the owner the file 
2) the users in the same group of owner of the file 
3) other users

Typically, the permissions will displayed in this format:
rwx r-x --x
- the first 3 characters set the permissions for the user
- the next 3 are for the group
- the last group is for other users

rwx:
- the first  character is always 'r' (read permision) or '-' (no read permission) 
- the second character is always 'w' (write permision) or '-' (no write permission) 
- the third  character is always 'x' (execution permision) or '-' (no execution permission) 


Example:
rwx r-x --x:
- the owner and the users of the same group can read the file. Other users cannot.
- only the owner can write the file
- everybody can execute the file

Note: 
if you type ls -l in a directory, you may see a character before the permission. This indicates the type of the item. 
- '-' is for a file
- 'd' is for a directory
- 'l' is for a symbolink Link (shortcut)
- and a few more...

You may also see an item named '.' and another one named '..':
- '.' is a reference to the current folder
- '..' is a reference to the parent folder

