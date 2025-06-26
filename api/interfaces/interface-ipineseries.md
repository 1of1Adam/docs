---
title: "Interface: IPineSeries | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPineSeries"
extracted_at: "2025-06-22T09:39:23.758Z"
---

- [](/charting-library-docs/)- Interfaces- IPineSeriesOn this page# Interface: IPineSeries[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).IPineSeries

## Methods[​](#methods)
### adopt[​](#adopt)
▸ adopt(`source`, `destination`, `mode`): `number`

Map some values from one time scale to another.

#### Parameters[​](#parameters)
NameTypeDescription`source`[`IPineSeries`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPineSeries)Source times.`destination`[`IPineSeries`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPineSeries)Destination times.`mode``0` | `1`Adopt mode. `0` for continuous, `1` for precise. In continuous mode (`0`) every source time will be mapped to a destination time if one exists. Multiple source times may be mapped to the same destination time. In precise mode (`1`) every source time will be mapped to a destination time AT MOST ONCE if one exists. Some source times may not be mapped.
#### Returns[​](#returns)
`number`

`Example`

```
// A pine series with values [5, 5]const sourceTimes = ctx.new_var();// A pine series with values [4, 5]const destinationTimes = ctx.new_var();// A pine series with values [1, 2]const values = ctx.new_var();// Creates a pine series with values [2, 2]const adopted1 = values.adopt(sourceTimes, destinationTimes, 0);// Creates a pine series with values [NaN, 2]const adopted2 = values.adopt(sourceTimes, destinationTimes, 1);
```
`Example`

Pseudocode of the adopt algorithm:

```
adopt(sourceSeries, destinationSeries, mode) =  destinationValue = most recent value in destinationSeries  sourceIndex = index of destinationValue in sourceSeries  if mode equals 1 then    previousDestinationValue = second most recent value in destinationSeries    previousSourceIndex = index of previousDestinationValue in sourceSeries    if sourceIndex equals previousSourceIndex      return NaN  return value at sourceIndex
```

### get[​](#get)
▸ get(`n?`): `number`

Get the value at a specific index.

Note: The indices of a pine series is opposite.

Example:

- s.get(1) returns second last,
- s.get(2) - third last
- and so on

#### Parameters[​](#parameters-1)
NameTypeDescription`n?``number`index
#### Returns[​](#returns-1)
`number`

### indexOf[​](#indexof)
▸ indexOf(`time`): `number`

Get the index for the bar at the specified timestamp

#### Parameters[​](#parameters-2)
NameTypeDescription`time``number`timestamp
#### Returns[​](#returns-2)
`number`

### set[​](#set)
▸ set(`value`): `void`

Set the value for the pine series at the current index interation.

#### Parameters[​](#parameters-3)
NameTypeDescription`value``number`value to be set
#### Returns[​](#returns-3)
`void`

- [Methods](#methods)[adopt](#adopt)- [get](#get)- [indexOf](#indexof)- [set](#set)