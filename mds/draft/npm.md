[&larr; Back](./README.md)

# NPM

**Node Package Manager (NPM)** is a package manager used for managing and distributing software packages written in JavaScript. It is the default package manager for **Node.js** (a JS runtime environment).

Before using **npm**, you need to install [**Node.js**](https://nodejs.org/en).

- Check if node is installed with `node -v`
- Check if npm is installed with `npm -v`

<!-- leaflet -->
<!-- lodash -->

<br>

## npm init

- Initialize **npm** with `npm init` inside your project directory.

- A `package.json` file will be created containing the definitions of our project.

<br>

## npm install

- Install Sass: `npm install sass --save-dev`

- The `--save-dev` option (or `-D`) indicates that the package we install is a tool for development, and it should be listed in _package.json_ under the field `"devDependencies"`.

- Install jQuery: `npm install jquery --save`

- The `--save` option informs that the package is a tool that offers programming functions, so it should be listed under the field `"dependencies"`

- Uninstall a pacakge: `npm uninstall jquery --save`

Right after we install any package, we get the `node_modules` directory which is responsible for making our packages work.

Why do we need to care about `dependencies` and `devDependencies` fields from the "package.json" file? To ease our development workflow.

For example, in case we need to send our project to someone else, we should omit the "node_modules" folder which is too big. Using the "package.json" file and the data it contains we can reproduce the exact development workflow from "node_modules" by running `npm init` which will install the project's dependencies and devDependencies.

<br>
 
## npm scripts

**A npm script** is a command defined in the project's `package.json` file that can be executed using the `npm run` command. npm scripts are used for automating common development tasks, such as running tests, building code, starting servers, or other custom workflows.

```
npm install sass npm-run-all -D
```

```json
"scripts": {
    "sass": "sass main.scss style.css -w",
    "live": "live-server",
    "dev": "npm-run-all --parallel sass live"
}
```

```
npm run dev
```

Example of a **development workflow** using Sass and live-server.

<!-- **A Build Process** is a sequence of tasks we perform automatically after we finish developing a project, or a certain feature of the project. The result of the build process is the final files ready for deployment. -->

<br>
