# The .gitignore file

`.gitignore` is a plain text file that instructs git to intentionally ignore certain files.

Each line in `.gitignore` corresponds to a file, directory or pattern we would like to ignore when staging.

_Files and Directories we should ignore:_

- Configuration files with API or secret keys such as `.env`, log files as well
- Compiled binary files or production directories such as `build` or `dist`
- Dependencies downloaded from a package manager such as `node_modules`
- System files such as `thumbs.db` on Windows or `.DS_Store` on macOS

This results in cleaner staging areas and prevent files containing sensitive information from being committed.

```
# Windows OS file
thumbs.db

# macOS OS file
.DS_Store

node_modules/
```

Blank lines are ignores and lines starting with `#` are treated as comments.

These files will never be committed regardless of their location in the project.

The `node_modules` directory and all subdirectories along with the files inside them will be ignored.

The forward slash `/` specifies that we are ignoring a directory.

`.gitignore` is usually placed in the root directory of the repository.

## gitignore patterns

[**gitignore patterns**](https://git-scm.com/docs/gitignore#_pattern_format)

- `*.html` ignore all files ending with the `.html` extension.

- `secret*` would match any file starting with `secret` such as `secret_data.txt`

- `!public/index.html` **negation** as a prefix to negate any file that would otherwise be ignored.

  But we cannot negate a file inside an ignored directory.

_p.s._ When we create a new repository on GitHub, we have the option to add a premade `.gitignore` file from a list of templates.
