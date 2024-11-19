# Links

## Hard links

- Location of file on the physical storage
- newly created files have a hard link
- you can see the number of links to a file with **ls -l**

## Soft (symbolic) links

- Location of file within the OS filesystem

### Creation

- **ln filename new_filename**
  - create **hard** link
- **ln -s filename new_filename**
  - creates **symbolic** link, no added link count in **ls -l**, but it shows the softlinked source file at the entry of the link

### Removal

- Removing the source file of links
  - for Hard links the data still exists on the link file
  - for symbolic links the data is gone
