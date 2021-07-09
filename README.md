# Belwerks | Styles

Simple utility styles to get up and running quickly and consistently. It's all written in plain CSS, with no dependencies or bloat. Link, download, or import any or all of the stylesheets and start using the utility classes right away!

Here's a silly example:

```html
<div class="page-height margin-center flex space-between top">
  <span class="grow">Hello there!</span>
  <span class="shrink visually-hidden">General Kenobi...</span>
</div>
```

## Install

```
npm i belwerks-styles
```

## Use (JSX)

You can grab the entire styles library by importing the package like you would any other CSS module:

```jsx
import 'belwerks-styles';
```

Or you can grab one or more separate stylesheets, if you don't want the whole thing:

```jsx
import 'belwerks-styles/layout.css';
import 'belwerks-styles/sizing.css';
import 'belwerks-styles/spacing.css';
import 'belwerks-styles/utilities.css';
```

Stylesheets aren't cross-dependant, so you won't run into errors from only grabbing the one(s) you want.

## Preview

You can serve the demo HTML page from the root directory by running:

```
npm run serve
```

And open http://localhost:9090 in your browser.

## Styles

### Layout

Use `.flex` and modifier classes to apply flexbox styles to a container element:

```css
.flex
  &.no-wrap
  &.space-around
  &.space-between
  &.space-evenly
  &.left
  &.right
  &.top
  &.bottom
  &.baseline
```

Children of a `.flex` container have a few modifiers as well:

```css
.flex
  > .shrink
  > .no-shrink
  > .grow
  > .no-grow
```

### Sizing

Use  `.page-` to set based on the page size (`vw`/`vh`) and `.container-` to set based on the element's parent.

```css
.page-height
.page-width
.container-height
.container-width
```

### Spacing

Remove existing margins or padding from an element:

```css
.margin-none
.padding-none
```

Center an element within its parent:

```css
.margin-center
```

### Utilities

Collapse padding and border sizes when calculating the width of an element:

```css
.border-box
```

Set an element's display to `block` or `inline-block`:

```css
.block
.inline
```

Hide an element entirely, or hide only from view - leaving it readable by assistive tech (eg. screen readers):

```css
.hidden
.visually-hidden
```