# Command Line Interface

## Introduction

**Terminal and Command Line** - terms used interchangeably. Technically, a _terminal_ is a software that starts and connects to a shell. The _command line_ is the literal line where you enter commands and the cursor blinks.

The **terminal** provides direct access to the computer's underlying file system and low-level features, it is incredibly useful for performing complex tasks rapidly.

The **command line** is a text interface for your computer. It is a program that takes in commands and passes them on to the computer's operating system to run.

From the Command Line you can navigate through files and folders on your computer, just like you do with Mac Finder App, the difference is that the command line is fully text-based.

The advantage of using the command line is in its power. You can run programs, write scripts to automate common tasks, and combine simple commands to handle difficult tasks. All of these traits come together to make it an important programming tool.

The fundamental aspect of the command line is that you're always in a folder. When we open the terminal, we are redirected to the home folder.

You can use the command line to traverse and edit your computer’s filesystem, create new files, edit the content of those files, delete files, and more.

- Unix-based system: Linux and Mac OS X.
- For windows, you can download [Git Bash](https://gitforwindows.org/) to use the same commands.

**A Command** is a _directive_ to the computer to perform a specific task.

In the terminal, the first things you see is `$` or `%`. This is called a _shell prompt_. It appears when the terminal is ready to accept a command.

MacOSX is a Unix OS and its command line is 99.9% the same as any Linux distribution. **bash** is your default shell and you can compile all of the same programs and utilities.

## Filesystem

When we use the command line, we refer to folders as **directories**.

Files and directories on your computer are organized into a **filesystem**.

**A Filesystem** organizes a computer's files and directories into a tree structure.

The first directory in the filesystem is the root directory, it is the parent of all other directories and files in the file system.

## Bash

[**Bash**](<https://en.wikipedia.org/wiki/Bash_(Unix_shell)>) (**B**ourne-**A**gain **Sh**ell) is a Command Line Interface (_created in 1989 by Brian Fox_).

- A **shell** is a specific kind of CLI.
- Bash is open source, anyone can read the code and suggest changes.
- Bash is the most used and widely distributed shell.

### MacOS

**Bash** is the default shell for Linux and Mac.

MacOS 10 and higher uses a similar, but slightly different default shell called **Z shell** or **Zsh**.

In most ways, **Zsh** is an exact replacement for Bash, so there is no need to switch over or install Bash instead.

We can access the CLI on MacOS through the "Terminal" application.

### Windows

Windows has a different CLI, called **Command Prompt**.

Because of the strength of the open source community and the tools they provide, mastering **Bash** is a better investment than mastering Command Prompt.

For windows we should install **git bash** instead.

## Helper Commands

- `clear` clear the terminal, aesthetic reasons.

- `date` shows the current date.

- `history` outputs the history of commands that were entered in the current session.

- `open file.txt` open the indicated file or directory.

- `code project` opens the directory in your default code editor.

- `echo "Hello"` prints the string.

- `tab` key can be used to autocomplete a command or a file/directory name.

- `↑↓` the up and down arrows can be used to cycle through your previous commands.
