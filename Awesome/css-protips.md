[![light bulb icon](https://camo.githubusercontent.com/6785766db499c7b89e9c6c426543c1056ca299015684b14ff94b8bf74a4644bf/68747470733a2f2f7261776769742e636f6d2f416c6c5468696e6773536d697474792f6373732d70726f746970732f6d61737465722f6d656469612f6c6f676f2e737667)](https://camo.githubusercontent.com/6785766db499c7b89e9c6c426543c1056ca299015684b14ff94b8bf74a4644bf/68747470733a2f2f7261776769742e636f6d2f416c6c5468696e6773536d697474792f6373732d70726f746970732f6d61737465722f6d656469612f6c6f676f2e737667)

## CSS Protips [![Awesome](https://camo.githubusercontent.com/abb97269de2982c379cbc128bba93ba724d8822bfbe082737772bd4feb59cb54/68747470733a2f2f63646e2e7261776769742e636f6d2f73696e647265736f726875732f617765736f6d652f643733303566333864323966656437386661383536353265336136336531353464643865383832392f6d656469612f62616467652e737667)](https://github.com/sindresorhus/awesome)

A collection of tips to help take your CSS skills pro.

> For other great lists check out [@sindresorhus](https://github.com/sindresorhus/)'s curated list of [awesome lists](https://github.com/sindresorhus/awesome/).

## Table of Contents

-   [Protips](https://github.com/AllThingsSmitty/css-protips#protips)
-   [Support](https://github.com/AllThingsSmitty/css-protips#support)
-   [Translations](https://github.com/AllThingsSmitty/css-protips#translations)
-   [Contribution Guidelines](https://github.com/AllThingsSmitty/css-protips/blob/master/CONTRIBUTING.md)

## Protips

1.  [Use a CSS Reset](https://github.com/AllThingsSmitty/css-protips#use-a-css-reset)
2.  [Inherit `box-sizing`](https://github.com/AllThingsSmitty/css-protips#inherit-box-sizing)
3.  [Use `unset` Instead of Resetting All Properties](https://github.com/AllThingsSmitty/css-protips#use-unset-instead-of-resetting-all-properties)
4.  [Use `:not()` to Apply/Unapply Borders on Navigation](https://github.com/AllThingsSmitty/css-protips#use-not-to-applyunapply-borders-on-navigation)
5.  [Check If Font Is Installed Locally](https://github.com/AllThingsSmitty/css-protips#check-if-font-is-installed-locally)
6.  [Add `line-height` to `body`](https://github.com/AllThingsSmitty/css-protips#add-line-height-to-body)
7.  [Set `:focus` for Form Elements](https://github.com/AllThingsSmitty/css-protips#set-focus-for-form-elements)
8.  [Vertically-Center Anything](https://github.com/AllThingsSmitty/css-protips#vertically-center-anything)
9.  [Comma-Separated Lists](https://github.com/AllThingsSmitty/css-protips#comma-separated-lists)
10.  [Select Items Using Negative `nth-child`](https://github.com/AllThingsSmitty/css-protips#select-items-using-negative-nth-child)
11.  [Use SVG for Icons](https://github.com/AllThingsSmitty/css-protips#use-svg-for-icons)
12.  [Use the "Lobotomized Owl" Selector](https://github.com/AllThingsSmitty/css-protips#use-the-lobotomized-owl-selector)
13.  [Use `max-height` for Pure CSS Sliders](https://github.com/AllThingsSmitty/css-protips#use-max-height-for-pure-css-sliders)
14.  [Equal-Width Table Cells](https://github.com/AllThingsSmitty/css-protips#equal-width-table-cells)
15.  [Get Rid of Margin Hacks With Flexbox](https://github.com/AllThingsSmitty/css-protips#get-rid-of-margin-hacks-with-flexbox)
16.  [Use Attribute Selectors with Empty Links](https://github.com/AllThingsSmitty/css-protips#use-attribute-selectors-with-empty-links)
17.  [Style "Default" Links](https://github.com/AllThingsSmitty/css-protips#style-default-links)
18.  [Intrinsic Ratio Boxes](https://github.com/AllThingsSmitty/css-protips#intrinsic-ratio-boxes)
19.  [Style Broken Images](https://github.com/AllThingsSmitty/css-protips#style-broken-images)
20.  [Use `rem` for Global Sizing; Use `em` for Local Sizing](https://github.com/AllThingsSmitty/css-protips#use-rem-for-global-sizing-use-em-for-local-sizing)
21.  [Hide Autoplay Videos That Aren't Muted](https://github.com/AllThingsSmitty/css-protips#hide-autoplay-videos-that-arent-muted)
22.  [Use `:root` for Flexible Type](https://github.com/AllThingsSmitty/css-protips#use-root-for-flexible-type)
23.  [Set `font-size` on Form Elements for a Better Mobile Experience](https://github.com/AllThingsSmitty/css-protips#set-font-size-on-form-elements-for-a-better-mobile-experience)
24.  [Use Pointer Events to Control Mouse Events](https://github.com/AllThingsSmitty/css-protips#use-pointer-events-to-control-mouse-events)
25.  [Set `display: none` on Line Breaks Used as Spacing](https://github.com/AllThingsSmitty/css-protips#set-display-none-on-line-breaks-used-as-spacing)

### Use a CSS Reset

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

#### [Demo](http://codepen.io/AllThingsSmitty/pen/kkrkLL)

**Note:** If you follow the [Inherit `box-sizing`](https://github.com/AllThingsSmitty/css-protips#inherit-box-sizing) tip below you might opt to not include the `box-sizing` property in your CSS reset.

[back to table of contents](https://github.com/AllThingsSmitty/css-protips#table-of-contents)

### Inherit `box-sizing`

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

#### [Demo](https://css-tricks.com/inheriting-box-sizing-probably-slightly-better-best-practice/)

[back to table of contents](https://github.com/AllThingsSmitty/css-protips#table-of-contents)

### Use `unset` Instead of Resetting All Properties

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

### Use `:not()` to Apply/Unapply Borders on Navigation

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

#### [Demo](http://codepen.io/AllThingsSmitty/pen/LkymvO)

[back to table of contents](https://github.com/AllThingsSmitty/css-protips#table-of-contents)

### Check If Font Is Installed Locally

You can check if a font is installed locally before fetching it remotely, which is a good performance tip, too.

```css
@font-face {
  font-family: "Dank Mono";
  src:
    /* Full name */
    local("Dank Mono"),
    /* Postscript name */
    local("Dank Mono"),
    /* Otherwise, download it! */
    url("//...a.server/fonts/DankMono.woff");
}

code {
  font-family: "Dank Mono", system-ui-monospace;
}
```

H/T to Adam Argyle for sharing this protip and [demo](https://codepen.io/argyleink/pen/VwYJpgR).

[back to table of contents](https://github.com/AllThingsSmitty/css-protips#table-of-contents)

### Add `line-height` to `body`

You don't need to add `line-height` to each `<p>`, `<h*>`, _et al_. separately. Instead, add it to `body`:

```css
body {
  line-height: 1.5;
}
```

This way textual elements can inherit from `body` easily.

#### [Demo](http://codepen.io/AllThingsSmitty/pen/VjbdYd)

[back to table of contents](https://github.com/AllThingsSmitty/css-protips#table-of-contents)

### Set `:focus` for Form Elements

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

#### [Demo](https://codepen.io/AllThingsSmitty/pen/ePzoOP/)

[back to table of contents](https://github.com/AllThingsSmitty/css-protips#table-of-contents)

### Vertically-Center Anything

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

#### [Demo](http://codepen.io/AllThingsSmitty/pen/GqmGqZ)

[back to table of contents](https://github.com/AllThingsSmitty/css-protips#table-of-contents)

### Comma-Separated Lists

Make list items look like a real, comma-separated list:

```css
ul > li:not(:last-child)::after {
  content: ",";
}
```

Use the `:not()` pseudo-class and no comma will be added to the last item.

**Note:** This tip may not be ideal for accessibility, specifically screen readers. And copy/paste from the browser doesn't work with CSS-generated content. Proceed with caution.

[back to table of contents](https://github.com/AllThingsSmitty/css-protips#table-of-contents)

### Select Items Using Negative `nth-child`

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

#### [Demo](http://codepen.io/AllThingsSmitty/pen/WxjKZp)

[back to table of contents](https://github.com/AllThingsSmitty/css-protips#table-of-contents)

### Use SVG for Icons

There's no reason not to use SVG for icons:

```css
.logo {
  background: url("logo.svg");
}
```

SVG scales well for all resolution types and is supported in all browsers [back to IE9](http://caniuse.com/#search=svg). Ditch your .png, .jpg, or .gif-jif-whatev files.

**Note:** If you have SVG icon-only buttons for sighted users and the SVG fails to load, this will help maintain accessibility:

```css
.no-svg .icon-only::after {
  content: attr(aria-label);
}
```

[back to table of contents](https://github.com/AllThingsSmitty/css-protips#table-of-contents)

### Use the "Lobotomized Owl" Selector

It may have a strange name but using the universal selector (`*`) with the adjacent sibling selector (`+`) can provide a powerful CSS capability:

```css
* + * {
  margin-top: 1.5em;
}
```

In this example, all elements in the flow of the document that follow other elements will receive `margin-top: 1.5em`.

For more on the "lobotomized owl" selector, read [Heydon Pickering's post](http://alistapart.com/article/axiomatic-css-and-lobotomized-owls) on _A List Apart_.

#### [Demo](http://codepen.io/AllThingsSmitty/pen/grRvWq)

[back to table of contents](https://github.com/AllThingsSmitty/css-protips#table-of-contents)

### Use `max-height` for Pure CSS Sliders

Implement CSS-only sliders using `max-height` with overflow hidden:

```css
.slider {
  max-height: 200px;
  overflow-y: hidden;
  width: 300px;
}

.slider:hover {
  max-height: 600px;
  overflow-y: scroll;
}
```

The element expands to the `max-height` value on hover and the slider displays as a result of the overflow.

[back to table of contents](https://github.com/AllThingsSmitty/css-protips#table-of-contents)

### Equal-Width Table Cells

Tables can be a pain to work with. Try using `table-layout: fixed` to keep cells at equal width:

```css
.calendar {
  table-layout: fixed;
}
```

Pain-free table layouts.

#### [Demo](http://codepen.io/AllThingsSmitty/pen/jALALm)

[back to table of contents](https://github.com/AllThingsSmitty/css-protips#table-of-contents)

### Get Rid of Margin Hacks With Flexbox

When working with column gutters you can get rid of `nth-`, `first-`, and `last-child` hacks by using flexbox's `space-between` property:

```css
.list {
  display: flex;
  justify-content: space-between;
}

.list .person {
  flex-basis: 23%;
}
```

Now column gutters always appear evenly-spaced.

[back to table of contents](https://github.com/AllThingsSmitty/css-protips#table-of-contents)

### Use Attribute Selectors with Empty Links

Display links when the `<a>` element has no text value but the `href` attribute has a link:

```css
a[href^="http"]:empty::before {
  content: attr(href);
}
```

That's pretty convenient.

#### [Demo](http://codepen.io/AllThingsSmitty/pen/zBzXRx)

[back to table of contents](https://github.com/AllThingsSmitty/css-protips#table-of-contents)

### Style "Default" Links

Add a style for "default" links:

```css
a[href]:not([class]) {
  color: #008000;
  text-decoration: underline;
}
```

Now links that are inserted via a CMS, which don't usually have a `class` attribute, will have a distinction without generically affecting the cascade.

[back to table of contents](https://github.com/AllThingsSmitty/css-protips#table-of-contents)

### Intrinsic Ratio Boxes

To create a box with an intrinsic ratio, all you need to do is apply top or bottom padding to a div:

```css
.container {
  height: 0;
  padding-bottom: 20%;
  position: relative;
}

.container div {
  border: 2px dashed #ddd;
  height: 100%;
  left: 0;
  position: absolute;
  top: 0;
  width: 100%;
}
```

Using 20% for padding makes the height of the box equal to 20% of its width. No matter the width of the viewport, the child div will keep its aspect ratio (100% / 20% = 5:1).

#### [Demo](http://codepen.io/AllThingsSmitty/pen/jALZvE)

[back to table of contents](https://github.com/AllThingsSmitty/css-protips#table-of-contents)

### Style Broken Images

Make broken images more aesthetically-pleasing with a little bit of CSS:

```css
img {
  display: block;
  font-family: sans-serif;
  font-weight: 300;
  height: auto;
  line-height: 2;
  position: relative;
  text-align: center;
  width: 100%;
}
```

Now add pseudo-elements rules to display a user message and URL reference of the broken image:

```css
img::before {
  content: "We're sorry, the image below is broken :(";
  display: block;
  margin-bottom: 10px;
}

img::after {
  content: "(url: " attr(src) ")";
  display: block;
  font-size: 12px;
}
```

Learn more about styling for this pattern in [Ire Aderinokun](https://github.com/ireade/)'s [original post](http://bitsofco.de/styling-broken-images/).

[back to table of contents](https://github.com/AllThingsSmitty/css-protips#table-of-contents)

### Use `rem` for Global Sizing; Use `em` for Local Sizing

After setting the base font size at the root (`html { font-size: 100%; }`), set the font size for textual elements to `em`:

```css
h2 {
  font-size: 2em;
}

p {
  font-size: 1em;
}
```

Then set the font-size for modules to `rem`:

```css
article {
  font-size: 1.25rem;
}

aside .module {
  font-size: .9rem;
}
```

Now each module becomes compartmentalized and easier to style, more maintainable, and flexible.

[back to table of contents](https://github.com/AllThingsSmitty/css-protips#table-of-contents)

### Hide Autoplay Videos That Aren't Muted

This is a great trick for a custom user stylesheet. Avoid overloading a user with sound from a video that autoplays when the page is loaded. If the sound isn't muted, don't show the video:

```css
video[autoplay]:not([muted]) {
  display: none;
}
```

Once again, we're taking advantage of using the [`:not()`](https://github.com/AllThingsSmitty/css-protips#use-not-to-applyunapply-borders-on-navigation) pseudo-class.

[back to table of contents](https://github.com/AllThingsSmitty/css-protips#table-of-contents)

### Use `:root` for Flexible Type

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

#### [Demo](http://codepen.io/AllThingsSmitty/pen/XKgOkR)

[back to table of contents](https://github.com/AllThingsSmitty/css-protips#table-of-contents)

### Set `font-size` on Form Elements for a Better Mobile Experience

To avoid mobile browsers (iOS Safari, _et al_.) from zooming in on HTML form elements when a `<select>` drop-down is tapped, add `font-size` to the selector rule:

```css
input[type="text"],
input[type="number"],
select,
textarea {
  font-size: 16px;
}
```

💃

[back to table of contents](https://github.com/AllThingsSmitty/css-protips#table-of-contents)

### Use Pointer Events to Control Mouse Events

[Pointer events](https://developer.mozilla.org/en-US/docs/Web/CSS/pointer-events) allow you to specify how the mouse interacts with the element it's touching. To disable the default pointer event on a button, for instance:

```css
.button-disabled {
  opacity: .5;
  pointer-events: none;
}
```

It's that simple.

[back to table of contents](https://github.com/AllThingsSmitty/css-protips#table-of-contents)

### Set `display: none` on Line Breaks Used as Spacing

As [Harry Roberts pointed out](https://twitter.com/csswizardry/status/1170835532584235008), this can help prevent CMS users from using extra line breaks for spacing:

```css
br + br {
  display: none;
}
```

[back to table of contents](https://github.com/AllThingsSmitty/css-protips#table-of-contents)
