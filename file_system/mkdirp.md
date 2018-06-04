### mkdirp

#### Introduction

Like mkdir -p, but in node.js.[document](https://www.npmjs.com/package/mkdirp)

#### Usage

```js
var mkdirp = require('mkdirp');
    
mkdirp('/tmp/foo/bar/baz', function (err) {
    if (err) console.error(err)
    else console.log('pow!')
});
```