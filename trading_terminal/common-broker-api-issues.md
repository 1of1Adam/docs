---
title: "Common Broker API issues | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/trading_terminal/common-issues"
extracted_at: "2025-06-22T09:16:00.772Z"
---

# Common Broker API issuesThis article describes common issues that you might face when implementing the [Broker API](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/#broker-api).

## Timeout issue
You may encounter one of the following timeout issues:

- *Failed to close position: Position closing timeout*.
- *Failed to modify order: timeout waiting for new order*.
- *Failed to reverse position: Position reversing timeout*.

These issues happen because the library either received incorrect information or failed to receive timely updates for an order
or a position from your Broker API implementation.
To avoid these issues, ensure that:

Your Broker API implementation calls [`orderUpdate`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost#orderupdate)/[`positionUpdate`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost#positionupdate) within 10 seconds
after the library sends a request to place/modify/cancel order or close/reverse position.
This update is confirmation to the library that your backend server received the request.
- Your backend server and Broker API implementation provide the correct information to the library.

Consider the following example: a user closes a position of 10 AAPL shares.
In this case, the library calls the [`closePosition`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal#closeposition) method to notify your backend server about the user's intent.
As a parameter, it provides your server with `positionId`.
After that, the library expects your backend server to close the position and provide an update on its new state within 10 seconds.
Your Broker API implementation should call the [`positionUpdate`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost#positionupdate) method on the Trading Host to provide updates.
As a parameter, it should send the correct [`Position`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.Position) object to the library, which means that:

- the `id` property should match `positionId`
- the `qty` property should be `0`
- other required properties are specified
- all properties correspond to the declared types

When the library gets a position update, for example with a non-zero quantity or a different ID,
it assumes the data is for a different position and waits for the correct data.
If the library waits more than 10 seconds, it returns *Failed to close position: Position closing timeout*.
## Empty fields in bracket controls
You may encounter an issue when the input fields for bracket controls are empty.
Besides, users cannot enter values when accessing the *Edit position brackets* dialog.
![Empty bracket controls](https://www.tradingview.com/charting-library-docs/assets/images/empty-bracket-controls-3a4aacb21e3caab407eecbedfeac7012.png)
This issue occurs because the library has not received all the necessary values for these fields.
To solve this issue, ensure that your integration meets the following requirements.

- The [`resolveSymbol`](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/required-methods#resolvesymbol) method returns all required fields within the `LibrarySymbolInfo` object.
- The [`symbolInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal#symbolinfo) method returns all required fields within the `InstrumentInfo` object.
You provide the library with the following updates:

- Quote values via the [`getQuotes`](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/trading-platform-methods#getquotes)/[`subscribeQuotes`](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/trading-platform-methods#subscribequotes) method of the Datafeed API.
Pip values via the [`pipValueUpdate`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost#pipvalueupdate) method of the Trading Host if [`subscribePipValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal#subscribepipvalue) is implemented.
Ignore this update if `subscribePipValue` is not implemented.
Equity values via the [`equityUpdate`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost#equityupdate) method of the Trading Host.

> **Tip:** It is advisable to send the equity updates once the broker has been created.
If you want to provide updates while constructing the broker, encapsulate the updates within the [`setTimeout`](https://developer.mozilla.org/en-US/docs/Web/API/setTimeout) method.```
setTimeout(() => {
  this._host.equityUpdate(12345678);
}, 5);

```