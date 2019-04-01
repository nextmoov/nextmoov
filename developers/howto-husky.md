# husky

husky allow to easily add git hooks in package.json, so that hooks can be shared between team members.

## install

```bash
yarn add --dev husky
```

## setup

add a husky entry in `package.json` with desired hooks, for instance

```json
{
  "scripts": {
    "lint": "eslint .",
    "test": "jest"
  },
  "husky": {
    "hooks": {
      "pre-commit": "yarn run lint && yarn run test"
    }
  }
}
```

each time you try to commit, husky hook is triggered to check for eslint and jest unit tests. If one command fails, commit is aborted

## bypass hook

use "--no-verify" flag in git command to bypass hook

```bash
git commit -m "Work in progress" --no-verify
```

## resources

- https://github.com/typicode/husky