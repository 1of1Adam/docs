---
title: "Common issues | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/customization/customization-issues"
extracted_at: "2025-06-22T09:15:21.201Z"
---

# Common issuesThis article describes common customization issues.

## Settings are not applied
The library supports extensive customization through a set of APIs. Some settings, such as the chart background color, can be adjusted with different API approaches.

If your setting does not take effect, it might be overridden by another API approach. Refer to the [Customization precedence](https://www.tradingview.com/charting-library-docs/latest/customization/customization-precedence) article to understand API priorities, and consider using an alternative approach if needed.

## User settings override default ones
In the library, [user settings](https://www.tradingview.com/charting-library-docs/latest/saving_loading/user-settings) take precedence over default configurations specified with the API. Therefore, replacing settings defined through [`overrides`](https://www.tradingview.com/charting-library-docs/latest/customization/customization-precedence#overrides) and [`custom_themes`](https://www.tradingview.com/charting-library-docs/latest/customization/customization-precedence#customThemes) with user input is expected behavior.

By default, user settings are stored in [`localStorage`](https://www.tradingview.com/charting-library-docs/latest/customization/customization-precedence#localStorage). To override them, you should adjust these settings with another API approach that has higher priority according to the [table](https://www.tradingview.com/charting-library-docs/latest/customization/customization-precedence#approaches).