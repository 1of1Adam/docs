---
title: "Interface: ActionsFactory | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ActionsFactory"
extracted_at: "2025-06-22T09:32:27.332Z"
---

- [](/charting-library-docs/)- Interfaces- ActionsFactoryOn this page# Interface: ActionsFactory[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).ActionsFactory

## Properties[​](#properties)
### createAction[​](#createaction)
• createAction: (`options`: [`ActionOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ActionOptions)) => [`IAction`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IAction)

Creates an action with provided options.

#### Type declaration[​](#type-declaration)
▸ (`options`): [`IAction`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IAction)

Parameters[​](#parameters)
NameType`options`[`ActionOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ActionOptions)
Returns[​](#returns)
[`IAction`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IAction)

### createAsyncAction[​](#createasyncaction)
• createAsyncAction: (`loader`: () => `Promise`<[`ActionOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ActionOptions)>) => [`IAction`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IAction)

Creates an action that will wait for a promise to get its options.
In terms of GUI until a promise is resolved the loader/spinner will be displayed.
#### Type declaration[​](#type-declaration-1)
▸ (`loader`): [`IAction`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IAction)

Parameters[​](#parameters-1)
NameType`loader`() => `Promise`<[`ActionOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ActionOptions)>
Returns[​](#returns-1)
[`IAction`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IAction)

### createSeparator[​](#createseparator)
• createSeparator: () => [`ISeparator`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISeparator)

Creates a separator item.

#### Type declaration[​](#type-declaration-2)
▸ (): [`ISeparator`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISeparator)

Returns[​](#returns-2)
[`ISeparator`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISeparator)

- [Properties](#properties)[createAction](#createaction)- [createAsyncAction](#createasyncaction)- [createSeparator](#createseparator)