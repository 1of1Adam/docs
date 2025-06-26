---
title: "Authentication | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/authentication"
extracted_at: "2025-06-22T09:29:19.453Z"
---

# AuthenticationTrading Platform provides trading capabilities.
Users can have accounts to trade, manage orders, track positions, monitor their potential profits and losses, and more.

> **Info:** Creating broker accounts, handling authentication and authorization processes should be implemented on your backend side.
Your backend server should also process users' trades and provide the library with users' data through the [Broker API](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/#broker-api).
The library only displays users' trading data and notifies your Broker API implementation about user actions.

You can design the authentication and authorization processes to fit your needs.
This article outlines [possible approaches](#authentication-approaches)
and describes [how the library handles users logging](#how-the-library-handles-login) into their broker accounts.
## Authentication approaches
### Before accessing the app
One approach is to handle authentication and authorization before users access your app.
This ensures that only authenticated users can enter the app and interact with their trading data.
### Through the top toolbar button
Another approach is to integrate authentication through a button in the top toolbar of the chart.
You can add this button using the [`createButton`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#createbutton) or [`createDropdown`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#createdropdown) methods.
Such a button can trigger the authentication process, allowing users to access their trading data once authenticated.
### Through Account Manager
The [Account Manager](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/) is designed to display the trading data of a particular user account.
Users can manage [multiple accounts](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/multiple-accounts) and switch between them using the drop-down menu in the Account Manager.
Authentication and authorization can be implemented when users select an account from the drop-down menu,
ensuring that each selected account is properly authenticated before data access is granted.
![Drop-down menu for selecting multiple accounts](https://www.tradingview.com/charting-library-docs/assets/images/multiple-accounts-4671270d3b8436d9de7763da75bee371.png)
## How the library handles login
On startup, the library calls [`accountsMetainfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal#accountsmetainfo) to get the information about accounts of a particular user.
This method should return an array that contains an ID and name for each account.
In general, the user login process looks as follows:

A user logs into their broker account.
Note that the library does not provide any login dialogs, you should implement them on your side.
- Your backend server prepares the user's data and provides a response to your [Broker API](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/#broker-api) implementation with updated information.
- Your Broker API implementation calls the [`currentAccountUpdate`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost#currentaccountupdate) method to notify the library about changes in account details.
- The library calls the [`accountsMetainfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal#accountsmetainfo) and [`currentAccount`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal#currentaccount) methods.