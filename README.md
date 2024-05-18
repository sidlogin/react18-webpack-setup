# react18-webpack-setup
Create new react application from scratch using webpack 5

## Basic steps:
1. Create a folder for react project
2. Go inside of newly created folder and run `npm init` command to generate package.json
3. Create `public` folder inside project folder and create `index.html` file
4. create the `src` folder inside the react project folder
5. create `App.css`, `App.js` and `index.js` inside the `src` folder
6. install the `react` and `react-dom` node packages `npm i react react-dom`

## Babel transpiler configutation:
1. To run react code `ES6` system which supports `jsx` systax install following node packages `npm i --save-dev @babel/core @babel/preset-env @babel/preset-react @babel/cli`
2. create the `.babelrc` configuration file, this tells babel transpiler to what preset and plugins to use to transpile our code

## Webpack setup and configutation
Webpack run the custom build on React code from source directory and convertd ES6 or JSX systax in to common-js syntax and host output in to our public directory to view our react application in to browser.
1. install following npm packages `npm i --save-dev webpack webpack-cli webpack-dev-server babel-loader css-loader style-loader url-loader sass sass-loader html-webpack-plugin`
2. Create the `webpack.config.js` file and add the webpack configuration
3. Add the following script in package.json `"dev": "webpack serve --mode development"`
4. Add the following script in package.json `"webpack --mode production"`



### App.js code
```
import React from 'react';
import './App/css';

const App = () => {
    return (
        <div className="App">
            <h1>Hello React</h1>
        </div>
    )
}
export default App;
```

### index.js code
```
import React from 'react';
import ReactDOM from 'react-dom';
import App from './App';

ReactDOM.render(<App />, document.getElementById('root'));
```

### HTML Code
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>React Ecosystem</title>
</head>
<body>
    <div id="root"></div>
    <noscript>Please enable the javascript to view this application.</noscript>
    <script src="../dist/bundle.js"></script>
</body>
</html>
```
