---
title: "Interface: IBrokerConnectionAdapterFactory | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerConnectionAdapterFactory"
extracted_at: "2025-06-22T09:54:30.201Z"
---

- [](/charting-library-docs/)- Interfaces- IBrokerConnectionAdapterFactoryOn this page# Interface: IBrokerConnectionAdapterFactory[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).IBrokerConnectionAdapterFactory

## Methods[​](#methods)
### createDelegate[​](#createdelegate)
▸ createDelegate<`T`>(): [`IDelegate`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IDelegate)<`T`>

Creates a Delegate object

#### Type parameters[​](#type-parameters)
NameType`T`extends `Function`
#### Returns[​](#returns)
[`IDelegate`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IDelegate)<`T`>

### createPriceFormatter[​](#createpriceformatter)
▸ createPriceFormatter(`priceScale?`, `minMove?`, `fractional?`, `minMove2?`, `variableMinTick?`): [`IPriceFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IPriceFormatter)

Creates a price formatter.

#### Parameters[​](#parameters)
NameTypeDescription`priceScale?``number`Defines the number of decimal places. It is `10^number-of-decimal-places`. If a price is displayed as `1.01`, `pricescale` is `100`; If it is displayed as `1.005`, `pricescale` is `1000`.`minMove?``number`The amount of price precision steps for 1 tick. For example, since the tick size for U.S. equities is `0.01`, `minmov` is 1. But the price of the E-mini S&P futures contract moves upward or downward by `0.25` increments, so the `minmov` is `25`.`fractional?``boolean`For common prices, is `false` or it can be skipped. For more information on fractional prices, refer to [Fractional format](https://www.tradingview.com/charting-library-docs/latest/connecting_data/Symbology#fractional-format).`minMove2?``number`For common prices, is `0` or it can be skipped.`variableMinTick?``string`For common prices, is `string` (for example, `0.01 10 0.02 25 0.05`) or it can be skipped. For more information, refer to [Variable tick size](https://www.tradingview.com/charting-library-docs/latest/connecting_data/Symbology#variable-tick-size).
#### Returns[​](#returns-1)
[`IPriceFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IPriceFormatter)

### createWatchedValue[​](#createwatchedvalue)
▸ createWatchedValue<`T`>(`value?`): [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IWatchedValue)<`T`>

Creates a WatchedValue object

#### Type parameters[​](#type-parameters-1)
Name`T`
#### Parameters[​](#parameters-1)
NameType`value?``T`
#### Returns[​](#returns-2)
[`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IWatchedValue)<`T`>

- [Methods](#methods)[createDelegate](#createdelegate)- [createPriceFormatter](#createpriceformatter)- [createWatchedValue](#createwatchedvalue)