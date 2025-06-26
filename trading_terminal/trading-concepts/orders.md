---
title: "Orders | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/orders"
extracted_at: "2025-06-22T09:29:12.264Z"
---

# Orders## Overview
An **order** is a request to buy or sell a financial instrument at a specified price and quantity.
In the UI, users can place orders via the [Order Ticket](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/order-ticket).
When the chart is initially loaded, the library calls the [`orders`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal#orders) method from the [Broker API](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/#broker-api) implementation.
As a result, your implementation should return either a [`PlacedOrder`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PlacedOrder) or [`BracketOrder`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.BracketOrder) object.
The object should contain data about orders that a user already had before the chart was created.
You can refer to the [step-by-step example](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/#how-components-work-together) and the [Bracket orders](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/brackets) article to learn how these objects should be used.
All user's orders are displayed in the *[Account Manager](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/) → Orders* page.

![The Orders page in the Account Manager](https://www.tradingview.com/charting-library-docs/assets/images/orders-page-in-account-manager-3f0f3c89a5462d2e0b0c5ee6b75fceb7.png)
## Order types
Order types allow users to place orders according to their specific strategies and risk tolerance.
The library supports four order types:

**Market order** is an order to buy or sell a financial instrument at the current market price.
This order type guarantees immediate execution but does not guarantee a specific price.
**Limit order** is an order to buy or sell a financial instrument when a given or better price is reached.
This order type guarantees a specific price but does not guarantee immediate execution.
- **Stop order** is an order to buy or sell a financial instrument at the market price as soon as it reaches a certain level.
- **Stop-limit order** is an order that combines a stop price and a limit price.

You can configure which types you want to support.
Refer to [Configure order types](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/order-ticket#configure-order-types) for more information.
## Bracket orders
Trading Platform supports creating bracket orders for positions.
A **bracket order** is an order that helps users limit their losses and secure their profits by bracketing positions with two opposing stop-loss and take-profit orders.

- **Stop-loss order** is a type of order designed to limit losses by automatically closing a position at a given price when it moves unfavorably.
- **Take-profit order** is a type of limit order that closes a position at a specific price to secure a profit.

Refer to [Bracket orders](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/brackets) for more information.

## Order statuses
When an order is placed, it enters the execution process.
In this process, orders have statuses that can be divided into two groups:

**Transitional**

- Placing: an order is registered by the broker, but the exchange has not confirmed the status yet.
- Working: an order is created and approved by the exchange but not executed yet.
- Inactive: an order is in the system, but not at work. Applied to bracket orders.

**Final**

- Filled: an order is executed.
- Canceled: an order is canceled by a user.
- Rejected: an order is rejected for some reason, for example, the exchange rejected the order.

Note that the order status can only change from transitional to final, not vice versa.
Refer to a [step-by-step example](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/#how-components-work-together) to see the whole order process: from placement to execution.