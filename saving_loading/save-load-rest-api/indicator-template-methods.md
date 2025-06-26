---
title: "Indicator template methods | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/saving_loading/save-load-rest-api/indicator-template-methods"
extracted_at: "2025-06-22T09:28:56.808Z"
---

# Indicator template methods## List indicator templates
GET request: `charts_storage_url/charts_storage_api_version/study_templates?client=client_id&user=user_id`

### Response content
The response is a JSON object containing the following properties:

 **|Parameter** | **Description** ||
| `status` | `ok` or `error` ||
| `data` | Array of objects where each object has a `name` property representing the template name (example: `Test`) ||

## Save indicator template
POST request: `charts_storage_url/charts_storage_api_version/study_templates?client=client_id&user=user_id`

### Request body

 **|Parameter** | **Description** ||
| `name` | Template name ||
| `content` | Template content ||

### Response content
The response is a JSON object containing the `status` property, which may have values of either `ok` or `error`.

## Load indicator template
GET request: `charts_storage_url/charts_storage_api_version/study_templates?client=client_id&user=user_id&chart=chart_id&template=name`,
where `name` is a template name.
### Response content
The response is a JSON object containing the following properties:

 **|Property** | **Description** ||
| `status`[#](#status) | `ok` or `error` ||
| `data`[#](#data) | Data object with the following properties: - `name` — template name- `content` — saved content of the template ||

## Delete indicator templates
DELETE request: `charts_storage_url/charts_storage_api_version/study_templates?client=client_id&user=user_id&template=name`,
where `name` is a template name.
### Response content
The response is a JSON object containing the `status` property, which may have values of either `ok` or `error`.