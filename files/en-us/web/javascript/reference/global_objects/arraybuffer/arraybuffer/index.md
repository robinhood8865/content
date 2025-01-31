---
title: ArrayBuffer() constructor
slug: Web/JavaScript/Reference/Global_Objects/ArrayBuffer/ArrayBuffer
tags:
  - ArrayBuffer
  - Constructor
  - JavaScript
  - Reference
  - Polyfill
browser-compat: javascript.builtins.ArrayBuffer.ArrayBuffer
---

{{JSRef}}

The **`ArrayBuffer()`** constructor is used to create {{jsxref("ArrayBuffer")}} objects.

{{EmbedInteractiveExample("pages/js/arraybuffer-constructor.html","shorter")}}

## Syntax

```js
new ArrayBuffer(length)
```

> **Note:** `ArrayBuffer()` can only be constructed with [`new`](/en-US/docs/Web/JavaScript/Reference/Operators/new). Attempting to call it without `new` throws a {{jsxref("TypeError")}}.

### Parameters

- `length`
  - : The size, in bytes, of the array buffer to create.

### Return value

A new `ArrayBuffer` object of the specified size. Its contents are
initialized to 0.

### Exceptions

- {{jsxref("RangeError")}}
  - : Thrown if the `length` is larger than {{jsxref("Number.MAX_SAFE_INTEGER")}} (≥ 2<sup>53</sup>) or negative.

## Examples

### Creating an ArrayBuffer

In this example, we create a 8-byte buffer with a {{jsxref("Global_Objects/Int32Array",
  "Int32Array")}} view referring to the buffer:

```js
const buffer = new ArrayBuffer(8);
const view = new Int32Array(buffer);
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

### Compatibility notes

Starting with ECMAScript 2015, `ArrayBuffer` constructors require to be
constructed with a {{jsxref("Operators/new", "new")}} operator. Calling an
`ArrayBuffer` constructor as a function without `new`, will throw
a {{jsxref("TypeError")}} from now on.

```js example-bad
const buffer = ArrayBuffer(10);
// TypeError: calling a builtin ArrayBuffer constructor
// without new is forbidden
```

```js example-good
const buffer = new ArrayBuffer(10);
```

## See also

- [Polyfill of `ArrayBuffer` in `core-js`](https://github.com/zloirock/core-js#ecmascript-typed-arrays)
- [JavaScript typed arrays](/en-US/docs/Web/JavaScript/Typed_arrays)
- {{jsxref("SharedArrayBuffer")}}
