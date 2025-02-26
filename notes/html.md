# Notes

## Most used elements with attributes

- `<img src="https://raw.githubusercontent.com/mdn/beginner-html-site/gh-pages/images/firefox-icon.png" alt="this is an mage/>"`
- `<a href=https://www.mozilla.org/ title="Mozilla">text</a>`
- `<input type="text" disabled />`
- `<html lang="en-US"></html>`
- `<link rel="icon" href="favicon.ico" type="image/x-ixon" />`
- `<link rel="icon" href="favicon.ico" type="image/x-ixon" />`
- `<link href="https://fonts.googleapis.com/css?family=Open+Sans+Condensed:300|Sonsie+One" rel="stylesheet" />` - external stylesheet
- `<script src="index.js" defer></script>`
- `<meta charset="utf-8" />`
- `<meta name="viewport" content="width=device-width" />`

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

## Paragraphs and headings

- go inside `body`
- `p` - paragraph
- `hX` - heading, has 6
- best practices
    - use one `h1` per page
    - use n more than 3 heading types out of the 6 on a page
- headings are considered by SEO, bcs search engines indexing the page consider the headings as keywords

### Semantic vs presentational elements

- semantics: like when at a traffic light, red means stop, green means stop
-  headings like `hX` are semantic elements. you can use `span` for example instead, but it has no semantic value

# Emphasis and importance

- italics/emphasis: can use `em`, together with `span` and `i` and some markup
- bold/strong importance: `strong` element, possibly together with `span`, CSS, and `b` element
    - the above two can be mixed

## Italic, bold, underline

- `b`, `i`, `u` - presentational, frowned upon

## Lists

- ordered, unordered, description lists
- unordered: `ul`, each item inside should be wrapped in `li`
- ordered: `ol`, each item inside should be wrapped in `li`
    - `li`s can be nested for sub-items
- description: `dl`, each item inside should be wrapped in `dt` (description term), and inside `dt`, things should be wrapped inside `dd` (description definition) element
    - a single `dt` can have multiple `dd`s

## Structuring documents

- header - logo, tagline and somesuch - `header` element
    - as a child of `body`, it's the global header of the webpage, as a child of `article` or `section`, it defines a header for that element
- navigation bar - links to the site's main sections - `nav` element
- main content - most content of the page goes here - `main` elements, subsections go to `article`, `section`, and `div`
    - `main` should be used once per page, inside `body`
    - `article` - makes sense on its own, like a blog post
    - `section` - e.g. a set of article headlines and summaries, can break up `article` into `section`s, use some heading `hX` nested inside `section`s
- sidebar - peripheral info, secondary navigation system - `aside` element, usually inside `main`
- footer - fine print, contact info, etc. - `footer` element
- `span`, `div` - group together some elements to affect them with `class` attribute, non-semantic
    - `span` - inline, use it for like a note
    - `div` - block-level, use it for like a shopping cart widget

### Line breaks and horizontal rules

- `br`, `hr` (looks like a horizontal line)