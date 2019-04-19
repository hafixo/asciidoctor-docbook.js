# DocBook converter for Asciidoctor.js

[![Travis build status](http://img.shields.io/travis/asciidoctor/asciidoctor-docbook.js.svg)](https://travis-ci.org/asciidoctor/asciidoctor-docbook.js)
[![npm version](http://img.shields.io/npm/v/@asciidoctor/docbook-converter.svg)](https://www.npmjs.com/package/@asciidoctor/docbook-converter)

## Install

```sh
$ npm i @asciidoctor/core @asciidoctor/docbook-converter
```

## Usage

```javascript
var asciidoctor = require('@asciidoctor/core')()
require('@asciidoctor/docbook-converter')()

const options = {
  attributes: { backend: 'docbook5', doctype: 'book' },
  standalone: true
}

const content = `= DocBook\n\
:doctitle: Awesome Asciidoctor\n\
:docdate: 2016-01-01\n\n\
== First section\n\
Once upon a time...`

const docbook = asciidoctor.convert(content, options)
//console.log(docbook)
```