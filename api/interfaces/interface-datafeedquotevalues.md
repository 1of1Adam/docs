---
title: "Interface: DatafeedQuoteValues | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.DatafeedQuoteValues"
extracted_at: "2025-06-22T09:51:49.836Z"
---

- [](/charting-library-docs/)- Interfaces- DatafeedQuoteValuesOn this page# Interface: DatafeedQuoteValues[Datafeed](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed).DatafeedQuoteValues

This object contains symbol quote values, where a [quote](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/quotes) represents a set of data describing the current price.
The library uses quote data for various trading functionalities, including the [Order Ticket](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/order-ticket), [Legend](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Legend),
and widgets, such as [Watchlist](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/Watch-List), [Details](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/#details),
[News](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/news), and [Depth of Market](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/#depth-of-market).
While all properties in this object are marked as optional, populating most of them is required for supporting trading functionalities.
Providing values that do not match the expected data types can cause issues such as UI [loading delays](https://www.tradingview.com/charting-library-docs/latest/connecting_data/Datafeed-Issues#delays-in-trading-platform-ui-elements) or [missing data](https://www.tradingview.com/charting-library-docs/latest/connecting_data/Datafeed-Issues#quotes-are-not-displayed-or-refreshed).
See property descriptions for more information.
## Indexable[​](#indexable)
▪ [valueName: `string`]: `string` | `number` | `string`[] | `number`[] | `undefined`

## Properties[​](#properties)
### ask[​](#ask)
• `Optional` ask: `number`

Ask price – the lowest price a seller is willing to accept for a security. The value is displayed in the [Order Ticket](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/order-ticket) and [Buy/Sell buttons](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/#buysell-buttons-and-lines).

### bid[​](#bid)
• `Optional` bid: `number`

Bid price – the highest price a buyer is willing to pay for a security. The value is displayed in the [Order Ticket](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/order-ticket) and [Buy/Sell buttons](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/#buysell-buttons-and-lines).

### ch[​](#ch)
• `Optional` ch: `number`

Price change. It is usually calculated as a difference between the current price and close price of the previous day (regular session).
In the UI, `ch` and [chp](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.DatafeedQuoteValues#chp) are represented as the last day change parameter in Data Window.
You can also display these values in the [legend](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Legend#last-day-change-values).
If `ch` and `chp` are not provided, `0.00 (0.00%)` is displayed instead.
Note that `ch` and `chp` are required for mobile apps. Otherwise, [`NaN` values](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Legend#nan-values-in-legend) will appear in the legend.

### chp[​](#chp)
• `Optional` chp: `number`

Price change percentage. In the UI, `chp` and [ch](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.DatafeedQuoteValues#ch) are represented as the last day change parameter in Data Window.
You can also display these values in the [Legend](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Legend#last-day-change-values).
If `ch` and `chp` are not provided, `0.00 (0.00%)` is displayed instead.
Note that `ch` and `chp` are required for mobile apps. Otherwise, [`NaN` values](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Legend#nan-values-in-legend) will appear in the Legend.

### description[​](#description)
• `Optional` description: `string`

A short description of the symbol. This description is displayed in the [Details](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/#details) widget and the tooltip of the [Watchlist](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/Watch-List) widget.

### exchange[​](#exchange)
• `Optional` exchange: `string`

The name of the exchange. The exchange name is displayed in the [Details](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/#details) widget.

### high_price[​](#high_price)
• `Optional` high_price: `number`

Today's high price. The value is displayed in the [Details](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/#details) widget.

### low_price[​](#low_price)
• `Optional` low_price: `number`

Today's low price. The value is displayed in the [Details](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/#details) widget.

### lp[​](#lp)
• `Optional` lp: `number`

The price at which the most recent trade of a security occurred, regardless of whether it was a buy or sell.
Required for the [Order Ticket](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/order-ticket), [Depth of Market](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/#depth-of-market), [Buy/Sell buttons](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/#buysell-buttons-and-lines), and [Details](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/#details) and [Watchlist](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/Watch-List) widgets.

### open_price[​](#open_price)
• `Optional` open_price: `number`

Today's opening price

### original_name[​](#original_name)
• `Optional` original_name: `string`

Original name

### prev_close_price[​](#prev_close_price)
• `Optional` prev_close_price: `number`

Closing price of the symbol from the previous regular market session.

Required for mobile apps. Otherwise, `NaN` values will appear in the [Legend](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Legend).

### rch[​](#rch)
• `Optional` rch: `number`

Pre-/post-market price change. This value is required to display information on the [extended session](https://www.tradingview.com/charting-library-docs/latest/connecting_data/Extended-Sessions) in the [Details](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/#details) widget.

### rchp[​](#rchp)
• `Optional` rchp: `number`

Pre-/post-market price change percentage. This value is required to display information on the [extended session](https://www.tradingview.com/charting-library-docs/latest/connecting_data/Extended-Sessions) the [Details](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/#details) widget.

### rtc[​](#rtc)
• `Optional` rtc: `number`

Pre-/post-market price. This value is required to display the [pre-/post-market price line](https://www.tradingview.com/charting-library-docs/latest/connecting_data/Extended-Sessions#enable-the-price-line) on the chart and information on the extended session in the [Details](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/#details) widget.

### rtc_time[​](#rtc_time)
• `Optional` rtc_time: `number`

Pre-/post-market price update time. This value is required to display information on the [extended session](https://www.tradingview.com/charting-library-docs/latest/connecting_data/Extended-Sessions) in the [Details](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/#details) widget.

### short_name[​](#short_name)
• `Optional` short_name: `string`

Short name for a symbol. Short name is used in the title for the [News](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/news), [Watchlist](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/Watch-List) and [Details](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/#details) widgets. You can disable the [`prefer_quote_short_name`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#prefer_quote_short_name) to use the [LibrarySymbolInfo.ticker](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.LibrarySymbolInfo#ticker) value instead.

### spread[​](#spread)
• `Optional` spread: `number`

Spread – the difference between the ask and bid prices. The value is displayed between [Buy/Sell buttons](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/#buysell-buttons-and-lines).

### volume[​](#volume)
• `Optional` volume: `number`

Today's trading volume. This value is displayed in the [Watchlist](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/Watch-List) widget.

- [Indexable](#indexable)- [Properties](#properties)[ask](#ask)- [bid](#bid)- [ch](#ch)- [chp](#chp)- [description](#description)- [exchange](#exchange)- [high_price](#high_price)- [low_price](#low_price)- [lp](#lp)- [open_price](#open_price)- [original_name](#original_name)- [prev_close_price](#prev_close_price)- [rch](#rch)- [rchp](#rchp)- [rtc](#rtc)- [rtc_time](#rtc_time)- [short_name](#short_name)- [spread](#spread)- [volume](#volume)