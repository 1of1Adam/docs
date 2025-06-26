---
title: "Drawings | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/ui_elements/drawings/"
extracted_at: "2025-06-22T09:14:51.830Z"
---

# DrawingsDrawings (shapes) are the tools that can help you analyze the charts and make clear annotations to them.
The drawings toolbar is located on the left panel.
Follow the [Drawings List](https://www.tradingview.com/charting-library-docs/latest/ui_elements/drawings/Drawings-List) article for a complete list of tools included in the drawing toolbar.
## Style customization
Each drawing tool has its own default properties, such as color and size, that users can change in the UI.

You can also customize the drawing style using the API.
Refer to the [Drawing Overrides](https://www.tradingview.com/charting-library-docs/latest/customization/overrides/Drawings-Overrides) article for more information.
## Drawing toolbar
You can show/hide the drawing toolbar on the fly as follows:

```
widget.activeChart().executeActionById("drawingToolbarAction");

```
Note that the toolbar is hidden in the fullscreen mode. To display the toolbar, enable the [`side_toolbar_in_fullscreen_mode`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#side_toolbar_in_fullscreen_mode) featureset.

### Favorite tools
You can specify a default list of favorite drawings using the [`favorites`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#favorites) property in [Widget Constructor](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Widget-Constructor).

In the UI, users can mark drawings as favorites using the *Add to favorites* button. The selected drawings are added to *Favorite Drawings Toolbar* that appears on the chart.
If you do not want users to specify favorites, you should disable the [`items_favoriting`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#items_favoriting) featureset. As a result, the *Add to favorites* button will be hidden in the UI.

### Custom restrictions
You can hide some drawings from the toolbar or apply custom restrictions to the chart.
To do this, use the [`drawings_access`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#drawings_access) property of [Widget Constructor](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Widget-Constructor).
For example, you can choose which tools will be shown to users or hidden/disabled from them.

## Drawing features
### Templates

> **Info:** These feature is only available in [Trading Platform](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/).

Users can use the template appliance option for multiple drawings of the same type.
This option is available in the floating toolbar.
To disable this feature, include the `drawing_templates` [featureset](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets) in the [`disabled_features`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#disabled_features) array.

> **Tip:** To save drawing templates on your server, you can use the [predefined REST API](https://www.tradingview.com/charting-library-docs/latest/saving_loading/save-load-rest-api/) or implement [API handlers](https://www.tradingview.com/charting-library-docs/latest/saving_loading/save-load-adapter).

## Drawing API
The library allows you to create and manage drawings using the built-in API. You can also combine drawings into groups and subscribe to drawing-related events. Refer to [Drawings API](https://www.tradingview.com/charting-library-docs/latest/ui_elements/drawings/drawings-api) for more information.