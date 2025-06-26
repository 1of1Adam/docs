---
title: "Interface: Favorites<TChartTypeFavorites> | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.Favorites"
extracted_at: "2025-06-22T09:37:02.459Z"
---

- [](/charting-library-docs/)- Interfaces- FavoritesOn this page# Interface: Favorites<TChartTypeFavorites>[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).Favorites

Favorites which can be defined within the Widget Constructor options (see [ChartingLibraryWidgetOptions.favorites](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#favorites)).

## Type parameters[​](#type-parameters)
Name`TChartTypeFavorites`
## Properties[​](#properties)
### chartTypes[​](#charttypes)
• `Optional` chartTypes: `TChartTypeFavorites`[]

An array of chart types that are marked as favorite.
The names of chart types are listed within the [ChartTypeFavorites](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#charttypefavorites) or [TradingTerminalChartTypeFavorites](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#tradingterminalcharttypefavorites) type.
Example: `["Area", "Candles"]`.

### drawingTools[​](#drawingtools)
• `Optional` drawingTools: [`DrawingToolIdentifier`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#drawingtoolidentifier)[]

An array of drawing tool identifiers that should be marked as favorite. These will only
be applied if there aren't existing favorites.
Example: ['LineToolBrush', 'LineToolCallout', 'LineToolCircle']

### indicators[​](#indicators)
• `Optional` indicators: `string`[]

An array of indicator titles that are marked as favorite.
The names of indicators are identical to the `title` property of the indicator. For built-in indicators
this will match the chart UI in the English version.
Example: `["Awesome Oscillator", "Bollinger Bands"]`.

### intervals[​](#intervals)
• `Optional` intervals: [`ResolutionString`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#resolutionstring)[]

An array of time intervals that are marked as favorite.

Example: `["D", "2D"]`

- [Type parameters](#type-parameters)- [Properties](#properties)[chartTypes](#charttypes)- [drawingTools](#drawingtools)- [indicators](#indicators)- [intervals](#intervals)