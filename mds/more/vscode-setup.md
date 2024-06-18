# Visual Studio Code

- [Install VS Code](https://formulae.brew.sh/cask/visual-studio-code)
- [Visual Studio Code](https://code.visualstudio.com/)
- [VS Code Docs](https://code.visualstudio.com/docs)
- [VS Code Extensions](https://marketplace.visualstudio.com/VSCode)

**Visual Studio Code** - code editor, open-source, IDE-like features, supported by a large community.

**Code Editor** - application used by developers to write code. Advantages: Language-specific syntax highlighting, easier to read and understand, automatic code formatting, error catching helpers, etc.

**IDE** _(Integrated Development Environment)_ - application that provides comprehensive features to edit, compile, and debug code.

## VS Code Extensions (suggestions)

- [Prettier - Code formatter](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
- [Material Icon Theme](https://marketplace.visualstudio.com/items?itemName=PKief.material-icon-theme)
- [One Monokai Theme](https://marketplace.visualstudio.com/items?itemName=azemoh.one-monokai)

<div></div>

- [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker)
- [Auto Rename Tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-rename-tag)
- [Auto Close Tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-close-tag)

<div></div>

- [Color Highlight](https://marketplace.visualstudio.com/items?itemName=naumovs.color-highlight)
- [Highlight Matching Tag](https://marketplace.visualstudio.com/items?itemName=vincaslt.highlight-matching-tag)
- [indent-rainbow](https://marketplace.visualstudio.com/items?itemName=oderwat.indent-rainbow)

<div></div>

- [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
- [Path Intellisense](https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense)
- [vscode-styled-components](https://marketplace.visualstudio.com/items?itemName=styled-components.vscode-styled-components)

## settings.json

Command + Shift + P -> Open `settings.json`

```json
{
  // VS CODE SETTINGS
  "editor.formatOnSave": true, // Automatically formats the code when you save the file.
  "files.autoSave": "onFocusChange", // Automatically saves your file when the editor loses focus.
  "explorer.confirmDelete": false, // Disables the confirmation dialog when deleting files using the file explorer.
  "explorer.compactFolders": false, //  Prevents the file explorer from compacting folders into single clickable paths.
  "workbench.startupEditor": "none", // No editor is open when VS Code starts.
  "workbench.statusBar.visible": false, // Hides the status bar at the bottom of the editor.
  "workbench.editor.enablePreview": false, // Opens files always in a permanent editor instead of in a preview mode.
  "workbench.editor.restoreViewState": true, // Restores the last viewed state of the editor when reopening a file.
  "editor.find.addExtraSpaceOnTop": true, // Adds extra space on top of the editor when using the Find feature.
  "editor.padding.top": 15, // Adds a top padding of 15 pixels inside the editor.
  "editor.stickyScroll.enabled": false, // Disables the feature where headers or important lines remain visible while scrolling.
  "editor.insertSpaces": true, // Replaces tabs with spaces in the editor.
  "editor.scrollBeyondLastLine": true, // Allows scrolling beyond the last line of the file.
  "editor.minimap.enabled": false, // Disables the minimap view on the right side of the editor.
  "editor.find.seedSearchStringFromSelection": "never", // Prevents pasting in the Find Widget from the editor selection.
  "breadcrumbs.enabled": false, // Disables the breadcrumb navigation at the top of the editor.
  "explorer.confirmDragAndDrop": false, // Disables the confirmation dialog when moving files or folders via drag and drop.
  "window.zoomLevel": 0.5, // Sets the zoom level of the window
  "editor.detectIndentation": false, // Disables automatic detection of tab settings based on opened files.
  "editor.renderWhitespace": "none", // Does not render any whitespace characters in the editor.

  // TEXT PREFERENCES
  "editor.fontFamily": "Hack Nerd Font Mono", // Sets the font family in the editor.
  "terminal.integrated.fontFamily": "MesloLGS NF", // Sets the font family of the integrated terminal.
  "editor.fontSize": 13, // Sets the font size in the editor to 14 pixels.
  "editor.tabSize": 2, // Sets the number of spaces per tab in the editor to 2.
  "editor.lineHeight": 1.7, // Sets the line height as a multiplier of the font size.
  "terminal.integrated.fontSize": 16, // terminal font size
  "terminal.integrated.lineHeight": 1.2, // terminal line height
  "editor.wordWrap": "off", // No word wrap

  // THEME
  "workbench.colorTheme": "One Monokai", // Sets the color theme of the entire editor
  "workbench.iconTheme": "material-icon-theme", // Sets the icons in the UI

  // LINE HIGHLIGHT
  "editor.renderLineHighlight": "all", // Highlights both the gutter and the current line where the cursor is located.
  "workbench.colorCustomizations": {
    "editor.lineHighlightBackground": "#223851" // Customizes the background color of the highlighted line
  },

  // PRETTIER
  "editor.defaultFormatter": "esbenp.prettier-vscode", // Sets the default formatter
  "prettier.singleQuote": true // Single quotes by default
}
```

## ESLint

[ESLint](https://eslint.org/) is a static code analysis tool used to identify problematic patterns found in JavaScript code. It aims to make code more consistent and avoid bugs.

```bash
# install and configure ESLint
npm init @eslint/config@latest
```

This command will guide you through setting up your ESLint config file.

## VS Code and Emmet

[Emmet](https://docs.emmet.io/) plugin for high-speed coding and editing in HTML.

Support for Emmet snippets is built right into VS Code, no extension required.

## Code Snippets

Templates for repeating code patterns.

_Snippets: Configure User Snippets -> New Global Snippets File_

```json
{
  "printToConsole": {
    "prefix": "cl",
    "scope": "javascript,typescript,javascriptreact,typescriptreact",
    "body": ["console.log($1)"],
    "description": "console.log"
  },
  "reactComponent": {
    "prefix": "rfc",
    "scope": "javascript,typescript,javascriptreact,typescriptreact",
    "body": [
      "function ${1:${TM_FILENAME_BASE}}() {",
      "\treturn (",
      "\t\t<div>",
      "\t\t\t$0",
      "\t\t</div>",
      "\t)",
      "}",
      "",
      "export default ${1:${TM_FILENAME_BASE}}",
      ""
    ],
    "description": "React component"
  },
  "importCSSModule": {
    "prefix": "csm",
    "scope": "javascript,typescript,javascriptreact,typescriptreact",
    "body": ["import styles from './${TM_FILENAME_BASE}.module.css'"],
    "description": "Import CSS Module as `styles`"
  },
  "reactStyledComponent": {
    "prefix": "rsc",
    "scope": "javascript,typescript,javascriptreact,typescriptreact",
    "body": [
      "import styled from 'styled-components'",
      "",
      "const Styled${TM_FILENAME_BASE} = styled.$0``",
      "",
      "function ${TM_FILENAME_BASE}() {",
      "\treturn (",
      "\t\t<Styled${TM_FILENAME_BASE}>",
      "\t\t\t${TM_FILENAME_BASE}",
      "\t\t</Styled${TM_FILENAME_BASE}>",
      "\t)",
      "}",
      "",
      "export default ${TM_FILENAME_BASE}",
      ""
    ],
    "description": "React styled component"
  }
}
```
