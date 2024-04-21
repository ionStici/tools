# Terminal Setup

## iTerm2

_Terminal emulator for macOS_

- [Download iTerm2](https://iterm2.com/downloads.html)
- [Install iTerm2 with Homebrew](https://formulae.brew.sh/cask/iterm2)

### iTerm2 Preferences

_Settings_

- Appearance -> Theme: Minimal
- Profiles -> Text -> Font: 20
- Session -> Status bar: CPU & RAM Utilization

## Oh My Zsh

_Framework for managing your **zsh** configuration_

- [Install Oh My Zsh](https://ohmyz.sh/#install)
- [Oh My Zsh : GitHub](https://github.com/ohmyzsh/ohmyzsh)

## PowerLevel10K

_Theme for Zsh_

- Install [PowerLevel10K](https://github.com/romkatv/powerlevel10k)
- Set `ZSH_THEME="powerlevel10k/powerlevel10k"` in `~/.zshrc`
- Install MesloLGS Font & Configure PowerLevel10K `p10k configure`

## ZSH Plugins

Install `zsh-autosuggestions`

```
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

Install `zsh-syntax-highlighting`

```
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

Open `~/.zshrc` and modify the `plugins` line:

```
plugins=(git zsh-autosuggestions zsh-syntax-highlighting web-search)
```
