# sma [![NPM version](https://img.shields.io/npm/v/sma.svg?style=flat)](https://www.npmjs.com/package/sma) [![NPM monthly downloads](https://img.shields.io/npm/dm/sma.svg?style=flat)](https://npmjs.org/package/sma) [![NPM total downloads](https://img.shields.io/npm/dt/sma.svg?style=flat)](https://npmjs.org/package/sma) [![Linux Build Status](https://img.shields.io/travis/doowb/sma.svg?style=flat&label=Travis)](https://travis-ci.org/doowb/sma)

> Calculate the simple moving average of an array.

Please consider following this project's author, [Brian Woodward](https://github.com/doowb), and consider starring the project to show your :heart: and support.

## Install

Install with [npm](https://www.npmjs.com/):

```sh
$ npm install --save sma
```

## Usage

```js
var sma = require('sma');
```

## API

### [sma](index.js#L24)

Calculate the simple moving average of an array. A new array is returned with the average of each range of elements. A range will only be calculated when it contains enough elements to fill the range.

**Params**

* `arr` **{Array}**: Array of numbers to calculate.
* `range` **{Number}**: Size of the window to use to when calculating the average for each range. Defaults to array length.
* `format` **{Function}**: Custom format function called on each calculated average. Defaults to `n.toFixed(2)`.
* `returns` **{Array}**: Resulting array of averages.

**Example**

```js
console.log(sma([1, 2, 3, 4, 5, 6, 7, 8, 9], 4));
//=> [ '2.50', '3.50', '4.50', '5.50', '6.50', '7.50' ]
//=>   │       │       │       │       │       └─(6+7+8+9)/4
//=>   │       │       │       │       └─(5+6+7+8)/4
//=>   │       │       │       └─(4+5+6+7)/4
//=>   │       │       └─(3+4+5+6)/4
//=>   │       └─(2+3+4+5)/4
//=>   └─(1+2+3+4)/4
```

## Attribution

Thanks to [@jonschlinkert](https://github.com/jonschlinkert) for simplifying the algorithm. For more moving average modules checkout the [related projects](#related-projects) below.

## About

<details>
<summary><strong>Contributing</strong></summary>

Pull requests and stars are always welcome. For bugs and feature requests, [please create an issue](../../issues/new).

Please read the [contributing guide](.github/contributing.md) for advice on opening issues, pull requests, and coding standards.

</details>

<details>
<summary><strong>Running Tests</strong></summary>

Running and reviewing unit tests is a great way to get familiarized with a library and its API. You can install dependencies and run tests with the following command:

```sh
$ npm install && npm test
```

</details>

<details>
<summary><strong>Building docs</strong></summary>

_(This project's readme.md is generated by [verb](https://github.com/verbose/verb-generate-readme), please don't edit the readme directly. Any changes to the readme must be made in the [.verb.md](.verb.md) readme template.)_

To generate the readme, run the following command:

```sh
$ npm install -g verbose/verb#dev verb-generate-readme && verb
```

</details>

### Related projects

You might also be interested in these projects:

[exponential-moving-average](https://www.npmjs.com/package/exponential-moving-average): Calculate an exponential moving average from an array of numbers. | [homepage](https://github.com/jonschlinkert/exponential-moving-average "Calculate an exponential moving average from an array of numbers.")

### Author

**Brian Woodward**

* [GitHub Profile](https://github.com/doowb)
* [Twitter Profile](https://twitter.com/doowb)
* [LinkedIn Profile](https://linkedin.com/in/jonschlinkert)

### License

Copyright © 2018, [Brian Woodward](https://doowb.com).
Released under the [MIT License](LICENSE).

***

_This file was generated by [verb-generate-readme](https://github.com/verbose/verb-generate-readme), v0.8.0, on September 12, 2018._