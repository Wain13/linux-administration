# Partitions

## Available Disks

- **sudo fdisk -l**
  - fdisk configures partitions and disks
- Disks get mounted in /dev/***

## Partitions

- Partitions are a sub-group of blocks on a disk used to create volumes
- Partitions are defined with a partition table at the top of the drive

### partition tables

- MBR
  - Master Boot Record
  - limited to 32-bit addresses
    - highly limited with modern drives
- GPT
  - GUID Partition Table
    - resolves issues with MBR
- **sudo fdisk -l**
  - shows available partitions
  - n - new partition (follow prompts inside of fdisk)
  - w - write changes (when done)

### partition types

Several different types all with hex IDs

- linux is not the same as swap
