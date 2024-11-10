# Permissions

Each file has a permission value defined as a 3 digit number
Each file has an owner

example **0644**
first digit:
set user ID, set group ID, sticky bit
6 - User Permissions
4 - group permissions
4 - world permissions

## SELinux on filesystems

SELinux context gets set
Provides context for blocking and permitting file access/viewing/etc regardless of file permissions, even if user has full root access.

