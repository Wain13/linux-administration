# linux-administration

**https://www.youtube.com/watch?v=JnhWJbZzL58&t=1074s**

**Kernel Process** and **User process space** are separated in CPUs from 386-onward

A Distro is Linux kernel bundled with OS software

**RedHat** family  
**Debian** Family  
**Source Code** Distros  
**System V Init** vs **System D**  

## Redhat Family system

- Comes out of Redhat Package Management software
- keeps track of versions and bundles pieces of software and dependencies to make sure they are all correctly tied togethes
- called **RPM** packages
- more corporate focused
  
## Debian

- More end user focused
- **.deb** package family

## Source Code

- Slackware, et al.
- You compile from source code, or installer compiles source code on install
- allows deeper customization and compatibility awareness.
- much more optimization possible

## System V Init vs SystemD

- Once kernel loads the rest has to be brought up
- init process after the kernel runs
- starts up services
- brings up GUI, etc

### SystemD has advantages:

- bring up multiple pieces at the "same" time or inspecific, easily customizable orders
- other additional configurations to the init process

**System V Init** is a series of scripts that run in order  
**SystemD** is a more organized and complete system

## Hardware considerations

- at least 1GB for GUI (need more, really)
- Video Card drivers
- Wireless card Drivers
- other less direct peripherals (scanners, printers, other devics, etc...)

## Installation methods

- DVD / ISO
- USB
- Hard Drive
- Network
  - requires a boot service and ability to install over network
  
## Time/Date

- Computer clocks run on quartz crystals, they oscillate at known frequencies
  - OS best uses network time
- Time on computer gets written to a chip either as local time or UTC
  - Windows uses local
    - update local time
    - then update time zone
- Linux uses UTC
  - Just needs to know the new time zone

## Software selections

- Minimal install
- Gnome Desktop

## Important questions

- can I install packags later?
- where does software come from?
- what are requirements of different packages?

## Partitions:

- Bootloader likely starts on beginning of hard drive on partition where Linux is installed
- SWAP partitions
- RAID partitions
- LVM partitions
- logical volume management
- resizable and movable data
- File system

## File Systems

- Minix FS from Unix
- Extfs - Extensions for Minix
  - Ext2
  - Ext3
  - Ext4
- xfs
  - default on a lot of newer machines
- fat32
- NTFS

 File systems are used through **mount points**

- a Directory in your directory structure
- First Main partition has directory structure, any directory inside of it can be designated as a mount point
- will redirect to a different partition
- merges 2 directories into a single directory tree
- the redirects are mount points.
  
## Networking

- Your machine works better with a hostname
- usually best if the host name matches a DNS entr on a DNS server somewhere
- mostly for internal functioning to avoid using "localhost"
- DHCP or manual configuration?
  - workstation - DHCP in most cases
  - Server - Manual in many cases
    - Different for something hands off with network orchestration like K8s
- GUI applets or nmtui can hange networking
  
## Root

- **Root User**
  - the main user that runs the entire system
  - process that makes everything work
  - not the same as an administrative user
    - these are usually part of a WHEEL group
  - When you aren't root but need root access to run something use "sudo"
    - "Super User DO this thing"
  - Additional Users ca be created to limit access and prevent catastrophic operations
  - Usernames shouldn't be **easy**
  - Password should match latest industry standard complexity rules and NOT have username in it
  
## initial setup

- Accept license
- Kdump
  - Allows you to have all memory written out to Hard Drive in case of Kernel crash
  - useful for a kernel developer, less so for the rest of us
  
## login

- CTRL+ALT+F# can usually drop from gui login to a command line
