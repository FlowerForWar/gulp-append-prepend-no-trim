# gulp-append-prepend-no-trim

### Fork from the original [gulp-append-prepend](https://github.com/JamesHemery/gulp-append-prepend) by [JamesHemery](https://github.com/JamesHemery).

---

Simple Gulp plugin.

[![License:MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://github.com/JamesHemery/gulp-append-prepend/blob/master/LICENCE)
[![npm](https://img.shields.io/npm/v/gulp-append-prepend.svg)](https://www.npmjs.com/package/gulp-append-prepend)
[![Build](https://travis-ci.org/JamesHemery/gulp-append-prepend.svg)](https://travis-ci.org/JamesHemery/gulp-append-prepend)

## Usage

First, install gulp-append-prepend-no-trim as a development dependency:

```
npm install gulp-append-prepend-no-trim --save-dev
```

Then, add it to your gulpfile.js:

```javascript
const { prependText, prependFile, appendText, appendFile } = require('gulp-append-prepend-no-trim');

function myAwesomeTask() {
  return src('index.html')
    .pipe(prependFile('header.html'))
    .pipe(prependText('<!-- HEADER -->'))
    .pipe(appendText('<!-- FOOTER -->'))
    .pipe(appendFile('footer.html'))
    .pipe(gulp.dest('www/'));
}
```

This example works with html but you can use any type of file.

## Methods

- `appendFile(filepath, separator)` The filepath can be an array. The separator is optional by default is "\n".
- `prependFile(filepath, separator)` The filepath can be an array. The separator is optional by default is "\n".
- `appendText(text, separator)` The text can be an array. The separator is optional by default is "\n".
- `prependText(text, separator)` The text can be an array. The separator is optional by default is "\n".

## Licence

This plugin is released under the [MIT licence](./LICENCE).

## Disclaimer

Feel free to make changes in this README.
