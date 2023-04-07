# ESLint config file for NestJS projects

## Installation

With `yarn`:

```bash
yarn add -D @geekmini/eslint-config-nestjs
```

With `npm`:

```bash
npm i -D @geekmini/eslint-config-nestjs
```

## Usage

Create `.eslintrc.js` file:

```js
module.exports = {
  "extends": [
    "@sotream/eslint-config-nestjs"
  ],
  "rules": {
      // overrides ...
  }
}
```

## Auto Format on File Save
in `.vscode/settings.json`
```json
{
    "eslint.validate": [
        "javascript",
        "typescript"
    ],
    "editor.codeActionsOnSave": {
        "source.fixAll.eslint": true
    },
    "javascript.preferences.importModuleSpecifier": "non-relative",
    "typescript.preferences.importModuleSpecifier": "non-relative",
}
``` 
