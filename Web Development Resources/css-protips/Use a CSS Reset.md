## Use a CSS Reset

CSS resets help enforce style consistency across different browsers with a clean slate for styling elements. You can use a CSS reset library like [Normalize](http://necolas.github.io/normalize.css/), _et al._, or you can use a more simplified reset approach:

```css
*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
```

Now elements will be stripped of margins and padding, and `box-sizing` lets you manage layouts with the CSS box model.

### [Demo](http://codepen.io/AllThingsSmitty/pen/kkrkLL)

**Note:** If you follow the [Inherit `box-sizing`](https://github.com/AllThingsSmitty/css-protips#inherit-box-sizing) tip below you might opt to not include the `box-sizing` property in your CSS reset.

[back to table of contents](https://github.com/AllThingsSmitty/css-protips#table-of-contents)