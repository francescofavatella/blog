---
title: Minimal React App
---

## Create package.json file

```
npm init -y
```

## Install required package

```
npm i react react-dom react-scripts
```

## Create minimal boilerplate

### public/index.html

```html
<!DOCTYPE html>
<html>
  <body>
    <div id="root"></div>
  </body>
</html>
```

### src/index.js

```jsx
import React from "react";
import ReactDOM from "react-dom";

const App = () => "My App";

ReactDOM.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>,
  document.getElementById("root")
);
```

## Add npm commands in package.json

```json
"scripts": {
    "start": "react-scripts start",
    "build": "react-scripts build"
},
```

## Start the React App

```
npm start
```

## Example

You can find an example at the following repo [minimal-react-app](https://github.com/francescofavatella/minimal-react-app)
