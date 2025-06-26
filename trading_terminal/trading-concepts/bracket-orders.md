---
title: "Bracket orders | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/brackets"
extracted_at: "2025-06-22T09:29:16.758Z"
---

# Bracket orders## Overview
**Bracket orders** (brackets) are orders that protect positions.
In other words, brackets help users limit their losses and secure their profits
by bracketing positions with two opposing [stop-loss](https://www.tradingview.com/charting-library-docs/latest/getting_started/glossary#stop-loss-order) and [take-profit](https://www.tradingview.com/charting-library-docs/latest/getting_started/glossary#take-profit-order) orders.
The term **parent** refers to an order or position for which brackets are created.
Bracket orders are linked to the parent order/position via the [`parentId`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BracketOrder#parentid) and [`parentType`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BracketOrder#parenttype) properties.
The quantity of the bracket order always matches the parent quantity.
Brackets always have the opposite side compared to their parent, for example:

- A buy order is bracketed by a sell-limit order or a sell-stop order.
- A sell order is bracketed by a buy-stop order or a buy-limit order.

Brackets can exist either in a pair as stop-loss and take-profit or independently.
This means that an order or position can have only one bracket order: stop-loss or take-profit.

> **Warning:** This article requires a thorough understanding of the Trading Platform components and their interactions.
Before continuing with this article, we recommend reading the [Core concepts](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/) article for a better understanding.

## UI interactions
Users can add brackets to a new or existing order or to a position.

- Place order with brackets- Add brackets via buttons- Add brackets via Protect position![Placing order with brackets](https://www.tradingview.com/charting-library-docs/assets/images/ui-place-order-with-brackets-44f9055ca67eb47254bcf3a37bcb453b.gif)![Adding brackets to position via bracket buttons](https://www.tradingview.com/charting-library-docs/assets/images/ui-add-position-brackets-cf4e15e71027a229ba853cec644a5602.gif)![Adding brackets to position via Protect position button](https://www.tradingview.com/charting-library-docs/assets/images/ui-protect-position-2ca8109bfcf0d06a859745ba0a5b2716.gif)
## Order brackets
To enable adding order brackets in the UI, set the [`supportOrderBrackets`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportorderbrackets) flag to `true`.
Refer to the [Trading features configuration](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/trading-features-configuration) section for more information about configuration flags.
### Place order with brackets
Users can place orders with two brackets or only one — either a stop-loss or take-profit.
When users place orders with brackets, the library calls the [`placeOrder`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal#placeorder) method and passes a [`PreOrder`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PreOrder) object as a parameter.
This object contains the [`stopLoss`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PreOrder#stoploss) and [`takeProfit`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PreOrder#takeprofit) fields.
Additionally, if a user places a [limit order](https://www.tradingview.com/charting-library-docs/latest/getting_started/glossary#limit-order) or [stop orders](https://www.tradingview.com/charting-library-docs/latest/getting_started/glossary#stop-order), the `PreOrder` object should contain the following fields:

- For limit order, the [`limitPrice`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PreOrder#limitprice) field.
- For stop order, the [`stopPrice`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PreOrder#stopprice) field.

#### Example
Consider the following example: a user places a [market order](https://www.tradingview.com/charting-library-docs/latest/getting_started/glossary#market-order) with two brackets.

Expand to view the diagram illustrating the process of placing a market order with brackets.

[![Diagram illustrating placing an order with brackets](https://www.tradingview.com/charting-library-docs/img/place-order-with-brackets-diagram-light.svg)](/charting-library-docs/img/place-order-with-brackets-diagram-light.svg)
The library calls the [`placeOrder`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal#placeorder) method, requesting to create an order.
You should implement this method within the Broker API.
Refer to the [Order creation](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/#1-order-creation) section for a detailed explanation.
After your backend server handles the order creation, it responds to your Broker API implementation with updated information.
Your Broker API implementation then calls the [`orderUpdate`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost#orderupdate) method three times.

The first call provides the [`PlacedOrder`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PlacedOrder) object that contains information about the **parent order**.
The [status](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PlacedOrder#status) of the parent order should be [`Working`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.OrderStatus#working).
Other object values must be identical to the data provided within the `placeOrder` method.
```
{
    "id": "1",
    "symbol": "NasdaqNM:AAPL",
    "qty": 100,
    "side": 1,   // Side.Buy
    "status": 6, // Status.Working
    "type": 2,   // Type.Market
    "takeProfit": 174.5,
    "stopLoss": 173.32
}

```

> **Info:** For limit and stop orders, make sure to include the `limitPrice` and `stopPrice` fields respectively in the [`PlacedOrder`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PlacedOrder) object
when updating the parent order using the [`orderUpdate`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost#orderupdate) method.

The second call provides the [`BracketOrder`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BracketOrder) object that contains information about the **take-profit order**.
The status of the take-profit order should be `Inactive`, and the `qty` and `symbol` values must be identical to the parent order values.
The data object must also include:

- The `parentId` field with a value **equal** to the `id` value of the parent order.
- The `parentType` field, indicating that the parent type is **order**.
- The `side` field with a value **opposite** to the `side` value of the parent order.
- The `limitPrice` field with a value **equal** to the `takeProfit` value of the parent order.
- The `type` value, indicating that the order type is **limit**.

```
{
  "id": "2",
  "symbol": "NasdaqNM:AAPL",
  "qty": 100,
  "parentId": "1",
  "parentType": 1,  // ParentType.Order
  "side": -1,       // Side.Sell
  "status": 3,      // Status.Inactive
  "type": 1,        // Type.Limit
  "limitPrice": 174.5
}

```

The third call provides the `BracketOrder` object that contains information about the **stop-loss order**.
The status of the stop-loss order should be `Inactive`, and the `qty` and `symbol` values must be identical to the parent order values.
The data object must also include:

- The `parentId` field with a value **equal** to the `id` value of the parent order.
- The `parentType` field, indicating that the parent type is **order**.
- The `side` field with a value **opposite** to the `side` value of the parent order.
- The `stopPrice` field with a value **equal** to the `stopLoss` value of the parent order.
- The `type` value, indicating that the order type is **stop**.

```
{
  "id": "3",
  "symbol": "NasdaqNM:AAPL",
  "qty": 100,
  "parentId": "1",
  "parentType": 1,  // ParentType.Order
  "side": -1,       // Side.Sell
  "status": 3,      // Status.Inactive
  "type": 3,        // Type.Stop
  "stopPrice": 173.32
}

```
### Execute parent order
Bracket orders are linked to the parent order by the *Order-Sends-Order (OSO)* condition.
This means that once the parent order is executed and its status transitions to `Filled`,
the bracket order [statuses](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.OrderStatus) should change to `Working`.
When the parent order is executed, it turns into a position.
Therefore, you should update the `parentId` and `parentType` fields in the bracket order objects to be associated with this new parent position.
Along with changing the order statuses, change the values of the following fields:

- [`parentId`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BracketOrder#parentid) should be equal to the `id` value of the position that resulted from the execution of the parent order.
- [`parentType`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BracketOrder#parenttype) should be changed to `2`, indicating that the parent type is **position**.

#### Example
Consider the following example: a user has placed a [market order](https://www.tradingview.com/charting-library-docs/latest/getting_started/glossary#market-order) with two brackets.
Following this, your backend server is responsible for executing the order, creating a position,
and updating the information within the bracket orders.
Expand to view the diagram illustrating the process of executing parent order.

[![Diagram illustrating executing the parent order and updating bracket orders](https://www.tradingview.com/charting-library-docs/img/execute-parent-order-diagram-light.svg)](/charting-library-docs/img/execute-parent-order-diagram-light.svg)
Your Broker API implementation calls the [`executionUpdate`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost#executionupdate) and [`positionUpdate`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost#positionupdate) methods.
Refer to the [Execution update](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/#2-execution-update) section for a detailed explanation for these methods.
Then, your Broker API implementation calls the [`orderUpdate`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost#orderupdate) method three times to provide the library with updated information.

The first call provides updated information about the **parent order**.
Its [status](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.OrderStatus) should be `Filled`.
```
{
    "id": "1",
    "symbol": "NasdaqNM:AAPL",
    "qty": 100,
    "side": 1,    // Side.Buy
    "status": 2,  // Status.Filled
    "type": 2,    // Type.Market
    "takeProfit": 174.5,
    "stopLoss": 173.32
}

```

The second call provides the `BracketOrder` object that contains updated information about the **take-profit order**.
The data object must contain the following changed values, while other fields should remain the same:

- The `parentId` field with a value **equal** to the `id` value of the position (`NasdaqNM:AAPL` in this example).
- The `parentType` field, indicating that the parent type is **position**.
- The `status` value, indicating that the order status is **working**.

```
{
  "id": "2",
  "symbol": "NasdaqNM:AAPL",
  "qty": 100,
  "parentId": "NasdaqNM:AAPL",
  "parentType": 2,  // ParentType.Position
  "status": 6,      // Status.Working
  "side": -1,       // Side.Sell
  "type": 1,        // Type.Limit
  "limitPrice": 174.5
}

```

The third call provides the `BracketOrder` object that contains information about the **stop-loss order**.
The data object must contain the following changed values, while other fields should remain the same:

- The `parentId` field with a value **equal** to the `id` value of the position.
- The `parentType` field, indicating that the parent type is **position**.
- The `status` value, indicating that the order status is **working**.

```
{
  "id": "3",
  "symbol": "NasdaqNM:AAPL",
  "qty": 100,
  "parentId": "NasdaqNM:AAPL",
  "parentType": 2,  // ParentType.Position
  "status": 6,      // Status.Working
  "side": -1,       // Side.Sell
  "type": 3,        // Type.Stop
  "stopPrice": 173.32
}

```

> **Tip:** To keep the UI data up-to-date, you should constantly provide updates of users' entity and P&L values whenever changes occur.
Refer to the [Equity update](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/#3-equity-update) section for more information.

## Position brackets
To enable adding position brackets in the UI, set the [`supportPositionBrackets`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportpositionbrackets) or [`supportIndividualPositionBrackets`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportindividualpositionbrackets) flag to `true`.
This activates buttons for creating brackets on the chart and enables the *Protect position* button.
For more details on configuration flags, check the [Trading features configuration](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/trading-features-configuration) section.
### Add position brackets
By default, users can add two brackets at the same time or only one of them.
However, you can set the [`supportOnlyPairPositionBrackets`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BrokerConfigFlags#supportindividualpositionbrackets) flag to `true`, so users can add two brackets together only.
When users add brackets to the existing position, the library calls the [`editPositionBrackets`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal#editpositionbrackets) method. In this method, the library provides the `stopLoss` and `takeProfit` fields.
After that, the library expects you to call the [`positionUpdate`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost#positionupdate) method within 10 seconds.
Note that the library will return a [timeout issue](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/common-issues#timeout-issue) if it fails to receive a timely position update.
#### Example
Consider the following example: the user has an APPL position and decides to place two bracket orders for this position.

Expand to view the diagram illustrating the process of adding two bracket orders to the position.

[![Diagram illustrating adding position brackets](https://www.tradingview.com/charting-library-docs/img/add-position-brackets-diagram-light.svg)](/charting-library-docs/img/add-position-brackets-diagram-light.svg)
The library calls the [`editPositionBrackets`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal#editpositionbrackets) method, providing the `stopLoss` and `takeProfit` fields.
You should implement this method within your Broker API implementation
and handle the user's request to add bracket orders.
Note that the position update and order creation might be processed on external sources, such as exchanges.
However, your backend server is expected to manage this information and provide it in the format required by the library.
After your backend server handles the position update and order creation, it responds to your Broker API implementation with updated information.
Your Broker API implementation then calls the [`positionUpdate`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost#positionupdate) and [`orderUpdate`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost#orderupdate) methods.

- The `positionUpdate` call updates a [Position](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.Position) object with the `stopLoss` and `takeProfit` fields.

```
{
  "id": "NasdaqNM:AAPL",
  "qty": 100,
  "side": 1,  // Side.Buy
  "symbol": "NasdaqNM:AAPL",
  "takeProfit": 174.5,
  "stopLoss": 173.32
}

```

The first `orderUpdate` call provides the `BracketOrder` object that contains information about the **take-profit order**.
The status of the take-profit order should be `Working`, and the `qty` and `symbol` values must be identical to the parent position values.
The data object must also include:

- The `parentId` field with a value **equal** to the `id` value of the parent position.
- The `parentType` field, indicating that the parent type is **position**.
- The `side` field with a value **opposite** to the `side` value of the parent position.
- The `limitPrice` field with a value **equal** to the `takeProfit` value of the parent position.
- The `type` value, indicating that the order type is **limit**.

```
{
   "symbol": "NasdaqNM:AAPL",
   "qty": 100,
   "id": "2",
   "parentId": "NasdaqNM:AAPL",
   "parentType": 2,  // ParentType.Position
   "side": -1,       // Side.Sell
   "status": 6,      // Status.Working
   "type": 1,        // Type.Limit
   "limitPrice": 174.5
}

```

The second `orderUpdate` call provides the `BracketOrder` object that contains information about the **stop-loss order**.
The status of the stop-loss order should be `Working`, and the `qty` and `symbol` values must be identical to the parent position values.
The data object must also include:

- The `parentId` field with a value **equal** to the `id` value of the parent position.
- The `parentType` field, indicating that the parent type is **position**.
- The `side` field with a value **opposite** to the `side` value of the parent position.
- The `stopPrice` field with a value **equal** to the `stopLoss` value of the parent position.
- The `type` value, indicating that the order type is **stop**.

```
{
   "symbol": "NasdaqNM:AAPL",
   "qty": 100,
   "id": "3",
   "parentId": "NasdaqNM:AAPL",
   "parentType": 2,  // ParentType.Position
   "side": -1,       // Side.Sell
   "status": 6,      // Status.Working
   "type": 3,        // Type.Stop
   "stopPrice": 173.32
}

```
### Execute bracket order
Bracket orders are linked to each other by the *One-Cancels-the-Other (OCO)* condition.
This means that when one of the bracket orders is executed, the other one gets canceled.
In this case, the position linked to the executed bracket order should change its quantity to zero, closing the position.
#### Example
Consider the following example: the user has a position with two bracket orders.
You broker server executes a stop-loss order and returns updated information.
Expand to view the diagram illustrating the process of executing a bracket order.

[![Diagram illustrating executing the stop-loss order](https://www.tradingview.com/charting-library-docs/img/execute-bracket-diagram-light.svg)](/charting-library-docs/img/execute-bracket-diagram-light.svg)
Your Broker API implementation then calls two consequent [`orderUpdate`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost#orderupdate) methods and then [`positionUpdate`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost#positionupdate).

The first `orderUpdate` call provides information about the executed **stop-loss order**.
The status of the order should be `Filled`.

```
{
  "symbol": "NasdaqNM:AAPL",
  "qty": 100,
  "id": "3",
  "parentId": "NasdaqNM:AAPL",
  "parentType": 2,  // ParentType.Position
  "side": -1,       // Side.Sell
  "status": 2,      // Status.Filled
  "type": 3,        // Type.Stop
  "stopPrice": 173.32
}

```

The second `orderUpdate` call provides information about the canceled **stop-loss order**.
The status of the order should be `Canceled`.

```
{
  "symbol": "NasdaqNM:AAPL",
  "qty": 100,
  "id": "3",
  "parentId": "NasdaqNM:AAPL",
  "parentType": 2,  // ParentType.Position
  "side": -1,       // Side.Sell
  "status": 1,      // Status.Canceled
  "type": 1,        // Type.Limit
  "limitPrice": 174.5
}

```

- The `positionUpdate` call changes the `qty` property to `0`.

```
{
  "id": "NasdaqNM:AAPL",
  "qty": 0,
  "side": 1,  // Side.Buy
  "symbol": "NasdaqNM:AAPL",
  "takeProfit": 174.5,
  "stopLoss": 173.32
}

```