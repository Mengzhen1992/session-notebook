## 2022.08.31

1. grid-auto-flow: row; does not work

- there must be "grid-column"
- not only "grid-area"

## 2022.09.01

1. Relative Units

Relative units are units that are relative to the size of the viewport, the current font size, or the size of their parent element.

- vh (viewport height): 1vh is 1% of the viewport height
- vw (viewport width): 1vw is 1% of the viewport width
- em: 1em is the current font size, is relative to the font-size of its direct or nearest parent
- rem: 1rem is the font size of the root element, is only relative to the html (root) font-size
- %: 1% is 1% of the size of the parent element (this is calculated for width and height separately)
- calc(): allows you to combine multiple units and do math
  - e.g. calc(100vh - 100px)
  - or calc(50% - 10rem)

2. Screen Size

You can target specific screen sizes with the min-width and max-width media features.

```css
@media (min-width: 600px) {
  /* CSS rules that are only applied when the screen is at least 600px wide */
}

@media (max-width: 600px) {
  /* CSS rules that are only applied when the screen is at most 600px wide */
}
```

Avoid max-width media queries, because they are harder to reason about. It's easier to think about the smallest screen size first, and then add media queries for larger screens.

3. Orientation

You can target specific orientations with the orientation media feature.

```css
@media (orientation: portrait) {
  /* CSS rules that are only applied when the screen is in portrait orientation */
}

@media (orientation: landscape) {
  /* CSS rules that are only applied when the screen is in landscape orientation */
}
```

You can also target a specific aspect ratio with the aspect-ratio media feature.

4. Color Scheme

You can target specific color schemes with the prefers-color-scheme media feature.

```css
@media (prefers-color-scheme: dark) {
  /* CSS rules that are only applied when the user prefers a dark color scheme */
}

@media (prefers-color-scheme: light) {
  /* CSS rules that are only applied when the user prefers a light color scheme */
}
```

You can change your preferred color scheme in your operating system settings. On macOS, you can do this in System Preferences > General > Appearance.

5. Showing different images based on media queries

```html
<picture>
  <source
    media="(min-width: 1280px)"
    srcset="https://source.unsplash.com/random/1400x1050"
  />
  <source
    media="(min-width: 768px)"
    srcset="https://source.unsplash.com/random/800x600"
  />
  <img src="https://source.unsplash.com/random/400x300" alt="" />
</picture>
```

6. css-responsive two columns

```css
@media (min-width: 1024px) {
  .card-section {
    display: flex;
    flex-flow: row wrap;
    justify-content: center;
    gap: 40px;
  }
  .product-card {
    width: 45vw;
  }
  .intro-text {
    width: 45vw;
    align-self: flex-start;
  }
}
```
