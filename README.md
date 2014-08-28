JSX
===

JSX is a XML-like syntax extension to ECMAScript without any defined semantics. It's NOT intended to be implemented by engines or browsers. It's intended to be used by various preprocessors (transpilers) to transform these tokens into standard ECMAScript.

Rationale
---------

The purpose of this specification is to define a concise and familiar syntax for defining tree structures with attributes. A generic but well defined syntax enables a community of independent parsers and syntax highlighters to conform to a single specification.

Embedding a new syntax in an existing language is a risky venture. Other syntax implementors or the existing language may introduce another incompatible syntax extension.

Through a stand-alone specification, we make it easier for implementors of other syntax extensions to consider JSX when designing their own syntax. This will hopefully allow various new syntax extensions to co-exist.

It is our intention to claim minimal syntactic real estate while keeping the syntax concise and familiar. That way we leave the door open for other extensions.

Syntax
------

TODO

Parser Implementations
----------------------

- [acorn-jsx](https://github.com/RReverser/acorn-jsx): A fork of acorn.
- [esprima-fb](https://github.com/facebook/esprima): A fork of esprima.
- [sweet-jsx](https://github.com/andreypopp/sweet-jsx): A sweet.js macro.

Transpilers
-----------

These are a set of transpilers that all conform to the JSX syntax but use different semantics on the output:

- [jsxdom](https://github.com/vjeux/jsxdom): Create DOM elements using JSX.
- [Mercury JSX](https://github.com/Raynos/mercury-jsx): Create virtual-dom VNodes or VText using JSX. 
- [React JSX](http://facebook.github.io/react/docs/jsx-in-depth.html): Create ReactElements using JSX.

Why not Template Literals?
--------------------------

[ECMAScript 6th Edition (ECMA-262)](http://people.mozilla.org/~jorendorff/es6-draft.html) introduces template literals which are intended to be used for embedding DSL in ECMAScript. Why not just use that instead of inventing a syntax that's not part of ECMAScript?

TODO

Prior Art
---------

The JSX syntax was derived from the [E4X Specification (ECMA-357)](http://www.ecma-international.org/publications/standards/Ecma-357.htm). E4X is a deprecated specification with deep reaching semantic meaning. JSX is a tiny subset of the E4X syntax with the addition of spread attributes. JSX is a stand-alone specification has no relation to the E4X specification.
