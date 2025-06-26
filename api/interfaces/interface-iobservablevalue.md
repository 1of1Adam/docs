---
title: "Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IObservableValue"
extracted_at: "2025-06-22T09:54:45.109Z"
---

- [](/charting-library-docs/)- Interfaces- IObservableValueOn this page# Interface: IObservableValue<T>[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).IObservableValue

## Type parameters[​](#type-parameters)
Name`T`
## Hierarchy[​](#hierarchy)

[`IBoxedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBoxedValue)<`T`>

[`IObservable`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IObservable)<`T`>

↳ `IObservableValue`

↳↳ [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IWatchedValue)

## Methods[​](#methods)
### setValue[​](#setvalue)
▸ setValue(`value`): `void`

Set boxed value

#### Parameters[​](#parameters)
NameTypeDescription`value``T`value to be set
#### Returns[​](#returns)
`void`

#### Inherited from[​](#inherited-from)
[IBoxedValue](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBoxedValue).[setValue](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBoxedValue#setvalue)

### subscribe[​](#subscribe)
▸ subscribe(`callback`): `void`

Subscribe to changes

#### Parameters[​](#parameters-1)
NameTypeDescription`callback`[`ObservableCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#observablecallback)<`T`>callback function to be evoked when observed value changes
#### Returns[​](#returns-1)
`void`

#### Inherited from[​](#inherited-from-1)
[IObservable](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IObservable).[subscribe](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IObservable#subscribe)

### unsubscribe[​](#unsubscribe)
▸ unsubscribe(`callback`): `void`

Unsubscribe from changes

#### Parameters[​](#parameters-2)
NameTypeDescription`callback`[`ObservableCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#observablecallback)<`T`>callback function to be unsubscribed
#### Returns[​](#returns-2)
`void`

#### Inherited from[​](#inherited-from-2)
[IObservable](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IObservable).[unsubscribe](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IObservable#unsubscribe)

### value[​](#value)
▸ value(): `T`

Value

#### Returns[​](#returns-3)
`T`

#### Inherited from[​](#inherited-from-3)
[IBoxedValue](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBoxedValue).[value](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBoxedValue#value)

- [Type parameters](#type-parameters)- [Hierarchy](#hierarchy)- [Methods](#methods)[setValue](#setvalue)- [subscribe](#subscribe)- [unsubscribe](#unsubscribe)- [value](#value)