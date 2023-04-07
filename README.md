# ESLint config file for NestJS projects

## Installation

With `yarn`:

```bash
yarn add -D @future.ai/eslint-config-nestjs
```

With `npm`:

```bash
npm i -D @future.ai/eslint-config-nestjs
```

## Usage

Create `.eslintrc.js` file:

```js
module.exports = {
  "extends": [
    "@future.ai/eslint-config-nestjs"
  ],
  "rules": {
      // overrides ...
  }
}
```

## Non-Relative Path
config vscode in `.vscode/settings.json`
```json
{
    "eslint.validate": [
        "javascript",
        "typescript"
    ],
    "javascript.preferences.importModuleSpecifier": "non-relative",
    "typescript.preferences.importModuleSpecifier": "non-relative",
}
```
config typescript in `tsconfig.json`
```json
{
    "compilerOptions": {
        "paths": {
            "@core/*": ["src/*"]
        }
    }
}
``` 
config jest in `jest.config.ts` or `jest-e2e.config.ts`
```js
module.exports = {
    // ...
    moduleNameMapper: {
        "@core/(.*)": "<rootDir>/src/$1"
    },
    collectCoverage: true,
    collectCoverageFrom: ["src/**/*.ts", "!src/**/{index,enum}.ts"]
}
```


## Format on Save
in `.vscode/settings.json`
```json
{
    "editor.codeActionsOnSave": {
        "source.fixAll.eslint": true
    }
}
```