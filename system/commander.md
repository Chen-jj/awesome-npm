### commander

#### Introduction

The complete solution for node.js command-line interfaces, inspired by Ruby's commander.[document](https://www.npmjs.com/package/commander)

#### Usage

```js
program
  .option('--type [typeName]', 'Build type, weapp/rn/h5')
  .option('--watch', 'Build type, weapp/rn/h5')
  .parse(process.argv)
```