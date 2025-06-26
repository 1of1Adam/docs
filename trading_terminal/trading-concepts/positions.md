---
title: "Positions | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/positions"
extracted_at: "2025-06-22T09:29:14.330Z"
---

# Positions## Overview
A **position** is the amount of a financial instrument held by an investor.
A position is always a result of the executed [order](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/orders).
In the library, positions can be categorized into two types:

**Regular positions**. These are positions that are aggregated regardless of the position side, whether [long](https://www.investopedia.com/terms/l/long.asp) or [short](https://www.investopedia.com/terms/s/short.asp).
With regular positions, each symbol can have only one position.
All user actions, such as buying or selling, result in either an increase or decrease in the position's quantity.
For example, if a user buys 100 shares of a stock and later sells 50 shares, their position would be 50 shares.
**Individual positions**. These positions are displayed based on the position side, meaning that long and short positions are treated separately.
Individual positions are used in the context of [position netting](#position-netting), where all individual positions are aggregated to calculate a single net position for a particular symbol.
For example, a user might have two individual positions for the same symbol: a long position of 100 shares and a short position of 50 shares.
In this case, the net position would be 50 shares long.

> **Tip:** Before continuing with this article, we recommend reading [Core concepts](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/) and [Trading features configuration](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/trading-features-configuration) articles for a better understanding.

## Handle and display regular positions
When the chart is initially loaded, the library calls the [`positions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal#positions) method from your [Broker API](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/#broker-api) implementation.
Your implementation should return an array of [`Position`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.Position) objects, containing data about the positions a user already held before the chart was created.
To update the library with any added or changed positions, your Broker API implementation should call the [`positionUpdate`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost#positionupdate) method on the Trading Host.

> **Warning:** You may encounter a [timeout issue](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/common-issues#timeout-issue) if the library fails to receive timely updates through `positionUpdate`.

User positions are displayed as follows:

- On the chart, as a line based on the [`avgPrice`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.Position#avgprice) value of the [`Position`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.Position) object.
- On the *Account Manager → Positions* page. For more information, refer to the [Orders and Positions](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/#orders-and-positions) section.

## Handle multiple positions for one symbol
The library supports two options for handling multiple positions for the same symbol: [position netting](#position-netting) and [multiposition](#multiposition).
Each option offers a different way of managing and displaying positions in the interface.
### Position netting
**Position netting** aggregates multiple individual positions for one symbol into a single net position.
For example, a user might have two individual positions for the same symbol: a long position of 100 shares and a short position of 50 shares.
In this case, the net position would be 50 shares long.
To enable position netting, use the [`supportPositionNetting`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportpositionnetting) flag.
Once activated, this flag adds two new pages to the [Account Manager](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/) within *Positions*: *Individual Positions* and *Net Positions*.
Note that the number on the *Positions* tab represents only the total count of net positions.
![Individual Positions and Net Positions pages in the Account Manager](https://www.tradingview.com/charting-library-docs/assets/images/account-manager-position-netting-3c48f16ba7022f40f289ad70aed16ceb.png)
Additionally, the library starts to operate with the following methods in the [Broker API](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/#broker-api):

- [`individualPositions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal#individualpositions) for handling individual positions
- [`positions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal#positions) for handling net positions

Your implementation should return arrays of [`IndividualPosition`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IndividualPosition) and [`Position`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.Position) objects, depending on the method the library calls.
These objects should contain data about the positions a user already held before the chart was created.
To update the library with any added or changed individual/net positions, your Broker API implementation should call the [`individualPositionUpdate`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost#individualpositionupdate)/[`positionUpdate`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost#positionupdate) methods on the Trading Host.

> **Warning:** You may encounter a [timeout issue](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/common-issues#timeout-issue) if the library fails to receive timely updates through `individualPositionUpdate`/`positionUpdate`.

### Multiposition
Alternatively, the **multiposition** option allows displaying multiple positions for the same symbol without aggregating them into a net position.
To enable multiposition, set the [`supportMultiposition`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportmultiposition) flag to `true`.
Unlike [position netting](#position-netting), this flag does not affect how positions are calculated but affects how they are displayed in the interface.
The library operates with the [Broker API](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/#broker-api) methods the same way as described in the [Handle and display regular positions](#handle-and-display-regular-positions) section.
## Close positions
The library supports two ways to close positions based on the value of the [`supportClosePosition`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportcloseposition)/[`supportCloseIndividualPosition`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportcloseindividualposition) flag.

Default behavior (`false`) — positions are closed using [market orders](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/orders#order-types) of the opposite side.
The library calls the [`placeOrder`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal#placeorder) method, passing the [`isClose`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PreOrder#isclose) property set to `true` in the [`PreOrder`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PreOrder) object.
Custom logic (`true`) — you can implement custom logic for closing positions.
In this case, the library calls the [`closePosition`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal#closeposition)/[`closeIndividualPosition`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal#closeindividualposition) method from the Broker API.

> **Info:** The library expects you to call the [`positionUpdate`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost#positionupdate) method whenever there is a new position added or existing one changed.
This call is confirmation to the library that your backend server received and handled the request. Otherwise, the library will return a [timeout issue](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/common-issues#timeout-issue).

### Partial closing
Partial position closing allows users to close part of a position while keeping the remainder open.
When a user clicks the close button for a position, a dialog appears, allowing the user to specify the number of shares to close.
For example, if the position size is 10, the user can choose any value between 1 and 10.
The position is then updated to reflect the remaining number of shares.
To enable partial position closing, set the [`supportPartialClosePosition`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportpartialcloseposition)/[`supportPartialCloseIndividualPosition`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportpartialcloseindividualposition) flag to `true`.
The library then handles the closing based on the value of the [`supportClosePosition`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportcloseposition)/[`supportCloseIndividualPosition`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportcloseindividualposition) flag:

- If `false`, the library calls the [`placeOrder`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal#placeorder) method, passing the specified quantity in the [`PreOrder`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PreOrder) object.
- If `true`, the library calls the [`closePosition`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal#closeposition)/[`closeIndividualPosition`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal#closeindividualposition) method, passing the `amount` parameter.

## Reverse positions
The library supports the reverse option that allows users to quickly switch a position from long to short and vice versa. To enable this option in the UI, set the [`supportReversePosition`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportreverseposition) flag to `true`.

Consider an example. A user has a long position in AAPL for 100 shares. When the user clicks *Reverse*, the position turns into a short one, while other position parameters remain the same.

Users can reverse positions in three ways:

Click the *Reverse Position* button on the chart.

Click the *Reverse* button in the [Depth of Market](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/depth-of-market) widget.

Right-click the position in the [Account Manager](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/) and select *Reverse Position*.

A reverse request can be handled in the following ways:

- [Default reversal](#default-reversal) — the library handles reversing.
- [Native reversal](#native-reversal) — you handle reversing on your backend side.

### Default reversal
The library includes a built-in mechanism for processing reversal. This mechanism is used by default when the [`supportReversePosition`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportreverseposition) flag is `true`, unless you explicitly enable the [native reversal](#native-reversal).

When a user requests to reverse a position, the library calls the [`placeOrder`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal#placeorder) method to close the original position and place a new market order with the following parameters:

- [`isClose`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PreOrder#isclose) — `true`, meaning that the original position should be closed.
- [`side`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PreOrder#side) — the opposite side to the original position.
- [`qty`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PreOrder#qty) — the number of units in the original position multiplied by 2.

For example, a user requests to reverse a long position in AAPL for 100 shares. In this case, the library places an order to sell 200 shares of AAPL. As a result, the user will have a short position in AAPL for 100 shares.

> **Warning:** Note that the library cannot handle reversing of [multiple positions](#multiposition). In this case, you need to implement the [native reversal](#native-reversal) on your backend side.
Otherwise, the following issue occurs: *Cannot reverse position on multiposition account*.

### Native reversal
Native reversal allows you to implement a custom reversing mechanism, depending on your specific requirements.
For example, you can handle different scenarios, such as the reversal of [multiple positions](#multiposition).
To enable the native reversal, set the [`supportReversePosition`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportreverseposition) and [`supportNativeReversePosition`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportnativereverseposition) flags to `true`.
On your backend side, you should implement the [`reversePosition`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal#reverseposition) method that is called when a user requests to reverse a position.
## Provide profit and loss
**Profit and loss** (P&L) values indicate the current profit or loss status of an account or a position.
P&L values are displayed in the [Account Manager](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/) and on the chart for the related position.
The P&L feature is enabled by default via the [`supportPLUpdate`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportplupdate) flag.
This means you should calculate the P&L value for a position on your backend server.
Once calculated, you should call the [`plUpdate`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost#plupdate) method to notify the library about P&L updates.
Note that the library will return a [timeout issue](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/common-issues#timeout-issue) if it fails to receive a timely update.
If [position netting](#position-netting) is enabled, you should also call [`individualPositionPLUpdate`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost#individualpositionplupdate).
This method functions the same way as `plUpdate` but provides updates specifically to individual positions.

> **Info:** When position netting is enabled, the chart displays P&L for individual positions only.
P&L for net positions are not shown.

If `supportPLUpdate` is set to `false`, the library automatically calculates P&L values as the difference between the current trade and the average position price.
However, we recommend using your own P&L calculations for positions.
This helps avoid any discrepancies between the P&L values of the account and positions due to potential delays.
## Add brackets
**Bracket orders** (brackets) are orders that protect positions.
In other words, brackets help users limit their losses and secure their profits by bracketing positions with either one or two opposing stop-loss and take-profit orders.
Refer to [Bracket orders](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/brackets) for more information.