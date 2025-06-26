---
title: "Interface: TimeFrameItem | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.TimeFrameItem"
extracted_at: "2025-06-22T09:48:54.522Z"
---

- [](/charting-library-docs/)- Interfaces- TimeFrameItemOn this page# Interface: TimeFrameItem[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).TimeFrameItem

Definition of visible time frames that can be selected at the bottom of the chart

`Example`

```
{ text: "3y", resolution: "1W", description: "3 Years", title: "3yr" }
```
## Properties[​](#properties)
### description[​](#description)
• `Optional` description: `string`

Optional text displayed in the pop-up menu. If not set, `title` wil be used instead.

### resolution[​](#resolution)
• resolution: [`ResolutionString`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#resolutionstring)

Resolution to be set

### text[​](#text)
• text: `string`

Defines the range to be set for the given resolution. It has the `<integer><y|m|d>` ( \d+(y|m|d) as Regex ) format.

### title[​](#title)
• `Optional` title: `string`

Optional text representing the time frame. If not set a generated string will be set based on `text` property.

- [Properties](#properties)[description](#description)- [resolution](#resolution)- [text](#text)- [title](#title)