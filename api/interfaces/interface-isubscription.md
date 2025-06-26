---
title: "Interface: ISubscription<TFunc> | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.ISubscription"
extracted_at: "2025-06-22T09:54:51.250Z"
---

- [](/charting-library-docs/)- Interfaces- ISubscriptionOn this page# Interface: ISubscription<TFunc>[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).ISubscription

A subscription. Used to subscribe callbacks to events.

## Type parameters[​](#type-parameters)
NameType`TFunc`extends `Function`
## Hierarchy[​](#hierarchy)

`ISubscription`

↳ [`IDelegate`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IDelegate)

## Methods[​](#methods)
### subscribe[​](#subscribe)
▸ subscribe(`obj`, `member`, `singleshot?`): `void`

Subscribe a callback function to this event. Subscribed callbacks are called when the event fires.

#### Parameters[​](#parameters)
NameTypeDescription`obj``object`Object used as the `this` value bound to the callback function.`member``TFunc`Function called when the event is fired.`singleshot?``boolean``true` if the subscription should be automatically removed after the first time it is fired.
#### Returns[​](#returns)
`void`

`Example`

```
// Log 'Series data loaded!' to the console the next time the data loaded event fires and then unsubscribe automatically.seriesApi.onDataLoaded().subscribe(null, () => { console.log('Series data loaded!'); }, true);
```
Subscribe to an event within a class. Manually unsubscribe when some condition is true.

```
class Example {  constructor(seriesApi) {    this._seriesApi = seriesApi;    this._seriesApi.onDataLoaded().subscribe(this, this._onDataLoaded);  }  _onDataLoaded() {    // Do something in response to the event.    if (someUnsubscribeCondition) {      this._seriesApi.onDataLoaded().unsubscribe(this, this._onDataLoaded);    }  }}
```

### unsubscribe[​](#unsubscribe)
▸ unsubscribe(`obj`, `member`): `void`

Unsubscribe a previously subscribed callback function.
It is important that the `obj` and `member` arguments are the same as the ones passed when the callback was subscribed.
#### Parameters[​](#parameters-1)
NameTypeDescription`obj``object`Object passed as the `this` value when the callback was subscribed.`member``TFunc`Function subscribed to the event.
#### Returns[​](#returns-1)
`void`

### unsubscribeAll[​](#unsubscribeall)
▸ unsubscribeAll(`obj`): `void`

Unsubscribe all callbacks that were subscribed with the same `obj` value.

#### Parameters[​](#parameters-2)
NameTypeDescription`obj``object``obj` value passed when the callbacks were subscribed.
#### Returns[​](#returns-2)
`void`

`Example`

```
// Unsubscribe all three callback functions at once in the `destroy` method.class Example {  constructor(seriesApi) {    this._seriesApi = seriesApi;    this._seriesApi.onDataLoaded().subscribe(this, this._callback1);    this._seriesApi.onDataLoaded().subscribe(this, this._callback2);    this._seriesApi.onDataLoaded().subscribe(this, this._callback3);  }  destroy() {    this._seriesapi.onDataLoaded().unsubscribeAll(this);  }  _callback1() { ... }  _callback2() { ... }  _callback3() { ... }}
```- [Type parameters](#type-parameters)- [Hierarchy](#hierarchy)- [Methods](#methods)[subscribe](#subscribe)- [unsubscribe](#unsubscribe)- [unsubscribeAll](#unsubscribeall)