# lunr

This plugin provides a backend for the [search](https://github.com/GitbookIO/plugin-search) plugin.

This plugin is a default plugin.

### Disable this plugin

This is a default plugin and it can be disabled using a `book.json` configuration:

```js
{
    "plugins": ["-lunr"]
}
```

### Limitations

Lunr can't index a huge book, by default the index size is limited at ~100ko.

You can change this limit by settings the configuration `maxIndexSize`:

```js
{
    "pluginsConfig": {
        "lunr": {
            "maxIndexSize": 200000
        }
    }
}
```

### Disable indexing of a page

You can disable the indexing of a specific page by adding a YAML header to the page:

```md
---
search: false
---

# My Page

This page is not indexed in Lunr.
```

