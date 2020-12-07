## Default instrument and resolution

Change the default symbol (instrument) and resolution (time interval).

Minimum supported resolution is 1 second.

[symbol, interval](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#symbol-interval)

## Default visible range (timeframe)

Change time range of bars for the default resolution

[timeframe](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#timeframe)

## Default visible range for resolutions

Change time range of bars when the resolution is changed by the user. A sample is available here:

[onIntervalChanged()](https://github.com/Abolfazl2647/Charts/blob/main/Chart-Methods.md#onintervalchanged)

## Initial timezone

You can set the default timezone. It can be changed by the user in the menu.

[timezone](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#timezone)

## Chart colors

Customize the colors of the chart so that it matches your site design.

1. [Toolbar color](https://github.com/Abolfazl2647/Charts/blob/main/Toolbars)
1. Chart color at the start - [overrides](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#overrides), on the fly - [Chart Style properties](https://github.com/Abolfazl2647/Charts/blob/main/Chart-Style-Properties.md)
1. [CSS Color Themes](https://github.com/Abolfazl2647/Charts/blob/main/CSS-Color-Themes.md)

## Default properties of a chart

You can change any available properties in the properties dialog.

1. [Initially](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#overrides)
1. [On the fly](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Methods.md#applyoverridesoverrides)

## Show/hide chart elements

Certain chart elements (toolbars, buttons, other controls) can be hidden if you don't need them.

1. Most of the chart elements can be shown/hidden by using [Featuresets](https://github.com/Abolfazl2647/Charts/blob/main/Featuresets)
1. You can add [your own CSS](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#custom_css_url)

## Initial list of favorite intervals / chart styles

You can select the intervals and chart styles that will be shown in the top toolbar by default. A user can change it if `items_favoriting` is enabled in the [Featuresets](https://github.com/Abolfazl2647/Charts/blob/main/Featuresets).

[favorites](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#favorites)

## Resolutions that are displayed in the menu

1. The complete [list of resolutions](https://github.com/Abolfazl2647/Charts/blob/main/JS-Api#supported_resolutions) is provided in the configuration of the datafeed
1. Resolutions are enabled or disabled in the list being based on the [symbol information](https://github.com/Abolfazl2647/Charts/blob/main/Symbology.md#supported_resolutions)
1. Initial list of favorite resolutions [can be adjusted](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#favorites)

## Context menu

You can add new elements to the context menu or hide the existing items.

[onContextMenu(callback)](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Methods.md#oncontextmenucallback)
