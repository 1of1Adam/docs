---
title: "Constructor | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/custom_studies/custom-indicator-constructor"
extracted_at: "2025-06-22T09:15:41.925Z"
---

# Constructor## Overview
`constructor` is a required field in the [`CustomIndicator`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CustomIndicator) object that you should specify to create a [custom indicator](https://www.tradingview.com/charting-library-docs/latest/custom_studies/).

```
custom_indicators_getter: function(PineJS) {
    return Promise.resolve([
        {
            // Indicator object
            // ...
            constructor: {
                // ...
            },
        }
    ]);
},

```
The field should contain an ES5 constructor function. The library applies the `new` operator to the constructor to create an instance of the custom indicator.

The constructor contains the [`main`](#main) and [`init`](#init) methods that accept the following arguments:

- [`ctx`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext) — context that stores an indicator state. It includes information about the current symbol, resolution, OHLC values of the current bar, and more.
- `inputs` — an array of input values. Elements in the array are arranged in the same order as [inputs](https://www.tradingview.com/charting-library-docs/latest/custom_studies/metainfo/#inputs) in the `metainfo`.

You should implement either both methods or only `main` to calculate indicator data. In your implementation, use mathematical, logical, and technical analysis functions provided in the [`PineJSStd`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PineJSStd) interface.

## init
The [`init`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LibraryPineStudy#init) method is **optional**.
It is designed to get additional information for an indicator and allows you to initialize variables needed for your data calculations. For example, you can reset a counter with this method.
The library calls `init` when the indicator should be calculated from scratch. This can occur when:

- The indicator is added to the chart.
- The indicator is added to a new pane.
- The symbol is changed.
- The resolution is changed.
- Additional historical data is loaded.

Consider the following example.
You want to display an indicator that compares values between the current symbol and a different one.
In this case, the indicator requires data for another symbol.
The code sample below shows how to request data for an additional symbol using the [`new_sym`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext#new_sym) method. In this case, requesting data should be done once, therefore, it is implemented within `init`.
```
this.init = function(context, inputCallback) {
    var symbol = "AAPL";
    var period = PineJS.Std.period(this._context);
    context.new_sym(symbol, period);
};

```
## main
The [`main`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LibraryPineStudy#main) method is **required** and should contain the main [data calculations](#data-calculations).
The library calls this method for each bar of the [main series](https://www.tradingview.com/charting-library-docs/latest/getting_started/glossary#series).

> **Info:** If there is more than one series, the library calls `main` for each bar of an additional series first, and then for each bar of the main series.

### Data calculations
As mentioned above, the library calls `main` for each bar of the [main series](https://www.tradingview.com/charting-library-docs/latest/getting_started/glossary#series).
On each iteration, you can get information about previous bars only. Therefore, when you calculate the tenth bar, you can access values of the bars in the [1..9] range.
The library does not provide future bars, and you should not use them in your calculations to avoid unexpected results.
To store data for intermediate calculations, you should create variables using API methods such as [`new_var`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext#new_var) and [`new_unlimited_var`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext#new_unlimited_var).
Consider the [Requesting Data for Another Ticker](https://www.tradingview.com/charting-library-docs/latest/custom_studies/Custom-Studies-Examples#requesting-data-for-another-ticker) example where the timestamp of the current bar is stored using `new_var`.
### Output values
As a result, the method should return an indicator value that corresponds to the current bar. An indicator is represented with [plots](https://www.tradingview.com/charting-library-docs/latest/custom_studies/metainfo/#plots) specified in `metainfo`. Therefore, you should provide a value for each plot.
If there is only one plot, `main` should return a number, for example `10`, or an array with one element — `[10]`.
Otherwise, the result is an array where elements are arranged in the same order as plots in `metainfo`.
Consider the [OHLC Plots](https://www.tradingview.com/charting-library-docs/latest/custom_studies/Custom-Studies-OHLC-Plots) example where four plots get the corresponding open, high, low, and close values.
Values in the array can be one of the following types:

- Numbers, for example, `[10, 20]`.
- Objects with the `{ offset: number, value: number, }` structure that allow you to display a value several bars forward or backward from the current bar. For example, `[{ value: 10, offset: 5, }, { value: 20, offset: 10, }]`.

## Example
The code sample below demonstrates the `constructor` implementation for a simple indicator that plots the close value.

```
constructor: function () {
    this.main = function (context, inputCallback) {
        this._context = context;
        this._input = inputCallback;
        var symbolClose = PineJS.Std.close(this._context);
        return [symbolClose];
    };
},

```