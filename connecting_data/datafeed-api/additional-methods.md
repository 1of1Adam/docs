---
title: "Additional methods | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/additional-methods"
extracted_at: "2025-06-22T09:28:28.954Z"
---

# Additional methodsThis article describes the additional methods in the [Datafeed API](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/).
With methods, you can enable additional features such as marks and a countdown to the bar close.
## getMarks
The library calls [`getMarks`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IDatafeedChartApi#getmarks) to request [marks](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Marks#marks-on-the-chart) for the visible bar range. The library assumes that you call [`GetMarksCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed#getmarkscallback) once per `getMarks` call. Pass an array of [`Mark`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.Mark) objects as a callback parameter.

Only ten marks can be attached to a bar. The time of each mark must match the time of a bar. For example, if the bar times are `2023-01-01`, `2023-01-08`, and `2023-01-15`, then a mark cannot have the time `2023-01-05`.

> **Warning:** This method is called only if your datafeed [supports marks](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.DatafeedConfiguration#supports_marks).

The code sample below demonstrates the example of `getMarks` implementation:

```
getMarks = (symbolInfo, startDate, endDate, onDataCallback, resolution) => {
    console.log('getMarks');

    onDataCallback(
        [
            {
                id: 1,
                time: endDate,
                color: 'red',
                text: ['This is the mark pop-up text.'],
                label: 'M',
                labelFontColor: 'blue',
                minSize: 25
            },
            {
                id: 2,
                time: endDate + 5260000, // 2 months
                color: 'red',
                text: ['Second marker'],
                label: 'S',
                labelFontColor: 'green',
                minSize: 25
            }
        ]);
};

```
## getTimescaleMarks
The library calls [`getTimescaleMarks`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IDatafeedChartApi#gettimescalemarks) to request [timescale marks](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Marks#marks-on-the-time-scale) for the visible bar range. The library assumes that you call [`GetMarksCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed#getmarkscallback) once per `getTimescaleMarks` call. Pass an array of [`TimescaleMark`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.TimescaleMark) objects as a callback parameter.

> **Warning:** These method is called only if your datafeed [supports marks](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.DatafeedConfiguration#supports_marks).

The code sample below demonstrates the example of `getTimescaleMarks` implementation:

```
getTimescaleMarks = (
    symbolInfo,
    startDate,
    endDate,
    onDataCallback,
    resolution
) => {
    // optional
    console.log('getTimescaleMarks');

    let marks = ;

    if (symbolInfo.name === 'AAPL') {
        marks = [
            {
                id: 1,
                time: startDate,
                color: 'red',
                label: 'Aa',
                minSize: 30,
                tooltip: [
                    'Lorem',
                    'Ipsum',
                    'Dolor',
                    'Sit',
                ]
            },
            {
                id: 2,
                time: startDate + 5260000, // 2 months
                color: 'blue',
                label: 'B',
                minSize: 30,
                tooltip: [
                    'Amet',
                    'Consectetur',
                    'Adipiscing',
                    'Elit',
                ]
            }
        ];
    } else {
        marks = [
            {
                id: 'String id',
                time: endDate,
                color: 'red',
                label: 'T',
                tooltip: ['Nulla']
            }
        ];
    }

    onDataCallback(marks);
};

```
## getServerTime
By default, the library gets the time from the user's machine. If the machine time is incorrect, the time used in the library is also incorrect.
To synchronize the library time with a server's time, enable the [`supports_time`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.DatafeedConfiguration#supports_time) property and implement the [`getServerTime`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IDatafeedChartApi#getservertime) method.
In the implementation, send a request to a time server and return the accurate value to the library using the [`ServerTimeCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed#servertimecallback).
The time value should be a Unix timestamp, for example, `1445324591`.
Note that the callback should be called only once.
The library allows you to display the countdown to the bar closing on the price scale.
If you use this feature, consider implementing `getServerTime` to make sure that the countdown is correct.

> **Info:** To display a countdown, set the [`mainSeriesProperties.showCountdown`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#mainseriespropertiesshowcountdown) property to `true`.
Note that the countdown can be displayed only for [intraday](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Resolution#resolution-in-minutes-intraday) resolutions.

## getVolumeProfileResolutionForPeriod
The library calls [`getVolumeProfileResolutionForPeriod`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IDatafeedChartApi#getvolumeprofileresolutionforperiod) to request the resolution that is used to calculate the *Volume Profile Visible Range* indicator. Implement this method if you want to calculate the indicator more accurately. The implementation depends on how much data you can transfer to the library and the depth of data in your datafeed.

If this method is not specified, the library uses `currentResolution`.