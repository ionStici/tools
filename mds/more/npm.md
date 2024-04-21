# NPM

[npm docs](https://docs.npmjs.com/)

**Node Package Manager (npm)** is the default package manager for **Node.js** (JavaScript runtime environment), it is used for managing and distributing software packages written in JavaScript.

## Installing npm

**npm** is installed together with Node. Check if Node and npm are installed:

```bash
node -v
npm -v
```

## Basic npm Commands

- `npm init` initialize npm in your project directory.
- `package.json` file will be created which holds various metadata relevant to the project.
- `npm install <package_name>` install a package under the `node_modules` directory in your project.
- `npm install` (no arguments) install all dependencies defined in the `package.json` file.
- `node_modules` directory contains the project's packages and dependencies.
- `npm update` update all packages in the `node_modules` directory and their dependencies.
- `npm uninstall <package_name>` remove a package from `node_modules`.

## package.json

`package.json` file is used to manage the project's dependencies and metadata.

- `name` : The name of the project.
- `version` : The project's current version.
- `scripts` : A collection of command line scripts to run various tasks such as testing, building, etc.
- `dependencies` : A list of npm packages that your project needs to run.
- `devDependencies` : Packages that are only needed for development and testing.

When sharing a project, we skip the `node_modules` directory because it is too large. Instead, we include the `package.json` file which can be used to reproduce the exact development workflow from `node_modules` by running `npm install`. This will install the dependencies and devDependencies of the project specified in `package.json`.

### dependencies and devDependencies

- `npm install <package> --save` install and save a package as a **dependency**.
- `npm install <package> --save-dev` (`-D` for short) install and save a package as a **dev dependency**.

If you want to remote the package name from `package.json` when you uninstall it, you must use these flags in the uninstall command as well.

`dependencies` are the packages your app needs to function correctly in production, such as programming functions. For example, `react` and `react-dom` are considered "dependencies" because they provide functionality required for your application to run in production.

`devDependencies` are packages necessary only during the development process, they are not needed when the application is running in production. For example, `vite` is used during development for bundling. Similarly `sass` is used during development to compile SCSS files to CSS.

## npm scripts

**npm scripts** are commands that can be defined in the `package.json` file, and that can be executed in the terminal using the `npm run` command. npm scripts are used for automating common development tasks, such as running tests, bundling code, starting servers, or other custom workflows.

Scripts are defined in the `scripts` section of the `package.json` file. You can create custom script names and associate them with command line commands.

```json
{
  "scripts": {
    "custom-script-name": "package-name",
    "dev": "vite",
    "build": "vite build"
  }
}
```

**To run an npm script**, use the `npm run` command followed by the script name `dev`

```bash
npm run dev
```

**Node:** You can chain scripts together using `&&` or handle more complex scenarios using other npm packages such as `npm-run-all`, etc.
