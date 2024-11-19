# Mounting

Mounting links a filesystem into your existing directory structure.
Using the **mount** command

- **mount /dev/sdb1 /newstorage**
  - mount \<device> \<location>

Unmount with **umount**

- can unmount with device name or with mount point
  - **umount /dev/sdb1**
  - **umount /newstorage**

mount and umount commands can reference **fstab** to determine location or device based on location

- **mount /newstorage**
  - mounts the device listed in fstab that is designated to attach to /newstorage
  - no need to designate the device if it's already in fstab

## mounting options

- read only
  - Access timestamps don't change when reading from readonly filesystem
- read/write

### example

prerequisites:

- I have a drive **/dev/sdb1**
- it's partitioned and formatted with xfs

Steps:

- create a directory I want to refer to the drive/partition/fs
  - **mkdir /newstorage**
    - creates empty directory
  - **mount /dev/sdb1 /newstorage/**
    - drive is now manualy mounted, will need to be mounted again on reboot
      - permanently mount options:
        - adding to filesystem table **/etc/fstab**
        - adding mount command to user profile such as .bashrc
