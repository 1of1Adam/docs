---
title: "Interface: ExportDataOptions | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ExportDataOptions"
extracted_at: "2025-06-22T09:36:58.273Z"
---

- [](/charting-library-docs/)- Interfaces- ExportDataOptionsOn this page# Interface: ExportDataOptions[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).ExportDataOptions

## Properties[​](#properties)
### from[​](#from)
• `Optional` from: `number`

Optional timestamp of the first exported bar.

### includeDisplayedValues[​](#includedisplayedvalues)
• `Optional` includeDisplayedValues: `boolean`

If true then the exported data will include formatted value as displayed to the user.

`Default`

```
false
```

### includeOHLCValuesForSingleValuePlots[​](#includeohlcvaluesforsinglevalueplots)
• `Optional` includeOHLCValuesForSingleValuePlots: `boolean`

Include open, high, low, and close values for plots that only display a single value on the chart. For example line series or symbols with visible_plot_set = 'c'.

### includeOffsetStudyValues[​](#includeoffsetstudyvalues)
• `Optional` includeOffsetStudyValues: `boolean`

Include study data that has a positive offset from the main series data. That is study data that is "to the right of" the last main series data point.

### includeSeries[​](#includeseries)
• `Optional` includeSeries: `boolean`

If true then the exported data will include open, high, low, close values from the main series.

`Default`

```
true
```

### includeTime[​](#includetime)
• `Optional` includeTime: `boolean`

If true then each exported data item will include a time value.

`Default`

```
true
```

### includeUserTime[​](#includeusertime)
• `Optional` includeUserTime: `boolean`

If true then each exported data item will include a user time value.
User time is the time that user sees on the chart.
This time depends on the selected time zone and resolution.
`Default`

```
false
```

### includedStudies[​](#includedstudies)
• includedStudies: readonly `string`[] | `"all"`

If true then each exported data item will include a value for the specified studies.

### to[​](#to)
• `Optional` to: `number`

Optional timestamp of the last exported bar.

- [Properties](#properties)[from](#from)- [includeDisplayedValues](#includedisplayedvalues)- [includeOHLCValuesForSingleValuePlots](#includeohlcvaluesforsinglevalueplots)- [includeOffsetStudyValues](#includeoffsetstudyvalues)- [includeSeries](#includeseries)- [includeTime](#includetime)- [includeUserTime](#includeusertime)- [includedStudies](#includedstudies)- [to](#to)