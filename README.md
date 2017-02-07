# acyort i18n module

Based on i18n-node-2 [i18n-node-2](https://github.com/jeresig/i18n-node-2)

### changes

> add `"zero"` support

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

> remove `writeFile` 
