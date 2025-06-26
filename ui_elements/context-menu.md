---
title: "Context menu | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/ui_elements/context-menu"
extracted_at: "2025-06-22T09:14:54.540Z"
---

# Context menuThe **context menu** is a dialog that users access through a right-mouse-click or ellipsis menu (…).

## Override context menu
You can override the default items in the context menu in two ways:

- [using Widget Constructor](#using-widget-constructor)
- [using API](#using-api)

> **Info:** Both approaches override all context menus.
If you only want to override specific menus, you should implement your own filtering logic for that particular use case.

### Using Widget Constructor
You can register a custom function for overriding default items when the context menu is created.
To do this, use the [`context_menu`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#context_menu) property of the [Widget Constructor](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Widget-Constructor).
`context_menu` has two properties:

[`items_processor`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ContextMenuOptions#items_processor) allows you to modify the items displayed in the context menu.
For example, you can provide a function that adds new items and removes or reorders existing ones.
The library calls this function each time users want to display the context menu.
This function should return an array of items to display.

[`renderer_factory`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ContextMenuOptions#renderer_factory) allows you to override the default renderer for the context menu so you can adjust existing menu items.

> **Tip:** You can also use the `context_menu` property to retrieve a list of items in the menu.
Check out the [Widget Constructor tutorial](https://www.youtube.com/watch?v=bdvmM3FNnSY&t=3715s) on YouTube for an implementation example.

#### Examples
The code sample below shows how to add a new item to the context menu using [`items_processor`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ContextMenuOptions#items_processor).

See the Pen 
UI. Add new button to context menu by TradingView ([@tradingview](https://codepen.io/tradingview))
on [CodePen](https://codepen.io).
The code sample below shows how to adjust existing items of the context menu using [`renderer_factory`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ContextMenuOptions#renderer_factory).

See the Pen 
UI. Adjust context menu items by TradingView ([@tradingview](https://codepen.io/tradingview))
on [CodePen](https://codepen.io).
#### Determine evoked menu
Both [`items_processor`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ContextMenuOptions#items_processor) and [`renderer_factory`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ContextMenuOptions#renderer_factory) provide menu names
and the associated IDs for items like series, drawings, indicators, orders, and positions.
You can determine which menu was triggered using the properties of the [`CreateContextMenuParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateContextMenuParams) interface.
### Using API
If you want to change the menu dynamically, use the [`onContextMenu`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#oncontextmenu) method.

```
widget.onChartReady(function() {
    widget.onContextMenu(function(unixtime, price) {
        return [{
            position: "top",
            text: "First top menu item, time: " + unixtime + ", price: " + price,
            click: function() { alert("First item clicked."); }
        },
        { text: "-", position: "top" }, // Adds a separator between buttons
        { text: "-Paste" },             // Removes the existing item from the menu
        {
            position: "top",
            text: "Second top menu item 2",
            click: function() { alert("Second item clicked."); }
        }, {
            position: "bottom",
            text: "Bottom menu item",
            click: function() { alert("Third item clicked."); }
        }];
    });
});

```