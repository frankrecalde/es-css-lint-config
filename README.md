[![Publish Package to npmjs](https://github.com/frankrecalde/es-css-lint-config/actions/workflows/npm-publish-package.yml/badge.svg)](https://github.com/frankrecalde/es-css-lint-config/actions/workflows/npm-publish-package.yml)

# JS and CSS lint configuration
JS and CSS lint configuration for projects

## Usage

`npm i --save-dev @frankrecalde/es-css-lint-config`

`.eslintrc`

```json
{
  "extends": ["@frankrecalde/es-css-lint-config/drupal"],
  "root": true
}
```

`.stylelintrc`

```json
{
  "extends": ["@frankrecalde/es-css-lint-config/style"]
}
```

`.prettierrc.js`

```js
module.exports = {
  ...require("@frankrecalde/es-css-lint-config/prettier"),
};
```

or

`package.json`

```json
{
  "devDependencies": {
    "@frankrecalde/es-css-lint-config": "^0.0.1"
  },
  "eslintConfig": {
    "extends": ["@frankrecalde/es-css-lint-config/drupal"],
    "root": true
  },
  "stylelint": { "extends": ["@frankrecalde/es-css-lint-config/style"] },
  "prettier": "@frankrecalde/es-css-lint-config/prettier"
}
```

## Vscode

### Recommended addons

- EsLint
- Prettier - Code formatter
- Stylelint

### Recommended settings

```json
  "[javascript]": {
    "editor.formatOnSave": false,
    "editor.formatOnType": false,
    "editor.formatOnPaste": false,
    "editor.codeActionsOnSave": {
      "source.fixAll.eslint": true
    },
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[typescript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[scss]": {
    "editor.formatOnSave": true,
    "editor.formatOnType": false,
    "editor.formatOnPaste": false,
    "editor.defaultFormatter": "esbenp.prettier-vscode",
    "editor.codeActionsOnSave": {
      "source.fixAll.stylelint": true
    }
  },
  "[vue]": {
    "editor.formatOnSave": true,
    "editor.formatOnType": false,
    "editor.formatOnPaste": false,
    "editor.codeActionsOnSave": {
      "source.fixAll.eslint": true,
      "source.fixAll.stylelint": true
    },
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "javascript.format.insertSpaceBeforeFunctionParenthesis": false,
```
