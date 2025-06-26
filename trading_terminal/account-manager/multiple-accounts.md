---
title: "Multiple accounts | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/multiple-accounts"
extracted_at: "2025-06-22T09:32:32.750Z"
---

# Multiple accounts
> **Info:** Creating broker accounts, handling authentication and authorization processes should be implemented on your backend side.
Your backend server should also process users' trades and provide the library with users' data through the [Broker API](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/#broker-api).
The library only displays users' trading data and notifies your Broker API implementation about user actions.
Refer to [Authentication](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/authentication) for more information on authentication approaches and how the library handles users logging into their broker accounts.

The [Account Manager](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/) is designed to display the trading data of a particular user account.
Users can have multiple accounts and switch between them using the drop-down menu in the Account Manager.
![Drop-down menu for selecting multiple accounts](https://www.tradingview.com/charting-library-docs/assets/images/multiple-accounts-4671270d3b8436d9de7763da75bee371.png)
This menu appears automatically when [`accountsMetainfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal#accountsmetainfo) returns an array of objects.
When users switch accounts, the library calls the [`setCurrentAccount`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal#setcurrentaccount) method, providing your backend server with the ID of the requested account.
See the CodePen example below.
See the Pen 
Trading Platform. Implement multiple user accounts. by TradingView ([@tradingview](https://codepen.io/tradingview))
on [CodePen](https://codepen.io).