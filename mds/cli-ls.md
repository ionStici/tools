# The `ls` command

- `ls` list all the files and directories inside the working directory.

  `ls dir_name` list the content from the `dir_name` directory, relatively to your filesystem location.

## Using ls along with options

**Options** modify the behavior of commands. Three common options for `ls`:

1. `-a` lists all contents, including hidden files and directories.
2. `-l` lists all contents of a directory in long format, as well as the file permissions.
3. `-t` orders files and directories by the time they were last modified and additional details.

- `ls -a` using an option
- `ls -alt` combining options

## The `-l` option

**`man ls`** find out what options each command has available.

`ls -l` this option lists files and directories in a table format, seven columns containing details about the file or directory, separated by spaces. What each column means:

1. **Access rights** - this indicate the read / write / execute permissions on the file or directory allowed to the owner / the group / all users.
2. **Number of hard links.** This number includes the parent directory link `..` and the current directory link `.`
3. The **username** of the file's owner.
4. The **name of the group** that owns the file.
5. The **size** of the file in bytes.
6. The **date & time** that the file was last modified.
7. The **name** of the file or directory.
