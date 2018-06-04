### cross-spawn

#### Introduction

A cross platform solution to node's spawn and spawnSync.[document](https://www.npmjs.com/package/cross-spawn)

#### Usage

```js
const spawn = require('cross-spawn');
 
// Spawn NPM asynchronously
const child = spawn('npm', ['list', '-g', '-depth', '0'], { stdio: 'inherit' });
 
// Spawn NPM synchronously
const result = spawn.sync('npm', ['list', '-g', '-depth', '0'], { stdio: 'inherit' });
```