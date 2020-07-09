### Understanding the Linux File System:
#### Working with Files
- In Linux, everything is a file. 
- A text file is a file, a directory is a file, your keyboard is a file (one that the system reads from only), your monitor is a file (one that the system writes to only) etc. 
- Linux is extension less system. 
- Linux is case sensitive.
- Under Linux the system actually ignores the extension and looks inside the file to determine what type of file it is. So for instance I could have a file myself.png which is a picture of me. I could rename the file to myself.txt or just myself and Linux would still happily treat the file as an image file.

#### File System structure
- / – this is known as “root”, the logical beginning of the Linux file system structure. Every single file path in Linux begins from root in one way or another. / contains the entirety of your operating system.
- /bin – Most of the binary files are stored in this folder. Typically Linux terminal commands and core utilities such cd,pwd,mv etc.
- /boot - All needed files for Linux boot are stored here
- /dev - Here, all the physical devices are mounted , such as hard drives, USB drives, optical drives etc.
- /etc - All the configuration files are stored here. Configurations stored in /etc will effect all users on the system. Configurations files under user's /home folders affect that particular user
- /home - All the user personal files are stored here
- /lib - All the libraries are stored here. These files are basically needed linux to work
- /media - External devices such optical drives and USB drives are mounted
- /mnt - This is used as placeholder folder used for mounting other folders or drives.
- /opt - Optional software for system.
- /proc - The "processes" folder where lot of system infomration is represented as files. It provides a way for Linux Kernel to send and receive information from various processes running in the Linux environment.
- /root - Similar to /home folder specifically used by root user also called as superuser
- /sbin - Similar to /bin, certain commands can only be run by the root user or superuser
- /tmp - This is where all temporary files are stored and are  deleted upon shutdown
- /usr - Contains files and utilites that are shared between users
- /var - variable data is stored, usually system logs but can also include other data

#### Commands used - File system structure

1. tree - is a recursive directory listing program that produces a depth-indented listing of files
Type following command to install tree command on
    - RHEL/CentOS and Fedora linux: yum install tree -y
    - Ubuntu or Debian: sudo apt install tree
    ##### Usage of tree
    1. tree -To view directory structure of a directory in tree format
    2. tree -d - Shows only the directories
    3. tree -a - Shows all files including hidden dot files
    4. tree -L 2 - Limit the level of recursion
    5. man tree - On how to use tree
2. cd - change directory
3. pwd - print working directory
4. cd.. - will take us to one level up close to the root directory
5. ls - list current directory contents
6. ls -a - lists the content of directory 
    Note : The hidden files may be having the extensions such as
                1. .profile − The Bourne shell ( sh) initialization script
                2. .kshrc − The Korn shell ( ksh) initialization script
                3. .cshrc − The C shell ( csh) initialization script
                4. .rhosts − The remote shell configuration file
                5. .cshrc − The C shell ( csh) initialization scrip
                6. .rhosts − The remote shell configuration file
7. ls -l - displays more information about the directory contents such as type and permission given on the file, memory blocks, owner of the file, size in bytes etc.
8. mkdir dirname - Creates the directory
9. rmdir dirname  - Removes/deletes the directory
10. mv olddir newdir - changing directory names
11. vi filename - Creates a new file.Press i to insert and make modification.press escape to come out of edit mode. To save the file without changes :q!. To save the changes,press :wq.
12. cat filename - Display the file
13. wc filename - Counting words in a file
14. cp source_file destination_file - Copy Source file to destination file
16. mv old_file new_file - Change the name of the files..renaming
17. rm filename - deleting files
#### File permission - Commands

#### Standard Unix Streams
- stdin − This is referred to as the standard input and the associated file descriptor is 0. This is also represented as STDIN. The Unix program will read the default input from STDIN.
- stdout − This is referred to as the standard output and the associated file descriptor is 1. This is also represented as STDOUT. The Unix program will write the default output at STDOUT
- stderr − This is referred to as the standard error and the associated file descriptor is 2. This is also represented as STDERR. The Unix program will write all the error messages at STDERR.




