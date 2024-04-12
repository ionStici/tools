# Build Tools

## [**Vite**](https://vitejs.dev/) Frontend Tooling

```
npm create vite@latest folder-name
```

<br>

## What are Build Tools?

Types of build tools:

- **Package Managers (npm)** are used to install and manage Node.js packages.
- **Bundlers** are used to efficiently bundle assets such as JavaScript files, images, and fonts.
- **Task runners** are used to automate the process of running repetitive workflows.

Build tools can assit you with:

- Combining JavaScript modules and CSS into bundled files for production.
- Minifying files for improved performance.
- Running unit tests with one command.
- Automatically previewing changes to your application.

**A Build Process** is a sequence of tasks we perform automatically after we finish developing a project, or a certain feature of the project. The result of the build process is the final files ready for deployment.

## The Web Development Ecosystem

Three stages of producing a web app:

1. Development
2. Testing
3. Deployment

Build tools can assist with all of them.

## Types of Build Tools

**Task Runners** automate certain development processes, such as compiling code from SCSS to CSS or TypeScript to JavaScript.

**Bundlers** package JavaScript files and other assets such as stylesheets, images, and fonts into bundled files. Bundlers remove unused and duplicated code, improving download speed.

## Dependency Graphs

The connections between assets need to be mapped by the bundler to produce an output containing everything the app needs. This process uses a data structure called a _dependency graph_.

A dependency graph is a type of data structure formed by a directed graph representing the relationship between different files. When one file depends on another, a connection is added to the graph. Once all the connections are added, the bundler knows exactly what it must incorporate into the build.

## Improving Performance

A large and complex application can take a long time to download in the browser if not optimized.

To reduce the size of downloads, build tools utilize processes such as:

- **Code-splitting** is a technique that allows you to split your code into multiple files or chunks that can be loaded as needed.
- **Minification** is a process that removes comments, whitespace, and other unneeded data from your code. References in the code can also be renamed so that the resulting bundle is smaller.
- **Dead-code elimination** aims to remove any code not actually used by the finished application.
- **Tree-shaking** is a type of dead-code elimination that searches included modules for files and functions that are not used.

<br>
