---
title: "Interface: IChartingLibraryWidget | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget"
extracted_at: "2025-06-22T09:38:34.635Z"
---

- [](/charting-library-docs/)- Interfaces- IChartingLibraryWidgetOn this page# Interface: IChartingLibraryWidget[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).IChartingLibraryWidget

The main interface for interacting with the library, returned by [ChartingLibraryWidgetConstructor](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetConstructor).
For more information, refer to the [Widget methods](https://www.tradingview.com/charting-library-docs/latest/core_concepts/widget-methods) article.
## Methods[​](#methods)
### activeChart[​](#activechart)
▸ activeChart(): [`IChartWidgetApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi)

Get an API object for interacting with the active chart.
For example, you can subscribe to events on the active chart, such as [IChartWidgetApi.onIntervalChanged](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#onintervalchanged).
Note that the library does not manage the event subscriptions when users switch between the charts on the [multiple-chart layout](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/#multiple-chart-layout).
If necessary, you should manually unsubscribe from the previous chart and subscribe to the newly selected one.
To track the currently active chart, use the [SubscribeEventsMap.activeChartChanged](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SubscribeEventsMap#activechartchanged) event.
#### Returns[​](#returns)
[`IChartWidgetApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi)

An API object for interacting with the chart.

### activeChartIndex[​](#activechartindex)
▸ activeChartIndex(): `number`

Get the index of the active chart in the layout.

#### Returns[​](#returns-1)
`number`

number.

### addCustomCSSFile[​](#addcustomcssfile)
▸ addCustomCSSFile(`url`): `void`

Add a custom CSS file for the library to load.

#### Parameters[​](#parameters)
NameTypeDescription`url``string`A url to the custom CSS file. Should be absolute or relative to the `static` folder.
#### Returns[​](#returns-2)
`void`

### applyOverrides[​](#applyoverrides)
▸ applyOverrides<`TOverrides`>(`overrides`): `void`

Apply overrides to the chart without reloading. See also [ChartingLibraryWidgetOptions.overrides](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#overrides).

#### Type parameters[​](#type-parameters)
NameType`TOverrides`extends `Partial`<[`ChartPropertiesOverrides`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides)>
#### Parameters[​](#parameters-1)
NameTypeDescription`overrides``TOverrides`An object of overrides to apply to the chart.
#### Returns[​](#returns-3)
`void`

### applyStudiesOverrides[​](#applystudiesoverrides)
▸ applyStudiesOverrides(`overrides`): `void`

Apply overrides to indicator styles and inputs without reloading.
Refer to [Indicator Overrides](https://www.tradingview.com/charting-library-docs/latest/customization/overrides/indicator-overrides#change-default-properties-on-the-fly) for more information.
Overrides for built-in indicators are listed in [StudyOverrides](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyOverrides).
#### Parameters[​](#parameters-2)
NameTypeDescription`overrides``object`An object of overrides to apply to the studies.
#### Returns[​](#returns-4)
`void`

### changeTheme[​](#changetheme)
▸ changeTheme(`themeName`, `options?`): `Promise`<`void`>

Change the theme of the chart.

#### Parameters[​](#parameters-3)
NameTypeDescription`themeName`[`ThemeName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#themename)A theme name.`options?`[`ChangeThemeOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChangeThemeOptions)An optional object of options for the theme.
#### Returns[​](#returns-5)
`Promise`<`void`>

A promise that resolves when the theme has been changed.

### chart[​](#chart)
▸ chart(`index?`): [`IChartWidgetApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi)

Get an API instance that can be used to interact with a chart.

#### Parameters[​](#parameters-4)
NameTypeDescription`index?``number`Zero based index of the chart.
#### Returns[​](#returns-6)
[`IChartWidgetApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi)

An API instance.

### chartsCount[​](#chartscount)
▸ chartsCount(): `number`

Get the number of charts in the current layout.

#### Returns[​](#returns-7)
`number`

A count of the charts in the current layout.

### clearUndoHistory[​](#clearundohistory)
▸ clearUndoHistory(): `void`

Clears the undo & redo history.

Warning: this should only be used in very specific cases where you have considered
the UX implications. It is generally unexpected for the user that the undo
history has been cleared.
An example of an acceptable use-case would be reusing a chart when switching
pages / tabs on a Single Page Application, and presenting it to the user as a
new chart.
#### Returns[​](#returns-8)
`void`

### closePopupsAndDialogs[​](#closepopupsanddialogs)
▸ closePopupsAndDialogs(): `void`

Close all open context menus, pop-ups or dialogs.

#### Returns[​](#returns-9)
`void`

### createButton[​](#createbutton)
▸ createButton(`options?`): `HTMLElement`

Create a button in the top toolbar. This should be called after [headerReady](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#headerready) has resolved.

Example

```
widget.headerReady().then(function() {    var button = widget.createButton();    button.setAttribute('title', 'My custom button tooltip');    button.addEventListener('click', function() { alert("My custom button pressed!"); });    button.textContent = 'My custom button caption';});
```
#### Parameters[​](#parameters-5)
NameTypeDescription`options?`[`CreateHTMLButtonOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateHTMLButtonOptions)A optional object of options for the button.
#### Returns[​](#returns-10)
`HTMLElement`

A `HTMLElement` you can customize.

▸ createButton(`options`): `string`

Create a button in the top toolbar. This should be called after [headerReady](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#headerready) has resolved.
If the `title` option is provided then the title text will be shown in a tooltip on hover.
If the `onClick` option is provided then the button will be clickable.
#### Parameters[​](#parameters-6)
NameTypeDescription`options`[`CreateTradingViewStyledButtonOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateTradingViewStyledButtonOptions)A object of options for the button.
#### Returns[​](#returns-11)
`string`

A `string` button id

▸ createButton(`options?`): `string` | `HTMLElement`

Create a button in the top toolbar. This should be called after [headerReady](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#headerready) has resolved.

#### Parameters[​](#parameters-7)
NameTypeDescription`options?`[`CreateButtonOptions`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#createbuttonoptions)A optional object of options for the button.
#### Returns[​](#returns-12)
`string` | `HTMLElement`

A `HTMLElement` if the `useTradingViewStyle` option is `false` or undefined. `string`(button id) if `useTradingViewStyle` is `true`.

### createDropdown[​](#createdropdown)
▸ createDropdown(`params`): `Promise`<[`IDropdownApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IDropdownApi)>

Add a custom dropdown menu to the top toolbar.

Example

```
widget.createDropdown(    {        title: 'dropdown',        tooltip: 'tooltip for this dropdown',        items: [            {                title: 'item#1',                onSelect: () => {console.log('1');},            },            {                title: 'item#2',                onSelect: () => {widget.setSymbol('IBM', '1D');},            },            {                title: 'item#3',                onSelect: () => {                    widget.activeChart().createStudy(                        'MACD',                        false,                        false,                        {                            in_0: 14,                            in_1: 30,                            in_3: 'close',                            in_2: 9                        }                    );                },            }        ],        icon: `<svg xmlns="http://www.w3.org/2000/svg" width="28" height="28"><g fill="none" stroke="currentColor"><circle cx="10" cy="10" r="2.5"/><circle cx="18" cy="18" r="2.5"/><path stroke-linecap="square" d="M17.5 7.5l-7 13"/></g></svg>`,    }).then(myDropdownApi => {    // Use myDropdownApi if you need to update the dropdown:    // myDropdownApi.applyOptions({    //     title: 'a new title!'    // });    // Or remove the dropdown:    // myDropdownApi.remove();});
```
#### Parameters[​](#parameters-8)
NameType`params`[`DropdownParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.DropdownParams)
#### Returns[​](#returns-13)
`Promise`<[`IDropdownApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IDropdownApi)>

### crosshairSync[​](#crosshairsync)
▸ crosshairSync(): [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

Only available in Trading Platform. Get a watched value that can be used to read/write/subscribe to the state of the crosshair sync between charts.

Example

```
widget.crosshairSync().setValue(true);
```
#### Returns[​](#returns-14)
[`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

A watched value of the state of the crosshair sync.

### currencyAndUnitVisibility[​](#currencyandunitvisibility)
▸ currencyAndUnitVisibility(): [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<[`VisibilityType`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.VisibilityType)>

Get a watched value that can be used to read/write/subscribe to the state of the currency and unit
visibility setting on the price scale.
#### Returns[​](#returns-15)
[`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<[`VisibilityType`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.VisibilityType)>

A watched value of the state of the currency and unit visibility option.

### customSymbolStatus[​](#customsymbolstatus)
▸ customSymbolStatus(): [`ICustomSymbolStatusApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ICustomSymbolStatusApi)

Get an API object for creating, and adjusting, custom status items to
be displayed within the legend for the main series of each chart.
This can only be accessed when the chart has been created. ([headerReady](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#headerready))

#### Returns[​](#returns-16)
[`ICustomSymbolStatusApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ICustomSymbolStatusApi)

An API object for controlling additional custom status items within the legend area.

### customThemes[​](#customthemes)
▸ customThemes(): `Promise`<[`ICustomThemesApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ICustomThemesApi)>

Get a promise that resolves with an API object for interacting with the custom themes. For more information on custom themes, refer to the [Custom themes API](https://www.tradingview.com/charting-library-docs/latest/customization/styles/custom-themes) article.

#### Returns[​](#returns-17)
`Promise`<[`ICustomThemesApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ICustomThemesApi)>

An API object for interacting with the custom themes.

### dateFormat[​](#dateformat)
▸ dateFormat(): [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`"qq 'yy"` | `"qq yyyy"` | `"dd MMM 'yy"` | `"MMM 'yy"` | `"MMM dd, yyyy"` | `"MMM yyyy"` | `"MMM dd"` | `"dd MMM"` | `"yyyy-MM-dd"` | `"yy-MM-dd"` | `"yy/MM/dd"` | `"yyyy/MM/dd"` | `"dd-MM-yyyy"` | `"dd-MM-yy"` | `"dd/MM/yy"` | `"dd/MM/yyyy"` | `"MM/dd/yy"` | `"MM/dd/yyyy"`>

Get a watched value that can be used to read/write/subscribe to the state of the date format.

#### Returns[​](#returns-18)
[`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`"qq 'yy"` | `"qq yyyy"` | `"dd MMM 'yy"` | `"MMM 'yy"` | `"MMM dd, yyyy"` | `"MMM yyyy"` | `"MMM dd"` | `"dd MMM"` | `"yyyy-MM-dd"` | `"yy-MM-dd"` | `"yy/MM/dd"` | `"yyyy/MM/dd"` | `"dd-MM-yyyy"` | `"dd-MM-yy"` | `"dd/MM/yy"` | `"dd/MM/yyyy"` | `"MM/dd/yy"` | `"MM/dd/yyyy"`>

A watched value of the state of the date format.

### dateRangeSync[​](#daterangesync)
▸ dateRangeSync(): [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

Only available in Trading Platform. Get a watched value that can be used to read/write/subscribe to the state of the date range sync between charts.

Example

```
widget.dateRangeSync().setValue(true);
```
#### Returns[​](#returns-19)
[`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

A watched value of the state of the date range sync.

### drawOnAllChartsEnabled[​](#drawonallchartsenabled)
▸ drawOnAllChartsEnabled(): [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

Get a watched value that read/write/subscribe to the state of the 'draw on all charts' mode.

When enabled new drawings will be replicated to all charts in the layout
and shown when the same ticker is selected.
#### Returns[​](#returns-20)
[`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

### exitFullscreen[​](#exitfullscreen)
▸ exitFullscreen(): `void`

Set the chart into non-fullscreen mode (if it isn't already).

#### Returns[​](#returns-21)
`void`

### getCSSCustomPropertyValue[​](#getcsscustompropertyvalue)
▸ getCSSCustomPropertyValue(`customPropertyName`): `string`

Returns the current value for a CSS custom property.

Example:

```
const currentValue = widget.getCSSCustomPropertyValue('--my-theme-color');
```
#### Parameters[​](#parameters-9)
NameTypeDescription`customPropertyName``string`A string representing the CSS custom property name to be checked. It is expected that the name should start with a double hyphen ('--').
#### Returns[​](#returns-22)
`string`

A string containing the value of the property. If not set, returns the empty string.

### getIntervals[​](#getintervals)
▸ getIntervals(): `string`[]

Get an array of supported intervals (resolutions).

#### Returns[​](#returns-23)
`string`[]

An array of supported intervals. E.g. `['1D', '5D', '1Y']`.

### getLanguage[​](#getlanguage)
▸ getLanguage(): [`LanguageCode`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#languagecode)

Get the configured locale of the widget. For example `en`, `zh`, `ru`.

#### Returns[​](#returns-24)
[`LanguageCode`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#languagecode)

A code representing the locale of the widget.

### getSavedCharts[​](#getsavedcharts)
▸ getSavedCharts(`callback`): `void`

Get a list of chart descriptions saved to the server for the current user.

#### Parameters[​](#parameters-10)
NameTypeDescription`callback`(`chartRecords`: [`SaveLoadChartRecord`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SaveLoadChartRecord)[]) => `void`A function called with an array of saved chart information as the first argument.
#### Returns[​](#returns-25)
`void`

### getStudiesList[​](#getstudieslist)
▸ getStudiesList(): `string`[]

Get an array of the names of all supported studies. These names can be used when calling [IChartWidgetApi.createStudy](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#createstudy).

#### Returns[​](#returns-26)
`string`[]

An array of supported study names. E.g. `['Accumulation/Distribution', 'Accumulative Swing Index', 'Advance/Decline', ...]`.

### getStudyInputs[​](#getstudyinputs)
▸ getStudyInputs(`studyName`): [`StudyInputInformation`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyInputInformation)[]

Get an array of information about indicator inputs, including their names.
You need to know an input name to refer to this property in the code.
For example, when you change an input value using the [overrides](https://www.tradingview.com/charting-library-docs/latest/customization/overrides/indicator-overrides).
Consider the [Input property](https://www.tradingview.com/charting-library-docs/latest/customization/overrides/indicator-overrides#input-property) section for more information.
#### Parameters[​](#parameters-11)
NameTypeDescription`studyName``string`The name of a study.
#### Returns[​](#returns-27)
[`StudyInputInformation`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyInputInformation)[]

### getStudyStyles[​](#getstudystyles)
▸ getStudyStyles(`studyName`): [`StudyStyleInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyStyleInfo)

Get information about indicator properties.
You can use this information to refer to the properties in the code.
For example, when you change property values using the [overrides](https://www.tradingview.com/charting-library-docs/latest/customization/overrides/indicator-overrides).
Note that `getStudyStyles` does not return actual property names but the indicator's [metadata](https://www.tradingview.com/charting-library-docs/latest/custom_studies/metainfo/).
Consider the [Property path](https://www.tradingview.com/charting-library-docs/latest/customization/overrides/indicator-overrides#property-path) section for more information on how to refer to the properties.
#### Parameters[​](#parameters-12)
NameTypeDescription`studyName``string`The name of a indicator.
#### Returns[​](#returns-28)
[`StudyStyleInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyStyleInfo)

### getTheme[​](#gettheme)
▸ getTheme(): [`ThemeName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#themename)

Get the current theme of the chart.

Example

```
console.log(widget.getTheme());
```
#### Returns[​](#returns-29)
[`ThemeName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#themename)

A theme name. The name of the current theme.

### headerReady[​](#headerready)
▸ headerReady(): `Promise`<`void`>

A promise that resolves if and when the header is ready to be used.

#### Returns[​](#returns-30)
`Promise`<`void`>

### hideAllDrawingTools[​](#hidealldrawingtools)
▸ hideAllDrawingTools(): [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

Get a watched value that can be used to read/write/subscribe to the state of the "Hide All Drawing Tools" button.

#### Returns[​](#returns-31)
[`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

A watched value of the state of the "Hide All Drawing Tools" button.

### intervalSync[​](#intervalsync)
▸ intervalSync(): [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

Only available in Trading Platform. Get a watched value that can be used to read/write/subscribe to the state of the interval sync between charts.

Example

```
widget.intervalSync().setValue(true);
```
#### Returns[​](#returns-32)
[`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

A watched value of the state of the interval sync.

### layout[​](#layout)
▸ layout(): [`LayoutType`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#layouttype)

Get the current chart layout type.

#### Returns[​](#returns-33)
[`LayoutType`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#layouttype)

A string representation of the current layout type. E.g. `'2h'` for two charts split vertically.

### layoutName[​](#layoutname)
▸ layoutName(): `string`

Get the name of the current chart layout. The return value will be `undefined` if the current layout has not been saved.

#### Returns[​](#returns-34)
`string`

A string of the name of the current chart layout.

### load[​](#load)
▸ load(`state`, `extendedData?`): `Promise`<`void`>

Loads the chart state from a object. This method is part of the low-level save/load API.

#### Parameters[​](#parameters-13)
NameTypeDescription`state``object`A chart state object to load.`extendedData?`[`SavedStateMetaInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SavedStateMetaInfo)A optional object of information about the saved state.
#### Returns[​](#returns-35)
`Promise`<`void`>

### loadChartFromServer[​](#loadchartfromserver)
▸ loadChartFromServer(`chartRecord`): `Promise`<`void`>

Load a saved chart from the server.

#### Parameters[​](#parameters-14)
NameTypeDescription`chartRecord`[`SaveLoadChartRecord`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SaveLoadChartRecord)A chart information object (returned by [getSavedCharts](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#getsavedcharts)).
#### Returns[​](#returns-36)
`Promise`<`void`>

### lockAllDrawingTools[​](#lockalldrawingtools)
▸ lockAllDrawingTools(): [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

Get a watched value that can be used to read/write/subscribe to the state of the "Lock All Drawing Tools" button.

#### Returns[​](#returns-37)
[`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

A watched value of the state of the "Lock All Drawing Tools" button.

### magnetEnabled[​](#magnetenabled)
▸ magnetEnabled(): [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

Get a watched value that can be used to read/write/subscribe to the state of the magnet.

#### Returns[​](#returns-38)
[`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

A watched value of the state of the magnet.

### magnetMode[​](#magnetmode)
▸ magnetMode(): [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`number`>

Get a watched value that can be used to read/write/subscribe to the state of the magnet mode.

#### Returns[​](#returns-39)
[`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`number`>

A watched value of the state of the magnet mode.

### mainSeriesPriceFormatter[​](#mainseriespriceformatter)
▸ mainSeriesPriceFormatter(): [`INumberFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.INumberFormatter)

Get the price formatter for the main series. You can use this to format prices as the char

#### Returns[​](#returns-40)
[`INumberFormatter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.INumberFormatter)

### navigationButtonsVisibility[​](#navigationbuttonsvisibility)
▸ navigationButtonsVisibility(): [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<[`VisibilityType`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.VisibilityType)>

Get a watched value that can be used to read/write/subscribe to the state of the navigation buttons.

#### Returns[​](#returns-41)
[`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<[`VisibilityType`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.VisibilityType)>

A watched value of the state of the navigation buttons.

### news[​](#news)
▸ news(): `Promise`<[`INewsApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.INewsApi)>

Trading Platform only. Get a promise that resolves with an API object for interacting with the widgetbar (right sidebar) news widget.

#### Returns[​](#returns-42)
`Promise`<[`INewsApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.INewsApi)>

An API object for interacting with the widgetbar (right sidebar) widget.

### onChartReady[​](#onchartready)
▸ onChartReady(`callback`): `void`

The library will call `callback` when the chart is ready to be used.

#### Parameters[​](#parameters-15)
NameTypeDescription`callback`[`EmptyCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#emptycallback)A function that will be called when the chart is ready to be used.
#### Returns[​](#returns-43)
`void`

### onContextMenu[​](#oncontextmenu)
▸ onContextMenu(`callback`): `void`

The widget will call the callback function each time the widget wants to display a context menu.
See also [ChartingLibraryWidgetOptions.context_menu](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#context_menu).
Example

```
widget.onChartReady(function() {    widget.onContextMenu(function(unixtime, price) {        return [{            position: "top",            text: "First top menu item, time: " + unixtime + ", price: " + price,            click: function() { alert("First clicked."); }        },        { text: "-", position: "top" }, // Adds a separator between buttons        { text: "-Paste" },             // Removes the existing item from the menu        {            position: "top",            text: "Second top menu item 2",            click: function() { alert("Second clicked."); }        }, {            position: "bottom",            text: "Bottom menu item",            click: function() { alert("Third clicked."); }        }];    });});
```
#### Parameters[​](#parameters-16)
NameTypeDescription`callback`(`unixTime`: `number`, `price`: `number`) => [`ContextMenuItem`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ContextMenuItem)[]A function called with the time and price of the location on the chart that triggered the context menu. The array of objects returned will add or remove items from the context menu.
#### Returns[​](#returns-44)
`void`

### onGrayedObjectClicked[​](#ongrayedobjectclicked)
▸ onGrayedObjectClicked(`callback`): `void`

The library will call `callback` when a greyed-out drawing tool or study is clicked.

#### Parameters[​](#parameters-17)
NameTypeDescription`callback`(`obj`: [`GrayedObject`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.GrayedObject)) => `void`A function that will be called when a greyed-out drawing tool or study is clicked.
#### Returns[​](#returns-45)
`void`

### onShortcut[​](#onshortcut)
▸ onShortcut(`shortCut`, `callback`): `void`

This method specifies an action that happens when a user presses certain keys.
It allows you to override the built‑in shortcuts or specify custom ones.
To do this, pass a keyboard shortcut and a callback function as parameters.
The library invokes the callback when the `shortCut` keys are pressed.
Note that the `shortCut` argument depends on the key types. Refer to the [Manage shortcuts](https://www.tradingview.com/charting-library-docs/latest/getting_started/Shortcuts#manage-shortcuts) section for more information and examples.

#### Parameters[​](#parameters-18)
NameTypeDescription`shortCut``string` | `number` | (`string` | `number`)[]A number, a string, or an array of numbers and strings.`callback`[`EmptyCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#emptycallback)A function that is called when the `shortCut` keys are pressed.
#### Returns[​](#returns-46)
`void`

### paneButtonsVisibility[​](#panebuttonsvisibility)
▸ paneButtonsVisibility(): [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<[`VisibilityType`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.VisibilityType)>

Get a watched value that can be used to read/write/subscribe to the state of the pane buttons.

#### Returns[​](#returns-47)
[`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<[`VisibilityType`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.VisibilityType)>

A watched value of the state of the pane buttons.

### remove[​](#remove)
▸ remove(): `void`

Remove the widget and all its data from the page. The widget cannot be interacted with after it has been removed.

#### Returns[​](#returns-48)
`void`

### removeButton[​](#removebutton)
▸ removeButton(`buttonIdOrHtmlElement`): `void`

Remove a button from the top toolbar. This should be called after [headerReady](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#headerready) has resolved.

Example

```
widget.headerReady().then(function() {    var button = widget.createButton();    widget.removeButton(button)});
```
#### Parameters[​](#parameters-19)
NameTypeDescription`buttonIdOrHtmlElement``string` | `HTMLElement`The button link or id that you receive from createButton method.
#### Returns[​](#returns-49)
`void`

### removeChartFromServer[​](#removechartfromserver)
▸ removeChartFromServer(`chartId`, `onCompleteCallback`): `void`

Remove a saved chart from the server.

#### Parameters[​](#parameters-20)
NameTypeDescription`chartId``string` | `number`A chart ID from a [SaveLoadChartRecord](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SaveLoadChartRecord) (returned by [getSavedCharts](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#getsavedcharts)).`onCompleteCallback`[`EmptyCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#emptycallback)A callback function called when the chart is successfully saved.
#### Returns[​](#returns-50)
`void`

### resetCache[​](#resetcache)
▸ resetCache(): `void`

Reset cached bar data from the datafeed, for all symbols.

This has the same effect as calling [`onResetCacheNeededCallback`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IDatafeedChartApi#subscribebars) for all symbol and resolution combinations at once.

#### Returns[​](#returns-51)
`void`

### resetLayoutSizes[​](#resetlayoutsizes)
▸ resetLayoutSizes(`disableUndo?`): `void`

Resets the sizes of all charts within a multiple-chart layout back to their initial default values.
This action redistributes the space equally among all charts to ensure consistency in layout design.
#### Parameters[​](#parameters-21)
NameTypeDescription`disableUndo?``boolean`When set to true, the reset action is not added to the undo stack. Hence, the user cannot undo the reset operation.
#### Returns[​](#returns-52)
`void`

### save[​](#save)
▸ save(`callback`, `options?`): `void`

Saves the chart state to a object. This method is part of the low-level save/load API.

#### Parameters[​](#parameters-22)
NameTypeDescription`callback`(`state`: `object`) => `void`A function called with the chart state as the first argument.`options?`[`SaveChartOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SaveChartOptions)Options for customising the saved data.
#### Returns[​](#returns-53)
`void`

### saveChartToServer[​](#savecharttoserver)
▸ saveChartToServer(`onComplete?`, `onFail?`, `options?`): `void`

Save the current chart to the server.

#### Parameters[​](#parameters-23)
NameTypeDescription`onComplete?`[`EmptyCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#emptycallback)An optional callback function called when the chart is successfully saved.`onFail?`(`error`: [`SaveChartErrorInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SaveChartErrorInfo)) => `void`An optional callback function called when the chart fails to save.`options?`[`SaveChartToServerOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SaveChartToServerOptions)An optional object of options for saving the chart.
#### Returns[​](#returns-54)
`void`

### selectLineTool[​](#selectlinetool)
▸ selectLineTool(`linetool`, `options?`): `Promise`<`void`>

Select an icon. It's the same as clicking on the corresponding button in the left toolbar.

#### Parameters[​](#parameters-24)
NameTypeDescription`linetool``"icon"`An icon drawing tool.`options?`[`IconOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IconOptions)An optional object with options.
#### Returns[​](#returns-55)
`Promise`<`void`>

▸ selectLineTool(`linetool`): `Promise`<`void`>

Select a drawing or a cursor. It's the same as clicking on the corresponding button in the left toolbar.

#### Parameters[​](#parameters-25)
NameTypeDescription`linetool``Omit`<`"icon"`, [`SupportedLineTools`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#supportedlinetools)>A drawing or cursor to select (excluding 'icon')
#### Returns[​](#returns-56)
`Promise`<`void`>

▸ selectLineTool(`linetool`, `options?`): `Promise`<`void`>

Select the Icon line tool. It's the same as clicking on the corresponding button in the left toolbar.

#### Parameters[​](#parameters-26)
NameTypeDescription`linetool``"icon"`Icon line tool.`options?`[`IconOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IconOptions)An optional object with options. Currently only used for the 'icon' drawing.
#### Returns[​](#returns-57)
`Promise`<`void`>

▸ selectLineTool(`linetool`, `options?`): `Promise`<`void`>

Select the Emoji line tool. It's the same as clicking on the corresponding button in the left toolbar.

#### Parameters[​](#parameters-27)
NameTypeDescription`linetool``"emoji"`Emoji line tool.`options?`[`EmojiOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.EmojiOptions)Options for the Emoji line tool
#### Returns[​](#returns-58)
`Promise`<`void`>

▸ selectLineTool(`linetool`, `options?`): `Promise`<`void`>

Select a drawing, icon, or a cursor. It's the same as clicking on the corresponding button in the left toolbar.

#### Parameters[​](#parameters-28)
NameTypeDescription`linetool`[`SupportedLineTools`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#supportedlinetools)A drawing or cursor to select.`options?`[`EmojiOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.EmojiOptions) | [`IconOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IconOptions)An optional object with options.
#### Returns[​](#returns-59)
`Promise`<`void`>

### selectedLineTool[​](#selectedlinetool)
▸ selectedLineTool(): [`SupportedLineTools`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#supportedlinetools)

Get the currently selected drawing or cursor.

#### Returns[​](#returns-60)
[`SupportedLineTools`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#supportedlinetools)

An identifier for drawing or cursor.

### setActiveChart[​](#setactivechart)
▸ setActiveChart(`index`): `void`

Set which chart is currently active.
It is recommended that this method is only used when linked to a user action
which should change the active chart.
Use [chartsCount](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#chartscount) to determine the number of charts currently available.
If an invalid index is supplied (less than zero, or greater than the number of charts minus 1)
then this method will not change the active chart.
#### Parameters[​](#parameters-29)
NameTypeDescription`index``number`index of chart to set as the active chart. Index is zero-based.
#### Returns[​](#returns-61)
`void`

### setCSSCustomProperty[​](#setcsscustomproperty)
▸ setCSSCustomProperty(`customPropertyName`, `value`): `void`

Sets the value for a CSS custom property.

Example:

```
widget.setCSSCustomProperty('--my-theme-color', '#123AAA');
```
#### Parameters[​](#parameters-30)
NameTypeDescription`customPropertyName``string`A string representing the CSS custom property name. It is expected that the name should start with a double hyphen ('--').`value``string`A string containing the new property value.
#### Returns[​](#returns-62)
`void`

### setDebugMode[​](#setdebugmode)
▸ setDebugMode(`enabled`): `void`

Enable or disable writing detailed [Datafeed API](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/) logs into the browser console.

#### Parameters[​](#parameters-31)
NameTypeDescription`enabled``boolean`A boolean flag. `true` to enable debug mode, `false` to disable.
#### Returns[​](#returns-63)
`void`

### setLayout[​](#setlayout)
▸ setLayout(`layout`): `void`

Set the current chart layout type.

#### Parameters[​](#parameters-32)
NameType`layout`[`LayoutType`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#layouttype)
#### Returns[​](#returns-64)
`void`

`Params`

layout A string representation of the new layout type. E.g. `'2h'` for two charts split vertically.

### setSymbol[​](#setsymbol)
▸ setSymbol(`symbol`, `interval`, `callback`): `void`

Set the symbol and resolution of the active chart.

#### Parameters[​](#parameters-33)
NameTypeDescription`symbol``string`A symbol to load.`interval`[`ResolutionString`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#resolutionstring)A interval (resolution) to load.`callback`[`EmptyCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#emptycallback)A callback. Called when the symbol's data has finished loading.
#### Returns[​](#returns-65)
`void`

### showConfirmDialog[​](#showconfirmdialog)
▸ showConfirmDialog(`params`): `void`

Show a dialog with custom title and text along with "OK" and "CANCEL" buttons.

#### Parameters[​](#parameters-34)
NameTypeDescription`params`[`DialogParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.DialogParams)<(`confirmed`: `boolean`) => `void`>A object of options for the created dialog.
#### Returns[​](#returns-66)
`void`

### showLoadChartDialog[​](#showloadchartdialog)
▸ showLoadChartDialog(): `void`

Show the "Load Chart Layout" dialog.

#### Returns[​](#returns-67)
`void`

### showNoticeDialog[​](#shownoticedialog)
▸ showNoticeDialog(`params`): `void`

Show a dialog with custom title and text along with an "OK" buttons.

#### Parameters[​](#parameters-35)
NameTypeDescription`params`[`DialogParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.DialogParams)<() => `void`>A object of options for the created dialog.
#### Returns[​](#returns-68)
`void`

### showSaveAsChartDialog[​](#showsaveaschartdialog)
▸ showSaveAsChartDialog(): `void`

Show the "Copy Chart Layout" dialog.

#### Returns[​](#returns-69)
`void`

### startFullscreen[​](#startfullscreen)
▸ startFullscreen(): `void`

Set the chart into fullscreen mode (if it isn't already).

#### Returns[​](#returns-70)
`void`

### subscribe[​](#subscribe)
▸ subscribe<`EventName`>(`event`, `callback`): `void`

Subscribe to library events.

#### Type parameters[​](#type-parameters-1)
NameType`EventName`extends keyof [`SubscribeEventsMap`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SubscribeEventsMap)
#### Parameters[​](#parameters-36)
NameTypeDescription`event``EventName`A event to subscribe to.`callback`[`SubscribeEventsMap`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SubscribeEventsMap)[`EventName`]A callback that will be called when the event happens.
#### Returns[​](#returns-71)
`void`

### supportedChartTypes[​](#supportedcharttypes)
▸ supportedChartTypes(): [`IWatchedValueReadonly`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValueReadonly)<[`ChartStyle`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.ChartStyle)[]>

This method returns a readonly WatchedValue ([IWatchedValueReadonly](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValueReadonly))
object that can be used to read/watch the current supported chart types
([SeriesType](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.SeriesType)) for an active chart.
The chart type is returned as a number.
You can see which number corresponds to which chart type in the
[Overrides](https://www.tradingview.com/charting-library-docs/latest/customization/overrides/)
documentation for `mainSeriesProperties.style`.
#### Returns[​](#returns-72)
[`IWatchedValueReadonly`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValueReadonly)<[`ChartStyle`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.ChartStyle)[]>

### symbolInterval[​](#symbolinterval)
▸ symbolInterval(): [`SymbolIntervalResult`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SymbolIntervalResult)

Get the symbol and interval of the active chart.

#### Returns[​](#returns-73)
[`SymbolIntervalResult`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SymbolIntervalResult)

### symbolSync[​](#symbolsync)
▸ symbolSync(): [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

Only available in Trading Platform. Get a watched value that can be used to read/write/subscribe to the state of the symbol sync between charts.

Example

```
if (widget.symbolSync().value()) {    // ...}
```
#### Returns[​](#returns-74)
[`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

A watched value of the state of the symbol sync.

### takeClientScreenshot[​](#takeclientscreenshot)
▸ takeClientScreenshot(`options?`): `Promise`<`HTMLCanvasElement`>

Create a snapshot of the chart and return it as a canvas.
Use this method to [implement your logic](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Snapshots#implement-your-logic) for taking snapshots.
#### Parameters[​](#parameters-37)
NameTypeDescription`options?``Partial`<[`ClientSnapshotOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ClientSnapshotOptions)>An optional object that customizes the returned snapshot.
#### Returns[​](#returns-75)
`Promise`<`HTMLCanvasElement`>

A promise containing a `HTMLCanvasElement` of the snapshot.

### takeScreenshot[​](#takescreenshot)
▸ takeScreenshot(): `void`

Create a snapshot of the chart and upload it to the server.
When it is ready callback functions subscribed to the `'onScreenshotReady'` event using [subscribe](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#subscribe) will be called.
The URL of the snapshot will be passed as an argument to the callback function.
#### Returns[​](#returns-76)
`void`

### timeHoursFormat[​](#timehoursformat)
▸ timeHoursFormat(): [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<[`TimeHoursFormat`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.TimeHoursFormat)>

Get a watched value that can be used to read/write/subscribe to the state of the timeHours format.

#### Returns[​](#returns-77)
[`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<[`TimeHoursFormat`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Charting_Library.TimeHoursFormat)>

### timeSync[​](#timesync)
▸ timeSync(): [`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

Only available in Trading Platform. Get a watched value that can be used to read/write/subscribe to the state of the time sync between charts.

Example

```
widget.timeSync().setValue(true);
```
#### Returns[​](#returns-78)
[`IWatchedValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchedValue)<`boolean`>

A watched value of the state of the time sync.

### undoRedoState[​](#undoredostate)
▸ undoRedoState(): [`UndoRedoState`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.UndoRedoState)

Get the state of the undo/redo stack.

#### Returns[​](#returns-79)
[`UndoRedoState`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.UndoRedoState)

### unloadUnusedCharts[​](#unloadunusedcharts)
▸ unloadUnusedCharts(): `void`

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
#### Returns[​](#returns-80)
`void`

void

### unsubscribe[​](#unsubscribe)
▸ unsubscribe<`EventName`>(`event`, `callback`): `void`

Unsubscribe from library events.

#### Type parameters[​](#type-parameters-2)
NameType`EventName`extends keyof [`SubscribeEventsMap`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SubscribeEventsMap)
#### Parameters[​](#parameters-38)
NameTypeDescription`event``EventName`A event to unsubscribe from.`callback`[`SubscribeEventsMap`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SubscribeEventsMap)[`EventName`]A callback to unsubscribe. Must be the same reference as a callback passed to [subscribe](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#subscribe).
#### Returns[​](#returns-81)
`void`

### watchList[​](#watchlist)
▸ watchList(): `Promise`<[`IWatchListApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchListApi)>

Trading Platform only. Get a promise that resolves with an API object for interacting with the widgetbar (right sidebar) watchlist.

Example

```
const watchlistApi = await widget.watchList();const activeListId = watchlistApi.getActiveListId();const currentListItems = watchlistApi.getList(activeListId);// append new section and item to the current watchlistwatchlistApi.updateList(activeListId, [...currentListItems, '###NEW SECTION', 'AMZN']);
```
#### Returns[​](#returns-82)
`Promise`<[`IWatchListApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatchListApi)>

An API object for interacting with the widgetbar (right sidebar) watchlist.

### watermark[​](#watermark)
▸ watermark(): [`IWatermarkApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatermarkApi)

Get an API object for adjusting the watermarks present on the charts.
This can only be accessed when the chart is ready to be used. ([onChartReady](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#onchartready))
#### Returns[​](#returns-83)
[`IWatermarkApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWatermarkApi)

An API object for adjusting the watermark settings.

### widgetbar[​](#widgetbar)
▸ widgetbar(): `Promise`<[`IWidgetbarApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWidgetbarApi)>

Trading Platform only. Get a promise that resolves with an API object for interacting with the widgetbar (right sidebar).

#### Returns[​](#returns-84)
`Promise`<[`IWidgetbarApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IWidgetbarApi)>

An API object for interacting with the widgetbar (right sidebar).

- [Methods](#methods)[activeChart](#activechart)- [activeChartIndex](#activechartindex)- [addCustomCSSFile](#addcustomcssfile)- [applyOverrides](#applyoverrides)- [applyStudiesOverrides](#applystudiesoverrides)- [changeTheme](#changetheme)- [chart](#chart)- [chartsCount](#chartscount)- [clearUndoHistory](#clearundohistory)- [closePopupsAndDialogs](#closepopupsanddialogs)- [createButton](#createbutton)- [createDropdown](#createdropdown)- [crosshairSync](#crosshairsync)- [currencyAndUnitVisibility](#currencyandunitvisibility)- [customSymbolStatus](#customsymbolstatus)- [customThemes](#customthemes)- [dateFormat](#dateformat)- [dateRangeSync](#daterangesync)- [drawOnAllChartsEnabled](#drawonallchartsenabled)- [exitFullscreen](#exitfullscreen)- [getCSSCustomPropertyValue](#getcsscustompropertyvalue)- [getIntervals](#getintervals)- [getLanguage](#getlanguage)- [getSavedCharts](#getsavedcharts)- [getStudiesList](#getstudieslist)- [getStudyInputs](#getstudyinputs)- [getStudyStyles](#getstudystyles)- [getTheme](#gettheme)- [headerReady](#headerready)- [hideAllDrawingTools](#hidealldrawingtools)- [intervalSync](#intervalsync)- [layout](#layout)- [layoutName](#layoutname)- [load](#load)- [loadChartFromServer](#loadchartfromserver)- [lockAllDrawingTools](#lockalldrawingtools)- [magnetEnabled](#magnetenabled)- [magnetMode](#magnetmode)- [mainSeriesPriceFormatter](#mainseriespriceformatter)- [navigationButtonsVisibility](#navigationbuttonsvisibility)- [news](#news)- [onChartReady](#onchartready)- [onContextMenu](#oncontextmenu)- [onGrayedObjectClicked](#ongrayedobjectclicked)- [onShortcut](#onshortcut)- [paneButtonsVisibility](#panebuttonsvisibility)- [remove](#remove)- [removeButton](#removebutton)- [removeChartFromServer](#removechartfromserver)- [resetCache](#resetcache)- [resetLayoutSizes](#resetlayoutsizes)- [save](#save)- [saveChartToServer](#savecharttoserver)- [selectLineTool](#selectlinetool)- [selectedLineTool](#selectedlinetool)- [setActiveChart](#setactivechart)- [setCSSCustomProperty](#setcsscustomproperty)- [setDebugMode](#setdebugmode)- [setLayout](#setlayout)- [setSymbol](#setsymbol)- [showConfirmDialog](#showconfirmdialog)- [showLoadChartDialog](#showloadchartdialog)- [showNoticeDialog](#shownoticedialog)- [showSaveAsChartDialog](#showsaveaschartdialog)- [startFullscreen](#startfullscreen)- [subscribe](#subscribe)- [supportedChartTypes](#supportedcharttypes)- [symbolInterval](#symbolinterval)- [symbolSync](#symbolsync)- [takeClientScreenshot](#takeclientscreenshot)- [takeScreenshot](#takescreenshot)- [timeHoursFormat](#timehoursformat)- [timeSync](#timesync)- [undoRedoState](#undoredostate)- [unloadUnusedCharts](#unloadunusedcharts)- [unsubscribe](#unsubscribe)- [watchList](#watchlist)- [watermark](#watermark)- [widgetbar](#widgetbar)