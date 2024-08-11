# Electron

---


## Installation

```bash
npm install --save-dev electron@latest
```


## Electron Forge is the new way to go

```bash
npm init electron-app@latest my-app --template=webpack
```

Then to run the dev version:

```bash
npm start
```

Then to build:

```bash
npm run make
```

## Dev

Dev/Prod boolean: ```app.isPackaged``` or ```electron-is-dev```


## HTML files

```mainWindow.loadURL(`file://${path.join(__dirname, '/build/index.html')}`)```


## Preload

```preload.js```

```javascript
const { contextBridge } = require('electron')

contextBridge.exposeInMainWorld('versions', {
  node: () => process.versions.node,
  chrome: () => process.versions.chrome,
  electron: () => process.versions.electron
  // we can also expose variables, not just functions
})
```

```main.js```

```javascript

```


## Boilerplates

React https://github.com/electron-react-boilerplate/electron-react-boilerplate

NextJs https://github.com/DarkGuy10/NextJS-Electron-Boilerplate

NextJs https://github.com/saltyshiomix/nextron

NextJs ts https://github.com/vercel/next.js/tree/canary/examples/with-electron-typescript


## Notes

The Electron team has changed how apps compiles
