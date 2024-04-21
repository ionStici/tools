# Visual Studio Code

## Resources

- [Visual Studio Code](https://code.visualstudio.com/)
- [VS Code Docs](https://code.visualstudio.com/docs)

## Terminology

**Code Editor :** application used by developers to write code. Advantages: Language-specific syntax highlighting, easier to read and understand, automatic code formatting and error catching helpers, etc.

**IDE** _(Integrated Development Environment)_ : application that provides comprehensive features to edit, compile and debug your code.

[**Visual Studio Code**](https://code.visualstudio.com/) : code editor, open source, IDE-like features, supported by a large community including Microsoft.

## VS Code Settings (suggestions)

Connect VS Code with your GitHub account to sync your settings

- _Format On Save:_ **ON**
- _Auto Save:_ **onFocusChange**
- _Word Wrap:_ **OFF**
- _File Icon Theme:_ **Seti** (Visual Studio Code)
- _Tab Size:_ **2** (prettier have default indentation)
- _Detect Indentation:_ **OFF** (to don't override "Tab Size")

## VS Code Extensions

- **Auto Close Tag** - to automatically close HTML tags. [Link→](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-close-tag)
- **Auto Rename Tag** - to automatically update matching HTML tags. [Link→](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-rename-tag)
- **Color Highlight** - to highlight colors in CSS code. [Link→](https://marketplace.visualstudio.com/items?itemName=naumovs.color-highlight)

<div></div>

- **Image Preview** - to display an image preview next to the code. [Link→](https://marketplace.visualstudio.com/items?itemName=kisstkondoros.vscode-gutter-preview)
- **Paste and Indent** - to automatically indent pasted code. [Link→](https://marketplace.visualstudio.com/items?itemName=Rubymaniac.vscode-paste-and-indent)
- **Path Intellisense** - to autocomplete filenames. [Link→](https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense)

<div></div>

- **Live Server** - to create a live preview for the current project. [Link→](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)
- **Emmet** - (built into VS Code) enhance coding in HTML. [Link→](https://docs.emmet.io/)
- **styled-components** - Syntax highlighting and IntelliSense. [Link→](https://marketplace.visualstudio.com/items?itemName=styled-components.vscode-styled-components)

<div></div>

- **Prettier** - to automatically format code. [Link→](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
- **Night Owl** - VS Code Theme. [Link→](https://marketplace.visualstudio.com/items?itemName=sdras.night-owl)
- **GitHub Theme** - VS Code Theme. [Link→](https://marketplace.visualstudio.com/items?itemName=GitHub.github-vscode-theme)

<div></div>

- **Better Comments** - create more human-friendly comments. [Link→](https://marketplace.visualstudio.com/items?itemName=aaron-bond.better-comments)
- **Highlight Matching Tag** - match opening and closing tags. [Link→](https://marketplace.visualstudio.com/items?itemName=vincaslt.highlight-matching-tag)
- **Color Picker** - Helper with GUI to generate color codes. [Link→](https://marketplace.visualstudio.com/items?itemName=anseki.vscode-color)

<div></div>

- **ESLint** - Code analyzer. [Link→](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
- **GitLens** - Visualize Git. [Link→](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)
- **Code Spell Checker** - spell checker. [Link→](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker)

<div></div>

- **Markdown All in One** - Markdown. [Link→](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one)
- **Markdown Preview Enhanced** - Markdown. [Link→](https://marketplace.visualstudio.com/items?itemName=shd101wyy.markdown-preview-enhanced)
- **vscode-icons** - Icons Theme. [Link→](https://marketplace.visualstudio.com/items?itemName=vscode-icons-team.vscode-icons)

## settings.json

Command + Shift + P -> Open settings.json

```json
{
  // VS Code Settings
  "editor.formatOnSave": true,
  "files.autoSave": "onFocusChange",
  "workbench.iconTheme": "vscode-icons",
  "window.title": "${activeEditorMedium}",
  "files.trimTrailingWhitespace": true,
  "explorer.confirmDelete": false,
  "explorer.compactFolders": false,
  "workbench.colorTheme": "Night Owl",
  "workbench.sideBar.location": "left",
  "workbench.startupEditor": "none",
  "workbench.statusBar.visible": true,
  "workbench.editor.enablePreview": false,
  "workbench.editor.restoreViewState": true,
  "terminal.integrated.fontFamily": "MesloLGS NF",
  "editor.find.addExtraSpaceOnTop": true,
  "editor.padding.top": 15,
  "editor.stickyScroll.enabled": false,
  "editor.fontFamily": "Hack Nerd Font Mono",
  "editor.fontSize": 14,
  "editor.tabSize": 2,
  "editor.lineHeight": 1.75,
  "editor.insertSpaces": true,
  "editor.detectIndentation": false,
  "editor.renderWhitespace": "none",
  "editor.scrollBeyondLastLine": true,
  "editor.minimap.enabled": false,
  "editor.find.seedSearchStringFromSelection": "never",
  "breadcrumbs.enabled": false,
  "explorer.confirmDragAndDrop": false,
  "window.zoomLevel": 1,

  // line highlight
  "editor.renderLineHighlight": "all",
  "workbench.colorCustomizations": {
    "editor.lineHighlightBackground": "#223851"
  },

  // prettier
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "prettier.singleQuote": true,
  "prettier.arrowParens": "avoid",

  // ESLint
  "eslint.run": "onSave",
  "editor.codeActionsOnSave": {
    "source.fixAll": "explicit",
    "source.fixAll.eslint": "explicit",
    "source.fixAll.tslint": "explicit",
    "source.addMissingImports": "explicit"
  },
  "eslint.validate": [
    "javascript",
    "javascriptreact",
    "typescript",
    "typescriptreact"
  ],
  "javascript.validate.enable": false,
  "javascript.updateImportsOnFileMove.enabled": "prompt",
  "typescript.updateImportsOnFileMove.enabled": "never",
  "js/ts.implicitProjectConfig.checkJs": true,
  "editor.formatOnPaste": true,
  "editor.formatOnType": true,
  "editor.inlineSuggest.enabled": true,

  // Git & GitHub
  "git.openRepositoryInParentFolders": "never",
  "gitlens.advanced.messages": {
    "suppressCommitHasNoPreviousCommitWarning": true
  },
  "github.copilot.enable": {
    "*": true,
    "plaintext": false,
    "markdown": true,
    "scminput": false
  },
  "cSpell.enableFiletypes": [
    "!asciidoc",
    "!c",
    "!cpp",
    "!csharp",
    "!css",
    "!elixir",
    "!erlang",
    "!git-commit",
    "!go",
    "!graphql",
    "!handlebars",
    "!haskell",
    "!html",
    "!jade",
    "!java",
    "!javascript",
    "!javascriptreact",
    "!json",
    "!jsonc",
    "!jupyter",
    "!less",
    "!php",
    "!pug",
    "!python",
    "!restructuredtext",
    "!rust",
    "!scala",
    "!scminput",
    "!scss",
    "!swift",
    "!typescript",
    "!typescriptreact",
    "!vue",
    "!yaml",
    "!yml",
    "mdx"
  ]
}
```

## Code Snippets

_Snippets -> Configure User Snippets -> New Global Snippets File_

```json
{
  "Print to console": {
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
  }
}
```
