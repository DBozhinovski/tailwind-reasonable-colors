# Reasonable colors for Tailwind

## Motivation

Tailwind's default color palette is excellent and works well for the most part. However, I found myself configuring projects with the [reasonable colors](https://reasonable.work/colors/) palette due to the easier accessibility reasonable colors offer. To avoid copying and pasting the same config over and over, I packaged this as a plugin. PRs open and contributions welcome 🍻

## Installation and usage

- Run `npm i tailwind-reasonable-colors` to install the package.
- The package comes in two flavors: `enhance` and `override`.
  - `enhance` adds the reasonable colors palette to the existing palette without causing clashes. All added colors come prefixed with an `r`. So `pink` becomes `rpink` and can be used, for example, via `bg-rpink-400`.
  - `override` simply overwrites color names, but otherwise leaves the existing tailwind palette intact.

## Examples

### Using enhance

```js
// tailwind.config.js
const reasonable = require('tailwind-reasonable-colors');

module.exports = {
  ...
  plugins: [
    reasonable.enhance,
  ]
}
```

### Using override

```js
// tailwind.config.js
const reasonable = require('tailwind-reasonable-colors');

module.exports = {
  ...
  plugins: [
    reasonable.override,
  ]
}
```

