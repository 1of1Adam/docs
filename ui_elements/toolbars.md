---
title: "Toolbars | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/ui_elements/Toolbars"
extracted_at: "2025-06-22T09:14:34.353Z"
---

# Toolbars## Overview
The term **toolbars** relates to several [UI elements](https://www.tradingview.com/charting-library-docs/latest/ui_elements/).

- [Top toolbar](https://www.tradingview.com/charting-library-docs/latest/ui_elements/#top-toolbar) is a primary bar at the top of the chart that contains elements such as Symbol Search, Indicators, and Resolutions.
- [Drawing toolbar](https://www.tradingview.com/charting-library-docs/latest/ui_elements/drawings/) is a left-side bar that contains drawings.
- [Widget bar](https://www.tradingview.com/charting-library-docs/latest/ui_elements/#widget-bar) is a right-side bar available in [Trading Platform](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/) only. This toolbar displays the Watchlist, Details, and News widgets.
- [Time frame toolbar](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Time-Scale#time-frame-toolbar) is a bottom bar that displays time period buttons.

> **Info:** For detailed information on customizing specific toolbar elements, refer to dedicated sections of the [UI elements](https://www.tradingview.com/charting-library-docs/latest/ui_elements/) and [Featuresets](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets) articles.

## Custom buttons in top toolbar
You can add your own buttons to the top toolbar using the following methods:

[`createButton`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#createbutton) — creates a customizable button.
This method provides maximum flexibility since it returns an HTML element (if `useTradingViewStyle` is `false`), which you can customize in any way you want.
For example, you can create a checkbox or a dropdown menu.
[`createDropdown`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#createdropdown) — creates a dropdown menu.
Use this method for a simpler dropdown menu when you don't require custom HTML.

Note that other toolbars do not currently support custom button placement using these methods.

> **Tip:** Check out the [How to add custom button to top toolbar](https://www.tradingview.com/charting-library-docs/latest/tutorials/add-custom-button-to-top-toolbar) guide for a hands-on understanding.

### Accessible buttons
Custom buttons, created using the [`createButton`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#createbutton) overload with `useTradingViewStyle` set to `true`, support [accessible keyboard navigation](https://www.tradingview.com/charting-library-docs/latest/getting_started/accessibility#keyboard-navigation).

## Change toolbar style
The library offers two ways to change the toolbar style:

- [Using custom themes API](https://www.tradingview.com/charting-library-docs/latest/customization/styles/custom-themes)
- [Using CSS color themes](https://www.tradingview.com/charting-library-docs/latest/customization/styles/CSS-Color-Themes)