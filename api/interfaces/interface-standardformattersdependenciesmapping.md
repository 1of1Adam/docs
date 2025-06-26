---
title: "Interface: StandardFormattersDependenciesMapping | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.StandardFormattersDependenciesMapping"
extracted_at: "2025-06-22T09:56:17.102Z"
---

- [](/charting-library-docs/)- Interfaces- StandardFormattersDependenciesMappingOn this page# Interface: StandardFormattersDependenciesMapping[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).StandardFormattersDependenciesMapping

The interface that describes the mapping of values in the [AccountManagerColumnBase.formatter](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.AccountManagerColumnBase#formatter) and [AccountManagerColumnBase.dataFields](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.AccountManagerColumnBase#datafields) properties of the Account Manager columns.
Refer to the [Value formatters](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/value-formatters) section for more information.
## Properties[​](#properties)
### date[​](#date)
• date: [dateProperty: string]

### dateOrDateTime[​](#dateordatetime)
• dateOrDateTime: [dateProperty: string]

### default[​](#default)
• default: `string`[]

### empty[​](#empty)
• empty: []

### fixed[​](#fixed)
• fixed: [valueProperty: string]

### fixedInCurrency[​](#fixedincurrency)
• fixedInCurrency: [valueProperty: string, currencyProperty: string]

### formatPrice[​](#formatprice)
• formatPrice: [priceProperty: string]

### formatPriceForexSup[​](#formatpriceforexsup)
• formatPriceForexSup: [priceProperty: string]

### formatPriceInCurrency[​](#formatpriceincurrency)
• formatPriceInCurrency: [priceProperty: string, currencyProperty: string]

### formatQuantity[​](#formatquantity)
• formatQuantity: [qtyProperty: string]

### integerSeparated[​](#integerseparated)
• integerSeparated: [valueProperty: string]

### localDate[​](#localdate)
• localDate: [dateProperty: string]

### localDateOrDateTime[​](#localdateordatetime)
• localDateOrDateTime: [dateProperty: string]

### marginPercent[​](#marginpercent)
• marginPercent: [valueProperty: string]

### percentage[​](#percentage)
• percentage: [valueProperty: string]

### pips[​](#pips)
• pips: [pipsProperty: string]

### positionSide[​](#positionside)
• positionSide: [sideProperty: string]

### profit[​](#profit)
• profit: [profitProperty: string]

### profitInInstrumentCurrency[​](#profitininstrumentcurrency)
• profitInInstrumentCurrency: [profitProperty: string, currencyProperty: string]

### side[​](#side)
• side: [sideProperty: string]

### status[​](#status)
• status: [statusProperty: string]

### symbol[​](#symbol)
• symbol: [brokerSymbolProperty: string, symbolProperty: string] | [brokerSymbolProperty: string, symbolProperty: string, messageProperty: string]

### text[​](#text)
• text: `string`[]

### type[​](#type)
• type: [orderTypeProperty: string, parentIdProperty: string, stopTypeProperty: string]

### variablePrecision[​](#variableprecision)
• variablePrecision: [valueProperty: string]

- [Properties](#properties)[date](#date)- [dateOrDateTime](#dateordatetime)- [default](#default)- [empty](#empty)- [fixed](#fixed)- [fixedInCurrency](#fixedincurrency)- [formatPrice](#formatprice)- [formatPriceForexSup](#formatpriceforexsup)- [formatPriceInCurrency](#formatpriceincurrency)- [formatQuantity](#formatquantity)- [integerSeparated](#integerseparated)- [localDate](#localdate)- [localDateOrDateTime](#localdateordatetime)- [marginPercent](#marginpercent)- [percentage](#percentage)- [pips](#pips)- [positionSide](#positionside)- [profit](#profit)- [profitInInstrumentCurrency](#profitininstrumentcurrency)- [side](#side)- [status](#status)- [symbol](#symbol)- [text](#text)- [type](#type)- [variablePrecision](#variableprecision)