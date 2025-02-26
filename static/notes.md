# Notes

## Most used elements with attributes

- `<img src="https://raw.githubusercontent.com/mdn/beginner-html-site/gh-pages/images/firefox-icon.png" alt="this is an mage/>"`
- `<a href=https://www.mozilla.org/ title="Mozilla">text</a>`
- `<input type="text" disabled />`

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