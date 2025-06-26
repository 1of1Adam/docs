---
title: "Interface: IStudyApi | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IStudyApi"
extracted_at: "2025-06-22T09:39:41.249Z"
---

- [](/charting-library-docs/)- Interfaces- IStudyApiOn this page# Interface: IStudyApi[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).IStudyApi

API object for interacting with a study.

You can retrieve this interface by using the [IChartWidgetApi.getStudyById](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#getstudybyid) method

## Methods[​](#methods)
### applyOverrides[​](#applyoverrides)
▸ applyOverrides<`TOverrides`>(`overrides`): `void`

Override one or more of the indicator's properties.
Refer to [Indicator Overrides](https://www.tradingview.com/charting-library-docs/latest/customization/overrides/indicator-overrides#change-the-existing-indicator) for more information.
Overrides for built-in indicators are listed in [SingleIndicatorOverrides](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#singleindicatoroverrides).
#### Type parameters[​](#type-parameters)
NameType`TOverrides`extends `Partial`<[`SingleIndicatorOverrides`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#singleindicatoroverrides)>
#### Parameters[​](#parameters)
NameTypeDescription`overrides``TOverrides`Property values to override.
#### Returns[​](#returns)
`void`

### applyToEntireLayout[​](#applytoentirelayout)
▸ applyToEntireLayout(): `Promise`<`void`>

Copies the study to all charts in the layout.
Only applicable to multi-chart layouts (Trading Platform).
#### Returns[​](#returns-1)
`Promise`<`void`>

### bringToFront[​](#bringtofront)
▸ bringToFront(): `void`

Move the study visually in front of all other chart objects.

#### Returns[​](#returns-2)
`void`

### changePriceScale[​](#changepricescale)
▸ changePriceScale(`newPriceScale`): `void`

Change the price scale that the study is attached to.

#### Parameters[​](#parameters-1)
NameTypeDescription`newPriceScale`[`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid) | [`StudyPriceScale`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#studypricescale)Price scale identifier, or the ID of another study whose price scale the study should be moved to.
#### Returns[​](#returns-3)
`void`

### getInputValues[​](#getinputvalues)
▸ getInputValues(): [`StudyInputValueItem`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyInputValueItem)[]

Get current values of the study inputs.

#### Returns[​](#returns-4)
[`StudyInputValueItem`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyInputValueItem)[]

### getInputsInfo[​](#getinputsinfo)
▸ getInputsInfo(): [`StudyInputInformation`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyInputInformation)[]

Get descriptions of the study inputs.

#### Returns[​](#returns-5)
[`StudyInputInformation`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyInputInformation)[]

### getStyleInfo[​](#getstyleinfo)
▸ getStyleInfo(): [`StudyStyleInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyStyleInfo)

Get descriptions of study styles.

#### Returns[​](#returns-6)
[`StudyStyleInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyStyleInfo)

### getStyleValues[​](#getstylevalues)
▸ getStyleValues(): [`StudyStyleValues`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyStyleValues)

Get current values of the study styles.

#### Returns[​](#returns-7)
[`StudyStyleValues`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyStyleValues)

### isUserEditEnabled[​](#isusereditenabled)
▸ isUserEditEnabled(): `boolean`

Get if user editing is enabled for the study.

#### Returns[​](#returns-8)
`boolean`

`true` if editing is enabled, `false` otherwise.

### isVisible[​](#isvisible)
▸ isVisible(): `boolean`

Get if the study is visible.

#### Returns[​](#returns-9)
`boolean`

`true` if visible, `false` otherwise.

### mergeDown[​](#mergedown)
▸ mergeDown(): `void`

Merge the study into the pane below, if possible.

#### Returns[​](#returns-10)
`void`

### mergeUp[​](#mergeup)
▸ mergeUp(): `void`

Merge the study into the pane above, if possible.

#### Returns[​](#returns-11)
`void`

### onDataLoaded[​](#ondataloaded)
▸ onDataLoaded(): [`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<() => `void`>

Get a subscription that can be used to subscribe a callback when the study data has loaded.

#### Returns[​](#returns-12)
[`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<() => `void`>

A subscription.

Example:

```
studyApi.onDataLoaded().subscribe(    null,    () => console.log('Study data is loaded'),    true);
```

### onStudyError[​](#onstudyerror)
▸ onStudyError(): [`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<() => `void`>

Get a subscription that can be used to subscribe a callback when the study has an error.

#### Returns[​](#returns-13)
[`ISubscription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISubscription)<() => `void`>

A subscription.

Example:

```
studyApi.studyApi.onStudyError().subscribe(    null,    () => console.log('Study error'),    true);
```

### paneIndex[​](#paneindex)
▸ paneIndex(): `number`

Get the index of the pane that the study is attached to.

#### Returns[​](#returns-14)
`number`

The pane index.

### sendToBack[​](#sendtoback)
▸ sendToBack(): `void`

Move the study visually behind of all other chart objects.

#### Returns[​](#returns-15)
`void`

### setInputValues[​](#setinputvalues)
▸ setInputValues(`values`): `void`

Set the value of one or more study inputs.

#### Parameters[​](#parameters-2)
NameTypeDescription`values`[`StudyInputValueItem`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyInputValueItem)[]Study input values to set.
#### Returns[​](#returns-16)
`void`

### setUserEditEnabled[​](#setusereditenabled)
▸ setUserEditEnabled(`enabled`): `void`

Set if user editing is enabled for the study.

#### Parameters[​](#parameters-3)
NameTypeDescription`enabled``boolean``true` if editing should be enabled, `false` otherwise.
#### Returns[​](#returns-17)
`void`

### setVisible[​](#setvisible)
▸ setVisible(`visible`): `void`

Set the study visibility.

#### Parameters[​](#parameters-4)
NameTypeDescription`visible``boolean``true` if the study should be visible, `false` otherwise.
#### Returns[​](#returns-18)
`void`

### unmergeDown[​](#unmergedown)
▸ unmergeDown(): `void`

Unmerge the study into the pane below, if possible.

#### Returns[​](#returns-19)
`void`

### unmergeUp[​](#unmergeup)
▸ unmergeUp(): `void`

Unmerge the study into the pane above, if possible.

#### Returns[​](#returns-20)
`void`

- [Methods](#methods)[applyOverrides](#applyoverrides)- [applyToEntireLayout](#applytoentirelayout)- [bringToFront](#bringtofront)- [changePriceScale](#changepricescale)- [getInputValues](#getinputvalues)- [getInputsInfo](#getinputsinfo)- [getStyleInfo](#getstyleinfo)- [getStyleValues](#getstylevalues)- [isUserEditEnabled](#isusereditenabled)- [isVisible](#isvisible)- [mergeDown](#mergedown)- [mergeUp](#mergeup)- [onDataLoaded](#ondataloaded)- [onStudyError](#onstudyerror)- [paneIndex](#paneindex)- [sendToBack](#sendtoback)- [setInputValues](#setinputvalues)- [setUserEditEnabled](#setusereditenabled)- [setVisible](#setvisible)- [unmergeDown](#unmergedown)- [unmergeUp](#unmergeup)