# Change Log

## [3.10.2] - 2023-07-12
- Fix strikethrough support by supporting striked0 keyword management

## [3.10.1] - 2023-06-23
- Support line height in RTF files

## [3.0.9] - 2022-07-16
- Support the META_DIBBITBLT record in WMF files

## [3.0.8] - 2022-04-18
- Add support for superscript and subscript

## [3.0.7] - 2021-04-06
- Make colortbl parsing more robust

## [3.0.6] - 2021-03-23
- Add support for text highlighting

## [3.0.5] - 2021-02-19
- Add support for implicitly defined par
- Fix exported typings so they work for users with strict null checks enabled

## [3.0.4] - 2020-11-29
- Add support for additional rtf special characters (e.g. dash and single quote)

## [3.0.3] - 2020-11-20
- Fix url rendering when passing in a onHyperlink() callback

## [3.0.2] - 2020-11-19
- Ignore unsupported right-to-left and left-to-right character hints to prevent them from breaking e.g. hyperlink parsing
- Fix source maps in Firefox

## [3.0.1] - 2020-04-19
- Fix the parsing of WMF `META_CREATEPALETTE` records
- Improve custom errors (RTFJSError, WMFJSError and EMFJSError) to get proper stack traces

## [3.0.0] - 2020-03-24
- Dropped requirement for jQuery and jQuery-Filter. This means that all public API methods now return html element instead of jQuery objects and also require any parameters to be html elements instead of jQuery options.
- Bundles are still transpiled to ES5 but will require polyfills for older browsers 

## [2.3.3] - 2020-01-11
- More double width character improvements
- Support for unicode characters outsider the basic multilingual plane (as used by new emojis etc.)
- Better symbol font handling

## [2.3.2] - 2019-08-31
- Improve support for double width characters

## [2.3.1] - 2018-07-29
- Fix picture rendering issues

## [2.3.0] - 2018-05-05
- Added minified bundles

## [2.2.1] - 2018-03-29
- Added getting started guide

## [2.2.0] - 2018-03-29
- Publish typings with npm package

## [2.1.0] - 2018-03-28
- support importing rtf.js as a module
- rtf.js is now published on npm: https://www.npmjs.com/package/rtf.js

## [2.0] - 2018-02-24
- rtf.js, wmf.js and emf.js are now in the `build` directory and named rtf.bundle.js, wmf.bundle.js and emf.bundle.js
- wmf.bundle.js and emf.bundle.js have to be loaded before rtf.bundle.js
- `loggingEnabled` used to be exposed as a property (RTFJS.loggingEnabled in rtf.js, same for wmf.js and emf.js), it is now a function which accepts a boolean value. The default is still true.
- rtf.js now requires a `Promise` polyfill to work on older browsers which don't support `Promise` (e.g. IE 11).
- The rtf.bundle.js file now contains both Symboltable.js and cptables.js so these files no longer have to be loaded manually through separate script tags.
- rtf.js `Document.render()` now returns a `Promise` which returns the generated HTML once it is fulfilled (see samples).

## [1.0] - 2018-02-19
- Stable
- ES5 compatible
- Supports IE 11
