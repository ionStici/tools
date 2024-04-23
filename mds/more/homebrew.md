# Homebrew

**Homebrew** is a package manager for macOS and Linux that facilitates the installation of software.

| [Install Homebrew](https://brew.sh/) | [Docs](https://docs.brew.sh/) | [FAQ](https://docs.brew.sh/FAQ) |
| ------------------------------------ | ----------------------------- | ------------------------------- |

## Install with Homebrew

| [Node](https://formulae.brew.sh/formula/node) | [Git](https://formulae.brew.sh/formula/git) | [VS Code](https://formulae.brew.sh/cask/visual-studio-code) | [Google Chrome](https://formulae.brew.sh/cask/google-chrome) | [iTerm2](https://formulae.brew.sh/cask/iterm2) | [Rectangle](https://formulae.brew.sh/cask/rectangle) |
| --------------------------------------------- | ------------------------------------------- | ----------------------------------------------------------- | ------------------------------------------------------------ | ---------------------------------------------- | ---------------------------------------------------- |

## Homebrew Essentials

```bash
# Install a package
brew install [package]

# Remove a package
brew uninstall [package]

# Get info about a specific installed package
brew info node

# Update all formulae and Homebrew itself
brew update

# List outdated packages (kegs)
brew outdated

# Upgrade everything
brew upgrade

# Upgrade a specific formula
brew upgrade node
```
