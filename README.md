# Reasonable colors for Tailwind

## Motivation

Tailwind's default color palette is excellent and works well for the most part. However, I found myself configuring projects with the [reasonable colors](https://reasonable.work/colors/) palette due to the easier accessibility reasonable colors offer. To avoid copying and pasting the same config over and over, I packaged this as a plugin. PRs open and contributions welcome 🍻

## Installation and usage

- Run `npm i tailwind-reasonable-colors` to install the package.
- The package comes in two flavors: `enhance` and `override`.
  - `enhance` adds the reasonable colors palette to the existing palette without causing clashes. All added colors come prefixed with an `r`. So `pink` becomes `rpink` and can be used, for example, via `bg-rpink-400`.
  - `override` simply overwrites color names, but otherwise leaves the existing tailwind palette intact.
  - `enhanceFull` does the same thing `enhance` does, but adds missing variations for 50, 700, 800 and 900 in the palette. Generated via https://color-scheme-builder.vercel.app.
  - `overrideFull` does the same thing `override` does, but adds missing variations for 50, 700, 800 and 900 in the palette. Generated via https://color-scheme-builder.vercel.app.
   
## Examples

### Using enhance

#### Partial, original reasonable colors only

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
#### Full, with generated variations for (50, 700, 800 and 900)

```js
// tailwind.config.js
const reasonable = require('tailwind-reasonable-colors');

module.exports = {
  ...
  plugins: [
    reasonable.enhanceFull,
  ]
}
```

### Using override
#### Partial, original reasonable colors only

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

#### Full, with generated variations for (50, 700, 800 and 900)

```js
// tailwind.config.js
const reasonable = require('tailwind-reasonable-colors');

module.exports = {
  ...
  plugins: [
    reasonable.overrideFull,
  ]
}
```
## Credits

- https://reasonable.work/colors/ (also has an explanation on the reasoning behind the limited variations).