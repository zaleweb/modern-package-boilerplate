<p align="center">
   <img src="https://raw.githubusercontent.com/eunikitin/modern-package-boilerplate/master/internals/img/header.png" alt="Header">
</p>

<p align="center">
  Powerful, flexible and easy-to-use boilerplate for creating modern npm packages
</p>

<p align="center">
  <a href="https://babeljs.io/">
    <img src="https://raw.githubusercontent.com/eunikitin/modern-package-boilerplate/master/internals/img/js.png" alt="Babel">
  </a>
  <a href="https://rollupjs.org/">
    <img src="https://raw.githubusercontent.com/eunikitin/modern-package-boilerplate/master/internals/img/rollup.png" alt="Rollup">
  </a>
  <a href="https://reactjs.org/">
    <img src="https://raw.githubusercontent.com/eunikitin/modern-package-boilerplate/master/internals/img/react.png" alt="React">
  </a>
  <a href="https://flow.org">
    <img src="https://raw.githubusercontent.com/eunikitin/modern-package-boilerplate/master/internals/img/flow.png" alt="FlowJS">
  </a>
  <a href="https://facebook.github.io/jest/">
    <img src="https://raw.githubusercontent.com/eunikitin/modern-package-boilerplate/master/internals/img/jest.png" alt="Jest">
  </a>
  <a href="https://eslint.org/">
    <img src="https://raw.githubusercontent.com/eunikitin/modern-package-boilerplate/master/internals/img/eslint.png" alt="ESLint">
  </a>
</p>

<p align="center">
  <a href="https://travis-ci.org/eunikitin/modern-package-boilerplate">
    <img src="https://travis-ci.org/eunikitin/modern-package-boilerplate.svg?branch=master" alt="Build Status">
  </a>
  <a href="https://coveralls.io/github/eunikitin/modern-package-boilerplate?branch=master">
    <img src="https://coveralls.io/repos/github/eunikitin/modern-package-boilerplate/badge.svg?branch=master" alt="Coverage Status">
  </a>
  <a href="https://david-dm.org/eunikitin/modern-package-boilerplate">
    <img src="https://david-dm.org/eunikitin/modern-package-boilerplate/status.svg" alt="dependencies Status">
  </a>
  <a href="https://david-dm.org/eunikitin/modern-package-boilerplate?type=dev">
    <img src="https://david-dm.org/eunikitin/modern-package-boilerplate/dev-status.svg" alt="devDependencies Status">
  </a>
  <a href="https://david-dm.org/eunikitin/modern-package-boilerplate?type=peer">
    <img src="https://david-dm.org/eunikitin/modern-package-boilerplate/peer-status.svg" alt="peerDependencies Status">
  </a>
</p>

# Features
## Key features
* Bundle your library with [Rollup](https://github.com/rollup/rollup)
* Write modern JavaScript with latest features of [Babel](https://babeljs.io/)
* Create your own distributable [React](https://reactjs.org/) components (optional)
* Check your types with [Flow](https://flow.org/) (optional)
* Test and cover with [Jest](https://facebook.github.io/jest/) and [Enzyme](http://airbnb.io/enzyme/)
* Lint with [ESLint](http://eslint.org/) ([air-bnb config](https://github.com/airbnb/javascript))


## Minor features
* Path aliases with babel [module-resolver](https://www.npmjs.com/package/babel-plugin-module-resolver) plugin
* CI with [travis-ci.org](https://travis-ci.org/)
* Coverage info with [coveralls.io](https://coveralls.io)
* Track and update your dependencies with [renovateapp.com](https://renovateapp.com/)

# Getting started
1. [Clone this repo from github](https://github.com/eunikitin/modern-package-boilerplate)
2. Inside the repo directory run `npm install && rm -r .git && git init`
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

#### `npm run coveralls`
Sends coverage details to [coveralls.io](https://coveralls.io).
Used in .travis.yml and should not be used manually.

#### `npm run lint`
Check your code for errors and code styles

#### `npm run prepublish`
Hook for npm, that executes when you publishing package in npm repository.

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
