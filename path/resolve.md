### resolve

#### Introduction

implements the node require.resolve() algorithm such that you can require.resolve() on behalf of a file asynchronously and synchronously[document](https://www.npmjs.com/package/resolve)

#### Usage

asynchronously resolve:

```js
var resolve = require('resolve');
resolve('tap', { basedir: __dirname }, function (err, res) {
    if (err) console.error(err)
    else console.log(res)
});
```

```
$ node example/async.js
/home/substack/projects/node-resolve/node_modules/tap/lib/main.js
```

synchronously resolve:

```
var resolve = require('resolve');
var res = resolve.sync('tap', { basedir: __dirname });
console.log(res);
```

```
$ node example/sync.js
/home/substack/projects/node-resolve/node_modules/tap/lib/main.js
```