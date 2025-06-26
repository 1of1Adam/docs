---
title: "Drawing template methods | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/saving_loading/save-load-rest-api/drawing-template-methods"
extracted_at: "2025-06-22T09:29:02.171Z"
---

# Drawing template methods
> **Info:** These endpoints are only available in [Trading Platform](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/).

## List drawing templates
GET request: `charts_storage_url/charts_storage_api_version/drawing_templates?client=client_id&user=user_id&tool=toolName`,
where `toolName` is a name of a drawing.
### Response content
The response is a JSON object containing the following properties:

 **|Parameter** | **Description** ||
| `status` | `ok` or `error` ||
| `data` | An array containing items with the `name` property. This property represents template names (example: `Test`) ||

## Save drawing template
POST request: `charts_storage_url/charts_storage_api_version/drawing_templates?client=client_id&user=user_id&tool=toolName&name=templateName`,
where:

- `toolName` is a drawing name
- `templateName` is a custom template name

### Request body
The request body contains a JSON object with the `content` property. This property represents the saved content of a template.

### Response content
The response is a JSON object containing the `status` property, which may have values of either `ok` or `error`.

## Load drawing template
GET request: `charts_storage_url/charts_storage_api_version/drawing_templates?client=client_id&user=user_id&chart=chart_id&tool=toolName&name=templateName`,
where:

- `toolName` is a name of a drawing
- `templateName` is a name of a template to get

### Response content
The response is a JSON object containing the following properties:

 **|Parameter** | **Description** ||
| `status` | `ok` or `error` ||
| `data` | Data object containing the `content` property. This property represents saved content of the template. ||

## Delete drawing template
DELETE request: `charts_storage_url/charts_storage_api_version/drawing_templates?client=client_id&user=user_id&chart=chart_id&tool=toolName&name=templateName`,
where:

- `toolName` is a name of a drawing
- `templateName` is a name of a template to remove

### Response content
The response is a JSON object containing the `status` property, which may have values of either `ok` or `error`.