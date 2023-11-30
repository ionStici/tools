[&larr; Back](./README.md)

# Command Line Environment Configurations

## Intro to CL Environment

Each time we launch the terminal app, it creates a new session. The session immediately loads settings and preferences that make up the command line **environment**. We can configure the environment, customize commands, create variables.

## Table of Content

- [Nano](#nano)
- [Bash Profile](#bash-profile)
- [Aliases](#aliases)
- [Environment Variables](#environment-variables)
- [PS1 Environment Variable](#ps1-environment-variable)
- [HOME Environment Variable](#home-environment-variable)
- [PATH Environment Variable](#path-environment-variable)
- [env](#env)
- [Review](#review)

<br>

## Nano

[**nano**](https://www.nano-editor.org/) is a command line text editor. It works the same way as a desktop text editor like TextEdit or Notepad, except that it is accessible from the command line and only accepts keyboard input.

```
nano file.txt
```

The `nano` command will open a new text file in the nano text editor. Here we can insert content.

- `^o` save the file.
- `^x` exit nano.
- `^g` open help menu.

<br>

## Bash Profile

A **bash profile** is a file used to store environment settings for your terminal, and it's accessible by the name `~/.bash_profile`

When a session starts, it loads the contents of the bash profile before executing any commands.

- `~` symbol represents the user's home directory.
- `.` indicates a hidden file.

To open and edit your bash profile, run the command:

```
nano ~/.bash_profile
```

Here, we can add an `echo "Welcome, John!"` statement, that will _echo_ when a terminal session begins.

To immediately activate the changes made to `~/.bash_profile` for the current session, run the command:

```
source ~/.bash_profile
```

<br>

## Aliases

We can add settings and command that execute every time a new terminal session starts.

We can create keyboard shortcuts for commonly used commands using the `alias` command.

```
alias hy="hystory"
```

Here, we create the `hy` **alias** for the `hystory` command, saved in the bash profile.

Now, by running `hy`, the command line outputs a history of commands that were entered in the current session.

<br>

## Environment Variables

**Environment Variables** hold information about the environment and can be used across commands and programs.

```
export USER="John"
```

Here, we set the environment variable `USER` to `John`. Usually, `USER` variable is set to the name of the computer's owner.

The statement `export` makes the variable available to all child sessions initiated from the session you are in, this is a way to make variables persist across programs.

```
echo $USER // John
```

After the environment variable was set and we ran `source` with our bash profile, the variable `$USER` returns the value we declared.

The `$` symbol must be used when returning a variable value.

<br>

## PS1 Environment Variable

`PS1` is an environment variable that defines the makeup and style of the command prompt.

```
export PS1=">>"
```

`PS1` will change the default command prompt from `%` to `>>`

<br>

## HOME Environment Variable

```
echo $HOME
```

The `$HOME` variable is an environment variable that displays the path of the home directory.

<br>

## PATH Environment Variable

`PATH` is an environment variable that stores a list of directories separated by a colon.

Each listed directory contains scripts for the CL to execute. The `PATH` variable simply lists which directories contain scripts.

For example, many commands we've learned are scripts stored in the `/bin` directory.

- `/bin/pwd` the script for `pwd`
- `/bin/ls` the script for `ls`

If we would run `/bin/pwd` and `/bin/ls` instead of `pwd` and `ls` then the output should be the same.

In advanced cases, you can customize the PATH variable and adding scripts of your own.

<br>

## env

The `env` command stands for **environment** and returns a list of environment variables for the current user.

```
env
```

This will returns a number of variables, including `PATH PWD PS1 HOME`

To select the value of a particular environment variable, for example `PATH`, use:

```
env | grep PATH
```

This displays the value of the `PATH` environment variable. Here the standard output of `env` is "piped" to `grep` which searches for the value of the variable `PATH` and outputs it to the terminal. The same as `echo $PATH`

<br>

## Review

- The **environment** refers to the preferences and settings of the user.

- The **nano** editor is a command line text editor used to configure the environment.

- `~/.bash_profile` is where the environment settings are stored. You can edit this file with **nano**.

- Environment variables are variables that can be used across commands and programs and hold information about the environment.

<br>
