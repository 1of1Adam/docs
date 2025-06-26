---
title: "Interface: CustomIndicator | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CustomIndicator"
extracted_at: "2025-06-22T09:35:34.429Z"
---

- [](/charting-library-docs/)- Interfaces- CustomIndicatorOn this page# Interface: CustomIndicator[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).CustomIndicator

## Properties[​](#properties)
### constructor[​](#constructor)
• `Readonly` constructor: [`LibraryPineStudyConstructor`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LibraryPineStudyConstructor)<[`IPineStudyResult`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#ipinestudyresult)> | (`this`: [`LibraryPineStudy`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LibraryPineStudy)<[`IPineStudyResult`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#ipinestudyresult)>) => `void`

The field should contain an ES5 constructor function. The library applies the `new` operator to the constructor to create an instance of the custom indicator.
The constructor contains the mandatory `main` method and the optional `init` method.
Once the indicator instance is created, the library calls `init` (if exists) and `main` sequentially with empty context to collect information about all variables.
Refer to the [Constructor](https://www.tradingview.com/charting-library-docs/latest/custom_studies/custom-indicator-constructor) article for more information.

### metainfo[​](#metainfo)
• `Readonly` metainfo: [`StudyMetaInfo`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#studymetainfo)

The metainfo field is designed to contain the main info about the custom study.

Refer to [Custom Studies Metainfo](https://www.tradingview.com/charting-library-docs/latest/custom_studies/metainfo/) for more information.

### name[​](#name)
• `Readonly` name: `string`

Your study name, it will be used internally by the library

- [Properties](#properties)[constructor](#constructor)- [metainfo](#metainfo)- [name](#name)