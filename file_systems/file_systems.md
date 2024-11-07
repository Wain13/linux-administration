# File Systems

Helps organize storage space.
Storage is a large collection of addressable bytes.

- Hard Drives
- USB storage/thumb drives
- floppy disk
- Optical Media

## Filesystem Table

### /etc/fstab

- Contains boot-time device mount information
- Can be edited to change device mounting on bootup
- WILL NOT create missing directories as mount points
  - fstab errors could easily cause problems at bootup

## Free space

The amount of space available isn't the amount of space on the storage, it's the amount available **in** the file system.

## Adding a filesystem to a partition

- mkfs
  - just is a front end to other mkfs commands with file system types
  - mkfs.exfat, mkfs.minix, ,mkfx.xfs, etc.....

## Difference between filesystems

Filesystems have varying features, such as:

- file permissions
- security
- journaling
  - Stores write commands as journla entries, then removes them once the write is complete.
  - provides security for failed/incomplete write tasks.
- additional filesystems can be installed using your package manager - dnf, yum, apt, etc...

## formatting

Formatting writes the file system at the beginning of the partition and then provides other setup initialization(superblocks, accounting information, etc) to configure the fs with the specified partition

## changing a filesystem

- **mkfs** can overwrite an filesystem. Sometimes this can hapen while preserving data, but not always.
- **tune2fs** - can be used to add a journal to change from ext2 to ext3, for example without harming data.

## how to tell if an FS/partition has been formatted

Try to mount it
