# Jest #

## install ##

```bash
yarn add jest --dev
```

## write test ##

Create test file close to file under test. A standard practice is to add a _.spec_ suffix, for instance:

```
foo.js
foo.spec.js
```

## run tests ##

create a script in package.json

```json
{
    "scripts": {
        "test": "jest"
    }
}
```
and run it with

```
yarn test
```

alterntative: to run jest binary (from node_modules/.bin), use `yarn` or `npx` as a shortcut

```bash
yarn jest
```

handy for running a single test file

```bash
yarn jest foo/bar.spec
```

## advance configuration

Create a `jest.config.js` file if advanced configuration is needed. Use jest binary to easily create default config file with commented documentation

```
yarn jest --init
```

## code coverage

```bash
yarn test --coverage
```

this generates a coverage directory with an HTML report you can open in your favorite browser

```bash
 google-chrome coverage/lcov-report/index.html
```

## add rules in ESLint ##

there is a plugin that can be used for adding eslint rules regarding jest tests. Useful to prevent focused or skipped tests

```bash
yarn add --dev eslint-plugin-jest
```

and add in your `.eslintrc` file

```json
{
    "plugins": [
        "jest"
    ],
    "extends": [
        "plugin:jest/recommended"
    ],
}
```

## advices ##

- unit tests should be fast so they can be ran at each minor modification
- unit tests should be standalone; anyone cloning a repo should be able to run tests without extra setup. For instance, a test should not assume a mongodb is running for tests to pass. 
- unit tests must be run in isolation and dependencies should be mocked

todo: some thoughts are needed on integration and e2e tests

## Test Driven Development

- write a failing test **first**
- write minimal implementation for the test to pass
- refactor code if necessary

You should write one test at a time and run **all** the tests at each modification to make sure you don't break anything. By using this technique, you benefit several advantages:

- coverage is near 100 %
- prevent regression
- tests are a living documentation
- help designing clean API (if test is hard to write, maybe you should redesign)


## resources ##

- https://jestjs.io/docs/en/getting-started
- https://www.npmjs.com/package/eslint-plugin-jest