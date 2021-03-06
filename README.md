# babel-plugin-react-primitives-svg
[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2FHermanya%2Fbabel-plugin-react-primitives-svg.svg?type=shield)](https://app.fossa.io/projects/git%2Bgithub.com%2FHermanya%2Fbabel-plugin-react-primitives-svg?ref=badge_shield)


A babel plugin that transforms SVG imports into
 [react-primitives-svg](https://github.com/chengyin/react-primitives-svg)-compatible [primitives](https://github.com/lelandrichardson/react-primitives).

🚨 This is super BETA 🚨

This is my first dip into the babel plugin pool, so any help testing or developing would be *greatly* appreciated.

## Usage

### Via `.babelrc` (Recommended)

**.babelrc**

```json
{
  "plugins": [
    "babel-plugin-react-primitives-svg"
  ]
}
```

#### Options
- *`verbose`* - Log level (`boolean`, default: `false`)
- *`defaultWidth`* - Default pixel width for SVG (`string` or `number`, default: `100%`)
- *`defaultHeight`* - Default pixel height for SVG (`string` or `number`, default: `100%`)
- ...inherited options from [babel-plugin-react-sketchapp-svg](https://github.com/alampros/babel-plugin-react-sketchapp-svg#options)

Example:

```json
{
  "plugins": [
    [
      "babel-plugin-react-primitives-svg",
      {
        "defaultWidth": 32,
        "defaultHeight": 32,
        "svgo": {
          "plugins": [
            {
              "removeAttrs": { "attrs": "(data-name)" }
            },
            {
              "cleanupIDs": true
            }
          ]
        }
      }
    ]
  ]
}

```


## License
[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2FHermanya%2Fbabel-plugin-react-primitives-svg.svg?type=large)](https://app.fossa.io/projects/git%2Bgithub.com%2FHermanya%2Fbabel-plugin-react-primitives-svg?ref=badge_large)