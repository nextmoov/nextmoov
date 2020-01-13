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

|Name|Status|Type|Summary|Notes
|:--|:--|:--|:--|:--|
| **[eslint-config-airbnb](https://github.com/airbnb/javascript/tree/master/packages/eslint-config-airbnb)**| * | Style | Coding Style Guide | [howto](./howto-eslint-airbnb)
| [Prettier](https://prettier.io/)|  | Style | Code Formater |_Usage under consideration. Potential conflicts with eslint-config-airbnb._
| [~~TypeScript~~](https://www.typescriptlang.org/)| **FORBIDDEN**|Type|Strongly typed superset of JS|Add strong typing to JS. Use Flow instead.|
| [Flow](https://flow.org)| |Type|Static Type checker for JS|Allows incremental usage|
| [Yarn](https://yarnpkg.com/fr/)| |Libs|Package manager |Drop-in replacement of NPM. Faster and more reliable.
| [npx](https://www.npmjs.com/package/npx)| |Libs|Package Runner| One-off run of npm packages. [Recommended by Yarn](https://github.com/yarnpkg/yarn/issues/3937) for one-off usage. 
| [~~npm~~](https://yarnpkg.com/fr/)|**FORBIDDEN**|Libs|Package manager|Use Yarn instead
| [Jest](https://jestjs.io/docs/en/getting-started) | | test | testing framework by Facebook | [howto](./howto-jest)

## Yarn Lock file

As we are using Yarn as a package manager, you should **never** manipulate the project dependencies manually, if you need a new dependency you can run `yarn add my-awesome-lib` or `yarn add my-awesome-dev-lib --dev` to add it, Yarn will automatically updates the `yarn.lock` file with your recently added dependency and lock it within its version at the moment you've added it.

*How to deal with `yarn.lock` conflicts* : If, at some point, you have conflicts between your current version of this file and an older/newer version of it, solve the conflicts using the right strategy, usually `ours` or `mine` (in opposition to `theirs` - see [git ours/theirs](https://nitaym.github.io/ourstheirs/) or [git merge strategies doc](https://www.oreilly.com/library/view/git-pocket-guide/9781449327507/ch07.html
)).
Once the conflicts are fixed, run `yarn --frozen-lockfile` to get your local packages synced according to the new lockfile state.

## Node.js

|Name|Required/Forbidden|Type|Summary|Notes
|:--|:--|:--|:--|:--|
| **[winston](https://github.com/winstonjs/winston)**| * |Logs|Logging library|Forward logs & errors to various outputs (STDOUT, Sentry, Slack) depending on severity and environnement|
| **[winston-raven-sentry](https://github.com/niftylettuce/winston-raven-sentry)**|*|Logs|Logging library|Sentry Adapter for Winston. Should point to our Sentry Instance
| [~~Babel~~](https://babeljs.io/)| **FORBIDDEN** |Compiler|ES6 compiler|As we control the runtime on backend project, Babel must not e used. Use ESM for import features.|
| [ESM](https://www.npmjs.com/package/esm)| |Libs|ECMAscript module loader|Add ECMAscript loading feature to NodeJS|

## React

|Name|Required|Type|Summary|Notes
|:--|:--|:--|:--|:--|
| **[@sentry/browser](https://docs.sentry.io/platforms/javascript/react/)**| * |Logs|Logging library|Sentry Adapter for Browser and React. Should point to our Sentry instance. 
| [~~PropTypes~~](https://reactjs.org/docs/typechecking-with-proptypes.html)| **FORBIDDEN**|Libs|Type|Use Flow Instead
| [**storybook**](https://github.com/storybooks/storybook)| * | UI Testing | UI Components testing | Mandatory for every /components|
| [Redux](https://github.com/reduxjs/redux)|  |State Manager| App State manager |


## ReactNative

|Name|Required/Forbidden|Type|Summary|Notes
|:--|:--|:--|:--|:--|
| **[react-native-sentry](https://github.com/getsentry/react-native-sentry)**| * |Logs|Logging library|Sentry Adapter for React Native. Should point to our Sentry instance. 
| [nextmoov-rn-commons](https://bitbucket.org/nextmoov/nextmoov-rn-commons/)|  |UI|Shared Components Library|Our own sets of re-usable components for RN apps: Input, DatePicker, List, Buttons,...
| [**storybook**](https://github.com/storybooks/storybook)| * | UI Testing | UI Components testing | Mandatory for every /components|
| [~~PropTypes~~](https://reactjs.org/docs/typechecking-with-proptypes.html)| **FORBIDDEN**|Libs|Type|Use Flow Instead

