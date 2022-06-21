# How to set up Typescript With Jest

- [reference](https://code.visualstudio.com/docs/typescript/typescript-debugging)

## 1. tsconfig.json
```json
{
  "compilerOptions": {
    "target": "es5",
    "module": "commonjs",
    "outDir": "out",
    "sourceMap": true // important!!!
  }
}
```

Then create launch.json file.

## 2. launch.json

First, Select Run and Debug Tab.

Second, Select settings icon to create configuration or modify configuration.

The details of the settings are as follows.

```json
{
  // Use IntelliSense to learn about possible attributes.
  // Hover to view descriptions of existing attributes.
  // For more information, visit: https://go.microsoft.com/fwlink/?linkid=830387
  "version": "0.2.0",
  "configurations": [
    {
      "type": "node",
      "request": "launch",
      "name": "Launch Program",
      "program": "${workspaceFolder}/src/server.ts", // Entrypoint of your program
      "preLaunchTask": "tsc: build - tsconfig.json",
      "outFiles": ["${workspaceFolder}/dist/**/*.js"], // results of compiled with typescript
    }
  ]
}
```