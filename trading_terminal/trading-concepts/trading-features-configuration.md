---
title: "Trading features configuration | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/trading-features-configuration"
extracted_at: "2025-06-22T09:29:21.824Z"
---

# Trading features configurationYou can configure trading features using the [`broker_config`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.TradingTerminalWidgetOptions#broker_config) property of the [Widget Constructor](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Widget-Constructor#trading-platform-parameters).
This property is primarily used to specify the `configFlags` object, which contains a list of [configuration flags](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags).
Some flags only enable or disable trading elements in the UI,
while others activate more advanced features that require corresponding methods to be implemented in the [Broker API](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/#broker-api).
Consider the [Widget Constructor](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Widget-Constructor#trading-platform-parameters) with the following properties.

```
const datafeed = new Datafeeds.UDFCompatibleDatafeed("https://demo-feed-data.tradingview.com");
new TradingView.widget({
    container: "chartContainer",
    locale: "en",
    library_path: "charting_library/",
    datafeed: datafeed,
    symbol: "AAPL",
    interval: "1D",
    broker_factory: function(host) { return new Brokers.BrokerSample(host, datafeed); },
    broker_config: {
        configFlags: {
            supportEditAmount: false,
            supportOrdersHistory: true,
        },
    },
})

```
In the code sample, the [`supportEditAmount`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supporteditamount) flag disables the order quantity control in the [Order Ticket](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/order-ticket) when users modify orders.
This flag only affects the UI.
The [`supportOrdersHistory`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportordershistory) flag enables the [*History*](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/#history) page in the Account Manager.
On this page, users can see details about all their orders with final [statuses](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/orders#order-statuses).
However, in addition to enabling `supportOrdersHistory`, you should also do the following:

- Implement the [`ordersHistory`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal#ordershistory) method to provide the library with the user's order history.
- Add the [`historyColumns`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.AccountManagerInfo#historycolumns) property to the [`AccountManagerInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal#accountmanagerinfo) object to define and display data columns.