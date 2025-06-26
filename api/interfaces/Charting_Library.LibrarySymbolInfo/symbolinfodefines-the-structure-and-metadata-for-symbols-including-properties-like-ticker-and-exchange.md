---
title: "Interface: LibrarySymbolInfo | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LibrarySymbolInfo/"
extracted_at: "2025-06-22T09:30:00.689Z"
---

# Interface: LibrarySymbolInfo[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).LibrarySymbolInfo

## Hierarchy

**`LibrarySymbolInfo`**

↳ [`SymbolExt`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SymbolExt)

## Properties
### base_name
• `Optional` **base_name**: [`string`]

Array of base symbols
Example: for `AAPL*MSFT` it is `['NASDAQ:AAPL', 'NASDAQ:MSFT']`

### build_seconds_from_ticks
• `Optional` **build_seconds_from_ticks**: `boolean`

The boolean value showing whether or not seconds bars for this symbol can be built from ticks. Only available in Trading Platform.

- [LibrarySymbolInfo.has_seconds](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LibrarySymbolInfo#has_seconds) must also be `true`
- [LibrarySymbolInfo.has_ticks](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LibrarySymbolInfo#has_ticks) must also be `true`
- [LibrarySymbolInfo.seconds_multipliers](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LibrarySymbolInfo#seconds_multipliers) must be an empty array or only contain multipliers that the datafeed provides itself

The library builds resolutions from ticks only if there are no seconds resolutions from the datafeed or the provided resolutions are larger then the required one. For example, the datafeed provides `3S` resolution. In this case, the library can build only `1S` or `2S` resolutions from ticks. Resolutions such as `15S` will be build with seconds bars.

**`Default`**

```
false

```

### corrections
• `Optional` **corrections**: `string`

List of corrections for a symbol. The corrections are days when the trading session differs from the default one set in [LibrarySymbolInfo.session](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LibrarySymbolInfo#session).
The `corrections` value is a string in the following format: `SESSION:YYYYMMDD`.
For more information, refer to [corrections](https://www.tradingview.com/charting-library-docs/latest/connecting_data/Symbology#corrections).
The string below specifies corrections for two trading days:

- November 13, 2018. This trading day is split into two sessions. The first session starts at 19:00 four days before (November 9, 2018) and ends at 23:50 four days before. The second session starts at 10:00 and ends at 18:45.
- November 14, 2018. The session starts at 10:00 and ends at 14:00.

**`Example`**

```
"1900F4-2350F4,1000-1845:20181113;1000-1400:20181114"

```

### currency_code
• `Optional` **currency_code**: `string`

The currency in which the instrument is traded or some other currency if currency conversion is enabled.
It is displayed in the Security Info dialog and on the price axes.

### daily_multipliers
• `Optional` **daily_multipliers**: `string`

An array of daily resolutions that your datafeed supports. Items in the array should be listed in ascending order and **should not** include letters, for example: `["1", "2"]`.
This property is required to enable daily resolutions. Refer to the [Resolution](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Resolution#resolution-in-days) article for more information.
The library also uses resolutions listed in `daily_multipliers` to display higher resolution that your datafeed does not explicitly support. If `daily_multipliers` is not specified, the library cannot build additional resolutions.

**`Default`**

```
["1"]

```

### data_status
• `Optional` **data_status**: `"streaming"` | `"endofday"` | `"delayed_streaming"`

The status code of a series with this symbol.
For `delayed_streaming` and `endofday` type of data, the status is displayed as an icon and the *Data is delayed* section in the [*Legend*](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Legend#display-delayed-data-information), next to the market status icon.
Note that you should also enable the [`display_data_mode`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#display_data_mode) featureset.
When declaring `delayed_streaming` you also have to specify its [LibrarySymbolInfo.delay](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LibrarySymbolInfo#delay) in seconds.

### delay
• `Optional` **delay**: `number`

Type of delay that is associated to the data or real delay for real time data.

- `0` for realtime
- `-1` for endofday
- or delay in seconds (for delayed realtime)

### description
• **description**: `string`

The description of the symbol.
Will be displayed in the chart legend for this symbol.

### exchange
• **exchange**: `string`

Traded exchange (current (proxy) exchange).
The name will be displayed in the chart legend for this symbol.
**`Example`**

```
"NYSE"

```

### exchange_logo
• `Optional` **exchange_logo**: `string`

URL of image to be displayed as the logo for the exchange. The `show_exchange_logos` featureset needs to be enabled for this to be visible in the UI.

The image should ideally be square in dimension. You can use any image type which
the browser supports natively. Simple SVG images are recommended.
Examples:

- `https://yourserver.com/exchangeLogo.svg`
- `/images/myImage.png`
- `data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3...`
- `data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAASABIAAD/4...`

### expiration_date
• `Optional` **expiration_date**: `number`

Unix timestamp of the expiration date. One must set this value when `expired` = `true`.
The library will request data for this symbol starting from that time point.

### expired
• `Optional` **expired**: `boolean`

Boolean showing whether this symbol is expired futures contract or not.

**`Default`**

```
false

```

### format
• **format**: [`SeriesFormat`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#seriesformat)

Format of displaying labels on the price scale:

`price` - formats decimal or fractional numbers based on `minmov`, `pricescale`, `minmove2`, `fractional` and `variableMinTick` values. See [Price format](https://www.tradingview.com/charting-library-docs/latest/connecting_data/Symbology#price-format) for more details.
`volume` - formats decimal numbers in thousands, millions, billions or trillions

### fractional
• `Optional` **fractional**: `boolean`

For common prices this can be skipped.

Fractional prices are displayed 2 different forms: 1) `xx'yy` (for example, `133'21`) 2) `xx'yy'zz` (for example, `133'21'5`).

- `xx` is an integer part.
- `minmov/pricescale` is a Fraction.
- `minmove2` is used in form 2.
- `fractional` is `true`.
- `variableMinTick` is skipped.

Example:

If `minmov = 1`, `pricescale = 128` and `minmove2 = 4`:

- `119'16'0` represents `119 + 16/32`
- `119'16'2` represents `119 + 16.25/32`
- `119'16'5` represents `119 + 16.5/32`
- `119'16'7` represents `119 + 16.75/32`

More examples:

- `ZBM2014 (T-Bond)` with `1/32`: `minmov = 1`, `pricescale = 32`, `minmove2 = 0`
- `ZCM2014 (Corn)` with `2/8`: `minmov = 2`, `pricescale = 8`, `minmove2 = 0`
- `ZFM2014 (5 year t-note)` with `1/4 of 1/32`: `minmov = 1`, `pricescale = 128`, `minmove2 = 4`

### has_daily
• `Optional` **has_daily**: `boolean`

A flag indicating whether your datafeed contains daily data for this symbol.
If `true`, the library requests this data when a daily resolution is selected. If `false`, *No data here* is displayed on the chart.
`has_daily` is set to `true` by default. However, you should also specify [daily_multipliers](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LibrarySymbolInfo#daily_multipliers) to enable daily resolutions. Refer to the [Resolution](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Resolution#resolution-in-days) article for more information.

**`Default`**

```
true

```

### has_empty_bars
• `Optional` **has_empty_bars**: `boolean`

The boolean value showing whether the library should generate empty bars in the session when there is no data from the data feed for this particular time.

I.e., if your session is `0900-1600` and your data has gaps between `11:00` and `12:00` and your `has_empty_bars` is `true`, then the Library will fill the gaps with bars for this time.

Flag `has_empty_bars` = `true` cannot be used if featureset `disable_resolution_rebuild` is enabled.

**`Default`**

```
false

```

### has_intraday
• `Optional` **has_intraday**: `boolean`

A flag indicating whether your datafeed contains intraday (minutes) data for this symbol.
If `true`, the library requests this data when an intraday resolution is selected. If `false`, *No data here* is displayed on the chart.
This property is required to enable intraday resolutions. Refer to the [Resolution](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Resolution#resolution-in-minutes-intraday) article for more information.

**`Default`**

```
false

```

### has_seconds
• `Optional` **has_seconds**: `boolean`

A flag indicating whether your datafeed contains seconds data for this symbol.
If `true`, the library requests this data when a seconds resolution is selected. If `false`, *No data here* is displayed on the chart.
You should set `has_seconds` to `true` to enable seconds resolutions. Refer to the [Resolution](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Resolution#resolution-in-seconds) article for more information.

**`Default`**

```
false

```

### has_ticks
• `Optional` **has_ticks**: `boolean`

A flag indicating whether your datafeed contains ticks data for this symbol.
If `true`, the library requests this data when a resolution in ticks is selected. If `false`, *No data here* is displayed on the chart.
You should set `has_ticks` to `true` to enable ticks resolutions. Refer to the [Resolution](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Resolution#resolution-in-ticks) article for more information.

**`Default`**

```
false

```

### has_weekly_and_monthly
• `Optional` **has_weekly_and_monthly**: `boolean`

A flag indicating whether your datafeed contains weekly or monthly data for this symbol. If `true`, the library requests this data when the corresponding resolution is selected.
To enable weekly or monthly resolutions, you should also specify the [weekly_multipliers](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LibrarySymbolInfo#weekly_multipliers) or [monthly_multipliers](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LibrarySymbolInfo#monthly_multipliers) properties.
Refer to the [Resolution](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Resolution#resolution-in-weeks--months) article for more information.
If `has_weekly_and_monthly` is set to `false`, the library attempts to build the resolutions using daily bars. Note that building bars requires a large number of requests to your datafeed.
If the library fails to build bars, *No data here* is displayed on the chart.
**`Default`**

```
false

```

### industry
• `Optional` **industry**: `string`

Industry for stocks to be displayed in the Security Info.

### intraday_multipliers
• `Optional` **intraday_multipliers**: `string`

An array of intraday (minutes) resolutions that your datafeed supports. Items in the array should be listed in ascending order, for example: `["1", "2"]`.

This property is required to enable intraday resolutions. Refer to the [Resolution](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Resolution#resolution-in-minutes-intraday) article for more information.
Note that each resolution in `intraday_multipliers` should be handled in the [IDatafeedChartApi.getBars](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IDatafeedChartApi#getbars) implementation.
Consider the [example](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Resolution#example).
The library also uses resolutions listed in `intraday_multipliers` to display higher resolution that your datafeed does not explicitly support. If `intraday_multipliers` is not specified, the library cannot build additional resolutions.

Note that the library **cannot** build daily, weekly, or monthly resolutions using intraday data.

**`Default`**

```
 — specifies that the datafeed can provide data for any requested resolution.

```

### library_custom_fields
• `Optional` **library_custom_fields**: `Record`<`string`, `unknown`>

Additional metadata to include with the symbol information.
These parameters will not affect existing properties such as 'ticker' or 'name'
and will not be processed by the library. However, they can be accessed later
through the [IChartWidgetApi.symbolExt](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#symbolext) method, impacting existing
properties such as 'ticker' or 'name'.

### listed_exchange
• **listed_exchange**: `string`

short name of the exchange where this symbol is traded (real listed exchange).
The name will be displayed in the chart legend for this symbol.
**`Example`**

```
"NYSE"

```

### logo_urls
• `Optional` **logo_urls**: [`string`, `string`] | [`string`]

URL of image/s to be displayed as the logo/s for the symbol. The `show_symbol_logos` featureset needs to be enabled for this to be visible in the UI.

- If a single url is returned then that url will solely be used to display the symbol logo.
If two urls are provided then the images will be displayed as two partially overlapping
circles with the first url appearing on top. This is typically used for FOREX where you would
like to display two country flags are the symbol logo.

The image/s should ideally be square in dimension. You can use any image type which
the browser supports natively.
Examples:

- `https://yourserver.com/apple.svg`
- `/images/myImage.png`
- `data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3...`
- `data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAASABIAAD/4...`

### long_description
• `Optional` **long_description**: `string`

Symbol Long description

Optional long(er) description for the symbol.

### minmov
• **minmov**: `number`

The number of units that make up one tick.
For example, U.S. equities are quotes in decimals, and tick in decimals, and can go up +/- `.01`.
Therefore, the tick increment is 1 and `minmov = 1`. But the e-mini S&P futures contract, though quoted in decimals, goes up in `.25` increments, so the tick increment is 25 and `minmov = 25`.
Refer to [Price format](https://www.tradingview.com/charting-library-docs/latest/connecting_data/Symbology#price-format) for more information.

### minmove2
• `Optional` **minmove2**: `number`

This property is used to display prices in the [fraction of a fraction](https://www.tradingview.com/charting-library-docs/latest/connecting_data/Symbology#fraction-of-a-fraction-format) format.
For example, the ZBM2023 tick size is 1/4 of a 32nd. To display this security, set `minmov = 1`, `pricescale = 128`, `minmove2 = 4`.
For common prices, `minmove2` can be skipped or set to `0`.

### monthly_multipliers
• `Optional` **monthly_multipliers**: `string`

An array of monthly resolutions that your datafeed supports. Items in the array should be listed in ascending order and **should not** include letters, for example: `["1", "3", "6", "12"]`.
This property is required to enable monthly resolutions. Refer to the [Resolution](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Resolution#resolution-in-weeks--months) article for more information.
The library also uses resolutions listed in `monthly_multipliers` to display higher resolution that your datafeed does not explicitly support. If `monthly_multipliers` is not specified, the library cannot build additional resolutions.

**`Default`**

```
['1']

```

### name
• **name**: `string`

It is a symbol name within an exchange, such as `AAPL` or `9988` (Hong Kong).
Note that it should not contain the exchange name.
This symbol name is visible to users and can be repeated.
By default, `name` is used to resolve symbols in the [Datafeed API](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/).
If you use [LibrarySymbolInfo.ticker](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LibrarySymbolInfo#ticker), the library will use the ticker for Datafeed API requests.

### original_currency_code
• `Optional` **original_currency_code**: `string`

The currency in which the instrument is traded.

### original_unit_id
• `Optional` **original_unit_id**: `string`

A unique identifier of a unit in which the instrument is traded.

### price_source_id
• `Optional` **price_source_id**: `string`

Optional ID of a price source for a symbol. Should match one of the price sources from the [price_sources](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LibrarySymbolInfo#price_sources) array.

Note that you should set the [`symbol_info_price_source`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#symbol_info_price_source) featureset to `true` to display the symbol price source in the main series legend.

### price_sources
• `Optional` **price_sources**: [`SymbolInfoPriceSource`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SymbolInfoPriceSource)

Supported price sources for the symbol.
Price sources appear in the series legend and indicate the origin of values represented by symbol bars.
Example price sources: "Spot Price", "Ask", "Bid", etc.
The price source information is valuable when viewing non-OHLC series types.
Note that you should set the [`symbol_info_price_source`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#symbol_info_price_source) featureset to `true` to display the symbol price source in the main series legend.

**`Example`**

```
[{ id: '1', name: 'Spot Price' }, { id: '321', name: 'Bid' }]

```

### pricescale
• **pricescale**: `number`

A number of decimal places or fractions that the price has.

The `pricescale` value depends on the [price format](https://www.tradingview.com/charting-library-docs/latest/connecting_data/Symbology#price-format).
If you want to display the price in the decimal format, `pricescale` should be `10^n`, where `n` is the number of decimal places.
**Examples:** `1`, `10`, `10000000`.
If you want to display the price in the fractional format, `pricescale` should be `2^n`.
This value represents the number of fractions.
**Examples:** `8`, `16`, `256`.

### seconds_multipliers
• `Optional` **seconds_multipliers**: `string`

An array of seconds resolutions that your datafeed supports. Items in the array should be listed in ascending order and **should not** include letters, for example: `["1", "2"]`.
This property is required to enable seconds resolutions. Refer to the [Resolution](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Resolution#resolution-in-seconds) article for more information.
The library also uses resolutions listed in `seconds_multipliers` to display higher resolution that your datafeed does not explicitly support. If `seconds_multipliers` is not specified, the library cannot build additional resolutions.
Consider the example. You need to enable one-second and five-second resolutions but your datafeed contains only one-second data. In this case, you should set `seconds_multipliers` to `["1"]`.
The library will build the five-second resolution from one-second data.

### sector
• `Optional` **sector**: `string`

Sector for stocks to be displayed in the Security Info.

### session
• **session**: `string`

Trading hours for the symbol. The time should be in the **exchange** time zone specified in the [LibrarySymbolInfo.timezone](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LibrarySymbolInfo#timezone) property. Refer to the [Trading sessions](https://www.tradingview.com/charting-library-docs/latest/connecting_data/Trading-Sessions) article for more information.

**`Example`**

```
"1700-0200"

```

### session_display
• `Optional` **session_display**: `string`

The session value to display in the UI. If not specified, then `session` is used.

### session_holidays
• `Optional` **session_holidays**: `string`

A string that contains a list of non-trading holidays for the symbol.
Holiday dates should be in the `YYYYMMDD` format.
These dates are not displayed on the chart.
You can specify a correction for a holiday using [LibrarySymbolInfo.corrections](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LibrarySymbolInfo#corrections).

**`Example`**

```
"20181105,20181107,20181112"

```

### subsession_id
• `Optional` **subsession_id**: `string`

An ID of a subsession specified in [subsessions](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LibrarySymbolInfo#subsessions). The value must match the subsession that is currently displayed on the chart.
For more information, refer to the [Extended sessions](https://www.tradingview.com/charting-library-docs/latest/connecting_data/Symbology#extended-sessions) section.

### subsessions
• `Optional` **subsessions**: [`LibrarySubsessionInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LibrarySubsessionInfo)

An array of objects that contain information about certain subsessions within the extended session.
For more information, refer to the [Extended sessions](https://www.tradingview.com/charting-library-docs/latest/connecting_data/Symbology#extended-sessions) section.

### supported_resolutions
• `Optional` **supported_resolutions**: [`ResolutionString`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#resolutionstring)

An array of [resolutions](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Resolution) which should be enabled in the *Resolution* drop-down menu for this symbol.
Each item of the array is expected to be a string that has a specific [format](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Resolution#resolution-format).
If one changes the symbol and the new symbol does not support the selected resolution, an error message will be shown on the chart.

**Resolution availability logic (pseudocode):**

```
resolutionAvailable  =
    resolution.isIntraday
        ? symbol.has_intraday && symbol.supported_resolutions(resolution)
        : symbol.supported_resolutions(resolution);

```
If `supported_resolutions` is `` (empty array), all resolutions are disabled in the *Resolution* drop-down menu.

If `supported_resolutions` is `undefined`, all resolutions that the chart support ([DatafeedConfiguration.supported_resolutions](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.DatafeedConfiguration#supported_resolutions)) and custom resolutions are enabled.

Note that the list of available time frames depends on supported resolutions.
Time frames that require resolutions that are unavailable for a particular symbol will be hidden.
Refer to [Time frame toolbar](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Time-Scale#time-frame-toolbar) for more information.

### ticker
• `Optional` **ticker**: `string`

It is an unique identifier for a particular symbol in your [symbology](https://www.tradingview.com/charting-library-docs/latest/connecting_data/Symbology).
If you specify this property, its value will be used for all data requests for this symbol.
`ticker` will be treated the same as [LibrarySymbolInfo.name](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LibrarySymbolInfo#name) if not specified explicitly.
You should avoid using colons (":") in ticker values unless you are following the TradingView format: "NYSE:IBM". Using colons may cause unexpected behaviour and display bugs.

### timezone
• **timezone**: [`Timezone`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#timezone)

The time zone of the **exchange** where the symbol is listed. The time zone value should be in the OlsonDB format.
Refer to [Time zones](https://www.tradingview.com/charting-library-docs/latest/ui_elements/timezones) for a full list of supported time zones.

### type
• **type**: `string`

Type of the instrument.
Possible values: [SymbolType](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#symboltype)

### unit_conversion_types
• `Optional` **unit_conversion_types**: `string`

Allowed unit conversion group names.

### unit_id
• `Optional` **unit_id**: `string`

A unique identifier of a unit in which the instrument is traded or some other identifier if unit conversion is enabled.
It is displayed on the price axes.

### variable_tick_size
• `Optional` **variable_tick_size**: `string`

Dynamic minimum price movement. It is used if the instrument's minimum price movement changes depending on the price range.

For example, '0.01 10 0.02 25 0.05', where the tick size is 0.01 for a price less than 10, the tick size is 0.02 for a price less than 25, the tick size is 0.05 for a price greater than or equal to 25.

### visible_plots_set
• `Optional` **visible_plots_set**: [`VisiblePlotsSet`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#visibleplotsset)

Represents what values are supported by the symbol. Possible values:

- `ohlcv` — the symbol supports open, high, low, close prices and has volume.
- `ohlc` — the symbol supports open, high, low, close, prices but doesn't have volume.
- `c` — the symbol supports only close price. This makes the chart show the symbol data using only line-based styles.

**`Default`**

```
'ohlcv'

```

### volume_precision
• `Optional` **volume_precision**: `number`

Integer showing typical volume value decimal places for a particular symbol.
0 means volume is always an integer.
1 means that there might be 1 numeric character after the comma.
**`Default`**

```
'0'

```

### weekly_multipliers
• `Optional` **weekly_multipliers**: `string`

An array of weekly resolutions that your datafeed supports. Items in the array should be listed in ascending order and **should not** include letters, for example: `["1", "3"]`.
This property is required to enable weekly resolutions. Refer to the [Resolution](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Resolution#resolution-in-weeks--months) article for more information.
The library also uses resolutions listed in `weekly_multipliers` to display higher resolution that your datafeed does not explicitly support. If `weekly_multipliers` is not specified, the library cannot build additional resolutions.

**`Default`**

```
['1']

```