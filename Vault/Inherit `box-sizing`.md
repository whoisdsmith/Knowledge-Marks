## Inherit `box-sizing`

Let `box-sizing` be inherited from `html`:

```css
html {
  box-sizing: border-box;
}

*,
*::before,
*::after {
  box-sizing: inherit;
}
```

This makes it easier to change `box-sizing` in plugins or other components that leverage other behavior.

### [Demo](https://css-tricks.com/inheriting-box-sizing-probably-slightly-better-best-practice/)

[back to table of contents](https://github.com/AllThingsSmitty/css-protips#table-of-contents)