---
title: "Interface: TradingCustomization | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.TradingCustomization"
extracted_at: "2025-06-22T09:49:14.376Z"
---

- [](/charting-library-docs/)- Interfaces- TradingCustomizationOn this page# Interface: TradingCustomization[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).TradingCustomization

Represents the structure of [TradingTerminalWidgetOptions.trading_customization](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.TradingTerminalWidgetOptions#trading_customization).

## Properties[​](#properties)
### brokerOrder[​](#brokerorder)
• `Optional` brokerOrder: `Partial`<[`BrokerOrderOverrides`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerOrderOverrides)>

Overrides for order lines created using the [Broker API](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/#broker-api).

### brokerPosition[​](#brokerposition)
• `Optional` brokerPosition: `Partial`<[`BrokerPositionOverrides`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerPositionOverrides)>

Overrides for position lines created using the [Broker API](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/#broker-api).

### order[​](#order)
• `Optional` order: `Partial`<[`OrderLineToolOverrides`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.OrderLineToolOverrides)>

Overrides for order lines created using the [IChartWidgetApi.createOrderLine](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#createorderline) method.

### position[​](#position)
• `Optional` position: `Partial`<[`PositionLineToolOverrides`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PositionLineToolOverrides)>

Overrides for position lines created using the [IChartWidgetApi.createPositionLine](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#createpositionline) method.

- [Properties](#properties)[brokerOrder](#brokerorder)- [brokerPosition](#brokerposition)- [order](#order)- [position](#position)