---
title: "Drawing methods | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/saving_loading/save-load-rest-api/drawing-methods"
extracted_at: "2025-06-22T09:28:59.404Z"
---

# Drawing methods
> **Info:** These endpoints are only required when the [`saveload_separate_drawings_storage`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#saveload_separate_drawings_storage) featureset is enabled.
This allows [saving drawings separately](https://www.tradingview.com/charting-library-docs/latest/saving_loading/saving_drawings_separately) from the chart layout.

## Save drawings
POST request: `charts_storage_url/charts_storage_api_version/drawings?client=client_id&user=user_id&chart=chart_id&layout=layout_id`

### Request body
The request body contains a JSON with the `state` property, which holds a [`LineToolsAndGroupsState`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LineToolsAndGroupsState) object.

### Response content
The response is a JSON object containing the `status` property, which may have values of either `ok` or `error`.

## Load drawings
GET request: `charts_storage_url/charts_storage_api_version/drawings?client=client_id&user=user_id&chart=chart_id&layout=layout_id&symbol=symbol`

### Response content
The response is a JSON object containing the following properties:

 **|Parameter** | **Description** ||
| `status` | `ok` or `error` ||
| `data` | An object containing the `state` property, which holds a [`LineToolsAndGroupsState`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LineToolsAndGroupsState) object ||