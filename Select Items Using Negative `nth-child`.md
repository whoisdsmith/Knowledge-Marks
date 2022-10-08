## Select Items Using Negative `nth-child`

Use negative `nth-child` in CSS to select items 1 through n.

```css
li {
  display: none;
}

/* select items 1 through 3 and display them */
li:nth-child(-n+3) {
  display: block;
}
```

Or, since you've already learned a little about [using `:not()`](https://github.com/AllThingsSmitty/css-protips#use-not-to-applyunapply-borders-on-navigation), try:

```css
/* select all items except the first 3 and display them */
li:not(:nth-child(-n+3)) {
  display: block;
}
```

### [Demo](http://codepen.io/AllThingsSmitty/pen/WxjKZp)

[back to table of contents](https://github.com/AllThingsSmitty/css-protips#table-of-contents)