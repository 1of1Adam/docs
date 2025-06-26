---
title: "Interface: IWatchedValue<T> | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IWatchedValue"
extracted_at: "2025-06-22T09:54:58.007Z"
---

- [](/charting-library-docs/)- Interfaces- IWatchedValueOn this page# Interface: IWatchedValue<T>[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).IWatchedValue

## Type parameters[​](#type-parameters)
Name`T`
## Hierarchy[​](#hierarchy)

[`IWatchedValueReadonly`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IWatchedValueReadonly)<`T`>

[`IObservableValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IObservableValue)<`T`>

↳ `IWatchedValue`

## Methods[​](#methods)
### setValue[​](#setvalue)
▸ setValue(`value`, `forceUpdate?`): `void`

Set value for the watched value

#### Parameters[​](#parameters)
NameTypeDescription`value``T`value to set`forceUpdate?``boolean`force an update
#### Returns[​](#returns)
`void`

#### Overrides[​](#overrides)
[IObservableValue](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IObservableValue).[setValue](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IObservableValue#setvalue)

### subscribe[​](#subscribe)
▸ subscribe(`callback`, `options?`): `void`

Subscribe to watched value changes

#### Parameters[​](#parameters-1)
NameTypeDescription`callback`[`WatchedValueCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#watchedvaluecallback)<`T`>callback to be evoked when change occurs`options?`[`WatchedValueSubscribeOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.WatchedValueSubscribeOptions)watch subscriber options
#### Returns[​](#returns-1)
`void`

#### Overrides[​](#overrides-1)
[IObservableValue](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IObservableValue).[subscribe](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IObservableValue#subscribe)

### unsubscribe[​](#unsubscribe)
▸ unsubscribe(`callback?`): `void`

Unsubscribe to watched value changes

#### Parameters[​](#parameters-2)
NameTypeDescription`callback?`[`WatchedValueCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#watchedvaluecallback)<`T`>callback to remove
#### Returns[​](#returns-2)
`void`

#### Overrides[​](#overrides-2)
[IObservableValue](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IObservableValue).[unsubscribe](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IObservableValue#unsubscribe)

### value[​](#value)
▸ value(): `T`

Value

#### Returns[​](#returns-3)
`T`

#### Inherited from[​](#inherited-from)
[IObservableValue](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IObservableValue).[value](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IObservableValue#value)

### when[​](#when)
▸ when(`callback`): `void`

A simplified version of subscription, with promise-like interface, generally for using with boolean-valued watched values

#### Parameters[​](#parameters-3)
NameTypeDescription`callback`[`WatchedValueCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#watchedvaluecallback)<`T`>a function to be called when the value became `true`. `once` and `callWithLast` are implicitly set to true.
#### Returns[​](#returns-4)
`void`

#### Inherited from[​](#inherited-from-1)
[IWatchedValueReadonly](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IWatchedValueReadonly).[when](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IWatchedValueReadonly#when)

- [Type parameters](#type-parameters)- [Hierarchy](#hierarchy)- [Methods](#methods)[setValue](#setvalue)- [subscribe](#subscribe)- [unsubscribe](#unsubscribe)- [value](#value)- [when](#when)