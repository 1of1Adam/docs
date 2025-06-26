---
title: "How to create a custom indicator | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/tutorials/create-custom-indicator/"
extracted_at: "2025-06-22T09:16:28.533Z"
---

# How to create a custom indicatorIn this tutorial we will create a [custom indicator](https://www.tradingview.com/charting-library-docs/latest/custom_studies/) that displays a [Simple Moving Average (SMA)](https://www.tradingview.com/support/solutions/43000696841-simple-moving-average/) and a Smoothing Line.
The line represents either SMA, [Exponential Moving Average (EMA)](https://www.tradingview.com/support/solutions/43000592270-exponential-moving-average/), or [Weighted Moving Average (WMA)](https://www.tradingview.com/support/solutions/43000594680-weighted-moving-average/) calculated based on the existing SMA.
See the Pen 
Chart customization order by TradingView ([@tradingview](https://codepen.io/tradingview))
on [CodePen](https://codepen.io).
After completing the tutorial, you will learn how to add a custom indicator to the library, specify the indicator look and feel, and implement data calculations.

## Before you start
Consider taking the following steps before proceeding with the tutorial:

- Set up the [Widget Constructor](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Widget-Constructor) and run the library. Refer to the [First run](https://www.tradingview.com/charting-library-docs/latest/tutorials/First-Run-Tutorial) tutorial for more information.
- Connect data to the library. Refer to the [Connecting data](https://www.tradingview.com/charting-library-docs/latest/tutorials/implement_datafeed_tutorial/) tutorial for more information.

## Tutorial structure
The tutorial is divided into three parts:

- [Add a custom indicator to the library](#add-a-custom-indicator-to-the-library)
- [Implement metainfo](https://www.tradingview.com/charting-library-docs/latest/tutorials/create-custom-indicator/metainfo-implementation)
- [Implement constructor](https://www.tradingview.com/charting-library-docs/latest/tutorials/create-custom-indicator/constructor-implementation)

> **Tip:** 
- At the end of each part, you will find the complete code blocks related to a specific step.
- Refer to the CodePen example above to see the complete tutorial code right away.

## Add a custom indicator to the library
To add a custom indicator to the library, specify a function that returns a Promise object and assign this function to the [`custom_indicators_getter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#custom_indicators_getter) property in the [Widget Constructor](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Widget-Constructor).
The Promise object should be resolved with an array of [`CustomIndicator`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CustomIndicator) instances.
In this tutorial, only one custom indicator will be created, therefore, the array contains one element.
`CustomIndicator` is an interface that you should implement to provide information on the indicator. The interface contains the following required fields:

- `name`: an indicator's internal name that is not visible in the UI. This name should be unique.
- `metainfo`: the field that describes how the indicator looks like.
- `constructor`: the field that contains data calculations.

At this stage of the tutorial, you should adjust the `name` filed only.

```
var widget = window.tvWidget = new TradingView.widget({
    // ...
    custom_indicators_getter: function(PineJS) {
        return Promise.resolve([
            // Indicator object
            {
                name: 'Custom Moving Average',
                metainfo: {
                    // ...
                },
                constructor: function() {
                    // ...
                }
            }
        ]);
    },
});

```
In the next steps, you will specify the `metainfo` and `constructor` fields.