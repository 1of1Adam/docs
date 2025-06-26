---
title: "Interface: IExternalSaveLoadAdapter | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IExternalSaveLoadAdapter#loadlinetoolsandgroups"
extracted_at: "2025-06-22T09:51:09.054Z"
---

- [](/charting-library-docs/)- Interfaces- IExternalSaveLoadAdapterOn this page# Interface: IExternalSaveLoadAdapter[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).IExternalSaveLoadAdapter

## Methods[​](#methods)
### getAllChartTemplates[​](#getallcharttemplates)
▸ getAllChartTemplates(): `Promise`<`string`[]>

Get names of all saved chart templates.

#### Returns[​](#returns)
`Promise`<`string`[]>

An array of names.

### getAllCharts[​](#getallcharts)
▸ getAllCharts(): `Promise`<[`ChartMetaInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartMetaInfo)[]>

Get all saved charts.

#### Returns[​](#returns-1)
`Promise`<[`ChartMetaInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartMetaInfo)[]>

Array of chart meta information

### getAllStudyTemplates[​](#getallstudytemplates)
▸ getAllStudyTemplates(): `Promise`<[`StudyTemplateMetaInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyTemplateMetaInfo)[]>

Get all saved study templates

#### Returns[​](#returns-2)
`Promise`<[`StudyTemplateMetaInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyTemplateMetaInfo)[]>

Array of study template meta information

### getChartContent[​](#getchartcontent)
▸ getChartContent(`chartId`): `Promise`<`string`>

Load the chart from the server

