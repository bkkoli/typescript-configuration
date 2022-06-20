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
```bash
npm i -D ts-jest @types/jest
```