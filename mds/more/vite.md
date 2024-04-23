# Vite

[Vite](https://vitejs.dev/) is a modern and fast frontend build tool.

## Creating an App with Vite

_This command sets up a new project directory:_

```bash
npm create vite@latest vite-app
```

It will prompt you with templates you can choose from.

### Project Structure

- `node_modules` : Contains all the project’s npm dependencies.
- `public/` : For static assets which aren't processed by Vite.
- `src/` : Source directory where your app's source code is located.
- `index.html` : The entry point to your application (located at the root).
- `vite.config.js` : Configuration file for Vite.

### Default Scripts

```bash
npm run dev # Runs the app in development mode with HMR enabled.
npm run build # Builds the app for production.
npm run preview # Preview the production build locally for testing.
```
