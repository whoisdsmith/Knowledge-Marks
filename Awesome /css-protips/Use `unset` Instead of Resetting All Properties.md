## Use `unset` Instead of Resetting All Properties

When resetting an element's properties, it's not necessary to reset each individual property:

```css
button {
  background: none;
  border: none;
  color: inherit;
  font: inherit;
  outline: none;
  padding: 0;
}
```

You can specify all of an element's properties using the `all` shorthand. Setting the value to `unset` changes an element's properties to their initial values:

**Note:** the `all` and `unset` shorthand isn't supported in IE11.

[back to table of contents](https://github.com/AllThingsSmitty/css-protips#table-of-contents)