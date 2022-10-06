## Use `:root` for Flexible Type

The type font size in a responsive layout should be able to adjust with each viewport. You can calculate the font size based on the viewport height and width using `:root`:

```css
:root {
  font-size: calc(1vw + 1vh + .5vmin);
}
```

Now you can utilize the `root em` unit based on the value calculated by `:root`:

```css
body {
  font: 1rem/1.6 sans-serif;
}
```

### [Demo](http://codepen.io/AllThingsSmitty/pen/XKgOkR)

[back to table of contents](https://github.com/AllThingsSmitty/css-protips#table-of-contents)