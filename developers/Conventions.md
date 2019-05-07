# Conventions

**"[Conventions over Configuration](https://en.wikipedia.org/wiki/Convention_over_configuration)"** is one of our core principles.  

We strongly believe sharing best practices, tools and libraries across project will help us produce code of a better uniformity and quality — and thus save a lot of time.

Following is a list of conventions, both shared across all projects, as well as specific to a Framework. 

## Shared

|Name|Type|Field|
|:--|:--|:--|
| **[GitFlow](https://nvie.com/posts/a-successful-git-branching-model/)**|Convention|Git Branching|
| **[Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0-beta.2/)**|Convention|Commits Message|


## JS Projects

|Name|Required|Type|Summary|Notes
|:--|:--|:--|:--|:--|
| **[eslint-config-airbnb](https://github.com/airbnb/javascript/tree/master/packages/eslint-config-airbnb)**| * | Style | Coding Style Guide | [howto](./howto-eslint-airbnb)
| [Prettier](https://prettier.io/)|  | Style | Code Formater |_Usage under consideration. Potential conflicts with eslint-config-airbnb._
| [~~TypeScript~~](https://www.typescriptlang.org/)| |Type|Strongly typed superset of JS|_Add strong typing to JS. More "All or Nothing" approach than Flow. Usage to be discussed, not to be used before decision taken_|
| [Flow](https://flow.org)| |Type|Static Type checker for JS|Allows incremental usage|
| [Yarn](https://yarnpkg.com/fr/)| |Libs|Package manager |Drop-in replacement of NPM. Faster and more reliable.
| [~~npm~~](https://yarnpkg.com/fr/)|deprecated|Libs|Package manager|Use yarn instead
| [Jest](https://jestjs.io/docs/en/getting-started) | | test | testing framework by Facebook | [howto](./howto-jest)


## Node.js

|Name|Required|Type|Summary|Notes
|:--|:--|:--|:--|:--|
| **[winston](https://github.com/winstonjs/winston)**| * |Logs|Logging library|Forward logs & errors to various outputs (STDOUT, Sentry, Slack) depending on severity and environnement|
| **[winston-raven-sentry](https://github.com/niftylettuce/winston-raven-sentry)**|*|Logs|Logging library|Sentry Adapter for Winston. Should point to our Sentry Instance
| **[nextmoov-ops-drone: nodejs template]()**| * |Deploy|Drone Integration|**TODO** CI/CD Config for your project to be tested and deployed on our infrastructure

## React

|Name|Required|Type|Summary|Notes
|:--|:--|:--|:--|:--|
| **[@sentry/browser](https://docs.sentry.io/platforms/javascript/react/)**| * |Logs|Logging library|Sentry Adapter for Browser and React. Should point to our Sentry instance. 
| [PropTypes](https://reactjs.org/docs/typechecking-with-proptypes.html)| |Libs|Type|Recommended for small projets. Use Flow for larger codebases, and nothing for tiny projects.| [storybook](https://github.com/storybooks/storybook)|  |UI Testing|UI Components testing|
| [Redux](https://github.com/reduxjs/redux)|  |State Manager| App State manager |
| **[nextmoov-ops-drone: ReactJS template]()**| * |Deploy|Drone Integration|**TODO** CI/CD Config for your project to be tested and deployed on our infrastructure


## ReactNative

|Name|Required|Type|Summary|Notes
|:--|:--|:--|:--|:--|
| **[react-native-sentry](https://github.com/getsentry/react-native-sentry)**| * |Logs|Logging library|Sentry Adapter for React Native. Should point to our Sentry instance. 
| [nextmoov-rn-commons](https://bitbucket.org/nextmoov/nextmoov-rn-commons/)|  |UI|Shared Components Library|Our own sets of re-usable components for RN apps: Input, DatePicker, List, Buttons,...
| [storybook](https://github.com/storybooks/storybook)|  |UI Testing|UI Components testing|
| [PropTypes](https://reactjs.org/docs/typechecking-with-proptypes.html)| |Libs|Type|Recommended for small projets. Use Flow for larger codebases, and nothing for tiny projects.

