---
title: "Interface: Mark | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.Mark"
extracted_at: "2025-06-22T09:52:07.129Z"
---

- [](/charting-library-docs/)- Interfaces- MarkOn this page# Interface: Mark[Datafeed](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed).Mark

## Properties[​](#properties)
### borderWidth[​](#borderwidth)
• `Optional` borderWidth: `number`

Border Width

### color[​](#color)
• color: [`MarkConstColors`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Datafeed#markconstcolors) | [`MarkCustomColor`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Datafeed.MarkCustomColor)

Color for the mark

### hoveredBorderWidth[​](#hoveredborderwidth)
• `Optional` hoveredBorderWidth: `number`

Border Width when hovering over bar mark

### id[​](#id)
• id: `string` | `number`

ID of the mark

### imageUrl[​](#imageurl)
• `Optional` imageUrl: `string`

Optional URL for an image to be displayed within the timescale mark.

The image should ideally be square in dimension. You can use any image type which
the browser supports natively.
Examples:

- `https://yourserver.com/adobe.svg`
- `/images/myImage.png`
- `data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3...`
- `data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAASABIAAD/4...`

### label[​](#label)
• label: `string`

Label for the mark

### labelFontColor[​](#labelfontcolor)
• labelFontColor: `string`

Text color for the mark

### minSize[​](#minsize)
• minSize: `number`

Minimum size for the mark

### showLabelWhenImageLoaded[​](#showlabelwhenimageloaded)
• `Optional` showLabelWhenImageLoaded: `boolean`

Continue to show text label even when an image has
been loaded for the timescale mark.
Defaults to `false` if undefined.

### text[​](#text)
• text: `string`

Text content for the mark

### time[​](#time)
• time: `number`

Time for the mark.
Unix timestamp in seconds.- [Properties](#properties)[borderWidth](#borderwidth)- [color](#color)- [hoveredBorderWidth](#hoveredborderwidth)- [id](#id)- [imageUrl](#imageurl)- [label](#label)- [labelFontColor](#labelfontcolor)- [minSize](#minsize)- [showLabelWhenImageLoaded](#showlabelwhenimageloaded)- [text](#text)- [time](#time)