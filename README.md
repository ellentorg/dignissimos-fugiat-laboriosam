# @ellentorg/dignissimos-fugiat-laboriosam <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

Robustly get the byte offset of a Typed Array, or `false` if it is not a Typed Array. Works cross-realm, in every engine, even if the `byteOffset` property is overridden.

## Example

```js
var typedArrayByteOffset = require('@ellentorg/dignissimos-fugiat-laboriosam');
var assert = require('assert');

assert.equal(false, typedArrayByteOffset(undefined));
assert.equal(false, typedArrayByteOffset(null));
assert.equal(false, typedArrayByteOffset(false));
assert.equal(false, typedArrayByteOffset(true));
assert.equal(false, typedArrayByteOffset([]));
assert.equal(false, typedArrayByteOffset({}));
assert.equal(false, typedArrayByteOffset(/a/g));
assert.equal(false, typedArrayByteOffset(new RegExp('a', 'g')));
assert.equal(false, typedArrayByteOffset(new Date()));
assert.equal(false, typedArrayByteOffset(42));
assert.equal(false, typedArrayByteOffset(NaN));
assert.equal(false, typedArrayByteOffset(Infinity));
assert.equal(false, typedArrayByteOffset(new Number(42)));
assert.equal(false, typedArrayByteOffset('foo'));
assert.equal(false, typedArrayByteOffset(Object('foo')));
assert.equal(false, typedArrayByteOffset(function () {}));
assert.equal(false, typedArrayByteOffset(function* () {}));
assert.equal(false, typedArrayByteOffset(x => x * x));
assert.equal(false, typedArrayByteOffset([]));

const buffer = new ArrayBuffer(32);

assert.equal(8, typedArrayByteOffset(new Int8Array(buffer, 8)));
assert.equal(8, typedArrayByteOffset(new Uint8Array(buffer, 8)));
assert.equal(8, typedArrayByteOffset(new Uint8ClampedArray(buffer, 8)));
assert.equal(4, typedArrayByteOffset(new Int16Array(buffer, 4)));
assert.equal(4, typedArrayByteOffset(new Uint16Array(buffer, 4)));
assert.equal(8, typedArrayByteOffset(new Int32Array(buffer, 8)));
assert.equal(8, typedArrayByteOffset(new Uint32Array(buffer, 8)));
assert.equal(16, typedArrayByteOffset(new Float32Array(buffer, 16)));
assert.equal(16, typedArrayByteOffset(new Float64Array(buffer, 16)));
assert.equal(16, typedArrayByteOffset(new BigInt64Array(buffer, 16)));
assert.equal(16, typedArrayByteOffset(new BigUint64Array(buffer, 16)));
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

[package-url]: https://npmjs.org/package/@ellentorg/dignissimos-fugiat-laboriosam
[npm-version-svg]: https://versionbadg.es/inspect-js/@ellentorg/dignissimos-fugiat-laboriosam.svg
[deps-svg]: https://david-dm.org/inspect-js/@ellentorg/dignissimos-fugiat-laboriosam.svg
[deps-url]: https://david-dm.org/inspect-js/@ellentorg/dignissimos-fugiat-laboriosam
[dev-deps-svg]: https://david-dm.org/inspect-js/@ellentorg/dignissimos-fugiat-laboriosam/dev-status.svg
[dev-deps-url]: https://david-dm.org/inspect-js/@ellentorg/dignissimos-fugiat-laboriosam#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@ellentorg/dignissimos-fugiat-laboriosam.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@ellentorg/dignissimos-fugiat-laboriosam.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@ellentorg/dignissimos-fugiat-laboriosam.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@ellentorg/dignissimos-fugiat-laboriosam
[codecov-image]: https://codecov.io/gh/inspect-js/@ellentorg/dignissimos-fugiat-laboriosam/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/inspect-js/@ellentorg/dignissimos-fugiat-laboriosam/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/inspect-js/@ellentorg/dignissimos-fugiat-laboriosam
[actions-url]: https://github.com/ellentorg/dignissimos-fugiat-laboriosam/actions
