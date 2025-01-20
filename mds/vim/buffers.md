# Buffers, Windows, Tags

## Buffers

- **Buffer:** In-memory storage for file contents. Each opened file corresponds to a buffer.

- List buffers: `:buffers`, `:ls`, `:files`

- Switch to a specific buffer: `:buffer <name-or-number>`

- Toggle to the last edited buffer: `Ctrl-^`

- Delete buffers: `:bdelete`, `:bdelete <name-or-number>`

## Windows

- **Window:** Viewport that display buffers. Multiple windows can show different or the same buffers simultaneously.

_Split Windows:_

- Horizontal split: `:split <file>`, `Ctrl-W S`
- Vertical split: `:vsplit <file>`m `Ctrl-W V`

_Navigate Windows:_

- `Ctrl-W H` Left
- `Ctrl-W J` Down
- `Ctrl-W K` Up
- `Ctrl-W L` Right

_Close Windows:_

- Close Windows: `:q`, `Ctrl-W C`
- Close all other windows except the current one: `Ctrl-W O`

## Tabs

**Tabs:** Collections of window layouts. Each tab can have its own set of windows and buffer arrangements.

- Open a new tab: `:tabnew <file>`

- Navigate tabs: `:tabnext`, `:tabprevious`

- Go to next tab: `gt`

- Go to previous tab: `gT`

- Go to third tab: `3gt`

- Close a tag: `:tabclose`

- Open multiple files in tabs: `vim -p file-1.txt file-2.txt`
