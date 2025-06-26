---
title: "Interface: ICustomThemesApi | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ICustomThemesApi"
extracted_at: "2025-06-22T09:38:45.200Z"
---

- [](/charting-library-docs/)- Interfaces- ICustomThemesApiOn this page# Interface: ICustomThemesApi[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).ICustomThemesApi

An API for controlling custom themes. To retrieve this interface, call the [IChartingLibraryWidget.customThemes](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#customthemes) method.
For more information on custom themes, refer to the [Custom Themes API](https://www.tradingview.com/charting-library-docs/latest/customization/styles/custom-themes) article.
## Methods[​](#methods)
### applyCustomThemes[​](#applycustomthemes)
▸ applyCustomThemes(`customThemes`): `Promise`<`void`>

Apply custom theme color definitions to the library widget after the widget is created.

You can also specify a custom theme using the [ChartingLibraryWidgetOptions.custom_themes](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#custom_themes) property in the Widget Constructor.

#### Parameters[​](#parameters)
NameTypeDescription`customThemes`[`CustomThemes`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CustomThemes)Custom theme color definitions
#### Returns[​](#returns)
`Promise`<`void`>

### resetCustomThemes[​](#resetcustomthemes)
▸ resetCustomThemes(): `Promise`<`void`>

Reset the widget's color theme colors back to the default values.

#### Returns[​](#returns-1)
`Promise`<`void`>

- [Methods](#methods)[applyCustomThemes](#applycustomthemes)- [resetCustomThemes](#resetcustomthemes)