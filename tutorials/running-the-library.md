---
title: "How to run the library | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/tutorials/First-Run-Tutorial"
extracted_at: "2025-06-22T09:16:21.513Z"
---

# How to run the libraryThis tutorial describes how to run the library on your machine.
You can also watch the video below that demonstrates running the library step-by-step.

## Prepare the project

Download the library ZIP file from the [Advanced Charts](https://github.com/tradingview/charting_library) 🔐 (access is [restricted](https://www.tradingview.com/charting-library-docs/latest/getting_started/quick-start#getting-access)) / [Trading Platform](https://github.com/tradingview/trading_platform) 🔐 (access is [restricted](https://www.tradingview.com/charting-library-docs/latest/getting_started/quick-start#getting-access)) repository.

Create a new folder (`example` in this tutorial). Copy the `charting_library` and `datafeed` folders from the archive to `example`.

Create the following `index.html` file in the `example` folder:

/example/index.html```
<!DOCTYPE HTML>
<html lang="en">
<head>
    <meta charset = "UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>

<body>

</body>
</html>

```

Add two script references into the `<head>` section:

```
<script src="charting_library/charting_library.standalone.js"></script>
<script src="datafeeds/udf/dist/bundle.js"></script>

```

- `charting_library/charting_library.standalone.js` contains the code that creates the chart widget.
- `datafeeds/udf/dist/bundle.js` contains a sample datafeed implementation that loads data to the chart.

Define the container for the chart in the `<body>` section:

```
<div id="chartContainer"></div>

```

To create a chart, you should initialize the [Widget Constructor](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetConstructor) in `<body>`. To do this, configure some basic Widget Constructor parameters:

```
<script>
    new TradingView.widget({
        container: 'chartContainer',
        locale: 'en',
        library_path: 'charting_library/',
        datafeed: new Datafeeds.UDFCompatibleDatafeed("https://demo-feed-data.tradingview.com"),
        symbol: 'AAPL',
        interval: '1D',
        fullscreen: true,
        debug: true
    });
</script>

```

- [`container`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#container) is set to the container ID from the previous step.
- [`library_path`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#library_path) specifies a path to additional HTML, JavaScript, and CSS files that allow you to render the chart. In this tutorial, the `charting_library` folder stores these files.
- [`datafeed`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#datafeed) is set to the [`UDFCompatibleDatafeed`](https://www.tradingview.com/charting-library-docs/latest/connecting_data/UDF#constructor) sample that TradingView provides.

## Run the library

Execute the following command in the `example` folder to run the library locally.

```
# Python 2.x
python -m SimpleHTTPServer 9090

# Python 3.x
python -m http.server 9090

```
In this tutorial, the Python [`http.server`](https://docs.python.org/3/library/http.server.html) module is used. You can use any server/port that you prefer. The tips below explain how to run the most common HTTP servers.

Node.js

Install `http-server`.

```
npm install http-server -g

```

Start `http-server` using the following command in the library folder.

```
http-server -p 9090

```

NGINX

[Install](https://www.nginx.com/resources/wiki/start/topics/tutorials/install/) NGINX.

Open the `nginx.conf` file and insert the following code into the `http` section of the file:

```
server {
    listen       9090;
    server_name  localhost;

    location / {
        root ABSOLUTE_PATH_TO_THE_TUTORIAL_FOLDER;
    }
}

```

Replace `ABSOLUTE_PATH_TO_THE_TUTORIAL_FOLDER` with the absolute path to the tutorial folder (`example` in this tutorial).

Run NGINX.

Open `http://localhost:9090/` in your web browser to see the result.

## Complete code
/example/index.html```
<!DOCTYPE HTML>
<html lang="en">
    <head>
        <meta charset = "UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>TradingView - Advanced Charts</title>

        <script src="charting_library/charting_library.standalone.js"></script>
        <script src="datafeeds/udf/dist/bundle.js"></script>
    </head>
    <body>

        <div id="chartContainer"></div>

        <script>
            new TradingView.widget({
                container: 'chartContainer',
                locale: 'en',
                library_path: 'charting_library/',
                datafeed: new Datafeeds.UDFCompatibleDatafeed("https://demo-feed-data.tradingview.com"),
                symbol: 'AAPL',
                interval: '1D',
                fullscreen: true,
                debug: true,
            });
        </script>
    </body>
</html>

```
## What's next?
In this tutorial, you have set up Widget Constructor and a static chart.
To further enhance your implementation, consider following the [How to connect data via Datafeed API](https://www.tradingview.com/charting-library-docs/latest/tutorials/implement_datafeed_tutorial/) tutorial to learn more about real-time data streaming.
Additionally, check out a guide on [enabling debug modes](https://www.tradingview.com/charting-library-docs/latest/tutorials/enable-debug-mode) to help identify potential issues and ensure your application is running smoothly.