## Price Scale API

### getMode()

Returns current [mode](https://github.com/Abolfazl2647/Charts/blob/main/Price-Scale-Api.md#pricescalemode) of the price scale.

### setMode(newMode)

1. `newMode` - new [mode](https://github.com/Abolfazl2647/Charts/blob/main/Price-Scale-Api.md#pricescalemode) for the price scale

Changes current mode of the price scale.

### isInverted()

_Since version 1.15._

Returns whether the price scale is inverted or not.

### setInverted(isInverted)

_Since version 1.15._

1. `isInverted` - new inverted state for the price scale

Changes current inverted state of the price scale.

### getVisiblePriceRange()

_Starting from version 1.15._

Returns current visible price range of the price scale. The result is an object with `from` and `to`, which are the boundaries of the price scale visible range.

### setVisiblePriceRange(range)

_Starting from version 1.15._

Sets current visible price range of the price scale, `range` is an object with `from` and `to`, which are the boundaries of the price scale visible range.

### getStudies()

_Starting from version 1.16._

Returns an array of IDs of all studies attached to the price scale.

### hasMainSeries()

_Starting from version 1.16._

Returns `true` if the price scale contains the main series.

## Primitive Types

### PriceScaleMode

Available modes price scale can operate in:

- `0` - normal mode of the price scale
- `1` - logarithmic mode of the price scale
- `2` - percentage mode of the price scale
- `3` - indexed to 100 mode of the price scale
