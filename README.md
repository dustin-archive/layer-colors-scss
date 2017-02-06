# layer-colors-scss

> layer transparent colors

## Installation

```sh
$ npm install --save layer-colors-scss
```

## Usage

#### `layer-colors($above, $below)`

Outputs a color from two colors as if they were layered in Photoshop or a browser.

The resulting color is not an average.

```scss
layer-colors(rgba(dodgerblue, 0.25), rgba(orange, 0.75))
// => rgba(143, 155, 128, 0.8125)
```

For comparison here is the result of `mix()`

```scss
mix(rgba(dodgerblue, 0.25), rgba(orange, 0.75))
// => rgba(199, 160, 64, 0.5)
```
