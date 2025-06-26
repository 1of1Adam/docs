---
title: "Interface: IBrokerAccountInfo | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerAccountInfo"
extracted_at: "2025-06-22T09:54:26.807Z"
---

- [](/charting-library-docs/)- Interfaces- IBrokerAccountInfoOn this page# Interface: IBrokerAccountInfo[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).IBrokerAccountInfo

## Hierarchy[​](#hierarchy)

`IBrokerAccountInfo`

↳ [`IBrokerTerminal`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerTerminal)

## Methods[​](#methods)
### accountsMetainfo[​](#accountsmetainfo)
▸ accountsMetainfo(): `Promise`<[`AccountMetainfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.AccountMetainfo)[]>

The library calls `accountsMetainfo` to get a list of accounts for a particular user.
The method should return an array that contains an ID and name for each account.
Note that if `accountsMetainfo` returns an array containing more than one element, you should implement the [setCurrentAccount](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerAccountInfo#setcurrentaccount) method.
Refer to [Multiple accounts](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/multiple-accounts) for more information.
#### Returns[​](#returns)
`Promise`<[`AccountMetainfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.AccountMetainfo)[]>

### currentAccount[​](#currentaccount)
▸ currentAccount(): [`AccountId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#accountid)

The library calls `currentAccount` to get the current account's ID.

#### Returns[​](#returns-1)
[`AccountId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#accountid)

### setCurrentAccount[​](#setcurrentaccount)
▸ setCurrentAccount(`id`): `void`

The library calls `setCurrentAccount` when users switch accounts using the drop-down menu in the [Account Manager](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/).
This method provides your backend server with the ID of the selected account.
Note that `setCurrentAccount` is required if [accountsMetainfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerAccountInfo#accountsmetainfo) returns an array containing more than one element.
Refer to [Multiple accounts](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/multiple-accounts) for more information.
#### Parameters[​](#parameters)
NameTypeDescription`id`[`AccountId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#accountid)The ID of the selected account.
#### Returns[​](#returns-2)
`void`

- [Hierarchy](#hierarchy)- [Methods](#methods)[accountsMetainfo](#accountsmetainfo)- [currentAccount](#currentaccount)- [setCurrentAccount](#setcurrentaccount)