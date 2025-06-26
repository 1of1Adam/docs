---
title: "API handlers for saving and loading | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/saving_loading/save-load-adapter"
extracted_at: "2025-06-22T09:15:27.754Z"
---

# API handlers for saving and loading## Overview
You can use the API handlers instead of the [predefined REST API](https://www.tradingview.com/charting-library-docs/latest/saving_loading/save-load-rest-api/) to store:

- [chart layouts](https://www.tradingview.com/charting-library-docs/latest/saving_loading/#chart-layouts)
- [chart templates](https://www.tradingview.com/charting-library-docs/latest/saving_loading/#chart-templates)
- [indicator templates](https://www.tradingview.com/charting-library-docs/latest/saving_loading/#indicator-templates)
- [drawing templates](https://www.tradingview.com/charting-library-docs/latest/saving_loading/#drawing-templates)

When users click the save or load buttons in the UI, these actions initiate the saving and loading processes.
API handlers allow implementing custom logic for save/load actions coming from UI.
For example, you can add authorization headers or manage specific errors.
Note that you need to have your own backend service to use API handlers.
## How to implement
Add the [`save_load_adapter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#save_load_adapter) property to the [Widget Constructor](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Widget-Constructor).
`save_load_adapter` is an [`​IExternalSaveLoadAdapter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IExternalSaveLoadAdapter) object that contains the save/load functions.
The library calls these functions when users click save/load UI elements.
## Examples
### localStorage
The TypeScript example below shows how to implement in-memory saving logic, so that the data is saved within the browser's [localStorage](https://developer.mozilla.org/en-US/docs/Web/API/Window/localStorage).

See the Pen 
Saving chart content to browser's localStorage using save_load_adapter by TradingView ([@tradingview](https://codepen.io/tradingview))
on [CodePen](https://codepen.io).
### In-memory
The JavaScript example below shows how to implement in-memory saving logic, so that the data is saved only within the memory of the current tab.
You can use this example for testing purposes or improve it by replacing the internals of these methods with calls to an external server.
See the Pen 
Saving templates to in-memory storage using save_load_adapter by TradingView ([@tradingview](https://codepen.io/tradingview))
on [CodePen](https://codepen.io).