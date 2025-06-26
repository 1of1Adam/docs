---
title: "Interface: IContext | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext"
extracted_at: "2025-06-22T09:38:36.213Z"
---

- [](/charting-library-docs/)- Interfaces- IContextOn this page# Interface: IContext[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).IContext

PineJS execution context.

## Properties[​](#properties)
### symbol[​](#symbol)
• symbol: [`ISymbolInstrument`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISymbolInstrument)

Symbol Instrument

## Methods[​](#methods)
### is_main_symbol[​](#is_main_symbol)
▸ is_main_symbol(`symbol`): `boolean`

Checks if symbol is the main symbol

#### Parameters[​](#parameters)
NameTypeDescription`symbol`[`ISymbolInstrument`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISymbolInstrument)symbol to check
#### Returns[​](#returns)
`boolean`

`true` if symbol is the main symbol

### new_ctx[​](#new_ctx)
▸ new_ctx(): [`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)

Creates a new context

#### Returns[​](#returns-1)
[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)

### new_sym[​](#new_sym)
▸ new_sym(`tickerid`, `period`, `currencyCode?`, `unitId?`, `subsessionId?`): [`ISymbolInstrument`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISymbolInstrument)

Load a new symbol for the custom indicator

#### Parameters[​](#parameters-1)
NameTypeDescription`tickerid``string`Symbol identifier`period``string`period for the new symbol`currencyCode?``string`Currency code`unitId?``string`Unit ID`subsessionId?``string`Subsession ID
#### Returns[​](#returns-2)
[`ISymbolInstrument`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISymbolInstrument)

### new_unlimited_var[​](#new_unlimited_var)
▸ new_unlimited_var(`value?`): [`IPineSeries`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPineSeries)

Creates an in-memory temporary storage with unlimited depth.

#### Parameters[​](#parameters-2)
NameTypeDescription`value?``number`variable's value
#### Returns[​](#returns-3)
[`IPineSeries`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPineSeries)

### new_var[​](#new_var)
▸ new_var(`value?`): [`IPineSeries`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPineSeries)

Creates an in-memory temporary storage with depth defined by the first call `new_var(value).get(n)`

#### Parameters[​](#parameters-3)
NameTypeDescription`value?``number`variable's value
#### Returns[​](#returns-4)
[`IPineSeries`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPineSeries)

### select_sym[​](#select_sym)
▸ select_sym(`i`): `void`

Switch context to the other symbol received through [IContext.new_sym](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext#new_sym)

#### Parameters[​](#parameters-4)
NameTypeDescription`i``number`the index of the symbol (`0` for the main series)
#### Returns[​](#returns-5)
`void`

### setMinimumAdditionalDepth[​](#setminimumadditionaldepth)
▸ setMinimumAdditionalDepth(`value`): `void`

Allows the minimum depth to be forced.

#### Parameters[​](#parameters-5)
NameTypeDescription`value``number`minimum depth to set
#### Returns[​](#returns-6)
`void`

- [Properties](#properties)[symbol](#symbol)- [Methods](#methods)[is_main_symbol](#is_main_symbol)- [new_ctx](#new_ctx)- [new_sym](#new_sym)- [new_unlimited_var](#new_unlimited_var)- [new_var](#new_var)- [select_sym](#select_sym)- [setMinimumAdditionalDepth](#setminimumadditionaldepth)