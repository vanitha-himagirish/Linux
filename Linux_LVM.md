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
