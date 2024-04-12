[&larr; Back](./README.md)

# Linting

A **linter** is a tool that scans source code for potential issues, including syntax errors, faulty code structures, stylistic inconsistencies, and security.

Linters can automatically detect missing semicolons or future security breaches early on during the development cycle to reduce the number of errors that need to be resolved during testing.

Popular linters: [ESLint](https://eslint.org/) for JS and [Stylelist](https://stylelint.io/) for CSS.

Linters provides a number of automated checks that help streamline software development.

- **Syntax Errors:** Linters can automatically find and fix syntax errors before running your code, meaning fewer bugs to deal with during production.
- **Problematic Code Structures:** Linters can also flag potentially problematic code structures, or “code smells”. These are weak points in your application design, such as unnecessarily long methods and duplicated code, that could result in future bugs and impaired app performance.
- **Stylistic Code Conventions:** Linters also push developers to adhere to a consistent set of stylistic code standards, improving code readability and maintainability. Sticking to a consistent coding style saves time by enabling developers to focus on the application’s architecture and core logic rather than code aesthetics.
- **Security:** Some linters, such as ESLint, can detect potential security vulnerabilities in your code to help you ensure that the application is secure and well-protected.

<br>

## ESLint

Settings > ESLint: Run > onSave

<br>

```
npx eslint --init
```
