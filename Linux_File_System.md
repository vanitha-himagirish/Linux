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

- tree - is a recursive directory listing program that produces a depth-indented listing of files
Type following command to install tree command on
    - RHEL/CentOS and Fedora linux: yum install tree -y
    - Ubuntu or Debian: sudo apt install tree
##### Usage of tree
1. tree -To view directory structure of a directory in tree format
2. tree -d - Shows only the directories
3. tree -a - Shows all files including hidden dot files
4. tree -L 2 - Limit the level of recursion
5. man tree - On how to use tree

- cd - change directory
- pwd - print working directory
- cd.. - will take us to one level up close to the root directory
- ls - list current directory contents

#### What is LVM?
LVM - Logical Volume Manager is a disk management solution that allow administrators to manage the disk and space more effectively. It also allows us to add, remove, resizing the size online in the existing volume.

#### Structure of LVM
- Physical Volume (PV): it is a whole disk or a partition of a disk
- Volume Group (VG): corresponds to one or more PV
- Logical Volume (LV): represents a portion of a VG. A LV can only belong to one VG. It’s on a LV that we can create a file system.

#### Steps to create the LVM
- Identify the correct disks to be used for LVM
- Create a Physical Volumes(PV) on the disk -  pvcreate /dev/sdb /dev/sdc - creates 2 disks sdb and sdc each with 10GB disk
- Create the Volume Group(VG) on Physical volume - vgcreate datavg /dev/sdb /dev/sdc - datavg volume group is created with 2 PVs ie. sdb and sdc
- Create Logical Volumes(LV) on the Volume Group -  lvcreate -L 10G -n datavol1 datavg - Logical Volume of 10GB is created
- Create a filesystem for logical volumes. After filesystem is created, logical volumes are mounted and volumes are used.

