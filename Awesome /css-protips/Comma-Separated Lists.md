## Comma-Separated Lists

Make list items look like a real, comma-separated list:

```css
ul > li:not(:last-child)::after {
  content: ",";
}
```

Use the `:not()` pseudo-class and no comma will be added to the last item.

**Note:** This tip may not be ideal for accessibility, specifically screen readers. And copy/paste from the browser doesn't work with CSS-generated content. Proceed with caution.

[back to table of contents](https://github.com/AllThingsSmitty/css-protips#table-of-contents)