# Boilerplate for creating npm packages with ES6 
[![dependencies Status](https://david-dm.org/eunikitin/npm-package-es6-boilerplate/status.svg)](https://david-dm.org/eunikitin/npm-package-es6-boilerplate)
[![devDependencies Status](https://david-dm.org/eunikitin/npm-package-es6-boilerplate/dev-status.svg)](https://david-dm.org/eunikitin/npm-package-es6-boilerplate?type=dev)

## Features
* Build with [webpack 2](https://webpack.js.org/) and [babel](https://babeljs.io/)
* Test with [mocha](https://mochajs.org/), [chai](http://chaijs.com/) and [sinon](http://sinonjs.org/)
* Cover with [istanbul](https://github.com/gotwarlost/istanbul)

## Installation
1. Clone this repo
2. Inside repo directory run `npm install && rm -r .git && git init`
2. Update package.json with your information

## Usage
### Commands
#### `npm run clean`
Delete all cache and output files
#### `npm run dev`
Build your library in development mode
#### `npm run build`
Build your library in production mode
#### `npm run test`
Run tests
#### `npm run test:watch`
Run tests in watch mode
#### `npm run cover`
Cover your code (Work with ES6)

### Lint
This boilerplate uses
[air-bnb code style conventions](https://github.com/airbnb/javascript#table-of-contents),
however if you don't like it, you can disable it, by removing the following line in 
`.eslintrc` config file:
```js
{
  //...
  
  "extends": "airbnb"
}
```

### Webpack aliases
If you are as tired as me to write '../../../' in the
require statements, you can use
[alias feature provided by webpack](https://webpack.js.org/configuration/resolve/#resolve-alias).
Here is an example of aliases, built in this boilerplate
by default (`builder/resolve.js`):
```js
resolve: {
    alias: {
        Src: path.resolve(process.cwd() + '/src'),
        Lib: path.resolve(process.cwd() + '/lib')
    }
}
```
Feel free to add your custom aliases, they are awesome.