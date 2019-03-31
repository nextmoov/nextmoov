# How to configure coding rules in a javascript project #

## Install ##

add required dependencies in your npm or yarn package

```bash
npx install-peerdeps --dev eslint-config-airbnb
```

## Setup ##

create a file `.eslintrc` in project root directory

```JSON
{
    "extends": "airbnb"
}
```

custom rules can be added, for instance

```JSON
{
    "extends": "airbnb",
    "env": {
        "es6": true,
        "node": true,
        "jest": true
    },
    "parserOptions": {
        "ecmaVersion": 2018
    },
    "rules": {
        "indent": [
            "error",
            4
        ],
        "no-use-before-define": "off"
    }
}
```

## Usage ##

in your `package.json`, add a script to run eslint on project root directory

```json
{
  "scripts": {
    "lint": "eslint ."
  },
}
```

The script can then be called with 

```bash
yarn lint
```

## Visual Studio Code integration ##

vscode automatically detects when `estlint` is installed when project is loaded. Any open file in editor is automatically checked on the fly and problems are reported in _problems_ tab:

![Screenshot_20190110_071730.png](https://bitbucket.org/repo/oLrBMq6/images/1556361938-Screenshot_20190110_071730.png)

Note: if you just installed eslint, restart vscode or use command `Reload Window` (`ctrl + shift + p`)

As a bonus, there is an option for automatically fixing some errors when possible when file is saved. To turn it on, open Settings (`ctrl + ,`) and search for `Eslint: Auto Fix On Save`. Useful to format code automatically.

## Disable eslint for specific line or file ##

Assuming you understand the rationales behind an eslint rule and that you want to disable the rule for a specific file or for a specific line, there are annotations that can be added in javascript comments

https://eslint.org/docs/user-guide/configuring#disabling-rules-with-inline-comments

Tip: in vscode, right-click on an error in _problems_ tab to add easily inline comment

Another way to disable entirely eslint checking for specific files is to add a `.eslintignore` file in project root directory.

Before disabling eslint rule, consider following options:

- search the web for rule rationales
- rewrite your code to be compliant to the rule
- discuss with colleague if rules should be reviewed in nextmoov conventions
- add a comment in code to explain why the rule has been exceptionally disabled

## Resources ##

- configure ESLint: https://eslint.org/docs/user-guide/configuring
- https://github.com/airbnb/javascript/tree/master/packages/eslint-config-airbnb

## Suggestions ##

Maybe we should create a repository to extend airbnb rules and add/overwrite some rules according to nextmoov conventions.