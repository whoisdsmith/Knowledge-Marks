## Set `:focus` for Form Elements

Sighted keyboard users rely on focus to determine where keyboard events go in the page. Make focus for form elements stand out and consistent then a browser's default implementation:

```css
a:focus,
button:focus,
input:focus,
select:focus,
textarea:focus {
  box-shadow: none;
  outline: #000 dotted 2px;
  outline-offset: .05em;
}
```

### [Demo](https://codepen.io/AllThingsSmitty/pen/ePzoOP/)

[back to table of contents](https://github.com/AllThingsSmitty/css-protips#table-of-contents)