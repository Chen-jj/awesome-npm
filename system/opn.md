### opn

#### Introduction

A better node-open. Opens stuff like websites, files, executables. Cross-platform.[document](https://www.npmjs.com/package/opn)

#### Usage

```js
const opn = require('opn');
 
// Opens the image in the default image viewer
opn('unicorn.png').then(() => {
    // image viewer closed
});
 
// Opens the url in the default browser
opn('http://sindresorhus.com');
 
// Specify the app to open in
opn('http://sindresorhus.com', {app: 'firefox'});
 
// Specify app arguments
opn('http://sindresorhus.com', {app: ['google chrome', '--incognito']});
```