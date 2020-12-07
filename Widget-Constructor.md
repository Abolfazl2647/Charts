You may specify Charting library widget parameters when calling its constructor. Here is an example of a call.

```javascript
new TradingView.widget({
  symbol: "A",
  interval: "1D",
  timezone: "America/New_York",
  container_id: "tv_chart_container",
  locale: "ru",
  datafeed: new Datafeeds.UDFCompatibleDatafeed(
    "https://demo_feed.tradingview.com"
  ),
});
```

Below is a complete list of supported parameters. Use [Widget methods](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Methods.md) if you wish to modify the parameters after the creation of the Charting Library.

`* - Required`

## Parameters

- Library and Trading Terminal
  - [symbol, interval\*](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#symbol-interval)
  - [container_id\*](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#container_id)
  - [datafeed\*](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#datafeed)
  - [timeframe](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#timeframe)
  - [timezone](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#timezone)
  - [debug](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#debug)
  - [library_path](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#library_path)
  - [width, height](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#width-height)
  - [fullscreen](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#fullscreen)
  - [autosize](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#autosize)
  - [symbol_search_request_delay](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#symbol_search_request_delay)
  - [auto_save_delay](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#auto_save_delay)
  - [toolbar_bg](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#toolbar_bg)
  - [study_count_limit](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#study_count_limit)
  - [studies_access](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#studies_access)
  - [drawings_access](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#drawings_access)
  - [saved_data](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#saved_data)
  - [locale](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#locale)
  - [numeric_formatting](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#numeric_formatting)
  - [custom_formatters](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#custom_formatters)
  - [overrides](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#overrides)
  - [disabled_features, enabled_features](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#disabled_features-enabled_features)
  - [snapshot_url](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#snapshot_url)
  - [custom_indicators_getter](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#custom_indicators_getter)
  - [preset](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#preset)
  - [studies_overrides](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#studies_overrides)
  - [time_frames](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#time_frames)
  - [charts_storage_url, client_id, user_id](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#charts_storage_url-client_id-user_id)
  - [charts_storage_api_version](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#charts_storage_api_version)
  - [load_last_chart](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#load_last_chart)
  - [theme](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#theme)
  - [custom_css_url](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#custom_css_url)
  - [loading_screen](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#loading_screen)
  - [favorites](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#favorites)
  - [save_load_adapter](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#save_load_adapter)
  - [settings_adapter](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#settings_adapter)
- Trading Terminal only
  - [widgetbar](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#widgetbar)
  - [rss_news_feed](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#rss_news_feed)
  - [news_provider](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#news_provider)
  - [broker_factory](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#broker_factory)
  - [broker_config](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#broker_config)

## Library and Trading Terminal

### symbol, interval\*

The default symbol & time interval of your chart. The `interval` value is described in the [Section](https://github.com/Abolfazl2647/Charts/blob/main/Resolution.md).

```javascript
symbol: 'A',
interval: '1D',
```

### container_id\*

`id` is an attribute of a DOM element inside which the iframe with the chart will be placed.

```javascript
container_id: "tv_chart_container",
```

### datafeed\*

JavaScript object that implements the ([JS API](https://github.com/Abolfazl2647/Charts/blob/main/JS-Api.md)) interface to supply the chart with data.

```javascript
datafeed: new Datafeeds.UDFCompatibleDatafeed(
  "https://demo_feed.tradingview.com"
);
```

### timeframe

Sets the default timeframe of the chart. Timeframe is a period of bars that will be loaded and shown on the screen.
Valid timeframe is a number with a letter D for days and M for months.

```javascript
timeframe: '3M',
```

### timezone

Default timezone of the chart. The time on the timescale is displayed according to this timezone.
See the [list of supported timezones](https://github.com/Abolfazl2647/Charts/blob/main/Symbology.md#timezone) for available values. Set it to `exchange` to use the exchange timezone. Use the [overrides](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Constructor.md#overrides) section if you wish to override the default value.

```javascript
timezone: "America/New_York",
```

### debug

Setting this property to `true` will make the chart write detailed API logs into the browser console. Alternatively, you can use the `charting_library_debug_mode` featureset to enable it.

```javascript
debug: true,
```

### library_path

A path to a `static` folder.

```javascript
library_path: "charting_library/",
```

### width, height

The desired size of a widget. Please make sure that there is enough space for the widget to be displayed correctly.

```javascript
width: 300,
height: 600,
```

**Remark**: If you want the chart to use all the available space use the `fullscreen` parameter instead of setting it to '100%'.

### fullscreen

_Default:_ `false`

Boolean value showing whether the chart should use all the available space in the window.

```javascript
fullscreen: true,
```

### autosize

_Default:_ `false`

Boolean value showing whether the chart should use all the available space in the container and resize when the container itself is resized.

```javascript
autosize: true,
```

### symbol_search_request_delay

A threshold delay in milliseconds that is used to reduce the number of symbol search requests when the user is typing a name of a symbol in the search box.

```javascript
symbol_search_request_delay: 1000,
```

### auto_save_delay

A threshold delay in seconds that is used to reduce the number of `onAutoSaveNeeded` calls.

```javascript
auto_save_delay: 5,
```

### toolbar_bg

Background color of the toolbars.

```javascript
toolbar_bg: '#f4f7f9',
```

### study_count_limit

_Starting from version 1.5._

Maximum amount of studies on the chart of a multichart layout. Minimum value is 2.

```javascript
study_count_limit: 5,
```

### studies_access

_Starting from version 1.1._

An object with the following structure:

```javascript
studies_access: {
    type: "black" | "white",
    tools: [
        {
            name: "<study name>",
            grayed: true
        },
        < ... >
    ]
}
```

- `type` is the list type. Supported values are: `black` (all listed items should be disabled), `white` (only the listed items should be enabled).
- `tools` is an array of objects. Each object could have the following properties:
  - `name` (_Mandatory_) is the name of a study. Use the same names as in the pop-ups of indicators.
  - `grayed` is a boolean showing whether this study should be visible but look as if it's disabled. If the study is grayed out and user clicks it, then the `onGrayedObjectClicked` function is called.

### drawings_access

_Starting from version 1.1._

This property has the same structure as the `studies_access`argument that is described above. Use the same names as you see in the UI.

```javascript
drawings_access: {
    type: 'black',
    tools: [
        {
            name: 'Trend Line',
            grayed: true
        },
    ]
},
```

**Remark**: There is a special case for font-based drawings. Use the "Font Icons" name for them. Those drawings cannot be enabled or disabled separately - the entire group will have to be either enabled or disabled.

### saved_data

JS object containing saved chart content. Use this parameter when creating the widget if you have a saved chart already. If you want to load the chart content when the chart is initialized then use [load() method](https://github.com/Abolfazl2647/Charts/blob/main/https://github.com/tradingview/charting_library/wiki/Widget-Methods.md#loadstate) of the widget.

### locale

Locale to be used by Charting Library. See [Localization](https://github.com/Abolfazl2647/Charts/blob/main/Localization.md) section for details.

```javascript
locale: 'en',
```

### numeric_formatting

The object containing formatting options for numbers. The only possible option is `decimal_sign` currently.

```javascript
numeric_formatting: { decimal_sign: "," },
```

### custom_formatters

It is an object that contains the following fields:

1. timeFormatter
1. dateFormatter

You can use these formatters to adjust the display format of the date and time values.
Both values are objects that include functions such as `format` and `formatLocal`:

```javascript
function format(date)
function formatLocal(date)
```

These functions should return the text that specifies date or time. `formatLocal` should convert date and time to local timezone.

Example:

```javascript
custom_formatters: {
  timeFormatter: {
    format: function(date) { var _format_str = '%h:%m'; return _format_str.replace('%h', date.getUTCHours(), 2). replace('%m', date.getUTCMinutes(), 2). replace('%s', date.getUTCSeconds(), 2); }
  },
  dateFormatter: {
    format: function(date) { return date.getUTCFullYear() + '/' + (date.getUTCMonth() + 1) + '/' + date.getUTCDate(); }
  }
}
```

### overrides

The object that contains new values for default widget properties.
You can override most of the Charting Library properties (which also may be edited by user through UI) using `overrides` parameter of Widget constructor. `overrides` is supposed to be an object. The keys of this object are the names of overridden properties. The values of these keys are the new values of the properties. Example:

```javascript
overrides: {
    "mainSeriesProperties.style": 0
}
```

This code will make the watermark 100% opaque (invisible). All customizable properties are listed in [separate article](https://github.com/Abolfazl2647/Charts/blob/main/Overrides.md). You can use [Drawings-Overrides](https://github.com/Abolfazl2647/Charts/blob/main/Drawings-Overrides.md) starting from v 1.5.

### disabled_features, enabled_features

The array containing names of features that should be enabled/disabled by default. `Feature` means part of the functionality of the chart (part of the UI/UX). Supported features are listed [here](https://github.com/Abolfazl2647/Charts/blob/main/Featuresets.md).

Example:

```javascript
disabled_features: ["header_widget", "left_toolbar"],
enabled_features: ["move_logo_to_main_pane"],
```

### snapshot_url

This URL is used to send a POST request with base64-encoded chart snapshots when a user presses the snapshot button. This endpoint should return the full URL of the saved image in the the response.

```javascript
snapshot_url: "https://myserver.com/snapshot",
```

### custom_indicators_getter

Function that returns a Promise object with an array of your custom indicators.

`PineJS` variable will be passed as the first argument of this function and can be used inside your indicators to access internal helper functions.

See more details [here](https://github.com/Abolfazl2647/Charts/blob/main/Creating-Custom-Studies.md).

```javascript
custom_indicators_getter: function(PineJS) {
    return Promise.resolve([
        // *** your indicator object, created from the template ***
    ]);
},
```

### preset

`preset` is a name of predefined widget settings. For now, the only value supported in the `preset` is `mobile`. The example of this `preset` is [available here](https://charting-library.tradingview.com).

```javascript
preset: "mobile",
```

### studies_overrides

Use this option to customize the style or inputs of the indicators. You can also customize the styles and inputs of the `Compare` series using this argument. See more details [here](https://github.com/Abolfazl2647/Charts/blob/main/Studies-Overrides.md)

```javascript
studies_overrides: {
    "volume.volume.color.0": "#00FFFF",
},
```

### time_frames

List of visible timeframes that can be selected at the bottom of the chart.

Example:

```javascript
time_frames: [
  { text: "50y", resolution: "6M", description: "50 Years" },
  { text: "3y", resolution: "W", description: "3 Years", title: "3yr" },
  { text: "8m", resolution: "D", description: "8 Month" },
  { text: "3d", resolution: "5", description: "3 Days" },
  { text: "1000y", resolution: "W", description: "All", title: "All" },
];
```

Timeframe is an object containing the `text` and `resolution` properties. The `text` property should have the following format: `<integer><y|m|d>` ( \d+(y|m|d) as Regex ). Resolution is a string and its format is described here - [here](https://github.com/Abolfazl2647/Charts/blob/main/Resolution.md). See [this topic](https://github.com/Abolfazl2647/Charts/blob/main/Time-Frames.md) to learn more about timeframes.

The `description` property was added in v 1.7 and is displayed in the pop-up menu. This parameter is optional. If it isn't specified then the `title` or `text` property is used as a description.

The `title` property was added in v 1.9 and its value will override the default title generated based on the `text` property. This parameter is optional.

### charts_storage_url, client_id, user_id

These arguments are related to the high-level API for saving/loading the charts. See more details [here](https://github.com/Abolfazl2647/Charts/blob/main/Saving-and-Loading-Charts.md).

```javascript
charts_storage_url: 'http://storage.yourserver.com',
client_id: 'yourserver.com',
user_id: 'public_user_id',
```

### charts_storage_api_version

A version of your backend. Supported values are: `"1.0"` | `"1.1"`. Study Templates are supported starting from version `"1.1"`.

```javascript
charts_storage_api_version: "1.1",
```

### load_last_chart

Set this parameter to `true` if you want the library to load the last saved chart for a user (you should implement [save/load](https://github.com/Abolfazl2647/Charts/blob/main/Saving-and-Loading-Charts.md) first to make it work).

```javascript
load_last_chart: true,
```

### theme

_Starting from version 1.13._

Adds custom theme color for the chart. Supported values are: `"Light"` | `"Dark"`.

```javascript
theme: "Light",
```

### custom_css_url

_Starting from version 1.4._

Adds your custom CSS to the chart. `url` should be an absolute or relative path to the `static` folder.

```javascript
custom_css_url: 'css/style.css',
```

### loading_screen

_Starting from version 1.12._

Customization of the loading spinner. Value is an object with the following possible keys:

- `backgroundColor`
- `foregroundColor`

Example:

```javascript
loading_screen: {
  backgroundColor: "#000000";
}
```

### favorites

Items that should be marked as favorite by default. This option requires that the usage of localstorage is disabled (see [featuresets](https://github.com/Abolfazl2647/Charts/blob/main/Featuresets.md) to know more). The `favorites` property is supposed to be an object. The following properties are supported:

- **intervals**: an array of time intervals that are marked as favorite. Example: `["D", "2D"]`
- **chartTypes**: an array of chart types that are marked as favorite. The names of chart types are identical to chart's UI in the English version. Example: `["Area", "Candles"]`.

```javascript
favorites: {
    intervals: ["1D", "3D", "3W", "W", "M"],
    chartTypes: ["Area", "Line"]
},
```

### save_load_adapter

An object containing the save/load functions. It is used to customize the `Save` button behaviour. Please see details and example on [Saving and Loading Charts page](https://github.com/Abolfazl2647/Charts/blob/main/Saving-and-Loading-Charts.md#save_load_adapter).

### settings_adapter

_Starting from version 1.11._

An object that contains set/remove functions. Use it to save chart settings to your preferred storage (including server-side). If it is available then it should have the following methods:

1. `initialSettings: Object`

   An object with the initial settings

1. `setValue(key: string, value: string): void`

   A function that is called to store key/value pair.

1. `removeValue(key: string): void`

   A function that is called to remove a key.

```javascript
settings_adapter: {
    initialSettings: { ... },
    setValue: function(key, value) { ... },
    removeValue: function(key) { ... },
}
```

## Trading Terminal only

### widgetbar

:chart: _applies to [Trading Terminal](https://github.com/Abolfazl2647/Charts/blob/main/Trading-Terminal.md) only_

The object that contains settings for the widget panel on the right side of the chart. Watchlist, news and details widgets on the right side of the chart can be enabled using the `widgetbar` field in Widget constructor:

```javascript
widgetbar: {
    details: true,
    watchlist: true,
    watchlist_settings: {
        default_symbols: ["NYSE:AA", "NYSE:AAL", "NASDAQ:AAPL"],
        readonly: false
    }
}
```

- `details` (_default:_ `false`): Enables details widget in the widget panel on the right.
- `watchlist` (_default:_ `false`): Enables watchlist widget in the widget panel on the right.
- `watchlist_settings.default_symbols` (_default:_ `[]`): Sets the list of default symbols for watchlist.
- `watchlist_settings.readonly` (_default:_ `false`): Enables read-only mode for the watchlist.

### rss_news_feed

:chart: _applies to [Trading Terminal](https://github.com/Abolfazl2647/Charts/blob/main/Trading-Terminal.md) only_

Use this property to change the RSS feed for news. You can set a different RSS for each symbol type or use a single RSS for all symbols. The object should have the `default` property, other properties are optional. The names of the properties match the symbol types. Each property is an object (or an array of objects) with the following properties:

1. `url` - is a URL to be requested. It can contain tags in curly brackets that will be replaced by the terminal: `{SYMBOL}`, `{TYPE}`, `{EXCHANGE}`.
1. `name` - is a name of the feed to be displayed underneath the news.

Here is an example:

```javascript
rss_news_feed: {
    default: [ {
        url: "https://articlefeeds.nasdaq.com/nasdaq/symbols?symbol={SYMBOL}",
        name: "NASDAQ"
      }, {
        url: "http://feeds.finance.yahoo.com/rss/2.0/headline?s={SYMBOL}&region=US&lang=en-US",
        name: "Yahoo Finance"
      } ]
},
```

Another example:

```javascript
rss_news_feed: {
    "default": {
        url: "https://articlefeeds.nasdaq.com/nasdaq/symbols?symbol={SYMBOL}",
        name: "NASDAQ"
    }
}
```

One more example:

```javascript
rss_news_feed: {
    "default": {
        url: "https://articlefeeds.nasdaq.com/nasdaq/symbols?symbol={SYMBOL}",
        name: "NASDAQ"
     },
    "stock": {
        url: "http://feeds.finance.yahoo.com/rss/2.0/headline?s={SYMBOL}&region=US&lang=en-US",
        name: "Yahoo Finance"
    }
}
```

### news_provider

:chart: _applies to [Trading Terminal](https://github.com/Abolfazl2647/Charts/blob/main/Trading-Terminal.md) only_

An object that specifies the news provider. It may contain the following properties:

1. `is_news_generic` - if set to `true` then the title of the news widget will not include a symbol name (`Headlines` will be included only). Otherwise `for SYMBOL_NAME` will be added.
1. `get_news` - use this property to set your own news getter function. Both the `symbol` and `callback` will be passed to the function.

   The callback function should be called with an array of news objects that have the following structure:

   - `title` (required) - the title of news item.
   - `published` (required) - the time of news item in ms (UTC).
   - `source` (optional) - source of the news item title.
   - `shortDescription` (optional) - Short description of a news item that will be displayed under the title.
   - `link` (optional) - URL to the news story.
   - `fullDescription` (optional) - full description (body) of a news item.

   **NOTE:** When a user clicks on a news item a new tab with the `link` URL will be opened. If `link` is not specified then a pop-up dialog with `fullDescription` will be shown.

   **NOTE 2:** If both `news_provider` and `rss_news_feed` are available then the `rss_news_feed` will be ignored.

Example:

```javascript
news_provider: {
    is_news_generic: true,
    get_news: function(symbol, callback) {
        callback([
            {
                title: 'News for symbol ' + symbol,
                shortDescription: 'Short description of the news item',
                fullDescription: 'Full description of the news item',
                published: new Date().valueOf(),
                source: 'My own source of news',
                link: 'https://www.tradingview.com/'
            },
            {
                title: 'Another news for symbol ' + symbol,
                shortDescription: 'Short description of the news item',
                fullDescription: 'Full description of the news item. Long text here.',
                published: new Date().valueOf(),
                source: 'My own source of news',
            }
        ]);
    }
}
```

### broker_factory

:chart: _applies to [Trading Terminal](https://github.com/Abolfazl2647/Charts/blob/main/Trading-Terminal.md) only_

Use this field to pass the function that returns a new object which implements [Broker API](https://github.com/Abolfazl2647/Charts/blob/main/Broker-API.md). This is a function that accepts [Trading Host](https://github.com/Abolfazl2647/Charts/blob/main/Trading-Host.md) and returns [Broker API](https://github.com/Abolfazl2647/Charts/blob/main/Broker-API.md).

```javascript
broker_factory: function(host) { ... }
```

### broker_config

:chart: _applies to [Trading Terminal](https://github.com/Abolfazl2647/Charts/blob/main/Trading-Terminal.md) only_

Use this field to set the configuration flags for the Trading Terminal. [Read more](https://github.com/Abolfazl2647/Charts/blob/main/Trading-Objects-and-Constants.md#configflags-object).

```javascript
broker_config: {
    supportReversePosition: true,
    supportPLUpdate: true,
    ...
},
```

## See Also

- [Widget Methods](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Methods.md)
- [Featuresets](https://github.com/Abolfazl2647/Charts/blob/main/Featuresets.md)
- [Saving and Loading Charts](https://github.com/Abolfazl2647/Charts/blob/main/Saving-and-Loading-Charts.md)
- [Overriding Default Properties of the Studies](https://github.com/Abolfazl2647/Charts/blob/main/Studies-Overrides.md)
- [Overriding Default Properties of the Chart](https://github.com/Abolfazl2647/Charts/blob/main/Overrides.md)
