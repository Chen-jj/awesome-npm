### through2

#### Introduction

A tiny wrapper around Node streams.[document](https://www.npmjs.com/package/through2)

#### Usage

```js
fs.createReadStream('ex.txt')
  .pipe(through2(function (chunk, enc, callback) {
    for (var i = 0; i < chunk.length; i++)
      if (chunk[i] == 97)
        chunk[i] = 122 // swap 'a' for 'z'
 
    this.push(chunk)
 
    callback()
   }))
  .pipe(fs.createWriteStream('out.txt'))
  .on('finish', function () {
    doSomethingSpecial()
  })
```

Or object streams:

```js
var all = []
 
fs.createReadStream('data.csv')
  .pipe(csv2())
  .pipe(through2.obj(function (chunk, enc, callback) {
    var data = {
        name    : chunk[0]
      , address : chunk[3]
      , phone   : chunk[10]
    }
    this.push(data)
 
    callback()
  }))
  .on('data', function (data) {
    all.push(data)
  })
  .on('end', function () {
    doSomethingSpecial(all)
  })
```