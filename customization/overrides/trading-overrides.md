---
title: "Trading overrides | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/customization/overrides/trading-overrides"
extracted_at: "2025-06-22T09:28:49.839Z"
---

# Trading overrides
> **Info:** Trading overrides are only available in [Trading Platform](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/).

This article explains how to use the [`trading_customization`](#customize-order-and-position-lines) property and the [Overrides API](#adjust-display-of-trading-features) to customize trading elements, including order and position lines, profit and loss information, and visibility settings.

## Customize order and position lines
You can override the style of order and position lines using the [`trading_customization`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.TradingTerminalWidgetOptions#trading_customization) property of the [Widget Constructor](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Widget-Constructor).
This property is defined by the [`TradingCustomization`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.TradingCustomization) interface, which offers four customization options:

- `brokerOrder` and `brokerPosition` for lines created with the [Broker API](#created-with-broker-api).
- `order` and `position` for lines created with [trading primitives](#created-with-trading-primitives).

### Created with Broker API
The [Broker API](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/#broker-api) is a component that enables trading.
When the chart is initially loaded, the library requests user's orders and positions from the Broker API implementation through the [`orders`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal#orders) and [`positions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal#positions) methods.
Order and position lines are displayed on the chart.
You can override their style using the `brokerOrder` and `brokerPosition` properties of the [`trading_customization`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.TradingTerminalWidgetOptions#trading_customization) object.
See [`BrokerOrderOverrides`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerOrderOverrides) and [`BrokerPositionOverrides`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerPositionOverrides) for full lists of override properties.
```
new TradingView.widget({
  /* Other Widget Constructor properties */

  trading_customization: {
    brokerOrder: { /* Override properties for order lines */ },
    brokerPosition: { /* Override properties for position lines */ },
  },
})

```
The example below shows how to create order and position lines using the Broker API and customize their colors.
Note that "normal" in the property name indicates the line is active and visible in the UI, while "disabled" means the line is inactive, such as when another dialog is open.
See the Pen 
Customize order and position lines created with Broker API. Trading Platform by TradingView ([@tradingview](https://codepen.io/tradingview))
on [CodePen](https://codepen.io).
### Created with trading primitives

> **Warning:** Starting from version 29, the methods for creating trading primitives are only available in [Trading Platform](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/).

[Trading primitives](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/Trading-Primitives) is a low-level mechanism for creating order and position lines using the [`createOrderLine`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#createorderline) and [`createPositionLine`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#createpositionline) methods.
You can override the style of these lines using the `order` and `position` properties within the [`trading_customization`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.TradingTerminalWidgetOptions#trading_customization) object.
See [`OrderLineToolOverrides`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.OrderLineToolOverrides) and [`PositionLineToolOverrides`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PositionLineToolOverrides) for full lists of override properties.
```
new TradingView.widget({
  /* Other Widget Constructor properties */

  trading_customization: {
    order: { /* Override properties for order lines */ },
    position: { /* Override properties for position lines */ },
  }
})

```
The example below shows how to create order and position lines and customize their quantity text color, line color, style, and width.

See the Pen 
Customize order and position lines by TradingView ([@tradingview](https://codepen.io/tradingview))
on [CodePen](https://codepen.io).
## Adjust display of trading features
The [Overrides API](https://www.tradingview.com/charting-library-docs/latest/customization/overrides/) offers properties to adjust the display, alignment, and style of profit and loss information, as well as manage the visibility of positions, orders, and execution details.
The properties are listed on the [ChartPropertiesOverrides](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#tradingpropertiesbracketspldisplay) page and their names start with `tradingProperties`.
For example, you can hide profit and loss values for [bracket orders](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/brackets).

```
widget.applyOverrides({
  "tradingProperties.bracketsPL.visibility": false,
});

```