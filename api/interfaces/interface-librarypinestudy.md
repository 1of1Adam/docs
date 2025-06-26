---
title: "Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LibraryPineStudy"
extracted_at: "2025-06-22T09:40:42.828Z"
---

- [](/charting-library-docs/)- Interfaces- LibraryPineStudyOn this page# Interface: LibraryPineStudy<TPineStudyResult>[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).LibraryPineStudy

## Type parameters[​](#type-parameters)
Name`TPineStudyResult`
## Indexable[​](#indexable)
▪ [key: `string`]: `any`

## Methods[​](#methods)
### init[​](#init)
▸ init(`ctx`, `inputs`): `void`

The method is designed to get additional information for an indicator and allows you to initialize variables needed for your data calculations.
For example, you can reset a counter with this method. The library calls `init` when the indicator should be calculated from scratch.
For more information, refer to the [Constructor](https://www.tradingview.com/charting-library-docs/latest/custom_studies/custom-indicator-constructor#init) article.
Example:

```
this.init = function(context, inputCallback) {    var symbol = '#EQUITY';    var period = PineJS.Std.period(this._context);    context.new_sym(symbol, period);};
```
#### Parameters[​](#parameters)
NameTypeDescription`ctx`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)An object containing symbol info along with some useful methods to load/store symbol`inputs`<T>(`index`: `number`) => `T`The inputs callback is an array of input values, placed in order of inputs in Metainfo.
#### Returns[​](#returns)
`void`

### main[​](#main)
▸ main(`ctx`, `inputs`): `TPineStudyResult`

Called every time the library wants to calculate the study. Also it's called for every bar of every symbol.
Thus, if you request several additional symbols inside your indicator it will increase the count of runs.
#### Parameters[​](#parameters-1)
NameTypeDescription`ctx`[`IContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IContext)An object containing symbol info along with some useful methods to load/store symbol`inputs`<T>(`index`: `number`) => `T`The inputs callback is an array of input values, placed in order of inputs in Metainfo.
#### Returns[​](#returns-1)
`TPineStudyResult`

- [Type parameters](#type-parameters)- [Indexable](#indexable)- [Methods](#methods)[init](#init)- [main](#main)