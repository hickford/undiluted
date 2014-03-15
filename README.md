undiluted
=========

A 'hello world' app written in 100% CoffeeScript.

Installation
-----

Install from npm package registry https://www.npmjs.org/package/undiluted

    $ npm install -g undiluted

Usage
----

    $ undiluted
    hello

### Known issue

This happens:

    /usr/bin/undiluted: line 1: //: Is a directory
    /usr/bin/undiluted: line 2: syntax error near unexpected token `('
    /usr/bin/undiluted: line 2: `(function() {'

The problem is, the coffee-script compile doesn't (and can't be made to) prepend a shebang line to the Javascript. This is https://github.com/jashkenas/coffee-script/issues/2215

Development
------

[![Build Status](https://travis-ci.org/matt-hickford/undiluted.png?branch=master)](https://travis-ci.org/matt-hickford/undiluted)

    $ npm publish

(This calls `coffee --compile --output bin src`)

### Challenge

Either:

1. Edit this repo so that `npm install -g` correctly installs a working app. It must work both on Linux and Windows.
2. Fix the Coffeescript issue https://github.com/jashkenas/coffee-script/issues/2215 so the compiler can be made to prepend shebangs.
