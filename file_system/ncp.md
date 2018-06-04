### ncp

#### Introduction

Asynchronous recursive file & directory copying.[document](https://www.npmjs.com/package/ncp)

#### Usage

```js
var ncp = require('ncp').ncp;
 
ncp.limit = 16;
 
ncp(source, destination, function (err) {
 if (err) {
   return console.error(err);
 }
 console.log('done!');
});
```