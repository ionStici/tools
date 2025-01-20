# Searching Files

## Opening and Editing Files

- Open or create a file: `:edit file.txt`
- Open directory with **netrw**: `:edit .`

- Autocomplete: `:edit file<Tab>`
- `*` matches any file: `:edit *.html<Tab>` will return `index.html`
- `**` searches recursively: `:edit **/*.md<Tab>`

## Searching Files with `:find`

- Find and open files in `path` : `:find src/main.jsx`
- Check current `path` : `:set path?`
- Add directories to `path` : `:set path+=app/controllers/`
