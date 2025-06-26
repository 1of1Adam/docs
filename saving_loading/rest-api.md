---
title: "Save and load REST API | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/saving_loading/save-load-rest-api/"
extracted_at: "2025-06-22T09:15:24.992Z"
---

# Save and load REST API## Overview
The library provides a predefined REST API to save [chart layouts](https://www.tradingview.com/charting-library-docs/latest/saving_loading/#chart-layouts) and [indicator templates](https://www.tradingview.com/charting-library-docs/latest/saving_loading/#indicator-templates) on your server.
When users click the save or load buttons in the UI, these actions initiate the saving and loading processes.
This article describes the [request formats](#develop-your-own-storage) sent by the library.
Additionally, you can find a server-side [storage example](#storage-example), which can serve as a starting point for implementation.

> **Info:** This approach does not support saving [chart templates](https://www.tradingview.com/charting-library-docs/latest/saving_loading/#chart-templates).
Consider implementing the [API handlers](https://www.tradingview.com/charting-library-docs/latest/saving_loading/save-load-adapter) instead.
Besides, using API handlers is recommended for greater flexibility and control over operations such as adding authorization headers or managing errors.

## Use demo storage
You can use a demo chart storage for saving and loading charts and indicator templates as soon as you build your application.
To use this storage, specify [`charts_storage_url`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#charts_storage_url) in the [Widget Constructor](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Widget-Constructor) as shown below:
```
const datafeed = new Datafeeds.UDFCompatibleDatafeed("https://demo-feed-data.tradingview.com");
new TradingView.widget({
    container: "chartContainer",
    locale: "en",
    library_path: "charting_library/",
    datafeed: datafeed,
    symbol: "AAPL",
    interval: "1D",
    charts_storage_url: "https://saveload.tradingview.com",
})

```
Note that the demo storage is provided "as is", and its stability is not guaranteed.
The data within the storage is regularly deleted.
Therefore, we recommend using this storage for testing purposes only.
## Storage example
Refer to our [GitHub repository](https://github.com/tradingview/saveload_backend) for a storage example implemented with Python and PostgreSQL.
You can use this storage and run it on your server to process your users' saved data.
Note that this storage does not support the endpoints that allow [saving and loading drawings separately](https://www.tradingview.com/charting-library-docs/latest/saving_loading/saving_drawings_separately).
Follow the steps below to get started:

Clone the repository to your host machine.

Run the data service or use our demo service.

If you are not familiar with Django, follow the steps below.

Install Python 3.x and pip.

Install PostgreSQL or any other Django-friendly database engine.

Navigate to your chart storage folder and install the required dependencies:

```
cd your-repository
pip install -r requirements.txt

```

Configure your database connection in `charting_library_charts/settings.py` (see `DATABASES` at [line 16](https://github.com/tradingview/saveload_backend/blob/master/charting_library_charts/settings.py#L16)). Do not forget to create the appropriate database in your PostgreSQL instance.

Run migrations to create the database schema without any data:

```
python manage.py migrate

```

Start a test instance of your database:

```
python manage.py runserver

```
**Note:** for production environments, avoid using `runserver` and instead use a suitable WSGI (Web Server Gateway Interface) server like Gunicorn.

Set [`charts_storage_url`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#charts_storage_url) in the [Widget Constructor](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Widget-Constructor) to the URL of your chart storage. Additionally, ensure to set [`client_id` and `user_id`](#manage-access-to-saved-charts).

```
const datafeed = new Datafeeds.UDFCompatibleDatafeed("https://demo-feed-data.tradingview.com");
new TradingView.widget({
    container: "chartContainer",
    locale: "en",
    library_path: "charting_library/",
    datafeed: datafeed,
    symbol: "AAPL",
    interval: "1D",
    charts_storage_url: "https://example.com",
    client_id: "tradingview.com",
    user_id: "public_user_id",
})

```

> **Info:** 
- Manual database filling/editing is not recommended as it may disrupt the Django infrastructure.
- This example does not support authorization. We do not recommend it for production use without implementing proper security measures.

## Develop your own storage
If you want to develop your own storage that accepts predefined REST API requests, implement the endpoints described in this section.
Note that your implementation should process 4 requests: save, load, delete, and list.
The library sends HTTP/HTTPS commands to the following endpoints:

- [For chart layouts](https://www.tradingview.com/charting-library-docs/latest/saving_loading/save-load-rest-api/chart-layout-methods): `charts_storage_url/charts_storage_api_version/charts?client=client_id&user=user_id`
- [For indicator templates](https://www.tradingview.com/charting-library-docs/latest/saving_loading/save-load-rest-api/indicator-template-methods): `charts_storage_url/charts_storage_api_version/study_templates?client=client_id&user=user_id`
- [For drawings](https://www.tradingview.com/charting-library-docs/latest/saving_loading/save-load-rest-api/drawing-methods): `charts_storage_url/charts_storage_api_version/drawings?client=client_id&user=user_id`
- [For drawing templates](https://www.tradingview.com/charting-library-docs/latest/saving_loading/save-load-rest-api/drawing-template-methods): `charts_storage_url/charts_storage_api_version/drawing_templates?client=client_id&user=user_id`

These endpoints include arguments that correspond to the properties defined within the [Widget Constructor](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Widget-Constructor).

 **|Parameter** | **Description** ||
| [`charts_storage_url`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions/#charts_storage_url)[#](#charts_storage_url) | A storage URL endpoint. ||
| [`charts_storage_api_version`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions/#charts_storage_api_version)[#](#charts_storage_api_version) | A version of your backend. Supported values are: `1.0` or `1.1`. ||
| [`client_id`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions/#client_id)[#](#client_id) | A client ID that represents a user group. ||
| [`user_id`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions/#user_id)[#](#user_id) | A user ID that uniquely identifies each user within a `client_id` group. ||

## Manage access to saved charts
You should manage how the charts are accessible to users.
Each user can view and load charts associated with their [`client_id`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#client_id) and [`user_id`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#user_id).

`client_id` represents a user group, typically set as your site's URL `client_id = your-site-URL`.
Use this property for scenarios where you manage multiple user groups or when several sites share the same chart storage.
`user_id` uniquely identifies each user within a `client_id` group.
You can configure it:

- for individual users providing private storage for each user
- for all users or user groups allowing public access to the storage

Here are a few examples:

 **|`client_id`** | **`user_id`** | **Effect** ||
| Your site URL or other link | Unique user ID | Each user has a private chart storage that other users cannot see. ||
| Your site URL or other link | Same value for all users | Each user can see and load any saved chart. ||
| Your site URL or other link | Unique user ID for registered users, along with a separate setting for anonymous users | Each registered user has a private chart storage, not visible to other users. All anonymous users share a single storage. ||