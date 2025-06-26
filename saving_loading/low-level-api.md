---
title: "Low-level API for saving and loading | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/saving_loading/low-level-api"
extracted_at: "2025-06-22T09:15:30.377Z"
---

# Low-level API for saving and loading## Overview
The low-level API is recommended when you want to use save/load UI elements that are not part of the TradingView UI.
With the low-level API, you can save and load [chart layouts](https://www.tradingview.com/charting-library-docs/latest/saving_loading/#chart-layouts) and [indicator templates](https://www.tradingview.com/charting-library-docs/latest/saving_loading/#indicator-templates).
Note that the low-level API methods are meant to be called directly by your JavaScript code.

> **Info:** This approach does not support saving [chart templates](https://www.tradingview.com/charting-library-docs/latest/saving_loading/#chart-templates).
Consider implementing the [API handlers](https://www.tradingview.com/charting-library-docs/latest/saving_loading/save-load-adapter) instead.

## How to implement
To access the chart layout content directly, use the [`save`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#save) and [`load`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#load) methods.
These methods are defined in the [`IChartingLibraryWidget`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget) interface and allow controlling the `widget` object.
```
// Function to store the chart layout
function storeChartLayout(layout) {
    // Implement your logic here
};

const widget = new TradingView.widget(/* Widget properties */);
widget.save((layout) => { storeChartLayout(layout) }); // Save the layout using the save() method

widget.load(storedLayout); // Later in your code, you can load the stored layout

```
To access the indicator templates, use the [`createStudyTemplate`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#createstudytemplate) and [`applyStudyTemplate`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#applystudytemplate) methods.
Note that you can access these methods through the [`chart`](https://www.tradingview.com/charting-library-docs/latest/core_concepts/widget-methods#chart) or [`activeChart`](https://www.tradingview.com/charting-library-docs/latest/core_concepts/widget-methods#activechart) widget methods.
```
widget.onChartReady(() => {
    const options = { saveSymbol: true, saveInterval: true };
    const template = widget.activeChart().createStudyTemplate(options);

    widget.activeChart().applyStudyTemplate(template);
});

```
The content is saved as a JSON object which you can save where you wish.
For example, you can embed it in your saved pages or in the user's working area.
## Hide save/load layout buttons
You can disable the [`header_saveload`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#header_saveload) featureset to hide the built-in *Save layout* and *Load layout* buttons from the header toolbar.