---
title: "Interface: IObservableValueReadOnly<T> | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IObservableValueReadOnly"
extracted_at: "2025-06-22T09:54:47.323Z"
---

- [](/charting-library-docs/)- Interfaces- IObservableValueReadOnlyOn this page# Interface: IObservableValueReadOnly<T>[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).IObservableValueReadOnly

## Type parameters[​](#type-parameters)
Name`T`
## Hierarchy[​](#hierarchy)

[`IBoxedValueReadOnly`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBoxedValueReadOnly)<`T`>

[`IObservable`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IObservable)<`T`>

↳ `IObservableValueReadOnly`

↳↳ [`IWatchedValueReadonly`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IWatchedValueReadonly)

## Methods[​](#methods)
### subscribe[​](#subscribe)
▸ subscribe(`callback`): `void`

Subscribe to changes

#### Parameters[​](#parameters)
NameTypeDescription`callback`[`ObservableCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#observablecallback)<`T`>callback function to be evoked when observed value changes
#### Returns[​](#returns)
`void`

#### Inherited from[​](#inherited-from)
[IObservable](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IObservable).[subscribe](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IObservable#subscribe)

### unsubscribe[​](#unsubscribe)
▸ unsubscribe(`callback`): `void`

Unsubscribe from changes

#### Parameters[​](#parameters-1)
NameTypeDescription`callback`[`ObservableCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#observablecallback)<`T`>callback function to be unsubscribed
#### Returns[​](#returns-1)
`void`

#### Inherited from[​](#inherited-from-1)
[IObservable](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IObservable).[unsubscribe](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IObservable#unsubscribe)

### value[​](#value)
▸ value(): `T`

Value

#### Returns[​](#returns-2)
`T`

#### Inherited from[​](#inherited-from-2)
[IBoxedValueReadOnly](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBoxedValueReadOnly).[value](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBoxedValueReadOnly#value)

- [Type parameters](#type-parameters)- [Hierarchy](#hierarchy)- [Methods](#methods)[subscribe](#subscribe)- [unsubscribe](#unsubscribe)- [value](#value)