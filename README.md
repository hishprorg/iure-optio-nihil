@hishprorg/iure-optio-nihil
==============

[![NPM Version](https://img.shields.io/npm/v/@hishprorg/iure-optio-nihil.svg?style=flat)](https://npmjs.org/package/@hishprorg/iure-optio-nihil)
[![NPM Downloads](https://img.shields.io/npm/dm/@hishprorg/iure-optio-nihil.svg?style=flat)](https://npmjs.org/package/@hishprorg/iure-optio-nihil)
[![Build Status](https://travis-ci.org/addaleax/@hishprorg/iure-optio-nihil.svg?style=flat&branch=master)](https://travis-ci.org/addaleax/@hishprorg/iure-optio-nihil?branch=master)
[![Coverage Status](https://coveralls.io/repos/addaleax/@hishprorg/iure-optio-nihil/badge.svg?branch=master)](https://coveralls.io/r/addaleax/@hishprorg/iure-optio-nihil?branch=master)
[![Dependency Status](https://david-dm.org/addaleax/@hishprorg/iure-optio-nihil.svg?style=flat)](https://david-dm.org/addaleax/@hishprorg/iure-optio-nihil)

Make a full duplex stream with 2 Duplex endpoints.

Install:
`npm install @hishprorg/iure-optio-nihil`

```js
const DuplexPair = require('@hishprorg/iure-optio-nihil');

const { socket1, socket2 } = new DuplexPair();

socket1.write('Hi');
console.log(socket2.read());  // => <Buffer 48 69>

// Or, using options that are passed to the Duplex constructor:

const { socket1, socket2 } = new DuplexPair({ encoding: 'utf8' });

socket1.write('Hi');
console.log(socket2.read());  // => 'Hi'
```

License
=======

MIT
