# CLI Manipulation

_Copy, move, remove files and directories using the command line._

- **`cat`** `folder/hello.txt` this command outputs in your terminal the content of the specified file.

- **`cp`** command copies files or directiories.

  `cp hello.txt new.txt` copy the content from "hello.txt" to "new.txt"

  `cp hello.txt folder` copy a file to a destination directory.

  `cp file1.txt file2.txt folder` copy a list of files to a destination directory.

- **Wildcards** - special characters.

  **`*`** the asterisk means "all"

  `cp * folder` copy all files in the current working directorty into another directory.

  `cp w*.txt folder` select all files that start with "w' (prefix) and end with ".txt" (suffix), and copy to "folder"

  `cp file.txt ..` copy the file to the directorty above.

- **`mv`** moves files (similar to `cp` in usage)

  `mv hello.txt folder` moves "hello.txt" within "folder"

  `mv hello.txt hi.txt` **rename a file** by moving. First arg: the file we want to rename. Second arg: the new file name.

- **`rm`** delete files and directories.

  `rm hello.txt` delete the "hello.txt" file from the filesystem.

  `rm -r folder` use the `-r` (recursive) option to delete a directory.

  `rm folder/*` delete all files from "folder", but not the "folder" itself.

  `rm` deletes files and directories permanently, you can't get them back.

- **Asterisk `*` as wildcard character** - means _"any sequence of characters"_.

  `rm draft-*.md` would delete all files that start with `draft-` and end with `.md`

  This allows you to run an operation against a potentially large number of files at once, all of which match the specified pattern.
