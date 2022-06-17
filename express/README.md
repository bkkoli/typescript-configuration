# How to set up Typescript With Express

- [reference](https://blog.logrocket.com/how-to-set-up-node-typescript-express/)

## Install Dependencies

- Related with Express 

```bash
npm i -D express
```

- Related with Typescript
```bash
npm i -D typescript @types/express @types/node
```

## Create tsconfig.json

- [reference](https://github.com/tsconfig/bases/tree/main/bases)

```bash
npx tsc --init
```

## Install Linting Library

```bash
npm i -D eslint @typescript-eslint/parser @typescript-eslint/eslint-plugin
```

## Configure Eslint

- eslintrc.json
```json
{
  "parser": "@typescript-eslint/parser",
  "parserOptions": {
    "ecmaVersion": 12,
    "sourceType": "module"
  },
  "plugins": ["@typescript-eslint"],
  "extends": ["eslint:recommended", "plugin:@typescript-eslint/recommended"],
  "env": {
    "browser": true,
    "es2021": true
  },
  "rules": {
    "semi": [2, "never"],
    "no-console": ["warn", { "allow": ["debug", "warn", "info", "error"] }],
    "no-unused-vars": "warn",
    "no-empty": ["error", { "allowEmptyCatch": true }],
    "prettier/prettier": ["error", { "trailingComma": "es5", "semi": false, "singleQuote": true, "printWidth": 160, "arrowParens": "avoid" }]
  },
}
```
