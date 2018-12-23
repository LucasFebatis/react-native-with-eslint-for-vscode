# React Native Project with eslint for VS Code

This project aims to offer a step-by-step creation of a React Native project to be developed with VS Code

The project of this repository is configured as follows

Assuming that you have already created the project with the react-native cli as described on the [React Native page](https://facebook.github.io/react-native/docs/getting-started) and the command terminal / command prompt is open in the project folder (Preference with VS Code integrated), follow these steps:

## Disabling Typescript Lint for Workspace

* On Windows/Linux - File > Preferences > Settings
* On macOS - Code > Preferences > Settings

Change to the Workspace tab, then change in JSON mode by pressing the button in the upper right corner and add the following lines

    "typescript.validate.enable": false,
    "javascript.validate.enable": false,

## Instale o Plugin do VS Code: ESLint by Dirkbaeumer

It can be either the VS Code tab or if you prefer the link:

https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint

## Install the Development Dependencies and configure them

    # At the time of creation of this project was in the version 5.11.0
    npm install --save-dev eslint

### Start eslint

    # Windows:
    node_modules\.bin\eslint --init
    # OS X/Linux:
    ./node_modules/.bin/eslint --init

### Answer the questions as follows

    ? How would you like to configure ESLint? Answer questions about your style

    ? Which version of ECMAScript do you use? ES2015

    ? Are you using ES6 modules? Yes

    ? Where will your code run? Browser

    ? Do you use CommonJS? No

    ? Do you use JSX? Yes

    ? Do you use React? Yes

    ? What style of indentation do you use? Spaces

    ? What quotes do you use for strings? Single

    ? What line endings do you use? Unix

    ? Do you require semicolons? Yes

    ? What format do you want your config file to be in? JavaScript

### Install the required dependency for React

    # At the time of creation of this project was in the version 7.11.1
    npm install --save-dev eslint-plugin-react

### Install dependency to recognize Props

    # At the time of creation of this project was in the version 10.0.1
    npm install --save-dev babel-eslint

## Configure the .eslintrc.js file

### Add the following line

    "parser": "babel-eslint",

### In Rules add the following value
    "no-unused-vars": [
        "warn",
    ]

### Still in Rules, modify the indent attribute this way
        "indent": [
            "warn",
            2
        ],


## Links
 - https://chariotsolutions.com/blog/post/configure-visual-studio-code-lint-react-jsx-syntax/

 - https://github.com/babel/babel-eslint/issues/312

 - https://facebook.github.io/react-native/docs/getting-started
