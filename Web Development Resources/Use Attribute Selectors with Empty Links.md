## Use Attribute Selectors with Empty Links

Display links when the `<a>` element has no text value but the `href` attribute has a link:

```css
a[href^="http"]:empty::before {
  content: attr(href);
}
```

That's pretty convenient.

### [Demo](http://codepen.io/AllThingsSmitty/pen/zBzXRx)

[back to table of contents](https://github.com/AllThingsSmitty/css-protips#table-of-contents)