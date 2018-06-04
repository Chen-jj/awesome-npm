### vinyl-fs

#### Introduction

Vinyl adapter for the file system.[document](https://www.npmjs.com/package/vinyl-fs)

#### Usage

```js
var map = require('map-stream');
var vfs = require('vinyl-fs');
 
var log = function(file, cb) {
  console.log(file.path);
  cb(null, file);
};
 
vfs.src(['./js/**/*.js', '!./js/vendor/*.js'])
  .pipe(map(log))
  .pipe(vfs.dest('./output'));
```