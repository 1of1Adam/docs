---
title: "Interface: ContextMenuOptions | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ContextMenuOptions"
extracted_at: "2025-06-22T09:34:41.944Z"
---

- [](/charting-library-docs/)- Interfaces- ContextMenuOptionsOn this page# Interface: ContextMenuOptions[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).ContextMenuOptions

Use this interface to override the [context menu](https://www.tradingview.com/charting-library-docs/latest/ui_elements/context-menu).

## Properties[​](#properties)
### items_processor[​](#items_processor)
• `Optional` items_processor: [`ContextMenuItemsProcessor`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#contextmenuitemsprocessor)

Provide this function if you want to change the set of actions being displayed in the context menu.

You can filter out, add yours and re-order items.

The library will call your function each time it wants to display a context menu and will provide a list of items to display.
This function should return an array of items to display.
Example:

```
context_menu: {  items_processor: function(items, actionsFactory, params) {     console.log(`Menu name is: ${params.menuName}`);     const newItem = actionsFactory.createAction({        actionId: 'hello-world',        label: 'Say Hello',        onExecute: function() {           alert('Hello World');        },     });     items.unshift(newItem);     return Promise.resolve(items);  },},
```

### renderer_factory[​](#renderer_factory)
• `Optional` renderer_factory: [`ContextMenuRendererFactory`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#contextmenurendererfactory)

Provide this function to override the default renderer for context menu so you can adjust existing menu items.

- [Properties](#properties)[items_processor](#items_processor)- [renderer_factory](#renderer_factory)