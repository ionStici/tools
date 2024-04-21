# Git Aliases

**Git Aliases** are a workflow tool that create custom shortcuts to frequently used git commands.

### Why Git Aliases

- **Efficiency:** Shorten commonly used or complex Git commands to a few keystrokes.
- **Convenience:** Customize your command set to match your workflow and preferences.
- **Consistency:** Help standardize commands across a team by simplifying complex command sequences.

### Create Git Aliases

Any configuration variable we change in the global `.gitconfig` file will be applied across all git repositories.

```
git config --global alias.br "branch"
git br feature
```

This creates an alias `br` that stands for `branch`

### Alias with Multiple Commands Consecutively

```
git config --global alias.a '!git add . && git status'
```

The `!` at the beginning allows the alias to run shell commands.

### List All Global Git Configurations

```
git config --global --list
```

### Delete a Global Git Configuration

```
git config --global --unset user.email
```

Deleting the `~/.gitconfig` file removes all your global settings, effectively resetting Git's global configuration to default.

### Formatted alias for git log

```
git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit"
```
