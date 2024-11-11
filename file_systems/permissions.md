# Permissions

Each file has a permission value defined as a 3 digit number, sometimes 4
Each file has an owner

## Permission types

- R - read
- W - write
- X - execute
  - on a directory means you can cd into/access fies in the directory
- S - special
  - When in User permissions: always execute as the owner account (regardless of who invoked the program)
  - When in group permissions: always execute as the group owner of the file
  - t (lowercase)
    - restricts file deletion inside a directory to owner and root only

example **0644**

- 0 sets user ID/group ID/sticky bit
- 6 - User Permissions
- 4 - group permissions
- 4 - world permissions
  
Permission values are in Octal:

- Start at 0
- If the read permission should be set, add 4
- If the write permission should be set, add 2
- If the execute permission should be set, add 1

## Sticky bits

First value in 4-digit permissions

- 4: runs as root
- 6: runs as root user and root group
- 7: Sticky bit
  - when program runs it stays cached in memory

## SELinux on filesystems

SELinux context gets set
Provides context for blocking and permitting file access/viewing/etc regardless of file permissions, even if user has full root access.
  
## Owners

- Files have both a User owner and a Group owner
- permisions are set appropriately
  - files can be set to permit a group to acess a file regardless of whether the user is the owner.
- Files include permissions for Owner, Group Owner, and Universe (everyone account doesn't apply under the first two).

