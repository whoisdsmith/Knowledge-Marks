## Hide Autoplay Videos That Aren't Muted

This is a great trick for a custom user stylesheet. Avoid overloading a user with sound from a video that autoplays when the page is loaded. If the sound isn't muted, don't show the video:

```css
video[autoplay]:not([muted]) {
  display: none;
}
```

Once again, we're taking advantage of using the [`:not()`](https://github.com/AllThingsSmitty/css-protips#use-not-to-applyunapply-borders-on-navigation) pseudo-class.

[back to table of contents](https://github.com/AllThingsSmitty/css-protips#table-of-contents)