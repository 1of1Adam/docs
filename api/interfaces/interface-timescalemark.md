---
title: "Interface: TimescaleMark | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.TimescaleMark"
extracted_at: "2025-06-22T09:52:23.277Z"
---

- [](/charting-library-docs/)- Interfaces- TimescaleMarkOn this page# Interface: TimescaleMark[Datafeed](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed).TimescaleMark

## Properties[​](#properties)
### color[​](#color)
• color: `string`

Color for the timescale mark

### id[​](#id)
• id: `string` | `number`

ID of the timescale mark

### imageUrl[​](#imageurl)
• `Optional` imageUrl: `string`

Optional URL for an image to be displayed within the timescale mark.

The image should ideally be square in dimension. You can use any image type which
the browser supports natively.
Examples:

- `https://s3-symbol-logo.tradingview.com/crypto/XTVCBTC.svg`
- `/images/myImage.png`
- `data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3...`
- `data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAASABIAAD/4...`

### label[​](#label)
• label: `string`

Label for the timescale mark

### labelFontColor[​](#labelfontcolor)
• `Optional` labelFontColor: `string`

Color for the timescale mark text label.
If undefined then the value provided for `color` will be used.

### shape[​](#shape)
• `Optional` shape: [`TimeScaleMarkShape`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed#timescalemarkshape)

Shape of the timescale mark

### showLabelWhenImageLoaded[​](#showlabelwhenimageloaded)
• `Optional` showLabelWhenImageLoaded: `boolean`

Continue to show text label even when an image has
been loaded for the timescale mark.
Defaults to `false` if undefined.

### time[​](#time)
• time: `number`

Time for the mark.
Unix timestamp in seconds.

### tooltip[​](#tooltip)
• tooltip: `string`[]

Tooltip content

- [Properties](#properties)[color](#color)- [id](#id)- [imageUrl](#imageurl)- [label](#label)- [labelFontColor](#labelfontcolor)- [shape](#shape)- [showLabelWhenImageLoaded](#showlabelwhenimageloaded)- [time](#time)- [tooltip](#tooltip)