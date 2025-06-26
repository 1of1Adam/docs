---
title: "Inputs | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/custom_studies/metainfo/Custom-Studies-Inputs"
extracted_at: "2025-06-22T09:29:04.854Z"
---

# Inputs## Overview
When you create a [custom indicator](https://www.tradingview.com/charting-library-docs/latest/custom_studies/), you can make some indicator parameters variable and allow users to adjust them in the UI.
Such parameters are called **input parameters** or **inputs**. Users should provide values for the input parameters in the *Inputs* tab of the indicator settings dialog.
Then, these values will be used in the indicator [calculations](#handle-input-values-in-the-constructor).
For example, a custom indicator can accept a [source symbol](https://www.tradingview.com/charting-library-docs/latest/getting_started/glossary#source-symbol) and length as input parameters.

![Inputs tab](https://www.tradingview.com/charting-library-docs/assets/images/inputs-custom-indicator-3bea3a4208fb6aa48883cd1fd9e4549f.png)
To enable input parameters, you should take the following steps:

- [Define a list of input parameters](#define-a-list-of-input-parameters)
- [Specify default values](#specify-default-values)
- [Handle input values in the constructor](#handle-input-values-in-the-constructor)

## Define a list of input parameters
To define a list of input parameters, you should assign an array of objects to the [`inputs`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfo#inputs) property in [`StudyMetaInfo`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#studymetainfo).

```
custom_indicators_getter: function(PineJS) {
    return Promise.resolve([
        // Indicator object
        {
            // Define indicator metadata
            metainfo: {
                /* Other StudyMetaInfo properties */

                // Define input parameters
                inputs: [
                    /* A list of input objects */
                ]
            },
        }
    ]);
},

```

> **Tip:** `StudyMetaInfo` is an interface that you should implement to provide metadata for the custom indicator. For more information, refer to the [Metainfo](https://www.tradingview.com/charting-library-docs/latest/custom_studies/metainfo/) article.

Input parameters can be of multiple types, including numeric, text, time, and others.
Therefore, each object in `inputs` should implement a certain interface depending on the parameter type. The table below contains frequently used interfaces:

 **|Interface** | **Definition** ||
| [`StudyNumericInputInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyNumericInputInfo) | Designed for numeric parameters. ||
| [`StudyTextInputInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyTextInputInfo) | Designed for parameters represented with text. For example, types of a smoothing line: SMA, EMA, and WMA. ||
| [`StudySourceInputInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudySourceInputInfo) | Designed to specify values that are used to calculate the indicator. For example, open or close prices of the bars. ||
| [`StudySymbolInputInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudySymbolInputInfo) | Designed to specify a [source symbol](https://www.tradingview.com/charting-library-docs/latest/getting_started/glossary#source-symbol). ||

Refer to [`StudyInputInfo`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#studyinputinfo) for a complete list of interfaces.

Consider the following example. A custom indicator has two input parameters: length (a time period) and source (a type of bar values).
To specify these parameters, you should implement a [`StudyNumericInputInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyNumericInputInfo) and [`StudySourceInputInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudySourceInputInfo) objects, respectively.
Both interfaces have the following properties:

- `id` that is used to refer to the input parameter
- `name` that specifies the parameter name in the *Inputs* tab
- `type` that specifies the parameter data type
- `defval` that specifies the default parameter value

Other properties depend on the parameter type. The code sample below shows the implementation of the input parameters.

```
metainfo: {
    // ...
    inputs: [
        // StudyNumericInputInfo object
        {
            id: "length",
            name: "Length",
            defval: 9,       // 9 bars
            type: "integer",
            min: 1,
            max: 10000,
        },
        // StudySourceInputInfo object
        {
            id: "source",
            name: "Source",
            defval: "close", // Close price
            type: "source",
            options: [       // Options in the drop-down menu
                "open",
                "high",
                "low",
                "close",
                "hl2",
                "hlc3",
                "ohlc4",
            ],
        },
    ]
}

```
## Specify default values
[`StudyMetaInfo`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#studymetainfo) contains the [`defaults`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfo#defaults) property that stores default values for all indicator settings, including input parameters.
For each parameter defined in [`inputs`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfo#inputs), you should provide the corresponding value in `defaults`.

> **Warning:** Your custom indicator will not work unless you provide values in `defaults` for each input parameter.

To specify default values, assign a [`StudyInputsSimple`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyInputsSimple) object to the `inputs` property in [`StudyDefaults`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyDefaults).
`StudyInputsSimple` contains pairs of keys and values, where a key is a certain input parameter's `id`, and a value is the default value for this parameter.
In the [previous section](#define-a-list-of-input-parameters), you can see an example of the indicator with two input parameters: length and source. The code sample below demonstrates how to specify default input values for this indicator.

```
metainfo: {
    // ...
    inputs: [
        {
            id: "length", // This value is used as ID to refer to the input parameter
            // ...
        },
        {
            id: "source", // This value is used as ID to refer to the input parameter
            // ...
        },
    ]
    // StudyDefaults object
    defaults: {
        // ...
        inputs: {
            // ID : default value
            length: 9,
            source: "close",
        },
    }
}

```
## Handle input values in the constructor
To create a custom indicator, you should implement a [constructor](https://www.tradingview.com/charting-library-docs/latest/custom_studies/custom-indicator-constructor) that calculates indicator data.
In the constructor, you can retrieve input values and then use them in your data calculations.
To do this, use the `inputCallback` provided with [`main`](https://www.tradingview.com/charting-library-docs/latest/custom_studies/custom-indicator-constructor#main) and [`init`](https://www.tradingview.com/charting-library-docs/latest/custom_studies/custom-indicator-constructor#init) functions. The callback returns an array of input values arranged in the same order as in the [`inputs`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RawStudyMetaInfo#inputs) property.
In the [Define a list of input parameters](#define-a-list-of-input-parameters) section, you can see an example of the indicator with two input parameters: length and source. The code sample below demonstrates how to get input values for this indicator.

```
constructor: function () {
    this.main = function(ctx, inputCallback) {
        // ...
        this._input = inputCallback;
        var length = this._input(0);
        var source = this._input(1);
    };
}

```