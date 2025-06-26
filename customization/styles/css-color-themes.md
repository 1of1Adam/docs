---
title: "CSS Color Themes | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/customization/styles/CSS-Color-Themes"
extracted_at: "2025-06-22T09:28:51.914Z"
---

# CSS Color Themes
> **Warning:** This article describes a legacy method for adjusting the colors of UI elements such as toolbars and context menus. We recommend using the [Custom themes API](https://www.tradingview.com/charting-library-docs/latest/customization/styles/custom-themes) instead, as it provides greater flexibility and precision.

## Connect the CSS file
You can change the colors of UI elements with the [CSS custom properties](#list-of-css-custom-properties). To do this, you should specify these properties in a CSS file and connect the file to the library using the [`custom_css_url`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#custom_css_url) property in the [Widget Constructor](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Widget-Constructor). See customization example in [themed.html](https://github.com/tradingview/charting_library/blob/master/themed.html) and [themed.css](https://github.com/tradingview/charting_library/blob/master/themed.css) files 🔐 (access is [restricted](https://www.tradingview.com/charting-library-docs/latest/getting_started/quick-start#getting-access)).

Use the following CSS selectors to specify colors depending on the theme:

- `: root: not (.theme-dark)` — for the light theme
- `.theme-dark: root` — for the dark theme

Expand to view the code sample that sets up the pink widget for both light and dark theme.

```
:root:not(.theme-dark) {
    --tv-color-platform-background: #d1c4e9;
    --tv-color-pane-background: rgb(251, 223, 244);
    --tv-color-toolbar-button-background-hover: rgb(244, 143, 177);
    --tv-color-toolbar-button-background-expanded: rgb(244, 143, 177);
    --tv-color-toolbar-button-background-active: rgb(249, 185, 233);
    --tv-color-toolbar-button-background-active-hover: rgb(244, 143, 177);
    --tv-color-toolbar-button-text: rgb(136, 24, 79);
    --tv-color-toolbar-button-text-hover: rgb(74, 20, 140);
    --tv-color-toolbar-button-text-active: red;
    --tv-color-toolbar-button-text-active-hover: red;
    --tv-color-item-active-text: rgb(6, 6, 255);
    --tv-color-toolbar-toggle-button-background-active: red;
    --tv-color-toolbar-toggle-button-background-active-hover: magenta;
    --tv-color-toolbar-divider-background: rgb(251, 223, 244);
    --tv-color-toolbar-save-layout-loader: rgb(106, 109, 120);

    --tv-color-popup-background: rgb(241, 188, 225);
    --tv-color-popup-element-text: rgb(136, 24, 79);
    --tv-color-popup-element-text-hover: rgb(74, 20, 140);
    --tv-color-popup-element-background-hover: rgb(244, 143, 177);
    --tv-color-popup-element-divider-background: rgb(251, 223, 244);
    --tv-color-popup-element-secondary-text: rgb(74, 20, 140);
    --tv-color-popup-element-hint-text: rgb(74, 20, 140);
    --tv-color-popup-element-text-active: rgb(6, 6, 255);
    --tv-color-popup-element-background-active: red;
    --tv-color-popup-element-toolbox-text: rgb(136, 24, 79);
    --tv-color-popup-element-toolbox-text-hover: rgb(74, 20, 140);
    --tv-color-popup-element-toolbox-text-active-hover: rgb(74, 20, 140);
    --tv-color-popup-element-toolbox-background-hover: rgb(222, 89, 132);
    --tv-color-popup-element-toolbox-background-active-hover: magenta;
}

.theme-dark:root {
    --tv-color-platform-background: #d1c4e9;
    --tv-color-pane-background: rgb(251, 223, 244);
    --tv-color-toolbar-button-background-hover: rgb(244, 143, 177);
    --tv-color-toolbar-button-background-expanded: rgb(244, 143, 177);
    --tv-color-toolbar-button-background-active: rgb(249, 185, 233);
    --tv-color-toolbar-button-background-active-hover: rgb(244, 143, 177);
    --tv-color-toolbar-button-text: rgb(136, 24, 79);
    --tv-color-toolbar-button-text-hover: rgb(74, 20, 140);
    --tv-color-toolbar-button-text-active: red;
    --tv-color-toolbar-button-text-active-hover: red;
    --tv-color-item-active-text: rgb(6, 255, 6);
    --tv-color-toolbar-toggle-button-background-active: red;
    --tv-color-toolbar-toggle-button-background-active-hover: magenta;
    --tv-color-toolbar-divider-background: rgb(251, 223, 244);
    --tv-color-toolbar-save-layout-loader: rgb(134, 137, 147);

    --tv-color-popup-background: rgb(241, 188, 225);
    --tv-color-popup-element-text: rgb(136, 24, 79);
    --tv-color-popup-element-text-hover: rgb(74, 20, 140);
    --tv-color-popup-element-background-hover: rgb(244, 143, 177);
    --tv-color-popup-element-divider-background: rgb(251, 223, 244);
    --tv-color-popup-element-secondary-text: rgb(74, 20, 140);
    --tv-color-popup-element-hint-text: rgb(74, 20, 140);
    --tv-color-popup-element-text-active: rgb(6, 6, 255);
    --tv-color-popup-element-background-active: red;
    --tv-color-popup-element-toolbox-text: rgb(136, 24, 79);
    --tv-color-popup-element-toolbox-text-hover: rgb(74, 20, 140);
    --tv-color-popup-element-toolbox-text-active-hover: rgb(74, 20, 140);
    --tv-color-popup-element-toolbox-background-hover: rgb(222, 89, 132);
    --tv-color-popup-element-toolbox-background-active-hover: magenta;
}

```
## Adjust properties on the fly
To change or get the [CSS custom properties](#list-of-css-custom-properties) values at runtime, use the [`setCSSCustomProperty`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#setcsscustomproperty) or [`getCSSCustomPropertyValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#getcsscustompropertyvalue) methods, respectively.

```
widget.setCSSCustomProperty('--tv-color-pane-background', 'rgb(251, 223, 244)')

```
You can also use these methods to adjust your own variables defined in the [CSS file](#connect-the-css-file).

## List of CSS custom properties

- `--tv-color-platform-background` — the main color of the page where all elements are placed on
- `--tv-color-pane-background` — toolbar background color
- `--tv-color-toolbar-button-background-hover` — hover effect color for a toolbar button
- `--tv-color-toolbar-button-background-expanded` — hover effect color for the active button on the right toolbar
- `--tv-color-toolbar-button-background-active` — background color for the active button on the right toolbar
- `--tv-color-toolbar-button-background-active-hover` — background color for the active button on the right toolbar when hovering over it
- `--tv-color-toolbar-button-text` — text and icon color for toolbar buttons
- `--tv-color-toolbar-button-text-hover` — text and icon color for toolbar buttons when hovering over them
- `--tv-color-toolbar-button-text-active` — text and icon color for toolbar buttons that are active
- `--tv-color-toolbar-button-text-active-hover` — text and icon color for toolbar buttons that are active when hovering over them
- `--tv-color-item-active-text` — text color for toggle toolbar buttons (e.g. Magnet Mode, Lock All Drawings)
- `--tv-color-toolbar-toggle-button-background-active` — fill color for toggle toolbar buttons (e.g. Magnet Mode, Lock All Drawings)
- `--tv-color-toolbar-toggle-button-background-active-hover` — fill color for toggle toolbar buttons when hovering over them (e.g. Magnet Mode, Lock All Drawings)
- `--tv-color-toolbar-divider-background` — toolbar dividers color
- `--tv-color-toolbar-save-layout-loader` — loader color for toolbar save layout button

### Pop-up menu properties
Pop-up and pop-over menus appear when the user clicks on a toolbar icon. The pop-over menu typically presents a list of tools, options, or commands that are relevant to the context of the icon or the current user task. These styling options are also applied for context menus.

- `--tv-color-popup-background`
- `--tv-color-popup-element-text`
- `--tv-color-popup-element-text-hover`
- `--tv-color-popup-element-background-hover`
- `--tv-color-popup-element-divider-background`
- `--tv-color-popup-element-secondary-text`
- `--tv-color-popup-element-hint-text`
- `--tv-color-popup-element-text-active`
- `--tv-color-popup-element-background-active`
- `--tv-color-popup-element-toolbox-text`
- `--tv-color-popup-element-toolbox-text-hover`
- `--tv-color-popup-element-toolbox-text-active-hover`
- `--tv-color-popup-element-toolbox-background-hover`
- `--tv-color-popup-element-toolbox-background-active-hover`

### Buy/Sell buttons properties
Use Chrome DevTools to inspect the code and identify CSS variables that allow styling the [Buy/Sell buttons](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/#buysell-buttons-and-lines).
For example, you can specify the color of the Sell button as follows:
```
:root:not(.theme-dark) {
    --themed-color-sell-btn-chart: rgb(251, 223, 244);
}

```