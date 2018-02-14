# acyort-i18n

[![Build Status](https://travis-ci.org/acyortjs/acyort-i18n.svg?branch=master)](https://travis-ci.org/acyortjs/acyort-i18n)

Based on [i18n-node-2](https://github.com/jeresig/i18n-node-2)

### Features

Add `"zero"` support

```js
{
    'cat': {
        'zero': 'no cats',
        'one': 'one cat',
        'other': '%d cats'
    }
}

i18n.__n('cat', 0)  // 'no cats'
i18n.__n('cat', 1)  // 'one cat'
i18n.__n('cat', 8)  // '8 cats'
```

### Usage

```js
const i18n = {}
const directory = 'path/to/language.yml'
const ymal = require('yamljs')
const language = 'en'

new I18n({
  locales: [language],
  registered: i18n,
  directory,
  extension: '.yml',
  parse: data => yaml.parse(data.toString()),
})
```
