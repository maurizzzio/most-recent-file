# recently-modified-files

[![NPM version][npm-image]][npm-url]
[![Build Status][travis-image]][travis-url]
[![Codecov Status][codecov-image]][codecov-url]
[![Standard][standard-image]][standard-url]

> Gets a list of recently modified files in a dir

## Install

```sh
npm install --save recently-modified-files
```

## Usage

```js
import rmf from 'recently-modified-files'
```

### `rmf(dir, fn)`

**params**

- `dir` {string} The dir to test for files
- `fn` {Function} Callback, the arguments are
  - `err` {Error} Possible exception or null
  - `files` {Array} An array with the names of the files where the first one is the most recently modified file or an empty array when there are no files

### `const filenames = rmf.sync(dir)`

**params**

- `dir` {string} The path to test for files

**return**

An array of strings with the filenames on `path` in descending order with respect to the modified time

### `rmf.promise(dir)`

**params**

- `dir` {string} The path to test for files

**return**

A native promise, note that it's required that `global.Promise` is defined

**NOTE: the test to check if a file is a file is by calling `stat.isFile()` which means that folders/symlinks are ignored** 

## License

MIT © 2016 [Mauricio Poppe](http://maurizzzio.com)

[npm-url]: https://npmjs.org/package/recently-modified-files
[npm-image]: https://img.shields.io/npm/v/recently-modified-files.svg?style=flat

[travis-url]: https://travis-ci.org/maurizzzio/recently-modified-files
[travis-image]: https://img.shields.io/travis/maurizzzio/recently-modified-files.svg?style=flat

[codecov-url]: https://codecov.io/github/maurizzzio/recently-modified-files
[codecov-image]: https://img.shields.io/codecov/c/github/maurizzzio/recently-modified-files.svg?style=flat

[depstat-url]: https://david-dm.org/maurizzzio/recently-modified-files
[depstat-image]: https://david-dm.org/maurizzzio/recently-modified-files.svg?style=flat

[download-image]: http://img.shields.io/npm/dm/recently-modified-files.svg?style=flat

[standard-image]: https://img.shields.io/badge/code%20style-standard-brightgreen.svg?style=flat
[standard-url]: http://standardjs.com/

