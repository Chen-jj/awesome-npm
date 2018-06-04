### ora

#### Introduction

Elegant terminal spinner.[document](https://www.npmjs.com/package/ora)

#### Usage

```js
const ora = require('ora');
 
const spinner = ora('Loading unicorns').start();
 
setTimeout(() => {
    spinner.color = 'yellow';
    spinner.text = 'Loading rainbows';
}, 1000);
```