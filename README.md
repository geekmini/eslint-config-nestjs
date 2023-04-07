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
in `.vscode/settings.json`
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
in `tsconfig.json`
```json
{
    "compilerOptions": {
        "paths": {
            "@core/*": ["src/*"]
        }
    }
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