# color-composite-scss

> compose multiple colors with alpha channels into one

## Installation

```sh
$ npm install --save color-composite-scss
```

## Usage

### `composite($top ... $bottom)`

Compose multiple colors with alpha channels into one.

The resulting color is not an average.

```scss
composite(rgba(127, 195, 255, 0.5) rgba(195, 127, 255, 0.75))
// => rgba(156, 166, 255, 0.875)
```

For comparison here is the result of `mix()`

```scss
mix(rgba(127, 195, 255, 0.5), rgba(195, 127, 255, 0.75))
// => rgba(170, 153, 255, 0.625)
```

### `composite-over($top, $bottom)`

Composites `$top` over `$bottom`. This is a bare implementation of composite.

```scss
composite-over(rgba(127, 195, 255, 0.5), rgba(195, 127, 255, 0.75))
// => rgba(156, 166, 255, 0.875)
```

### `composite-merge($a, $b, $a-alpha, $b-alpha, $alpha)`

Composites two parallel channel values together with their associated color's alpha.

This function is used internally.

```scss
composite-merge(127, 195, 0.5, 0.75, 0.875)
// => rgba(156, 166, 255, 0.875)
```

## Related

* [color-composite](https://github.com/colorjs/color-composite) — compose multiple colors with alpha channels into one
