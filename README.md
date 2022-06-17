# How to set up Typescript With Express

- [reference](https://blog.logrocket.com/how-to-set-up-node-typescript-express/)

## Install Dependencies

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
```
{
  "parser": "@typescript-eslint/parser",
  "parserOptions": {
    "ecmaVersion": 12,
    "sourceType": "module"
  },
  "plugins": ["@typescript-eslint"],
  "extends": ["eslint:recommended", "plugin:@typescript-eslint/recommended"],
  "rules": {

  },
  "env": {
    "browser": true,
    "es2021": true
  },
}
```