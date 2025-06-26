---
title: "Chart layout methods | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/saving_loading/save-load-rest-api/chart-layout-methods"
extracted_at: "2025-06-22T09:28:54.052Z"
---

# Chart layout methods## List charts
GET request: `charts_storage_url/charts_storage_api_version/charts?client=client_id&user=user_id`

### Response content
The response is a JSON object containing the following properties:

 **|Property** | **Description** ||
| `status`[#](#status) | `ok` or `error` ||
| `data`[#](#data) | Data object with the following properties: - `timestamp` — UNIX time when the chart was saved (example: `1449084321`)- `symbol` — base symbol of the chart (example: `AA`)- `resolution` — chart resolution (example: `1D`)- `id` —  unique integer identifier of the chart (example: `9163`)- `name` — chart name (example: `Test`) ||

## Save chart
POST request: `charts_storage_url/charts_storage_api_version/charts?client=client_id&user=user_id`

### Request body

 **|Parameter** | **Description** ||
| `name` | Chart name ||
| `content` | Chart content ||
| `symbol` | Chart symbol (example: `AA`) ||
| `resolution` | Chart resolution (example: `1D`) ||

### Response content
The response is a JSON object containing the following properties:

 **|Parameter** | **Description** ||
| `status` | `ok` or `error` ||
| `id` | Unique string identifier of the chart (example: `9163`) ||

## Save as chart
POST request: `charts_storage_url/charts_storage_api_version/charts?client=client_id&user=user_id&chart=chart_id`

### Request body

 **|Parameter** | **Description** ||
| `name` | Chart name ||
| `content` | Chart content ||
| `symbol` | Chart symbol (example: `AA`) ||
| `resolution` | Chart resolution (example: `1D`) ||

### Response content
The response is a JSON object containing the `status` property, which may have values of either `ok` or `error`.

## Load chart
GET request: `charts_storage_url/charts_storage_api_version/charts?client=client_id&user=user_id&chart=chart_id`

### Response content
The response is a JSON object containing the following properties:

 **|Property** | **Description** ||
| `status`[#](#status) | `ok` or `error` ||
| `data`[#](#data) | Data object with the following properties: - `content` — saved content of the chart- `timestamp` — UNIX time when the chart was saved (example: `1449084321`)- `id` —  unique integer identifier of the chart (example: `9163`)- `name` — chart name ||

## Delete chart
DELETE request: `charts_storage_url/charts_storage_api_version/charts?client=client_id&user=user_id&chart=chart_id`

### Response content
The response is a JSON object containing the `status` property, which may have values of either `ok` or `error`.