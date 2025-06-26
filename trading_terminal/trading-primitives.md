---
title: "Trading Primitives | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/trading_terminal/Trading-Primitives"
extracted_at: "2025-06-22T09:16:12.409Z"
---

# Trading PrimitivesTrading Primitives is a low-level mechanism that is designed to give you the most detailed control over trading primitives behavior.

## Generic data
### Properties
You can use special value `inherit` for some properties of the Trading Primitives. This will make the Library use its default value for this property.

You can enable the `trading_options` feature to show Trading GUI controls in the chart properties window.

You can’t control the visibility of a specific object. Properties of positions, orders and executions can be changed in the Trading tab of the Chart Properties window.

### Override properties
You can override the style of the order and position lines.
For more information refer to [Customize trading primitives](https://www.tradingview.com/charting-library-docs/latest/customization/overrides/trading-overrides#created-with-trading-primitives).
### Colors and Fonts
You can use following string formats for setting the colors:

- `#RGB`
- `#RRGGBB`
- `rgb(red, green, blue)`
- `rgba(red, green, blue, alpha)`

You can use the following string format for setting the fonts: `<bold> <italic> <size>pt <family>`.

### Line Styles
The following line styles are supported:

 **|Style** | **Value** ||
| Solid | 0 ||
| Dotted | 1 ||
| Dashed | 2 ||

### Callbacks

- You can use `this` keyword to access an API-object from within the callback function
- You can pass two arguments to callback registration function - in this case first argument is an object which will be passed as first argument to callback function.
- If callback isn’t set, then respective button will be hidden (affects `onReverse`, `onClose` and `onCancel` callbacks).