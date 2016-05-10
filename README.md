# Axbit ESLint configuration

This is an opinionated ESLint configuration for server-side/Node.js ECMAScript 2015 (ES6) projects.
ESLint declares rules for code syntax and coding idioms. 

For Client-side/React (including transpiling with Babel) projects, proper extensions should be added, e.g.:
```json
{
    "plugins": [
        "react"
    ],
    "settings": {
        "react": {
            "version": "0.14.0"
        }
    },
    "extends": [
        "eslint:recommended",
        "plugin:react/recommended",
        "axbit"
    ],
    "parserOptions": {
        "sourceType": "module",
        "ecmaFeatures": {
            "jsx": true
        }
    },
    "env": {
        "browser": true,
        "node": false
    }
}    
```

## Usage

In your `package.json` file, include the config:
```json
"eslint-config-axbit": "Axbit/eslint-config-axbit"
```

In your `.eslintrc.json` config file, include the following at the top:
```json
"extends": "axbit"
```

Or if using [Grunt](http://gruntjs.com/) and [grunt-eslint](https://github.com/sindresorhus/grunt-eslint/), add the following in your Gruntfile.js:
```json
eslint: {
    server: {
        options: {
            baseConfig: 'axbit'
        },
        src: [
            ...
        ]
    },
},
```
