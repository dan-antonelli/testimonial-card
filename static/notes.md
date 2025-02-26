# Notes

## Most used elements with attributes

- `<img src="https://raw.githubusercontent.com/mdn/beginner-html-site/gh-pages/images/firefox-icon.png" alt="this is an mage/>"`
- `<a href=https://www.mozilla.org/ title="Mozilla">text</a>`
- `<input type="text" disabled />`
- `<html lang="en-US"></html>`
- `<link rel="icon" href="favicon.ico" type="image/x-ixon" />`
- `<link rel="icon" href="favicon.ico" type="image/x-ixon" />`
- `<script src="index.js" defer></script>`

## Character references

- escape sequence of characters that represent another character
- syntax: `&#;`
- example: `&amp;`

## Elements

- `em`: italics
- `strong`: bold
- void elements: no closing tag, like `img`

### Attributes

- class, src (image source), alt (adds text description to an image), width etc.
    - if you use css attributes, that's already in pixels, no need to add `px`: `width="300"`

### Comments

- `<!-- comment -->`

#### Boolean attributes

- do not take values, true by default, if absent, false
- `disabled` - at form input elements

## HTML page structure

```
html
    head
        meta
        title
    head
    body
        p
    body
html
```

## Webpage metadata

- `head`: its content is not displayed on the page, holds metadata instead
    - property for example: `lang`
- `title`: used in search results
- all the examples below go ino the `head`

### The meta element

- attributes
    - `charset="utf-8"` - so it can handle most languages
    - `name="author"`
    - `content="dantonelli"`
        - basically key-value pairs, good idea to add two metas: one for the author, one for the page description
        - keywords in the description help with SEO
        - sitelinks can be added to have better search results in Google that display sub-pages
        - can use open graph data to show an image of the website as well with the title and description when you link to a page

### The link element - favicon

- `<link rel="icon" href="favicon.ico" type="image/x-ixon" />`
- `rel` attribute controls which favicon to show on which devices, like `rel="apple-touch-icon"`

### Reference CSS and JS

- css
    - `<link rel="stylesheet" href="styles.css" />`
- script
    - `<script src="index.js" defer></script>`
    - altenatively, you can also add the JS inside the script tag
    - `defer` ensures that the HTML is all loaded before JS runs, so there are no unreachable html elements