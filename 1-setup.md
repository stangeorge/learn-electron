# Setup

## Install

Install nodejs by downloading the installers from nodejs.org or using homebrew. Then clone the following repo. This gives you the basic files: `package.json, index.html, main.js, , renderer.js,`

```bash
$ git clone https://github.com/electron/electron-quick-start
cd electron-quick-start
npm start
```

## Basic Files
`package.json` contains properties, dependencies etc. A few properties you may set right away are:

```json
  "name": "my-app",
  "productName": "My App",
```

`index.html` is loaded and displayed when your app starts

`productName` shows up in your file menu options such as "About My App" and "Quit My App"

`main.js` is where your application starts. `createWindow` and `mainWindow.loadURL` are two key methods:

```js
function createWindow () {
  // Create the browser window.
  mainWindow = new BrowserWindow({width: 800, height: 600,
    title: "My App" //shows on title bar
  }
)

// and load the index.html of the app.
  mainWindow.loadURL(url.format({
    pathname: path.join(__dirname, 'index.html'),
    protocol: 'file:',
    slashes: true
  }))
  ```

  `renderer.js` is for Node.js APIs. More at [https://electronjs.org/docs/glossary#renderer-process](https://electronjs.org/docs/glossary#renderer-process)

