# [JSON](http://json.org)-HONEY

[![NPM version](https://badge.fury.io/js/json-honey.svg)](http://badge.fury.io/js/json-honey)
[![Build Status](https://travis-ci.org/gobwas/json-honey.svg?branch=master)](https://travis-ci.org/gobwas/json-honey)

> Yet another sweetest json prettifier (the best, of course).

![Winnie The Pooh](http://www.valdosta.edu/~kddykes/pooh_hunny.jpg)

## Whatsup

This is a simple tool, that convert your objects to JSON format, aligning the values and sorting the keys. 

Example:

```js

var honey = require("json-honey");

honey({
	aaaa: 1,
	a: 2,
	b: { b: 2, bb: 3, bbb: [1,2,3,null] },
  c: new Object
});
```

Will output:

```
{
  "aaaa": 1,
  "a":    2,
  "b": {
    "b":  2,
    "bb": 3,
    "bbb": [
      1,
      2,
      3,
      null
    ]
  },
  "c": {}
}
```

## API

#### honey(obj, [options])

##### obj
Type: `*`
Object to be stringified.

##### options
Type: `Object`

Optional options.

##### options.pad
Type: `number`
Default: `2`

##### options.sortBy
Type: `Function|Function[]`
Default: `null`

Function (or list of functions) to be applied at each key-value pair of object. Called with definition object with properties `key`, `value`.
It also have properties `parents` with parent nodes keys list, and `scalar` flag, that shows is it primitive value or not.

##### options.sortScalar
Type: `boolean`
Default: `true`

Indicates to sort or not by type of value in the object - is it scalar (primitive) (`boolean`, `string`, `number`) or not.

##### options.sortKey
Type: `boolean`
Default: `true`

Indicates to sort or not by key.

## Install

Of course, via npm.

```bash
npm install json-honey
```
