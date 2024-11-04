# Linux Boot Process

# Bootloader
    Loads the operating system
        - BIOS loads first 512 bytes on hard drive
          - This is how early machines would start, just with those 512 bytes
        - Those 512 bytes load the OS
        - OS starts the initial process
          - Init or SystemD
        - SystemD:
          - loads services
          - loads GUI
          - Creates terminal logins
          - etc..

# GRUB
    Sets up boot options - What Kernel loads

    look for GRUB configurations to set boot options
    normally stored in **/etc/boot**

    boot files normally located in /boot
        - kernel
        - ramdisk
        - grub configurations
  

