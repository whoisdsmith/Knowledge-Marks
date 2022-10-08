## Use `:not()` to Apply/Unapply Borders on Navigation

Instead of putting on the border...

```css
/* add border */
.nav li {
  border-right: 1px solid #666;
}
```

...and then taking it off the last element...

```css
/* remove border */
.nav li:last-child {
  border-right: none;
}
```

...use the `:not()` pseudo-class to only apply to the elements you want:

```css
.nav li:not(:last-child) {
  border-right: 1px solid #666;
}
```

Here, the CSS selector is read as a human would describe it.

### [Demo](http://codepen.io/AllThingsSmitty/pen/LkymvO)

[back to table of contents](https://github.com/AllThingsSmitty/css-protips#table-of-contents)