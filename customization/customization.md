---
title: "Customization overview | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/customization/"
extracted_at: "2025-06-22T09:15:09.855Z"
---

# Customization overviewThe library supports extensive customization through a set of APIs, each designed for specific tasks. For example, [Featuresets](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets) should be used to control the visibility of chart elements, and the [Widget Constructor](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Widget-Constructor) to configure the chart size and default symbol.

For color adjustments, either [Overrides](https://www.tradingview.com/charting-library-docs/latest/customization/overrides/) or [Custom themes API](https://www.tradingview.com/charting-library-docs/latest/customization/styles/custom-themes) may be used. The image below illustrates specific areas of the chart and indicates the appropriate API to use for their customization.

## Customization APIs

> **Warning:** Note that some settings, such as the chart background color, can be adjusted with different API approaches. These approaches may override each other depending on their priority. Refer to the [Customization precedence](https://www.tradingview.com/charting-library-docs/latest/customization/customization-precedence) article for more information.

[##  OverridesCustomize elements on the chart like panes, scales, series, indicators, and drawings

](https://www.tradingview.com/charting-library-docs/latest/customization/overrides/)[##  Custom themes APIOverride the default light and dark themes with a custom color palette

](https://www.tradingview.com/charting-library-docs/latest/customization/styles/custom-themes/)[##  FeaturesetsShow/hide UI elements and modify chart interaction behavior

](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets)[##  Widget ConstructorCustomize the chart size, default symbol and resolution, font family, and other parameters

](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Widget-Constructor/)
## Commonly customized items
[##  UI elementsAdjust UI elements, such as drawings, indicators, and marks

](https://www.tradingview.com/charting-library-docs/latest/ui_elements/)[##  LanguageSet the chart language from more than 20 supported options

](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Localization)[##  Price formatConfigure how prices are displayed: decimal or fractional format, number of decimal places, tick size, and other parameters

](https://www.tradingview.com/charting-library-docs/latest/connecting_data/Symbology#price-format)
## TradingView logo
The visibility of the TradingView logo depends on the terms of your license agreement. Contact your TradingView account manager for more information.

## Theme
The library supports dark and light themes. Use the [`theme`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#theme) parameter in [Widget Constructor](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Widget-Constructor) to specify a theme. The default value is `light`. The chart layout does not contain buttons that switch the theme in the UI. Therefore, users cannot switch the theme unless you develop this option outside the library.

You should switch the chart's theme when the theme of your website changes. To do this, use the [`changeTheme`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#changetheme) method that changes the theme on the fly.

Note that the `theme` value is stored in the chart's configuration. Therefore, if you restore the chart that has the dark theme, you may see a black chart background in the light theme. In this case, you should apply the theme once again using the [`changeTheme`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#changetheme) method.

> **Tip:** If you want to override the default colors of the light and dark themes, you can use the [Custom themes API](https://www.tradingview.com/charting-library-docs/latest/customization/styles/custom-themes).

## Limitations

- You cannot customize icons on the toolbars.
- The library does not support injecting custom UI components. If you want to add a UI component, implement it outside the library.