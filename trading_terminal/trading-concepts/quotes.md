---
title: "Quotes | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/quotes"
extracted_at: "2025-06-22T09:29:10.187Z"
---

# Quotes## Overview
**Quotes** represent real-time price information for financial instruments, including the most recent bid and ask prices, opening and closing prices, price changes, and other market data.

In [Trading Platform](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/), quotes are essential for most trading features, including placing and modifying [orders](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/orders) or managing [positions](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/positions).
Quotes ensure that users see the most current data in key UI components such as the [Order Ticket](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/order-ticket) (for accurate order entry), [Watchlist](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/Watch-List) (for tracking price movements), and [Depth of Market](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/depth-of-market) (for real-time market depth).
## Provide quotes
To provide quotes, the [Datafeed API](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/) includes three quote-related methods that must be implemented before the [Broker API](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/#broker-api):

- [`getQuotes`](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/trading-platform-methods#getquotes) — retrieves the latest price information for specified symbols.
- [`subscribeQuotes`](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/trading-platform-methods#subscribequotes) — subscribes to real-time price updates for specified symbols.
- [`unsubscribeQuotes`](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/trading-platform-methods#unsubscribequotes) — stops receiving real-time price updates for specified symbols.

> **Warning:** Without these methods, the library cannot receive or process quotes, causing issues such as UI [loading delays](https://www.tradingview.com/charting-library-docs/latest/connecting_data/Datafeed-Issues#delays-in-trading-platform-ui-elements) or [missing data](https://www.tradingview.com/charting-library-docs/latest/connecting_data/Datafeed-Issues#quotes-are-not-displayed-or-refreshed).