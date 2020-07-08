### Understanding the Linux File System:
#### Working with Files
- In Linux, everything is a file. 
- A text file is a file, a directory is a file, your keyboard is a file (one that the system reads from only), your monitor is a file (one that the system writes to only) etc. 
- Linux is extension less system. 
- Linux is case sensitive.
- Under Linux the system actually ignores the extension and looks inside the file to determine what type of file it is. So for instance I could have a file myself.png which is a picture of me. I could rename the file to myself.txt or just myself and Linux would still happily treat the file as an image file.
 
#### Structure of LVM
- Physical Volume (PV): it is a whole disk or a partition of a disk
- Volume Group (VG): corresponds to one or more PV
- Logical Volume (LV): represents a portion of a VG. A LV can only belong to one VG. It’s on a LV that we can create a file system.

