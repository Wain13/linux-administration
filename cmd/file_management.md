# File Management

## Creating

- redirecting output
- **touch**
  - creates a new blank file, or touches the modified datetime of an existing file
- **mv**
  - move or rename
    - move and rename both update the entry on the filesstem for the particular file in the same way so there's no point in having two different commands.

## Deleting

- **rm**
  - remove
- **unlink**
  - removes symbolic link to file
    - file is only actually deleted at garbage collection when there are no more links to it

## Editing

- text editors
  - nano, vi, etc...

## Searching for files with certain content

- grep something *
  - searches all local files in pwd for content lines matching 'something'