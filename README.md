# Halloween JSDoc3 Theme

A clean, responsive documentation template theme for JSDoc 3, based on [Postman JSDoc3 Theme](https://github.com/postmanlabs/postman-jsdoc-theme)

## Install

```bash
$ npm install --save-dev halloween-jsdoc-theme
```

## Usage

Clone repository to your designated `jsdoc` template directory, then:

```bash
$ jsdoc entry-file.js -t path/to/halloween-jsdoc-theme
```

### Node.js Dependency

In your projects `package.json` file add a generate script:

```json
"script": {
  "generate-docs": "node_modules/.bin/jsdoc --configure .jsdoc.json --verbose"
}
```

In your `.jsdoc.json` file, add a template option.

```json
"opts": {
  "template": "node_modules/halloween-jsdoc-theme"
}
```

### Example JSDoc Config

```json
{
    "tags": {
        "allowUnknownTags": true,
        "dictionaries": ["jsdoc"]
    },
    "source": {
        "include": ["lib", "package.json", "README.md"],
        "includePattern": ".js$",
        "excludePattern": "(node_modules/|docs)"
    },
    "plugins": [
        "plugins/markdown"
    ],
    "templates": {
        "cleverLinks": true,
        "monospaceLinks": true
    },
    "opts": {
        "destination": "./docs/",
        "encoding": "utf8",
        "private": true,
        "recurse": true,
        "template": "./node_modules/halloween-jsdoc-theme"
    }
}
```

## License

Licensed under the MIT license.
