---
title: "Interface: IChartingLibraryWidget | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget/"
extracted_at: "2025-06-22T09:29:53.882Z"
---

# Interface: IChartingLibraryWidget[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).IChartingLibraryWidget

The main interface for interacting with the library, returned by [ChartingLibraryWidgetConstructor](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetConstructor).
For more information, refer to the [Widget methods](https://www.tradingview.com/charting-library-docs/latest/core_concepts/widget-methods) article.
## Methods
### activeChart
▸ **activeChart**(): [`IChartWidgetApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi)

Get an API object for interacting with the active chart.
For example, you can subscribe to events on the active chart, such as [IChartWidgetApi.onIntervalChanged](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#onintervalchanged).
Note that the library does not manage the event subscriptions when users switch between the charts on the [multiple-chart layout](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/#multiple-chart-layout).
If necessary, you should manually unsubscribe from the previous chart and subscribe to the newly selected one.
To track the currently active chart, use the [SubscribeEventsMap.activeChartChanged](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SubscribeEventsMap#activechartchanged) event.
#### Returns
[`IChartWidgetApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi)

An API object for interacting with the chart.

### activeChartIndex
▸ **activeChartIndex**(): `number`

Get the index of the active chart in the layout.

#### Returns
`number`

number.

### addCustomCSSFile
▸ **addCustomCSSFile**(`url`): `void`

Add a custom CSS file for the library to load.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `url` | `string` | A url to the custom CSS file. Should be absolute or relative to the `static` folder. ||

#### Returns
`void`

### applyOverrides
▸ **applyOverrides**<`TOverrides`>(`overrides`): `void`

Apply overrides to the chart without reloading. See also [ChartingLibraryWidgetOptions.overrides](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#overrides).

#### Type parameters

 **|Name** | **Type** ||
| `TOverrides` | extends `Partial`<[`ChartPropertiesOverrides`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides)> ||

#### Parameters

 **|Name** | **Type** | **Description** ||
| `overrides` | `TOverrides` | An object of overrides to apply to the chart. ||

#### Returns
`void`

### applyStudiesOverrides
▸ **applyStudiesOverrides**(`overrides`): `void`

Apply overrides to indicator styles and inputs without reloading.
Refer to [Indicator Overrides](https://www.tradingview.com/charting-library-docs/latest/customization/overrides/indicator-overrides#change-default-properties-on-the-fly) for more information.
Overrides for built-in indicators are listed in [StudyOverrides](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyOverrides).
#### Parameters

 **|Name** | **Type** | **Description** ||
| `overrides` | `object` | An object of overrides to apply to the studies. ||

#### Returns
`void`

### changeTheme
▸ **changeTheme**(`themeName`, `options?`): `Promise`<`void`>

Change the theme of the chart.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `themeName` | [`ThemeName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#themename) | A theme name. ||
| `options?` | [`ChangeThemeOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChangeThemeOptions) | An optional object of options for the theme. ||

#### Returns
`Promise`<`void`>

A promise that resolves when the theme has been changed.

### chart
▸ **chart**(`index?`): [`IChartWidgetApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi)

Get an API instance that can be used to interact with a chart.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `index?` | `number` | Zero based index of the chart. ||

#### Returns
[`IChartWidgetApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi)

An API instance.

### chartsCount
▸ **chartsCount**(): `number`

Get the number of charts in the current layout.

#### Returns
`number`

A count of the charts in the current layout.

### clearUndoHistory
▸ **clearUndoHistory**(): `void`

Clears the undo & redo history.

**Warning:** this should only be used in very specific cases where you have considered
the UX implications. It is generally unexpected for the user that the undo
history has been cleared.
An example of an acceptable use-case would be reusing a chart when switching
pages / tabs on a Single Page Application, and presenting it to the user as a
new chart.
#### Returns
`void`

### closePopupsAndDialogs
▸ **closePopupsAndDialogs**(): `void`

Close all open context menus, pop-ups or dialogs.

#### Returns
`void`

### createButton
▸ **createButton**(`options?`): `HTMLElement`

Create a button in the top toolbar. This should be called after [headerReady](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#headerready) has resolved.

**Example**

```
widget.headerReady().then(function() {
    var button = widget.createButton();
    button.setAttribute('title', 'My custom button tooltip');
    button.addEventListener('click', function() { alert("My custom button pressed!"); });
    button.textContent = 'My custom button caption';
});

```
#### Parameters

 **|Name** | **Type** | **Description** ||
| `options?` | [`CreateHTMLButtonOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateHTMLButtonOptions) | A optional object of options for the button. ||

#### Returns
`HTMLElement`

A `HTMLElement` you can customize.

▸ **createButton**(`options`): `string`

Create a button in the top toolbar. This should be called after [headerReady](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#headerready) has resolved.
If the `title` option is provided then the title text will be shown in a tooltip on hover.
If the `onClick` option is provided then the button will be clickable.
#### Parameters

 **|Name** | **Type** | **Description** ||
| `options` | [`CreateTradingViewStyledButtonOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateTradingViewStyledButtonOptions) | A object of options for the button. ||

#### Returns
`string`

A `string` button id

▸ **createButton**(`options?`): `string` | `HTMLElement`

Create a button in the top toolbar. This should be called after [headerReady](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#headerready) has resolved.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `options?` | [`CreateButtonOptions`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#createbuttonoptions) | A optional object of options for the button. ||

#### Returns
`string` | `HTMLElement`

A `HTMLElement` if the `useTradingViewStyle` option is `false` or undefined. `string`(button id) if `useTradingViewStyle` is `true`.

### createDropdown
▸ **createDropdown**(`params`): `Promise`<[`IDropdownApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IDropdownApi)>

Add a custom dropdown menu to the top toolbar.

**Example**

```
widget.createDropdown(
    {
        title: 'dropdown',
        tooltip: 'tooltip for this dropdown',
        items: [
            {
                title: 'item#1',
                onSelect: () => {console.log('1');},
            },
            {
                title: 'item#2',
                onSelect: () => {widget.setSymbol('IBM', '1D');},
            },
            {
                title: 'item#3',
                onSelect: () => {
                    widget.activeChart().createStudy(
                        'MACD',
                        false,
                        false,
                        {
                            in_0: 14,
                            in_1: 30,
                            in_3: 'close',
                            in_2: 9
                        }
                    );
                },
            }
        ],
        icon: `<svg xmlns="http://www.w3.org/2000/svg" width="28" height="28"><g fill="none" stroke="currentColor"><circle cx="10" cy="10" r="2.5"/><circle cx="18" cy="18" r="2.5"/><path stroke-linecap="square" d="M17.5 7.5l-7 13"/></g></svg>`,
    }
).then(myDropdownApi => {
    // Use myDropdownApi if you need to update the dropdown:
    // myDropdownApi.applyOptions({
    //     title: 'a new title!'
    // });

    // Or remove the dropdown:
    // myDropdownApi.remove();
});

```
#### Parameters

 **|Name** | **Type** ||
| `params` | [`DropdownParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.DropdownParams) ||

#### Returns
`Promise`<[`IDropdownApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IDropdownApi)>

### crosshairSync
▸ **crosshairSync**(): [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

Only available in Trading Platform. Get a watched value that can be used to read/write/subscribe to the state of the crosshair sync between charts.

**Example**

```
widget.crosshairSync().setValue(true);

```
#### Returns
[`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

A watched value of the state of the crosshair sync.

### currencyAndUnitVisibility
▸ **currencyAndUnitVisibility**(): [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<[`VisibilityType`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.VisibilityType)>

Get a watched value that can be used to read/write/subscribe to the state of the currency and unit
visibility setting on the price scale.
#### Returns
[`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<[`VisibilityType`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.VisibilityType)>

A watched value of the state of the currency and unit visibility option.

### customSymbolStatus
▸ **customSymbolStatus**(): [`ICustomSymbolStatusApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ICustomSymbolStatusApi)

Get an API object for creating, and adjusting, custom status items to
be displayed within the legend for the main series of each chart.
This can only be accessed when the chart has been created. ([headerReady](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#headerready))

#### Returns
[`ICustomSymbolStatusApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ICustomSymbolStatusApi)

An API object for controlling additional custom status items within the legend area.

### customThemes
▸ **customThemes**(): `Promise`<[`ICustomThemesApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ICustomThemesApi)>

Get a promise that resolves with an API object for interacting with the custom themes. For more information on custom themes, refer to the [Custom themes API](https://www.tradingview.com/charting-library-docs/latest/customization/styles/custom-themes) article.

#### Returns
`Promise`<[`ICustomThemesApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ICustomThemesApi)>

An API object for interacting with the custom themes.

### dateFormat
▸ **dateFormat**(): [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`"qq 'yy"` | `"qq yyyy"` | `"dd MMM 'yy"` | `"MMM 'yy"` | `"MMM dd, yyyy"` | `"MMM yyyy"` | `"MMM dd"` | `"dd MMM"` | `"yyyy-MM-dd"` | `"yy-MM-dd"` | `"yy/MM/dd"` | `"yyyy/MM/dd"` | `"dd-MM-yyyy"` | `"dd-MM-yy"` | `"dd/MM/yy"` | `"dd/MM/yyyy"` | `"MM/dd/yy"` | `"MM/dd/yyyy"`>

Get a watched value that can be used to read/write/subscribe to the state of the date format.

#### Returns
[`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`"qq 'yy"` | `"qq yyyy"` | `"dd MMM 'yy"` | `"MMM 'yy"` | `"MMM dd, yyyy"` | `"MMM yyyy"` | `"MMM dd"` | `"dd MMM"` | `"yyyy-MM-dd"` | `"yy-MM-dd"` | `"yy/MM/dd"` | `"yyyy/MM/dd"` | `"dd-MM-yyyy"` | `"dd-MM-yy"` | `"dd/MM/yy"` | `"dd/MM/yyyy"` | `"MM/dd/yy"` | `"MM/dd/yyyy"`>

A watched value of the state of the date format.

### dateRangeSync
▸ **dateRangeSync**(): [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

Only available in Trading Platform. Get a watched value that can be used to read/write/subscribe to the state of the date range sync between charts.

**Example**

```
widget.dateRangeSync().setValue(true);

```
#### Returns
[`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

A watched value of the state of the date range sync.

### drawOnAllChartsEnabled
▸ **drawOnAllChartsEnabled**(): [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

Get a watched value that read/write/subscribe to the state of the 'draw on all charts' mode.

When enabled new drawings will be replicated to all charts in the layout
and shown when the same ticker is selected.
#### Returns
[`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

### exitFullscreen
▸ **exitFullscreen**(): `void`

Set the chart into non-fullscreen mode (if it isn't already).

#### Returns
`void`

### getCSSCustomPropertyValue
▸ **getCSSCustomPropertyValue**(`customPropertyName`): `string`

Returns the current value for a CSS custom property.

**Example:**

```
const currentValue = widget.getCSSCustomPropertyValue('--my-theme-color');

```
#### Parameters

 **|Name** | **Type** | **Description** ||
| `customPropertyName` | `string` | A string representing the CSS custom property name to be checked. It is expected that the name should start with a double hyphen ('--'). ||

#### Returns
`string`

A string containing the value of the property. If not set, returns the empty string.

### getIntervals
▸ **getIntervals**(): `string`

Get an array of supported intervals (resolutions).

#### Returns
`string`

An array of supported intervals. E.g. `['1D', '5D', '1Y']`.

### getLanguage
▸ **getLanguage**(): [`LanguageCode`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#languagecode)

Get the configured locale of the widget. For example `en`, `zh`, `ru`.

#### Returns
[`LanguageCode`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#languagecode)

A code representing the locale of the widget.

### getSavedCharts
▸ **getSavedCharts**(`callback`): `void`

Get a list of chart descriptions saved to the server for the current user.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `callback` | (`chartRecords`: [`SaveLoadChartRecord`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SaveLoadChartRecord)) => `void` | A function called with an array of saved chart information as the first argument. ||

#### Returns
`void`

### getStudiesList
▸ **getStudiesList**(): `string`

Get an array of the names of all supported studies. These names can be used when calling [IChartWidgetApi.createStudy](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#createstudy).

#### Returns
`string`

An array of supported study names. E.g. `['Accumulation/Distribution', 'Accumulative Swing Index', 'Advance/Decline', ...]`.

### getStudyInputs
▸ **getStudyInputs**(`studyName`): [`StudyInputInformation`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyInputInformation)

Get an array of information about indicator inputs, including their names.
You need to know an input name to refer to this property in the code.
For example, when you change an input value using the [overrides](https://www.tradingview.com/charting-library-docs/latest/customization/overrides/indicator-overrides).
Consider the [Input property](https://www.tradingview.com/charting-library-docs/latest/customization/overrides/indicator-overrides#input-property) section for more information.
#### Parameters

 **|Name** | **Type** | **Description** ||
| `studyName` | `string` | The name of a study. ||

#### Returns
[`StudyInputInformation`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyInputInformation)

### getStudyStyles
▸ **getStudyStyles**(`studyName`): [`StudyStyleInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyStyleInfo)

Get information about indicator properties.
You can use this information to refer to the properties in the code.
For example, when you change property values using the [overrides](https://www.tradingview.com/charting-library-docs/latest/customization/overrides/indicator-overrides).
Note that `getStudyStyles` does not return actual property names but the indicator's [metadata](https://www.tradingview.com/charting-library-docs/latest/custom_studies/metainfo/).
Consider the [Property path](https://www.tradingview.com/charting-library-docs/latest/customization/overrides/indicator-overrides#property-path) section for more information on how to refer to the properties.
#### Parameters

 **|Name** | **Type** | **Description** ||
| `studyName` | `string` | The name of a indicator. ||

#### Returns
[`StudyStyleInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyStyleInfo)

### getTheme
▸ **getTheme**(): [`ThemeName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#themename)

Get the current theme of the chart.

**Example**

```
console.log(widget.getTheme());

```
#### Returns
[`ThemeName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#themename)

A theme name. The name of the current theme.

### headerReady
▸ **headerReady**(): `Promise`<`void`>

A promise that resolves if and when the header is ready to be used.

#### Returns
`Promise`<`void`>

### hideAllDrawingTools
▸ **hideAllDrawingTools**(): [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

Get a watched value that can be used to read/write/subscribe to the state of the "Hide All Drawing Tools" button.

#### Returns
[`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

A watched value of the state of the "Hide All Drawing Tools" button.

### intervalSync
▸ **intervalSync**(): [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

Only available in Trading Platform. Get a watched value that can be used to read/write/subscribe to the state of the interval sync between charts.

**Example**

```
widget.intervalSync().setValue(true);

```
#### Returns
[`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

A watched value of the state of the interval sync.

### layout
▸ **layout**(): [`LayoutType`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#layouttype)

Get the current chart layout type.

#### Returns
[`LayoutType`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#layouttype)

A string representation of the current layout type. E.g. `'2h'` for two charts split vertically.

### layoutName
▸ **layoutName**(): `string`

Get the name of the current chart layout. The return value will be `undefined` if the current layout has not been saved.

#### Returns
`string`

A string of the name of the current chart layout.

### load
▸ **load**(`state`, `extendedData?`): `Promise`<`void`>

Loads the chart state from a object. This method is part of the low-level save/load API.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `state` | `object` | A chart state object to load. ||
| `extendedData?` | [`SavedStateMetaInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SavedStateMetaInfo) | A optional object of information about the saved state. ||

#### Returns
`Promise`<`void`>

### loadChartFromServer
▸ **loadChartFromServer**(`chartRecord`): `Promise`<`void`>

Load a saved chart from the server.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `chartRecord` | [`SaveLoadChartRecord`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SaveLoadChartRecord) | A chart information object (returned by [getSavedCharts](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#getsavedcharts)). ||

#### Returns
`Promise`<`void`>

### lockAllDrawingTools
▸ **lockAllDrawingTools**(): [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

Get a watched value that can be used to read/write/subscribe to the state of the "Lock All Drawing Tools" button.

#### Returns
[`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

A watched value of the state of the "Lock All Drawing Tools" button.

### magnetEnabled
▸ **magnetEnabled**(): [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

Get a watched value that can be used to read/write/subscribe to the state of the magnet.

#### Returns
[`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

A watched value of the state of the magnet.

### magnetMode
▸ **magnetMode**(): [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`number`>

Get a watched value that can be used to read/write/subscribe to the state of the magnet mode.

#### Returns
[`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`number`>

A watched value of the state of the magnet mode.

### mainSeriesPriceFormatter
▸ **mainSeriesPriceFormatter**(): [`INumberFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.INumberFormatter)

Get the price formatter for the main series. You can use this to format prices as the char

#### Returns
[`INumberFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.INumberFormatter)

### navigationButtonsVisibility
▸ **navigationButtonsVisibility**(): [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<[`VisibilityType`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.VisibilityType)>

Get a watched value that can be used to read/write/subscribe to the state of the navigation buttons.

#### Returns
[`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<[`VisibilityType`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.VisibilityType)>

A watched value of the state of the navigation buttons.

### news
▸ **news**(): `Promise`<[`INewsApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.INewsApi)>

Trading Platform only. Get a promise that resolves with an API object for interacting with the widgetbar (right sidebar) news widget.

#### Returns
`Promise`<[`INewsApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.INewsApi)>

An API object for interacting with the widgetbar (right sidebar) widget.

### onChartReady
▸ **onChartReady**(`callback`): `void`

The library will call `callback` when the chart is ready to be used.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `callback` | [`EmptyCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#emptycallback) | A function that will be called when the chart is ready to be used. ||

#### Returns
`void`

### onContextMenu
▸ **onContextMenu**(`callback`): `void`

The widget will call the callback function each time the widget wants to display a context menu.
See also [ChartingLibraryWidgetOptions.context_menu](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#context_menu).
**Example**

```
widget.onChartReady(function() {
    widget.onContextMenu(function(unixtime, price) {
        return [{
            position: "top",
            text: "First top menu item, time: " + unixtime + ", price: " + price,
            click: function() { alert("First clicked."); }
        },
        { text: "-", position: "top" }, // Adds a separator between buttons
        { text: "-Paste" },             // Removes the existing item from the menu
        {
            position: "top",
            text: "Second top menu item 2",
            click: function() { alert("Second clicked."); }
        }, {
            position: "bottom",
            text: "Bottom menu item",
            click: function() { alert("Third clicked."); }
        }];
    });
});

```
#### Parameters

 **|Name** | **Type** | **Description** ||
| `callback` | (`unixTime`: `number`, `price`: `number`) => [`ContextMenuItem`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ContextMenuItem) | A function called with the time and price of the location on the chart that triggered the context menu. The array of objects returned will add or remove items from the context menu. ||

#### Returns
`void`

### onGrayedObjectClicked
▸ **onGrayedObjectClicked**(`callback`): `void`

The library will call `callback` when a greyed-out drawing tool or study is clicked.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `callback` | (`obj`: [`GrayedObject`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.GrayedObject)) => `void` | A function that will be called when a greyed-out drawing tool or study is clicked. ||

#### Returns
`void`

### onShortcut
▸ **onShortcut**(`shortCut`, `callback`): `void`

This method specifies an action that happens when a user presses certain keys.
It allows you to override the built‑in shortcuts or specify custom ones.
To do this, pass a keyboard shortcut and a callback function as parameters.
The library invokes the callback when the `shortCut` keys are pressed.
Note that the `shortCut` argument depends on the key types. Refer to the [Manage shortcuts](https://www.tradingview.com/charting-library-docs/latest/getting_started/Shortcuts#manage-shortcuts) section for more information and examples.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `shortCut` | `string` | `number` | (`string` | `number`) | A number, a string, or an array of numbers and strings. ||
| `callback` | [`EmptyCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#emptycallback) | A function that is called when the `shortCut` keys are pressed. ||

#### Returns
`void`

### paneButtonsVisibility
▸ **paneButtonsVisibility**(): [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<[`VisibilityType`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.VisibilityType)>

Get a watched value that can be used to read/write/subscribe to the state of the pane buttons.

#### Returns
[`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<[`VisibilityType`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.VisibilityType)>

A watched value of the state of the pane buttons.

### remove
▸ **remove**(): `void`

Remove the widget and all its data from the page. The widget cannot be interacted with after it has been removed.

#### Returns
`void`

### removeButton
▸ **removeButton**(`buttonIdOrHtmlElement`): `void`

Remove a button from the top toolbar. This should be called after [headerReady](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#headerready) has resolved.

**Example**

```
widget.headerReady().then(function() {
    var button = widget.createButton();
    widget.removeButton(button)
});

```
#### Parameters

 **|Name** | **Type** | **Description** ||
| `buttonIdOrHtmlElement` | `string` | `HTMLElement` | The button link or id that you receive from createButton method. ||

#### Returns
`void`

### removeChartFromServer
▸ **removeChartFromServer**(`chartId`, `onCompleteCallback`): `void`

Remove a saved chart from the server.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `chartId` | `string` | `number` | A chart ID from a [SaveLoadChartRecord](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SaveLoadChartRecord) (returned by [getSavedCharts](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#getsavedcharts)). ||
| `onCompleteCallback` | [`EmptyCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#emptycallback) | A callback function called when the chart is successfully saved. ||

#### Returns
`void`

### resetCache
▸ **resetCache**(): `void`

Reset cached bar data from the datafeed, for all symbols.

This has the same effect as calling [`onResetCacheNeededCallback`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IDatafeedChartApi#subscribebars) for all symbol and resolution combinations at once.

#### Returns
`void`

### resetLayoutSizes
▸ **resetLayoutSizes**(`disableUndo?`): `void`

Resets the sizes of all charts within a multiple-chart layout back to their initial default values.
This action redistributes the space equally among all charts to ensure consistency in layout design.
#### Parameters

 **|Name** | **Type** | **Description** ||
| `disableUndo?` | `boolean` | When set to true, the reset action is not added to the undo stack. Hence, the user cannot undo the reset operation. ||

#### Returns
`void`

### save
▸ **save**(`callback`, `options?`): `void`

Saves the chart state to a object. This method is part of the low-level save/load API.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `callback` | (`state`: `object`) => `void` | A function called with the chart state as the first argument. ||
| `options?` | [`SaveChartOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SaveChartOptions) | Options for customising the saved data. ||

#### Returns
`void`

### saveChartToServer
▸ **saveChartToServer**(`onComplete?`, `onFail?`, `options?`): `void`

Save the current chart to the server.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `onComplete?` | [`EmptyCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#emptycallback) | An optional callback function called when the chart is successfully saved. ||
| `onFail?` | (`error`: [`SaveChartErrorInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SaveChartErrorInfo)) => `void` | An optional callback function called when the chart fails to save. ||
| `options?` | [`SaveChartToServerOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SaveChartToServerOptions) | An optional object of options for saving the chart. ||

#### Returns
`void`

### selectLineTool
▸ **selectLineTool**(`linetool`, `options?`): `Promise`<`void`>

Select an icon. It's the same as clicking on the corresponding button in the left toolbar.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `linetool` | `"icon"` | An icon drawing tool. ||
| `options?` | [`IconOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IconOptions) | An optional object with options. ||

#### Returns
`Promise`<`void`>

▸ **selectLineTool**(`linetool`): `Promise`<`void`>

Select a drawing or a cursor. It's the same as clicking on the corresponding button in the left toolbar.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `linetool` | `Omit`<`"icon"`, [`SupportedLineTools`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#supportedlinetools)> | A drawing or cursor to select (excluding 'icon') ||

#### Returns
`Promise`<`void`>

▸ **selectLineTool**(`linetool`, `options?`): `Promise`<`void`>

Select the Icon line tool. It's the same as clicking on the corresponding button in the left toolbar.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `linetool` | `"icon"` | Icon line tool. ||
| `options?` | [`IconOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IconOptions) | An optional object with options. Currently only used for the 'icon' drawing. ||

#### Returns
`Promise`<`void`>

▸ **selectLineTool**(`linetool`, `options?`): `Promise`<`void`>

Select the Emoji line tool. It's the same as clicking on the corresponding button in the left toolbar.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `linetool` | `"emoji"` | Emoji line tool. ||
| `options?` | [`EmojiOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.EmojiOptions) | Options for the Emoji line tool ||

#### Returns
`Promise`<`void`>

▸ **selectLineTool**(`linetool`, `options?`): `Promise`<`void`>

Select a drawing, icon, or a cursor. It's the same as clicking on the corresponding button in the left toolbar.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `linetool` | [`SupportedLineTools`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#supportedlinetools) | A drawing or cursor to select. ||
| `options?` | [`EmojiOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.EmojiOptions) | [`IconOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IconOptions) | An optional object with options. ||

#### Returns
`Promise`<`void`>

### selectedLineTool
▸ **selectedLineTool**(): [`SupportedLineTools`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#supportedlinetools)

Get the currently selected drawing or cursor.

#### Returns
[`SupportedLineTools`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#supportedlinetools)

An identifier for drawing or cursor.

### setActiveChart
▸ **setActiveChart**(`index`): `void`

Set which chart is currently active.
It is recommended that this method is only used when linked to a user action
which should change the active chart.
Use [chartsCount](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#chartscount) to determine the number of charts currently available.
If an invalid index is supplied (less than zero, or greater than the number of charts minus 1)
then this method will not change the active chart.
#### Parameters

 **|Name** | **Type** | **Description** ||
| `index` | `number` | index of chart to set as the active chart. Index is zero-based. ||

#### Returns
`void`

### setCSSCustomProperty
▸ **setCSSCustomProperty**(`customPropertyName`, `value`): `void`

Sets the value for a CSS custom property.

**Example:**

```
widget.setCSSCustomProperty('--my-theme-color', '#123AAA');

```
#### Parameters

 **|Name** | **Type** | **Description** ||
| `customPropertyName` | `string` | A string representing the CSS custom property name. It is expected that the name should start with a double hyphen ('--'). ||
| `value` | `string` | A string containing the new property value. ||

#### Returns
`void`

### setDebugMode
▸ **setDebugMode**(`enabled`): `void`

Enable or disable writing detailed [Datafeed API](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/) logs into the browser console.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `enabled` | `boolean` | A boolean flag. `true` to enable debug mode, `false` to disable. ||

#### Returns
`void`

### setLayout
▸ **setLayout**(`layout`): `void`

Set the current chart layout type.

#### Parameters

 **|Name** | **Type** ||
| `layout` | [`LayoutType`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#layouttype) ||

#### Returns
`void`

**`Params`**

layout A string representation of the new layout type. E.g. `'2h'` for two charts split vertically.

### setSymbol
▸ **setSymbol**(`symbol`, `interval`, `callback`): `void`

Set the symbol and resolution of the active chart.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `symbol` | `string` | A symbol to load. ||
| `interval` | [`ResolutionString`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#resolutionstring) | A interval (resolution) to load. ||
| `callback` | [`EmptyCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#emptycallback) | A callback. Called when the symbol's data has finished loading. ||

#### Returns
`void`

### showConfirmDialog
▸ **showConfirmDialog**(`params`): `void`

Show a dialog with custom title and text along with "OK" and "CANCEL" buttons.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `params` | [`DialogParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.DialogParams)<(`confirmed`: `boolean`) => `void`> | A object of options for the created dialog. ||

#### Returns
`void`

### showLoadChartDialog
▸ **showLoadChartDialog**(): `void`

Show the "Load Chart Layout" dialog.

#### Returns
`void`

### showNoticeDialog
▸ **showNoticeDialog**(`params`): `void`

Show a dialog with custom title and text along with an "OK" buttons.

#### Parameters

 **|Name** | **Type** | **Description** ||
| `params` | [`DialogParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.DialogParams)<() => `void`> | A object of options for the created dialog. ||

#### Returns
`void`

### showSaveAsChartDialog
▸ **showSaveAsChartDialog**(): `void`

Show the "Copy Chart Layout" dialog.

#### Returns
`void`

### startFullscreen
▸ **startFullscreen**(): `void`

Set the chart into fullscreen mode (if it isn't already).

#### Returns
`void`

### subscribe
▸ **subscribe**<`EventName`>(`event`, `callback`): `void`

Subscribe to library events.

#### Type parameters

 **|Name** | **Type** ||
| `EventName` | extends keyof [`SubscribeEventsMap`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SubscribeEventsMap) ||

#### Parameters

 **|Name** | **Type** | **Description** ||
| `event` | `EventName` | A event to subscribe to. ||
| `callback` | [`SubscribeEventsMap`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SubscribeEventsMap)[`EventName`] | A callback that will be called when the event happens. ||

#### Returns
`void`

### supportedChartTypes
▸ **supportedChartTypes**(): [`IWatchedValueReadonly`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValueReadonly)<[`ChartStyle`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.ChartStyle)>

This method returns a readonly WatchedValue ([IWatchedValueReadonly](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValueReadonly))
object that can be used to read/watch the current supported chart types
([SeriesType](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.SeriesType)) for an active chart.
The chart type is returned as a number.
You can see which number corresponds to which chart type in the
[Overrides](https://www.tradingview.com/charting-library-docs/latest/customization/overrides/)
documentation for `mainSeriesProperties.style`.
#### Returns
[`IWatchedValueReadonly`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValueReadonly)<[`ChartStyle`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.ChartStyle)>

### symbolInterval
▸ **symbolInterval**(): [`SymbolIntervalResult`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SymbolIntervalResult)

Get the symbol and interval of the active chart.

#### Returns
[`SymbolIntervalResult`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SymbolIntervalResult)

### symbolSync
▸ **symbolSync**(): [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

Only available in Trading Platform. Get a watched value that can be used to read/write/subscribe to the state of the symbol sync between charts.

**Example**

```
if (widget.symbolSync().value()) {
    // ...
}

```
#### Returns
[`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

A watched value of the state of the symbol sync.

### takeClientScreenshot
▸ **takeClientScreenshot**(`options?`): `Promise`<`HTMLCanvasElement`>

Create a snapshot of the chart and return it as a canvas.
Use this method to [implement your logic](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Snapshots#implement-your-logic) for taking snapshots.
#### Parameters

 **|Name** | **Type** | **Description** ||
| `options?` | `Partial`<[`ClientSnapshotOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ClientSnapshotOptions)> | An optional object that customizes the returned snapshot. ||

#### Returns
`Promise`<`HTMLCanvasElement`>

A promise containing a `HTMLCanvasElement` of the snapshot.

### takeScreenshot
▸ **takeScreenshot**(): `void`

Create a snapshot of the chart and upload it to the server.
When it is ready callback functions subscribed to the `'onScreenshotReady'` event using [subscribe](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#subscribe) will be called.
The URL of the snapshot will be passed as an argument to the callback function.
#### Returns
`void`

### timeHoursFormat
▸ **timeHoursFormat**(): [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<[`TimeHoursFormat`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.TimeHoursFormat)>

Get a watched value that can be used to read/write/subscribe to the state of the timeHours format.

#### Returns
[`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<[`TimeHoursFormat`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.TimeHoursFormat)>

### timeSync
▸ **timeSync**(): [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

Only available in Trading Platform. Get a watched value that can be used to read/write/subscribe to the state of the time sync between charts.

**Example**

```
widget.timeSync().setValue(true);

```
#### Returns
[`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

A watched value of the state of the time sync.

### undoRedoState
▸ **undoRedoState**(): [`UndoRedoState`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.UndoRedoState)

Get the state of the undo/redo stack.

#### Returns
[`UndoRedoState`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.UndoRedoState)

### unloadUnusedCharts
▸ **unloadUnusedCharts**(): `void`

This method deletes non-visible charts from a multiple-chart layout.

When a user transitions from a layout with a larger number of charts
to one with fewer charts, the unused chart APIs still exist behind the scenes.
This inherent behavior allows the library to restore previously displayed charts.
If you prefer that additional charts are displayed as new, with no record of previous
charts at the same position, you can use this method to delete all non-visible charts.
It is most effective to run this method right after a layout change (one can subscribe to
[SubscribeEventsMap.layout_changed](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SubscribeEventsMap#layout_changed) to know when this occurs).
Please ensure that any subscriptions or event listeners associated with the
hidden charts are removed prior to invoking this method.
#### Returns
`void`

void

### unsubscribe
▸ **unsubscribe**<`EventName`>(`event`, `callback`): `void`

Unsubscribe from library events.

#### Type parameters

 **|Name** | **Type** ||
| `EventName` | extends keyof [`SubscribeEventsMap`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SubscribeEventsMap) ||

#### Parameters

 **|Name** | **Type** | **Description** ||
| `event` | `EventName` | A event to unsubscribe from. ||
| `callback` | [`SubscribeEventsMap`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SubscribeEventsMap)[`EventName`] | A callback to unsubscribe. Must be the same reference as a callback passed to [subscribe](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#subscribe). ||

#### Returns
`void`

### watchList
▸ **watchList**(): `Promise`<[`IWatchListApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchListApi)>

Trading Platform only. Get a promise that resolves with an API object for interacting with the widgetbar (right sidebar) watchlist.

**Example**

```
const watchlistApi = await widget.watchList();
const activeListId = watchlistApi.getActiveListId();
const currentListItems = watchlistApi.getList(activeListId);
// append new section and item to the current watchlist
watchlistApi.updateList(activeListId, [...currentListItems, '###NEW SECTION', 'AMZN']);

```
#### Returns
`Promise`<[`IWatchListApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchListApi)>

An API object for interacting with the widgetbar (right sidebar) watchlist.

### watermark
▸ **watermark**(): [`IWatermarkApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatermarkApi)

Get an API object for adjusting the watermarks present on the charts.
This can only be accessed when the chart is ready to be used. ([onChartReady](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#onchartready))
#### Returns
[`IWatermarkApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatermarkApi)

An API object for adjusting the watermark settings.

### widgetbar
▸ **widgetbar**(): `Promise`<[`IWidgetbarApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWidgetbarApi)>

Trading Platform only. Get a promise that resolves with an API object for interacting with the widgetbar (right sidebar).

#### Returns
`Promise`<[`IWidgetbarApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWidgetbarApi)>

An API object for interacting with the widgetbar (right sidebar).