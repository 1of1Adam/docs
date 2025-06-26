---
title: "Interface: IWatchedValueReadonly<T> | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IWatchedValueReadonly"
extracted_at: "2025-06-22T09:54:59.874Z"
---

- [](/charting-library-docs/)- Interfaces- IWatchedValueReadonlyOn this page# Interface: IWatchedValueReadonly<T>[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).IWatchedValueReadonly

## Type parameters[​](#type-parameters)
Name`T`
## Hierarchy[​](#hierarchy)

[`IObservableValueReadOnly`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IObservableValueReadOnly)<`T`>

↳ `IWatchedValueReadonly`

↳↳ [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IWatchedValue)

## Methods[​](#methods)
### subscribe[​](#subscribe)
▸ subscribe(`callback`, `options?`): `void`

Subscribe to watched value changes

#### Parameters[​](#parameters)
NameTypeDescription`callback`(`value`: `T`) => `void`callback to be evoked when change occurs`options?`[`WatchedValueSubscribeOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.WatchedValueSubscribeOptions)watch subscriber options
#### Returns[​](#returns)
`void`

#### Overrides[​](#overrides)
[IObservableValueReadOnly](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IObservableValueReadOnly).[subscribe](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IObservableValueReadOnly#subscribe)

### unsubscribe[​](#unsubscribe)
▸ unsubscribe(`callback?`): `void`

Unsubscribe to watched value changes

#### Parameters[​](#parameters-1)
NameTypeDescription`callback?`(`value`: `T`) => `void`callback to remove
#### Returns[​](#returns-1)
`void`

#### Overrides[​](#overrides-1)
[IObservableValueReadOnly](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IObservableValueReadOnly).[unsubscribe](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IObservableValueReadOnly#unsubscribe)

### value[​](#value)
▸ value(): `T`

Value

#### Returns[​](#returns-2)
`T`

#### Inherited from[​](#inherited-from)
[IObservableValueReadOnly](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IObservableValueReadOnly).[value](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IObservableValueReadOnly#value)

### when[​](#when)
▸ when(`callback`): `void`

A simplified version of subscription, with promise-like interface, generally for using with boolean-valued watched values

#### Parameters[​](#parameters-2)
NameTypeDescription`callback`[`WatchedValueCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#watchedvaluecallback)<`T`>a function to be called when the value became `true`. `once` and `callWithLast` are implicitly set to true.
#### Returns[​](#returns-3)
`void`

- [Type parameters](#type-parameters)- [Hierarchy](#hierarchy)- [Methods](#methods)[subscribe](#subscribe)- [unsubscribe](#unsubscribe)- [value](#value)- [when](#when)