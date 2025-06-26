---
title: "Custom themes API | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/customization/styles/custom-themes/"
extracted_at: "2025-06-22T09:28:41.581Z"
---

# Custom themes API## Overview
A theme is a set of colors arranged to create a cohesive visual design of the widget. Themes change the colors of UI elements inside and outside the chart.
The library ships with the [light and dark themes](https://www.tradingview.com/charting-library-docs/latest/customization/#theme) that use the default [color palette](#default-color-palette).
The Custom themes API allows you to override the default colors in the palette for the light and dark themes. In this way, you can change the colors of the following UI elements:

- Toolbars
- Dialogs
- Context menus
- Tooltips
- Buttons
- Chart background
- Main series bars
- Grid
- Axes

Note that changing a color in the palette might affect multiple elements. To tweak a color of the certain element, for example the [*Price Scale*](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Price-Scale), use the [Overrides API](https://www.tradingview.com/charting-library-docs/latest/customization/overrides/) that applies above the palette colors. Refer to the [Customization precedence](https://www.tradingview.com/charting-library-docs/latest/customization/customization-precedence) article for more information on customization approaches and their priorities.

> **Info:** The library supports only the light and dark themes. It is not possible to create an additional theme at the moment.

### Default color palette
In the demo below, you can see the default color palette that contains seven colors besides black and white. Each color comes with 20 shades, ranging from the lightest to the darkest.
Shades of one color are assigned to different UI elements. For example, light gray is used for the toolbar separators, while dark gray is applied to the tooltips.
The demo allows you to identify the original colors of the certain UI elements and test your colors on the chart. Click any color in the palette and specify a new one using the color picker.
Changes in the palette will be applied to the chart. Therefore, if you change blue, all the elements that originally use it, for example buttons in the dialogs, will adopt the new color.
The currently applied colors are represented in the JSON format. You can use this code later to [specify your custom palette](#specify-custom-palettes) with the Custom themes API.

See the Pen 
Interactive Custom Themes by TradingView ([@tradingview](https://codepen.io/tradingview))
on [CodePen](https://codepen.io).
## Specify custom palettes
To specify palettes for the light and dark themes, create a [`CustomThemes`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CustomThemes) object and assign it to the [`custom_themes`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#custom_themes) property of the [Widget Constructor](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Widget-Constructor).
As mentioned in the previous [section](#default-color-palette), a color palette should contain seven colors, each with 20 shades.
The palette is configured in the [`CustomThemeColors`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CustomThemeColors) object that contains the following properties:

 **|Property name** | **Definition** ||
| `color1` | Blue by default ||
| `color2` | Grey by default ||
| `color3` | Red by default ||
| `color4` | Green by default ||
| `color5` | Orange by default ||
| `color6` | Purple by default ||
| `color7` | Yellow by default ||

To override a default color, create an array of color strings from the lightest to the darkest and assign it to the corresponding property.
You can also specify colors used instead of black and white. If any color is not provided, the default one will be used.
```
var widget = window.tvWidget = new TradingView.widget({
    // ...
    custom_themes: {
        // The new palette for the light theme
        light: {
            // Color that overrides blue
            "color1": ["#f5ebff", "#ead6fe", "#e0c2fe", "#d5adfe", "#cb99fd", "#c184fd", "#b670fd", "#ac5bfc", "#a147fc", "#9732fc", "#8209fb", "#7708e6", "#6c08d1", "#6207bc", "#5706a7", "#4c0592", "#41057e", "#360469", "#2b0354", "#21023f"],
            // Color that overrides grey
            "color2": ["#f2edf7", "#e6dcef", "#d9cae7", "#ccb9df", "#bfa7d7", "#b396d0", "#a684c8", "#9972c0", "#8c61b8", "#804fb0", "#662ca0", "#5e2893", "#552585", "#4d2178", "#441d6b", "#3c1a5d", "#331650", "#2b1243", "#220f35", "#1a0b28"],
            // Color that overrides red
            "color3": ["#fff0f0", "#ffe1e1", "#ffd3d3", "#ffc4c4", "#ffb5b5", "#ffa6a6", "#ff9797", "#ff8888", "#ff7a7a", "#ff6b6b", "#ff4d4d", "#ea4747", "#d54040", "#bf3a3a", "#aa3333", "#952d2d", "#802727", "#6a2020", "#551a1a", "#401313"],
            // Color that overrides green
            "color4": ["#f2fdf8", "#e5faf0", "#d7f8e9", "#caf5e1", "#bdf3da", "#b0f1d2", "#a2eecb", "#95ecc3", "#88e9bc", "#7be7b4", "#60e2a5", "#58cf97", "#50bc8a", "#48aa7c", "#40976e", "#388460", "#307153", "#285e45", "#204b37", "#183929"],
            // Color that overrides orange
            "color5": ["#fef5ea", "#fdecd5", "#fbe2bf", "#fad9aa", "#f9cf95", "#f8c680", "#f6bc6a", "#f5b255", "#f4a940", "#f39f2b", "#f08c00", "#dc8000", "#c87500", "#b46900", "#a05d00", "#8c5200", "#784600", "#643a00", "#502f00", "#3c2300"],
            // Color that overrides purple
            "color6": ["#feeafe", "#fcd5fc", "#fbbffb", "#f9aaf9", "#f895f8", "#f780f7", "#f56af5", "#f455f4", "#f240f2", "#f12bf1", "#ee00ee", "#da00da", "#c600c6", "#b300b3", "#9f009f", "#8b008b", "#770077", "#630063", "#4f004f", "#3c003c"],
            // Color that overrides yellow
            "color7": ["#fefeea", "#fcfcd5", "#fbfbbf", "#f9f9aa", "#f8f895", "#f7f780", "#f5f56a", "#f4f455", "#f2f240", "#f1f12b", "#eeee00", "#dada00", "#c6c600", "#b3b300", "#9f9f00", "#8b8b00", "#777700", "#636300", "#4f4f00", "#3c3c00"],
            "white": "#f2e6ff",
            "black": "#421b50"
        },
        dark: {
            "color1": ["#fbefea", "#f7dfd5", "#f3cfc0", "#efbfaa", "#ebaf95", "#e89f80", "#e48f6b", "#e07f56", "#dc6f41", "#d85f2b", "#d03f01", "#bf3a01", "#ad3501", "#9c2f01", "#8b2a01", "#792501", "#682001", "#571a00", "#451500", "#341000"],
            "color2": ["#f8eeee", "#f1dede", "#eacdcd", "#e2bcbc", "#dbacac", "#d49b9b", "#cd8a8a", "#c67a7a", "#bf6969", "#b75858", "#a93737", "#9b3232", "#8d2e2e", "#7f2929", "#712525", "#632020", "#551c1c", "#461717", "#381212", "#2a0e0e"],
            "color3": ["#fff0f0", "#ffe1e1", "#ffd3d3", "#ffc4c4", "#ffb5b5", "#ffa6a6", "#ff9797", "#ff8888", "#ff7a7a", "#ff6b6b", "#ff4d4d", "#ea4747", "#d54040", "#bf3a3a", "#aa3333", "#952d2d", "#802727", "#6a2020", "#551a1a", "#401313"],
            "color4": ["#f2fffb", "#e6fff7", "#d9fff2", "#ccffee", "#bfffea", "#b3ffe6", "#a6ffe1", "#99ffdd", "#8cffd9", "#80ffd5", "#66ffcc", "#5eeabb", "#55d5aa", "#4dbf99", "#44aa88", "#3c9577", "#338066", "#2b6a55", "#225544", "#1a4033"],
            "color5": ["#fffff0", "#ffffe0", "#feffd1", "#feffc2", "#feffb2", "#feffa3", "#fdff94", "#fdff84", "#fdff75", "#fdff66", "#fcff47", "#e7ea41", "#d2d53b", "#bdbf35", "#a8aa2f", "#939529", "#7e8024", "#696a1e", "#545518", "#3f4012"],
            "color6": ["#fff1ff", "#ffe2ff", "#ffd4ff", "#ffc5ff", "#ffb7ff", "#ffa9ff", "#ff9aff", "#ff8cff", "#ff7dff", "#ff6fff", "#ff52ff", "#ea4bea", "#d544d5", "#bf3ebf", "#aa37aa", "#953095", "#802980", "#6a226a", "#551b55", "#401540"],
            "color7": ["#eff8ff", "#dff1ff", "#cfeaff", "#bee3ff", "#aedcff", "#9ed5ff", "#8eceff", "#7ec7ff", "#6ec0ff", "#5db9ff", "#3dabff", "#389dea", "#338fd5", "#2e80bf", "#2972aa", "#246495", "#1f5680", "#19476a", "#143955", "#0f2b40"],
            "white": "#ffffff",
            "black": "#000000"
        }
    }
});

```
## Manage palettes
To manage custom palettes after the chart is initialized, you should call the [`customThemes`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#customthemes) method. This method returns an instance of the [`ICustomThemesApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ICustomThemesApi) interface that provides an extensive API for controlling the palettes.

### Change palette on the fly
Call the [`applyCustomThemes`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ICustomThemesApi#applycustomthemes) method and pass a [`CustomThemes`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CustomThemes) object as a parameter.

```
let customThemesAPI = (await widget.customThemes());
customThemesAPI.applyCustomThemes(customThemes);

```
### Reset palettes
Call the [`resetCustomThemes`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ICustomThemesApi#resetcustomthemes) method as follows:

```
let customThemesAPI = (await widget.customThemes());
customThemesAPI.resetCustomThemes();

```
### Disable the API
You can disable the Custom themes API with the [`library_custom_color_themes`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#library_custom_color_themes) featureset.
If you try to call the API in this case, the following error occurs: *The library_custom_color_themes feature must be enabled to use the Custom themes API*.