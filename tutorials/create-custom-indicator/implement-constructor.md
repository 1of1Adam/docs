---
title: "Implement constructor | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/tutorials/create-custom-indicator/constructor-implementation"
extracted_at: "2025-06-22T09:32:49.273Z"
---

# Implement constructor
> **Tip:** This article is part of a tutorial about creating a custom indicator.
We recommend that you follow the guide from the [start](https://www.tradingview.com/charting-library-docs/latest/tutorials/create-custom-indicator/).

`CustomIndicator` has the required `constructor` field that you will specify at this part of the tutorial.
To do this, assign an ES5 constructor function to `constructor`. The function should contain the `main` method that calculates indicator data.
To implement the method, follow the steps below.
For a thorough understanding of the constructor implementation, consider the [Constructor](https://www.tradingview.com/charting-library-docs/latest/custom_studies/custom-indicator-constructor) article.

## 1. Handle method arguments
The `main` method accepts the following parameters:

- [`ctx`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext) — context that stores an indicator state. It includes information about the current symbol, resolution, OHLC values of the current bar, and more.
- `inputs` — an array of the input parameters' values. Elements in the array are arranged in the same order as [`inputs`](https://www.tradingview.com/charting-library-docs/latest/tutorials/create-custom-indicator/metainfo-implementation#inputs) in `metainfo`.

Handle the method arguments as follows:

```
constructor: function () {
    this.main = function (ctx, inputs) {
        this._context = ctx;
        this._input = inputs;

        var length = this._input(0);
        var offset = this._input(2);
        var smoothingLine = this._input(3);
        var smoothingLength = this._input(4);
         // If this._input(1) returns 'close', PineJS.Std.close(this._context) will be called
        var source = PineJS.Std[this._input(1)](https://www.tradingview.com/charting-library-docs/latest/this._context);
    }
}

```
One of the indicator's [input parameters](https://www.tradingview.com/charting-library-docs/latest/tutorials/create-custom-indicator/metainfo-implementation#inputs) is *Source*. The parameter specifies certain bar values, such as close or open price, that will be used in the indicator calculations.
To get the required values, you should call the corresponding method from [`PineJSStd`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PineJSStd).
For example, if the close price is specified as source, call the [`close`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PineJSStd#close) method.
## 2. Call setMinimumAdditionalDepth
Calculating any Moving Averages requires extra historical bars. Usually the library can calculate the number of extra bars to request from datafeed.
However, in this tutorial, you implement a Smoothing Line which is a Moving Average calculated based on another Moving Average.
In this exceptional case, you should specify the number of extra bars manually by calling the `setMinimumAdditionalDepth` method.
Call `setMinimumAdditionalDepth` and pass the sum of the *Length* and *Smoothing Length* values as a parameter:

```
this._context.setMinimumAdditionalDepth(length + smoothingLength);

```
## 3. Call new_var
The library calls the `main` method for each bar of the [main series](https://www.tradingview.com/charting-library-docs/latest/getting_started/glossary#series).
To access values you get on the previous iterations, you should call the [`new_var`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext#new_var) method that creates a special variable.
In this tutorial, you need to store the main series to use it as the input to another calculation.
To do this, create the `series` variable as follows:
```
var series = this._context.new_var(source);

```
## 4. Calculate data
### For SMA
To calculate the SMA values, use the [`sma`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PineJSStd#sma) method.
The method returns a number — the SMA value for the current bar.
```
var sma = PineJS.Std.sma(series, length, this._context);

```
Additionally, you should store all SMA values to use them in the Smoothing Line calculations. To do this, create the `sma_series` variable with `new_var`:

```
var sma_series = this._context.new_var(sma);

```
### For Smoothing Line
The Smoothing Line is a Moving Average calculated based on the [SMA](#for-sma) data.
Depending on the type specified in the *Smoothing Line* input parameter, you should call either `sma`, [`ema`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PineJSStd#ema), or [`wma`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PineJSStd#wma) method to calculate the values:
```
var smoothedMA;
    if (smoothingLine === "EMA") {
    smoothedMA = PineJS.Std.ema(
        sma_series,
        smoothingLength,
        this._context
    );
    } else if (smoothingLine === "WMA") {
    smoothedMA = PineJS.Std.wma(
        sma_series,
        smoothingLength,
        this._context
    );
    } else {  // if (smoothingLine === "SMA") {
    smoothedMA = PineJS.Std.sma(
        sma_series,
        smoothingLength,
        this._context
    );
}

```
## 5. Return values
Return the calculated values for the SMA and Smoothing Line as follows:

```
return [
    { value: sma, offset: offset },
    { value: smoothedMA, offset: offset },
];

```
## Complete code
At this stage, you have implemented the constructor function and assigned it to the `constructor` field.

Expand to view the complete code for the constructor.

```
var widget = window.tvWidget = new TradingView.widget({
    // ...
    custom_indicators_getter: function(PineJS) {
        return Promise.resolve([
            // Indicator object
            {
                constructor: function () {
                    this.main = function (ctx, inputs) {
                        this._context = ctx;
                        this._input = inputs;

                        var length = this._input(0);
                        var offset = this._input(2);
                        var smoothingLine = this._input(3);
                        var smoothingLength = this._input(4);
                        var source = PineJS.Std[this._input(1)](https://www.tradingview.com/charting-library-docs/latest/this._context);

                        this._context.setMinimumAdditionalDepth(length + smoothingLength);

                        var series = this._context.new_var(source);
                        var sma = PineJS.Std.sma(series, length, this._context);
                        var sma_series = this._context.new_var(sma);

                        var smoothedMA;
                        if (smoothingLine === "EMA") {
                        smoothedMA = PineJS.Std.ema(
                            sma_series,
                            smoothingLength,
                            this._context
                        );
                        } else if (smoothingLine === "WMA") {
                        smoothedMA = PineJS.Std.wma(
                            sma_series,
                            smoothingLength,
                            this._context
                        );
                        } else {  // if (smoothingLine === "SMA") {
                        smoothedMA = PineJS.Std.sma(
                            sma_series,
                            smoothingLength,
                            this._context
                        );
                        }

                        return [
                            { value: sma, offset: offset },
                            { value: smoothedMA, offset: offset },
                        ];
                    };
                },
            }
        ]);
    },
});

```
## Tutorial results
This was the final step of the custom indicator implementation. You have created a custom indicator and specified its appearance and data.

Expand to view the complete code for the custom indicator.

```
var widget = window.tvWidget = new TradingView.widget({
    // ...
    custom_indicators_getter: function(PineJS) {
        return Promise.resolve([
            // Indicator object
            {
                name: 'Custom Moving Average',
                metainfo: {
                    _metainfoVersion: 53,
                    id: "Custom Moving Average@tv-basicstudies-1",
                    description: "Custom Moving Average",
                    shortDescription: "Custom MA",
                    format: { type: "inherit" },
                    linkedToSeries: true,
                    is_price_study: true,
                    plots: [
                        { id: "plot_0", type: "line" },
                        { id: "smoothedMA", type: "line" },
                    ],
                    defaults: {
                        styles: {
                            plot_0: {
                                linestyle: 0,
                                linewidth: 1,
                                plottype: 0,
                                trackPrice: false,
                                transparency: 0,
                                visible: true,
                                color: "#2196F3",
                            },
                            smoothedMA: {
                                linestyle: 0,
                                linewidth: 1,
                                plottype: 0,
                                trackPrice: false,
                                transparency: 0,
                                visible: true,
                                color: "#9621F3",
                            },
                        },
                        inputs: {
                            length: 9,
                            source: "close",
                            offset: 0,
                            smoothingLine: "SMA",
                            smoothingLength: 9,
                        },
                    },
                    styles: {
                        plot_0: { title: "Plot", histogramBase: 0, joinPoints: true },
                        smoothedMA: {
                            title: "Smoothed MA",
                            histogramBase: 0,
                            joinPoints: false,
                        },
                    },
                    inputs: [
                        {
                            id: "length",
                            name: "Length",
                            defval: 9,
                            type: "integer",
                            min: 1,
                            max: 10000,
                        },
                        {
                            id: "source",
                            name: "Source",
                            defval: "close",
                            type: "source",
                            options: [
                                "open",
                                "high",
                                "low",
                                "close",
                                "hl2",
                                "hlc3",
                                "ohlc4",
                            ],
                        },
                        {
                            id: "offset",
                            name: "Offset",
                            defval: 0,
                            type: "integer",
                            min: -10000,
                            max: 10000,
                        },
                        {
                            id: "smoothingLine",
                            name: "Smoothing Line",
                            defval: "SMA",
                            type: "text",
                            options: ["SMA", "EMA", "WMA"],
                        },
                        {
                            id: "smoothingLength",
                            name: "Smoothing Length",
                            defval: 9,
                            type: "integer",
                            min: 1,
                            max: 10000,
                        },
                    ],
                },
                constructor: function () {
                    this.main = function (ctx, inputs) {
                        this._context = ctx;
                        this._input = inputs;

                        var length = this._input(0);
                        var offset = this._input(2);
                        var smoothingLine = this._input(3);
                        var smoothingLength = this._input(4);
                        var source = PineJS.Std[this._input(1)](https://www.tradingview.com/charting-library-docs/latest/this._context);

                        this._context.setMinimumAdditionalDepth(length + smoothingLength);

                        var series = this._context.new_var(source);
                        var sma = PineJS.Std.sma(series, length, this._context);
                        var sma_series = this._context.new_var(sma);

                        var smoothedMA;
                        if (smoothingLine === "EMA") {
                        smoothedMA = PineJS.Std.ema(
                            sma_series,
                            smoothingLength,
                            this._context
                        );
                        } else if (smoothingLine === "WMA") {
                        smoothedMA = PineJS.Std.wma(
                            sma_series,
                            smoothingLength,
                            this._context
                        );
                        } else {  // if (smoothingLine === "SMA") {
                        smoothedMA = PineJS.Std.sma(
                            sma_series,
                            smoothingLength,
                            this._context
                        );
                        }

                        return [
                            { value: sma, offset: offset },
                            { value: smoothedMA, offset: offset },
                        ];
                    };
                },
            }
        ]);
    },
});

```
If you want to dive deeper into the custom indicators, we recommend checking out the following documentation sections:

- [Custom indicators](https://www.tradingview.com/charting-library-docs/latest/custom_studies/)
- [Custom indicators examples](https://www.tradingview.com/charting-library-docs/latest/custom_studies/Custom-Studies-Examples)