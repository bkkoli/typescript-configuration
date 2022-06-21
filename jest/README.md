# How to set up Typescript With Jest

- [reference](https://jestjs.io/docs/getting-started)

## 1. Via babel
```bash
npm i -D @babel/preset-typescript
```

Then add @babel/preset-typescript to the list of presets in your babel.config.js.

```javascript
module.exports = {
  presets: [
    ['@babel/preset-env', {targets: {node: 'current'}}],
    '@babel/preset-typescript',
  ],
};
```

## 2. Via ts-jest

> Install Dependencies
```bash
npm i -D ts-jest @types/jest
```

> Modify jest configuration
```json
// OR package.json
{
  // ...
  "jest": {
    "extensionsToTreatAsEsm": [".ts"],
    "globals": {
      "ts-jest": {
        "useESM": true
      }
    },
    "moduleNameMapper": {
      "^(\\.{1,2}/.*)\\.js$": "$1"
    }
  }
}
```