#### Parameters[​](#parameters)
NameTypeDescription`chartId``string` | `number`Unique ID of the chart to load (see [getAllCharts](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IExternalSaveLoadAdapter#getallcharts))
#### Returns[​](#returns-3)
`Promise`<`string`>

chart content contained in the `content` field when saving the chart ([ChartData](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartData))

### getChartTemplateContent[​](#getcharttemplatecontent)
▸ getChartTemplateContent(`templateName`): `Promise`<[`ChartTemplate`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartTemplate)>

Load a chart template from the server

#### Parameters[​](#parameters-1)
NameTypeDescription`templateName``string`The name of the template.
#### Returns[​](#returns-4)
`Promise`<[`ChartTemplate`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartTemplate)>

The chart template content.

### getDrawingTemplates[​](#getdrawingtemplates)
▸ getDrawingTemplates(`toolName`): `Promise`<`string`[]>

Get names of all saved drawing templates

#### Parameters[​](#parameters-2)
NameTypeDescription`toolName``string`name of the drawing tool
#### Returns[​](#returns-5)
`Promise`<`string`[]>

names of saved drawing templates

### getStudyTemplateContent[​](#getstudytemplatecontent)
▸ getStudyTemplateContent(`studyTemplateInfo`): `Promise`<`string`>

load a study template from the server

#### Parameters[​](#parameters-3)
NameType`studyTemplateInfo`[`StudyTemplateMetaInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyTemplateMetaInfo)
#### Returns[​](#returns-6)
`Promise`<`string`>

Study template `content`

### loadDrawingTemplate[​](#loaddrawingtemplate)
▸ loadDrawingTemplate(`toolName`, `templateName`): `Promise`<`string`>

Load a drawing template from the server

#### Parameters[​](#parameters-4)
NameTypeDescription`toolName``string`name of the drawing tool`templateName``string`name of the template
#### Returns[​](#returns-7)
`Promise`<`string`>

content of the drawing template

### loadLineToolsAndGroups[​](#loadlinetoolsandgroups)
▸ loadLineToolsAndGroups(`layoutId`, `chartId`, `requestType`, `requestContext`): `Promise`<`Partial`<[`LineToolsAndGroupsState`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LineToolsAndGroupsState)>>

Load drawings and drawing groups associated with a chart layout.

#### Parameters[​](#parameters-5)
NameTypeDescription`layoutId``string`The chart layout ID`chartId``string` | `number`The chart ID`requestType`[`LineToolsAndGroupsLoadRequestType`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#linetoolsandgroupsloadrequesttype)Type of load request`requestContext`[`LineToolsAndGroupsLoadRequestContext`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LineToolsAndGroupsLoadRequestContext)Additional information for the request
#### Returns[​](#returns-8)
`Promise`<`Partial`<[`LineToolsAndGroupsState`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LineToolsAndGroupsState)>>

The drawings and drawing groups state

### removeChart[​](#removechart)
▸ removeChart(`id`): `Promise`<`void`>

Remove a chart.

#### Parameters[​](#parameters-6)
NameTypeDescription`id``string` | `number`Unique ID of the chart (see [getAllCharts](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IExternalSaveLoadAdapter#getallcharts))
#### Returns[​](#returns-9)
`Promise`<`void`>

### removeChartTemplate[​](#removecharttemplate)
▸ removeChartTemplate(`templateName`): `Promise`<`void`>

Remove a chart template.

#### Parameters[​](#parameters-7)
NameTypeDescription`templateName``string`The name of the template.
#### Returns[​](#returns-10)
`Promise`<`void`>

### removeDrawingTemplate[​](#removedrawingtemplate)
▸ removeDrawingTemplate(`toolName`, `templateName`): `Promise`<`void`>

Remove a drawing template

#### Parameters[​](#parameters-8)
NameTypeDescription`toolName``string`name of the drawing tool`templateName``string`name of the template
#### Returns[​](#returns-11)
`Promise`<`void`>

### removeStudyTemplate[​](#removestudytemplate)
▸ removeStudyTemplate(`studyTemplateInfo`): `Promise`<`void`>

Remove a study template

#### Parameters[​](#parameters-9)
NameType`studyTemplateInfo`[`StudyTemplateMetaInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyTemplateMetaInfo)
#### Returns[​](#returns-12)
`Promise`<`void`>

### saveChart[​](#savechart)
▸ saveChart(`chartData`): `Promise`<`string` | `number`>

Save the chart

#### Parameters[​](#parameters-10)
NameTypeDescription`chartData`[`ChartData`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartData)Chart description data
#### Returns[​](#returns-13)
`Promise`<`string` | `number`>

unique ID of the chart

### saveChartTemplate[​](#savecharttemplate)
▸ saveChartTemplate(`newName`, `theme`): `Promise`<`void`>

Save a chart template.

#### Parameters[​](#parameters-11)
NameTypeDescription`newName``string`The name of the template.`theme`[`ChartTemplateContent`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartTemplateContent)The template content.
#### Returns[​](#returns-14)
`Promise`<`void`>

### saveDrawingTemplate[​](#savedrawingtemplate)
▸ saveDrawingTemplate(`toolName`, `templateName`, `content`): `Promise`<`void`>

Save a drawing template

#### Parameters[​](#parameters-12)
NameTypeDescription`toolName``string`name of the drawing tool`templateName``string`name of the template`content``string`content of the drawing template
#### Returns[​](#returns-15)
`Promise`<`void`>

### saveLineToolsAndGroups[​](#savelinetoolsandgroups)
▸ saveLineToolsAndGroups(`layoutId`, `chartId`, `state`): `Promise`<`void`>

Save drawings and drawing groups associated with a chart layout.

#### Parameters[​](#parameters-13)
NameTypeDescription`layoutId``string`The chart layout ID`chartId``string` | `number`The chart ID`state`[`LineToolsAndGroupsState`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LineToolsAndGroupsState)The drawings and drawing groups state
#### Returns[​](#returns-16)
`Promise`<`void`>

### saveStudyTemplate[​](#savestudytemplate)
▸ saveStudyTemplate(`studyTemplateData`): `Promise`<`void`>

Save a study template

#### Parameters[​](#parameters-14)
NameTypeDescription`studyTemplateData`[`StudyTemplateData`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyTemplateData)Study template data to save
#### Returns[​](#returns-17)
`Promise`<`void`>

- [Methods](#methods)[getAllChartTemplates](#getallcharttemplates)- [getAllCharts](#getallcharts)- [getAllStudyTemplates](#getallstudytemplates)- [getChartContent](#getchartcontent)- [getChartTemplateContent](#getcharttemplatecontent)- [getDrawingTemplates](#getdrawingtemplates)- [getStudyTemplateContent](#getstudytemplatecontent)- [loadDrawingTemplate](#loaddrawingtemplate)- [loadLineToolsAndGroups](#loadlinetoolsandgroups)- [removeChart](#removechart)- [removeChartTemplate](#removecharttemplate)- [removeDrawingTemplate](#removedrawingtemplate)- [removeStudyTemplate](#removestudytemplate)- [saveChart](#savechart)- [saveChartTemplate](#savecharttemplate)- [saveDrawingTemplate](#savedrawingtemplate)- [saveLineToolsAndGroups](#savelinetoolsandgroups)- [saveStudyTemplate](#savestudytemplate)