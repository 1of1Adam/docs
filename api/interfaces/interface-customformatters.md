---
title: "Interface: CustomFormatters | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CustomFormatters"
extracted_at: "2025-06-22T09:35:30.025Z"
---

- [](/charting-library-docs/)- Interfaces- CustomFormattersOn this page# Interface: CustomFormatters[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).CustomFormatters

Formatters used to adjust the displayed format of the date and time values.

## Properties[​](#properties)
### dateFormatter[​](#dateformatter)
• `Optional` dateFormatter: [`CustomFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CustomFormatter)

Used to format the date displayed over the timescale when hovering over a chart.
Note that by declaring this formatter all the default ones defined in Chart settings/Scales/Date format
will display the exact same outcome as the formatter.

### priceFormatterFactory[​](#priceformatterfactory)
• `Optional` priceFormatterFactory: [`SeriesFormatterFactory`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#seriesformatterfactory)

Used to format the number displayed in the price axis

### studyFormatterFactory[​](#studyformatterfactory)
• `Optional` studyFormatterFactory: [`CustomStudyFormatterFactory`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#customstudyformatterfactory)

Used to format the numbers displayed within a custom study.

### tickMarkFormatter[​](#tickmarkformatter)
• `Optional` tickMarkFormatter: (`date`: `Date`, `tickMarkType`: [`TickMarkType`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#tickmarktype)) => `string`

Used to format date displayed in the time axis
Remark: `tickMarkFormatter` must display the UTC date, and not the date corresponding to your local time zone.
#### Type declaration[​](#type-declaration)
▸ (`date`, `tickMarkType`): `string`

Parameters[​](#parameters)
NameType`date``Date``tickMarkType`[`TickMarkType`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#tickmarktype)
Returns[​](#returns)
`string`

### timeFormatter[​](#timeformatter)
• `Optional` timeFormatter: [`CustomFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CustomFormatter)

Used to format the time displayed in the bottom toolbar (time zone)

- [Properties](#properties)[dateFormatter](#dateformatter)- [priceFormatterFactory](#priceformatterfactory)- [studyFormatterFactory](#studyformatterfactory)- [tickMarkFormatter](#tickmarkformatter)- [timeFormatter](#timeformatter)