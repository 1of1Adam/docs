---
title: "Interface: SubscribeEventsMap | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SubscribeEventsMap"
extracted_at: "2025-06-22T09:48:12.013Z"
---

- [](/charting-library-docs/)- Interfaces- SubscribeEventsMapOn this page# Interface: SubscribeEventsMap[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).SubscribeEventsMap

## Properties[​](#properties)
### activeChartChanged[​](#activechartchanged)
• activeChartChanged: (`chartIndex`: `number`) => `void`

Active chart has changed.
Note: this event is only applicable to Trading Platform.
#### Type declaration[​](#type-declaration)
▸ (`chartIndex`): `void`

Parameters[​](#parameters)
NameTypeDescription`chartIndex``number`index of the active chart
Returns[​](#returns)
`void`

### add_compare[​](#add_compare)
• add_compare: [`EmptyCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#emptycallback)

A compare instrument has been added

### chart_load_requested[​](#chart_load_requested)
• chart_load_requested: (`savedData`: `object`) => `void`

New chart is about to be loaded

#### Type declaration[​](#type-declaration-1)
▸ (`savedData`): `void`

Parameters[​](#parameters-1)
NameTypeDescription`savedData``object`chart data about to be loaded
Returns[​](#returns-1)
`void`

### chart_loaded[​](#chart_loaded)
• chart_loaded: [`EmptyCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#emptycallback)

Chart has finished loading

### chart_theme_changed[​](#chart_theme_changed)
• chart_theme_changed: (`themeName`: `string`, `isStandardTheme`: `boolean`, `onlyActiveChart`: `boolean`) => `void`

Fired when the chart theme is updated. This event can be triggered in several ways:

- When a user applies a saved [chart template](https://www.tradingview.com/charting-library-docs/latest/saving_loading/#chart-templates).
- When the chart theme is reset to the default settings. (`isStandardTheme` parameter will be true)
- When the [IChartingLibraryWidget.changeTheme](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#changetheme) method is called.
- When the [IChartWidgetApi.loadChartTemplate](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#loadcharttemplate) method is called.

#### Type declaration[​](#type-declaration-2)
▸ (`themeName`, `isStandardTheme`, `onlyActiveChart`): `void`

Parameters[​](#parameters-2)
NameTypeDescription`themeName``string`The name of the chart theme or template that was applied.`isStandardTheme``boolean``true` if the default built-in theme was restored; `false`, if a custom chart template was applied.`onlyActiveChart``boolean``false`, when applied to all charts
Returns[​](#returns-2)
`void`

### compare_add[​](#compare_add)
• compare_add: [`EmptyCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#emptycallback)

A compare dialog has been shown

### dragEnd[​](#dragend)
• dragEnd: [`EmptyCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#emptycallback)

Drag end

### dragStart[​](#dragstart)
• dragStart: (`params`: [`DragStartParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.DragStartParams)) => `void`

Drag start

#### Type declaration[​](#type-declaration-3)
▸ (`params`): `void`

Parameters[​](#parameters-3)
NameType`params`[`DragStartParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.DragStartParams)
Returns[​](#returns-3)
`void`

### drawing[​](#drawing)
• drawing: (`params`: [`StudyOrDrawingAddedToChartEventParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyOrDrawingAddedToChartEventParams)) => `void`

A drawing has been added to a chart.

#### Type declaration[​](#type-declaration-4)
▸ (`params`): `void`

Parameters[​](#parameters-4)
NameTypeDescription`params`[`StudyOrDrawingAddedToChartEventParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyOrDrawingAddedToChartEventParams)The arguments contain an object with the `value` field that corresponds with the name of the drawing.
Returns[​](#returns-4)
`void`

### drawing_event[​](#drawing_event)
• drawing_event: (`sourceId`: [`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid), `drawingEventType`: [`DrawingEventType`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#drawingeventtype)) => `void`

Drawing was hidden, shown, moved, removed, clicked, or created

#### Type declaration[​](#type-declaration-5)
▸ (`sourceId`, `drawingEventType`): `void`

Parameters[​](#parameters-5)
NameTypeDescription`sourceId`[`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)drawing ID`drawingEventType`[`DrawingEventType`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#drawingeventtype)drawing event type
Returns[​](#returns-5)
`void`

### edit_object_dialog[​](#edit_object_dialog)
• edit_object_dialog: (`params`: [`EditObjectDialogEventParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.EditObjectDialogEventParams)) => `void`

Chart / Study Properties dialog is shown

#### Type declaration[​](#type-declaration-6)
▸ (`params`): `void`

Parameters[​](#parameters-6)
NameTypeDescription`params`[`EditObjectDialogEventParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.EditObjectDialogEventParams)meta information about the dialog type and the title of the chart or study
Returns[​](#returns-6)
`void`

### indicators_dialog[​](#indicators_dialog)
• indicators_dialog: [`EmptyCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#emptycallback)

Indicators dialog is shown

### layout_about_to_be_changed[​](#layout_about_to_be_changed)
• layout_about_to_be_changed: (`newLayoutType`: [`LayoutType`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#layouttype)) => `void`

Amount or placement of the charts is about to be changed.
Note: this event is only applicable to Trading Platform.
#### Type declaration[​](#type-declaration-7)
▸ (`newLayoutType`): `void`

Parameters[​](#parameters-7)
NameTypeDescription`newLayoutType`[`LayoutType`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#layouttype)whether the layout is single or multi-chart
Returns[​](#returns-7)
`void`

### layout_changed[​](#layout_changed)
• layout_changed: [`EmptyCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#emptycallback)

Amount or placement of the charts is changed.
Note: this event is only applicable to Trading Platform.

### load_study_template[​](#load_study_template)
• load_study_template: [`EmptyCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#emptycallback)

A study template has been loaded

### mouse_down[​](#mouse_down)
• mouse_down: (`params`: [`MouseEventParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.MouseEventParams)) => `void`

Mouse button has been pressed

#### Type declaration[​](#type-declaration-8)
▸ (`params`): `void`

Parameters[​](#parameters-8)
NameType`params`[`MouseEventParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.MouseEventParams)
Returns[​](#returns-8)
`void`

### mouse_up[​](#mouse_up)
• mouse_up: (`params`: [`MouseEventParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.MouseEventParams)) => `void`

Mouse button has been released

#### Type declaration[​](#type-declaration-9)
▸ (`params`): `void`

Parameters[​](#parameters-9)
NameType`params`[`MouseEventParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.MouseEventParams)
Returns[​](#returns-9)
`void`

### onAutoSaveNeeded[​](#onautosaveneeded)
• onAutoSaveNeeded: [`EmptyCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#emptycallback)

User has changed the chart. `Chart change` means any user action that can be undone.
The callback function will not be called more than once every 5 seconds. See also `auto_save_delay` within the Widget constructor options ([ChartingLibraryWidgetOptions.auto_save_delay](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#auto_save_delay)).

### onMarkClick[​](#onmarkclick)
• onMarkClick: (`markId`: `string` | `number`) => `void`

User has clicked on a 'mark on a bar'.

#### Type declaration[​](#type-declaration-10)
▸ (`markId`): `void`

Parameters[​](#parameters-10)
NameTypeDescription`markId``string` | `number`ID of the clicked mark
Returns[​](#returns-10)
`void`

### onPlusClick[​](#onplusclick)
• onPlusClick: (`params`: [`PlusClickParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PlusClickParams)) => `void`

User clicked the Plus button on the [price scale](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Price-Scale#quick-trading).

#### Type declaration[​](#type-declaration-11)
▸ (`params`): `void`

Parameters[​](#parameters-11)
NameTypeDescription`params`[`PlusClickParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PlusClickParams)coordinates, price, and symbol information
Returns[​](#returns-11)
`void`

### onScreenshotReady[​](#onscreenshotready)
• onScreenshotReady: (`url`: `string`) => `void`

A screenshot URL has been returned by the server

#### Type declaration[​](#type-declaration-12)
▸ (`url`): `void`

Parameters[​](#parameters-12)
NameTypeDescription`url``string`url of the screenshot
Returns[​](#returns-12)
`void`

### onSelectedLineToolChanged[​](#onselectedlinetoolchanged)
• onSelectedLineToolChanged: [`EmptyCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#emptycallback)

Selected drawing tool has changed

### onTick[​](#ontick)
• onTick: (`tick`: [`Bar`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.Bar)) => `void`

Last bar has been updated

#### Type declaration[​](#type-declaration-13)
▸ (`tick`): `void`

Parameters[​](#parameters-13)
NameTypeDescription`tick`[`Bar`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.Bar)data for last bar
Returns[​](#returns-13)
`void`

### onTimescaleMarkClick[​](#ontimescalemarkclick)
• onTimescaleMarkClick: (`markId`: `string` | `number`) => `void`

User clicked a 'timescale mark'.

#### Type declaration[​](#type-declaration-14)
▸ (`markId`): `void`

Parameters[​](#parameters-14)
NameTypeDescription`markId``string` | `number`ID of the clicked timescale mark
Returns[​](#returns-14)
`void`

### panes_height_changed[​](#panes_height_changed)
• panes_height_changed: [`EmptyCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#emptycallback)

Panes' size has changed.

### panes_order_changed[​](#panes_order_changed)
• panes_order_changed: [`EmptyCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#emptycallback)

Panes' order has changed.

### redo[​](#redo)
• redo: [`EmptyCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#emptycallback)

Redo action occurred

### reset_scales[​](#reset_scales)
• reset_scales: [`EmptyCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#emptycallback)

Reset scales button has been clicked

### series_event[​](#series_event)
• series_event: (`seriesEventType`: `"price_scale_changed"`) => `void`

An event related to the series has occurred.

#### Type declaration[​](#type-declaration-15)
▸ (`seriesEventType`): `void`

Parameters[​](#parameters-15)
NameTypeDescription`seriesEventType``"price_scale_changed"`series event type
Returns[​](#returns-15)
`void`

### series_properties_changed[​](#series_properties_changed)
• series_properties_changed: (`id`: [`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)) => `void`

Main series properties have changed.

#### Type declaration[​](#type-declaration-16)
▸ (`id`): `void`

Parameters[​](#parameters-16)
NameTypeDescription`id`[`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)entity ID
Returns[​](#returns-16)
`void`

### study[​](#study)
• study: (`params`: [`StudyOrDrawingAddedToChartEventParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyOrDrawingAddedToChartEventParams)) => `void`

An indicator has been added to a chart.

#### Type declaration[​](#type-declaration-17)
▸ (`params`): `void`

Parameters[​](#parameters-17)
NameTypeDescription`params`[`StudyOrDrawingAddedToChartEventParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyOrDrawingAddedToChartEventParams)The arguments contain an object with the `value` field that corresponds with the name of the indicator.
Returns[​](#returns-17)
`void`

### study_dialog_save_defaults[​](#study_dialog_save_defaults)
• study_dialog_save_defaults: (`id`: [`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)) => `void`

The Save as default option is selected in the drop-down menu of the indicator settings.

#### Type declaration[​](#type-declaration-18)
▸ (`id`): `void`

Parameters[​](#parameters-18)
NameTypeDescription`id`[`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)entity ID
Returns[​](#returns-18)
`void`

### study_event[​](#study_event)
• study_event: (`entityId`: [`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid), `studyEventType`: [`StudyEventType`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#studyeventtype)) => `void`

An event related to the study has occurred.

#### Type declaration[​](#type-declaration-19)
▸ (`entityId`, `studyEventType`): `void`

Parameters[​](#parameters-19)
NameTypeDescription`entityId`[`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)study ID`studyEventType`[`StudyEventType`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#studyeventtype)study event type
Returns[​](#returns-19)
`void`

### study_properties_changed[​](#study_properties_changed)
• study_properties_changed: (`id`: [`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)) => `void`

Study properties have changed.

#### Type declaration[​](#type-declaration-20)
▸ (`id`): `void`

Parameters[​](#parameters-20)
NameTypeDescription`id`[`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)entity ID
Returns[​](#returns-20)
`void`

### timeframe_interval[​](#timeframe_interval)
• timeframe_interval: (`range`: [`RangeOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RangeOptions)) => `void`

Time interval has been changed.
Can come from either the bottom toolbar or the setTimeFrame API.
#### Type declaration[​](#type-declaration-21)
▸ (`range`): `void`

Parameters[​](#parameters-21)
NameTypeDescription`range`[`RangeOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RangeOptions)Object that represents a selected time frame.
Returns[​](#returns-21)
`void`

### toggle_header[​](#toggle_header)
• toggle_header: (`isHidden`: `boolean`) => `void`

Chart header is shown/hidden

#### Type declaration[​](#type-declaration-22)
▸ (`isHidden`): `void`

Parameters[​](#parameters-22)
NameTypeDescription`isHidden``boolean`is the chart header currently hidden
Returns[​](#returns-22)
`void`

### toggle_sidebar[​](#toggle_sidebar)
• toggle_sidebar: (`isHidden`: `boolean`) => `void`

Drawing toolbar is shown/hidden

#### Type declaration[​](#type-declaration-23)
▸ (`isHidden`): `void`

Parameters[​](#parameters-23)
NameTypeDescription`isHidden``boolean`is the drawing toolbar currently hidden
Returns[​](#returns-23)
`void`

### undo[​](#undo)
• undo: [`EmptyCallback`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#emptycallback)

Undo action occurred

### undo_redo_state_changed[​](#undo_redo_state_changed)
• undo_redo_state_changed: (`state`: [`UndoRedoState`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.UndoRedoState)) => `void`

The Undo / Redo state has been changed.

#### Type declaration[​](#type-declaration-24)
▸ (`state`): `void`

Parameters[​](#parameters-24)
NameTypeDescription`state`[`UndoRedoState`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.UndoRedoState)state of the Undo/Redo stack
Returns[​](#returns-24)
`void`

### widgetbar_visibility_changed[​](#widgetbar_visibility_changed)
• widgetbar_visibility_changed: (`isVisible`: `boolean`) => `void`

Chart's widget bar is shown/hidden.

#### Type declaration[​](#type-declaration-25)
▸ (`isVisible`): `void`

Parameters[​](#parameters-25)
NameTypeDescription`isVisible``boolean`if the widget bar is currently hidden
Returns[​](#returns-25)
`void`

- [Properties](#properties)[activeChartChanged](#activechartchanged)- [add_compare](#add_compare)- [chart_load_requested](#chart_load_requested)- [chart_loaded](#chart_loaded)- [chart_theme_changed](#chart_theme_changed)- [compare_add](#compare_add)- [dragEnd](#dragend)- [dragStart](#dragstart)- [drawing](#drawing)- [drawing_event](#drawing_event)- [edit_object_dialog](#edit_object_dialog)- [indicators_dialog](#indicators_dialog)- [layout_about_to_be_changed](#layout_about_to_be_changed)- [layout_changed](#layout_changed)- [load_study_template](#load_study_template)- [mouse_down](#mouse_down)- [mouse_up](#mouse_up)- [onAutoSaveNeeded](#onautosaveneeded)- [onMarkClick](#onmarkclick)- [onPlusClick](#onplusclick)- [onScreenshotReady](#onscreenshotready)- [onSelectedLineToolChanged](#onselectedlinetoolchanged)- [onTick](#ontick)- [onTimescaleMarkClick](#ontimescalemarkclick)- [panes_height_changed](#panes_height_changed)- [panes_order_changed](#panes_order_changed)- [redo](#redo)- [reset_scales](#reset_scales)- [series_event](#series_event)- [series_properties_changed](#series_properties_changed)- [study](#study)- [study_dialog_save_defaults](#study_dialog_save_defaults)- [study_event](#study_event)- [study_properties_changed](#study_properties_changed)- [timeframe_interval](#timeframe_interval)- [toggle_header](#toggle_header)- [toggle_sidebar](#toggle_sidebar)- [undo](#undo)- [undo_redo_state_changed](#undo_redo_state_changed)- [widgetbar_visibility_changed](#widgetbar_visibility_changed)