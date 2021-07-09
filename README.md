# Belwerks | Styles

Simple utility styles to get up and running quickly and consistently.

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
import 'belwerks-styles/utilities.css';
```

Stylesheets aren't cross-dependant, so you won't run into errors from only grabbing the one(s) you want.

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

Use  `.page-...` to set based on the page container (`vw`/`vh`) and `.container-...` to set to `100%` height or width of the element's parent.

```css
.page-height
.page-width
.container-height
.container-width
```

### Utilities

```css
.border-box
```

Collapse padding and border sizes when calculating the width of an element.

```css
.block
.inline
```

Set an element's display to `block` or `inline-block`.

```css
.hidden
.visually-hidden
```

Hide an element entirely, or hide only from view - leaving it to be read by assistive tech (eg. screen readers).