## Use the "Lobotomized Owl" Selector

It may have a strange name but using the universal selector (`*`) with the adjacent sibling selector (`+`) can provide a powerful CSS capability:

```css
* + * {
  margin-top: 1.5em;
}
```

In this example, all elements in the flow of the document that follow other elements will receive `margin-top: 1.5em`.

For more on the "lobotomized owl" selector, read [Heydon Pickering's post](http://alistapart.com/article/axiomatic-css-and-lobotomized-owls) on _A List Apart_.

### [Demo](http://codepen.io/AllThingsSmitty/pen/grRvWq)

[back to table of contents](https://github.com/AllThingsSmitty/css-protips#table-of-contents)