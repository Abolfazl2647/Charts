The Charting Library supports the display of [marks on bars](https://github.com/Abolfazl2647/Charts/blob/main/#marks-on-bars) and [on the timescale](https://github.com/Abolfazl2647/Charts/blob/main/#marks-on-the-timescale). Marks are requested from your back-end if it [supports them](https://github.com/Abolfazl2647/Charts/blob/main/JS-Api#supports_marks). Marks are designed to give you an ability to show events attached to bars/timescale. Here are a few examples:

- News
- Bar patterns
- Splits/Dividends
- .. etc.

You can subscribe to mark events using [subscribe(event, callback)](https://github.com/Abolfazl2647/Charts/blob/main/Widget-Methods#subscribeevent-callback) Widget Method. Also, there are Chart Methods to [refresh marks](https://github.com/Abolfazl2647/Charts/blob/main/Chart-Methods#refreshmarks) and [clear marks](https://github.com/Abolfazl2647/Charts/blob/main/Chart-Methods#clearmarks).

## Marks on bars

Marks on bars are colored circles with custom size and color with a letter inside. One bar can have a few marks. When user clicks on a mark, the tooltip appears. The tooltip can contain an HTML-code or a plain text.

Example:

![images/tv_bar_mark.png](https://github.com/Abolfazl2647/Charts/blob/main/images/tv_bar_mark.png)

Marks on bars are requested by the library for the visible data range using [getMarks() JS API method](https://github.com/Abolfazl2647/Charts/blob/main/JS-Api#getmarkssymbolinfo-from-to-ondatacallback-resolution) and [/marks UDF request](https://github.com/Abolfazl2647/Charts/blob/main/UDF#marks).

## Marks on the timescale

Marks on the timescale are basically lolipops above the timescale. Each mark has custom letter inside and the popup tooltip with one or two info strings.

Marks are requested from your back-end if it [supports them](https://github.com/Abolfazl2647/Charts/blob/main/JS-Api#supports_timescale_marks).

Example:

![images/tv_timescale_mark.png](https://github.com/Abolfazl2647/Charts/blob/main/images/tv_timescale_mark.png)

Marks on the timescale are requested by the library for the visible data range using [getTimescaleMarks() JS API method](https://github.com/Abolfazl2647/Charts/blob/main/JS-Api#gettimescalemarkssymbolinfo-from-to-ondatacallback-resolution) and [/timescale_marks UDF request](https://github.com/Abolfazl2647/Charts/blob/main/UDF#timescale-marks).
