## Vertically-Center Anything

No, it's not black magic, you really can center elements vertically. You can do this with flexbox...

```css
html,
body {
  height: 100%;
  margin: 0;
}

body {
  -webkit-align-items: center;
  -ms-flex-align: center;
  align-items: center;
  display: -webkit-flex;
  display: flex;
}
```

...and also with CSS Grid:

```css
body {
  display: grid;
  height: 100vh;
  margin: 0;
  place-items: center center;
}
```

Want to center something else? Vertically, horizontally...anything, anytime, anywhere? CSS-Tricks has [a nice write-up](https://css-tricks.com/centering-css-complete-guide/) on doing all of that.

**Note:** Watch for some [buggy behavior](https://github.com/philipwalton/flexbugs#3-min-height-on-a-flex-container-wont-apply-to-its-flex-items) with flexbox in IE11.

### [Demo](http://codepen.io/AllThingsSmitty/pen/GqmGqZ)

[back to table of contents](https://github.com/AllThingsSmitty/css-protips#table-of-contents)