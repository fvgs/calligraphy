<div align="center">
  <br>
  <br>
  <img src="https://raw.githubusercontent.com/fvgs/calligraphy/master/screenshot.png" alt="calligraphy" title="calligraphy" width="675px">
  <br>
  <br>
  <br>
</div>

# calligraphy [![npm](https://img.shields.io/npm/v/calligraphy.svg)](https://www.npmjs.com/package/calligraphy) [![downloads](https://img.shields.io/npm/dt/calligraphy.svg)](https://www.npmjs.com/package/calligraphy) [![maintained](https://img.shields.io/badge/maintained-%E2%9C%94-brightgreen.svg)](https://github.com/fvgs/calligraphy)

> Command-line Unicode block font

## Install

```
npm install --save calligraphy
```

## Usage

Currently supports the following characters:

> 0 1 2 3 4 5 6 7 8 9 \<space> : s

Each character is 5 (rows) x 7 (columns) and is provided as a 2D array of rows

```js
const {
  zero,
  one,
  two,
  three,
  four,
  five,
  six,
  seven,
  eight,
  nine,
  space,
  colon,
  s,
} = require('calligraphy')

const zipWith = require('lodash/zipWith')
const {EOL} = require('os')

// Prints '3'
three.forEach(line => console.log(line))

// Prints '12:45'
const time = [one, two, colon, three, four]
const output = zipWith(...time, (...args) => args.join('  ')).join(EOL)
console.log(output)
```
