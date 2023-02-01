<!--

@license Apache-2.0

Copyright (c) 2018 The Stdlib Authors.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

-->

# Bitwise Rotation

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Bitwise rotation to the left.



<section class="usage">

## Usage

```javascript
import rotl32 from 'https://cdn.jsdelivr.net/gh/stdlib-js/number-uint32-base-rotl@esm/index.mjs';
```

#### rotl32( x, shift )

Performs a bitwise rotation to the left.

```javascript
import toBinaryStringUint32 from 'https://cdn.jsdelivr.net/gh/stdlib-js/number-uint32-base-to-binary-string@esm/index.mjs';

var x = 2147483649;
var bstr = toBinaryStringUint32( x );
// returns '10000000000000000000000000000001'

var y = rotl32( x, 10 );
// returns 1536

bstr = toBinaryStringUint32( y );
// returns '00000000000000000000011000000000'
```

</section>

<!-- /.usage -->

<section class="notes">

## Notes

-   If provided a `shift` equal to `0`, the function returns the input value.

    ```javascript
    var y = rotl32( 3, 0 );
    // returns 3
    ```

-   If provided a `shift` greater than `31`, the function performs a bitwise rotation based on the `5` least significant bits of `shift` (i.e., `shift % 32`).

    ```javascript
    var shift = 34; // 00000000000000000000000000100010

    var y = rotl( 1, shift ); // 00000000000000000000000000000100
    // returns 4
    ```

</section>

<!-- /.notes -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script type="module">

import toBinaryStringUint32 from 'https://cdn.jsdelivr.net/gh/stdlib-js/number-uint32-base-to-binary-string@esm/index.mjs';
import MAX_INT from 'https://cdn.jsdelivr.net/gh/stdlib-js/constants-uint32-max@esm/index.mjs';
import rotl32 from 'https://cdn.jsdelivr.net/gh/stdlib-js/number-uint32-base-rotl@esm/index.mjs';

var HALF;
var x;
var y;
var i;

for ( i = 0; i < 100; i++ ) {
    x = i;
    y = rotl32( x, 10 );
    console.log( '%d => %s => %s => %d', x, toBinaryStringUint32( x ), toBinaryStringUint32( y ), y );
}

HALF = (MAX_INT+1) / 2;
for ( i = 0; i < 100; i++ ) {
    x = HALF + i;
    y = rotl32( x, 10 );
    console.log( '%d => %s => %s => %d', x, toBinaryStringUint32( x ), toBinaryStringUint32( y ), y );
}

</script>
</body>
</html>
```

</section>

<!-- /.examples -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2023. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/number-uint32-base-rotl.svg
[npm-url]: https://npmjs.org/package/@stdlib/number-uint32-base-rotl

[test-image]: https://github.com/stdlib-js/number-uint32-base-rotl/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/stdlib-js/number-uint32-base-rotl/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/number-uint32-base-rotl/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/number-uint32-base-rotl?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/number-uint32-base-rotl.svg
[dependencies-url]: https://david-dm.org/stdlib-js/number-uint32-base-rotl/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://gitter.im/stdlib-js/stdlib/

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/number-uint32-base-rotl/tree/deno
[umd-url]: https://github.com/stdlib-js/number-uint32-base-rotl/tree/umd
[esm-url]: https://github.com/stdlib-js/number-uint32-base-rotl/tree/esm
[branches-url]: https://github.com/stdlib-js/number-uint32-base-rotl/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/number-uint32-base-rotl/main/LICENSE

</section>

<!-- /.links -->
