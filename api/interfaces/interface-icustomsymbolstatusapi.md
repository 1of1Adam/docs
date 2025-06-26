---
title: "Interface: ICustomSymbolStatusApi | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ICustomSymbolStatusApi"
extracted_at: "2025-06-22T09:38:43.463Z"
---

- [](/charting-library-docs/)- Interfaces- ICustomSymbolStatusApiOn this page# Interface: ICustomSymbolStatusApi[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).ICustomSymbolStatusApi

The custom symbol status API provides the ability to create (and adjust)
additional status items to be displayed within the symbol status section
of the main series legend. This section is typically used to show the
market status (such as open or closed) but can additionally be used to
display warnings related to the current symbol.
This API allows custom status items to be added (which are tied to a
specific symbol). You can customise the icon, color, tooltip, and content
within the dropdown tooltip menu displayed when the user clicks on the
icon.
Example

```
widget .customSymbolStatus() .symbol('NASDAQNM:AAPL') // select the symbol .setVisible(true) // make the status visible .setColor('rgb(255, 40, 60)') // set the colour .setIcon(myCustomIconSvgString) // string for an svg icon, i.e. '<svg> ... </svg>' .setTooltip('Tooltip') // text to be displayed within the hover tooltip .setDropDownContent([ // content to be displayed within the large pop-up tooltip   {     title: 'Title', // title to be displayed within the pop-up     color: 'rgb(255, 60, 70)', // optional, if you want it to be different to above     content: [       'Explanation of status',       '<br/><br/>',       'More details...',     ],     action: { // Optional action to be displayed       text: 'Read more here',       tooltip: 'opens in a new window',       onClick: () => {         window.open('https://www.tradingview.com/', '_blank');       },     },   },]);
```
## Methods[​](#methods)
### hideAll[​](#hideall)
▸ hideAll(): `void`

Hide all the custom status items. This is equivalent to using
`setVisible(false)` on all of the current custom symbol status items.
#### Returns[​](#returns)
`void`

### symbol[​](#symbol)
▸ symbol(`symbolId`): [`ICustomSymbolStatusAdapter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ICustomSymbolStatusAdapter)

Get the custom symbol status adapter for a specific symbolId. The
symbolId should exactly match the resolved symbolId. This id can
be retrieved for a chart via the [IChartWidgetApi.symbol](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#symbol) method.
#### Parameters[​](#parameters)
NameTypeDescription`symbolId``string`symbol id for which you would like to create / adjust the custom status
#### Returns[​](#returns-1)
[`ICustomSymbolStatusAdapter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ICustomSymbolStatusAdapter)

- [Methods](#methods)[hideAll](#hideall)- [symbol](#symbol)