# Groups

## /etc/group file

File lists all of the groups and supplementary members
Doesn't necessarily show primary members

### id

command to see which groups user is part of:

- e.g. **id wain**

## etc/sudoers file

Designates groups and user accounts with specific permissions to run things like **sudo** as well as other machine and system-level commands such as shutdown, or permit system file access.
  
Allows you to add permissions for actions that normally can only be done by root to other users and groups. With and without passwords.

## Creating groups and modifying membership

- **groupadd**
- **groupdel**
- **usermod**
  - to add/remove a user from a group
- manually edit the /etc/group file directly
