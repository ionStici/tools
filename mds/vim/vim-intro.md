# Vim Introduction

_Vim : Powerful text editor_

## Essentials

- [Vim Website](https://www.vim.org/download.php) & [Vim on GitHub](https://github.com/vim/vim) & [Learn Vim](https://github.com/iggredible/Learn-Vim)
- `vim` start vim in your terminal
- `vim file.txt` open files in vim
- `:quit` or `:q` to exit vim
- `:write` or `:w` save a file
- `:w file.txt` save and name a new file
- `:wq` save a file and quit vim
- `:q!` quit without saving any changes (force quit)
- `:help {cmd}` or `:h {cmd}` for help
- `:version` check vim version
- `man vim` learn more about the `vim` command

## Modes

- **Normal Mode:** Default mode for navigation and commands.
- **Insert Mode:** Switch to insert mode with `i` to type text.
- **Return to Normal Mode:** Press `<Esc>`

## Open Multiple Windows

- `vim -o2` open two horizontal windows
- `vim -O2` open two vertical windows
- `vim -O4 file.txt draft.txt` open four vertical windows and fill up the first two with file.txt and draft.txt

To navigate between windows press `ctrl + w + h`

| `h` left | `j` below | `k` above | `l` right |
| -------- | --------- | --------- | --------- |

## Suspending Vim

- **Suspend Vim:** Press `Ctrl + z` or use `:suspend` or `:stop`
- **Resume Vim:** In terminal, type `fg`
