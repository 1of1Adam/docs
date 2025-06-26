---
title: "Interface: CrossHairMovedEventParams | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CrossHairMovedEventParams"
extracted_at: "2025-06-22T09:35:05.969Z"
---

- [](/charting-library-docs/)- Interfaces- CrossHairMovedEventParamsOn this page# Interface: CrossHairMovedEventParams[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).CrossHairMovedEventParams

Crosshair move event information.

## Properties[​](#properties)
### entityValues[​](#entityvalues)
• `Optional` entityValues: `Record`<[`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid), [`CrossHairMovedEventSource`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CrossHairMovedEventSource)>

Series and study values at the crosshair position. The object keys are study or series IDs, and the object value are study or series values.
The ID for the main series will always be the string `'_seriesId'`.

### offsetX[​](#offsetx)
• `Optional` offsetX: `number`

X coordinate of the crosshair relative to the left edge of the element containing the library.

### offsetY[​](#offsety)
• `Optional` offsetY: `number`

Y coordinate of the crosshair relative to the top edge of the element containing the library.

### price[​](#price)
• price: `number`

The price coordinate of the crosshair.

### time[​](#time)
• time: `number`

The crosshair time coordinate represented with a UNIX timestamp in UTC.
You can use this property to do some calculations or retrieve additional data from the datafeed.

### userTime[​](#usertime)
• `Optional` userTime: `number`

The crosshair time coordinate represented with a UNIX timestamp in the selected time zone.
You can use this property to display the crosshair time value in the UI, for example, in a tooltip or data window.- [Properties](#properties)[entityValues](#entityvalues)- [offsetX](#offsetx)- [offsetY](#offsety)- [price](#price)- [time](#time)- [userTime](#usertime)