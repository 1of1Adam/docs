---
title: "Set up the widget | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/tutorials/implement_datafeed_tutorial/Widget-Setup"
extracted_at: "2025-06-22T09:32:40.705Z"
---

# Set up the widget
> **Tip:** This article is part of a tutorial about implementing Datafeed API.
We recommend that you follow the guide from the [start](https://www.tradingview.com/charting-library-docs/latest/tutorials/implement_datafeed_tutorial/).

At this stage of the tutorial, you will initialize the basic elements of the integration and create a chart.

## Step 1. Clone the library

Create a directory for your project:

```
mkdir chart-project
cd chart-project

```

Clone the [library repository](https://github.com/tradingview/charting_library/) 🔐 (access is [restricted](https://www.tradingview.com/charting-library-docs/latest/getting_started/quick-start#getting-access)).

```
git clone https://github.com/tradingview/charting_library charting_library_cloned_data

```

## Step 2. Add a container
To display the chart, you need to add a DOM container.
To do this, create an initial `index.html` file in your project directory (`chart‑project` in this tutorial) and add the following code:
/chart‑project/index.html```
<!DOCTYPE HTML>
<html>
    <head>
        <title>TradingView Advanced Charts example</title>

        <!-- The script that loads the library -->
        <script
            type="text/javascript"
            src="charting_library_cloned_data/charting_library/charting_library.js">
        </script>

        <!-- Custom datafeed module -->
        <script type="module" src="src/main.js"></script>
    </head>

    <body style="margin:0px;">
        <!-- A container for the the library widget -->
        <div id="tv_chart_container">
        </div>
    </body>
</html>

```
At this point, you added a script that is used to load the library and a container that will be used as a placeholder for the chart.

## Step 3. Create Widget Constructor

Add the `src` folder to your project directory.

Create a `main.js` file in `src` and add the following code that creates [Widget Constructor](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Widget-Constructor).
Widget Constructor is the library entry point that allows embedding the library widget into your web page.
/chart‑project/src/main.js```
// Datafeed implementation that you will add later
import Datafeed from './datafeed.js';

window.tvWidget = new TradingView.widget({
    symbol: 'BTC/EUR',                     // Default symbol pair
    interval: '1D',                        // Default interval
    fullscreen: true,                      // Displays the chart in the fullscreen mode
    container: 'tv_chart_container',       // Reference to an attribute of a DOM element
    datafeed: Datafeed,
    library_path: '../charting_library_cloned_data/charting_library/',
});

```

> **Tip:** This tutorial uses only the required Widget Constructor parameters that will be enabled when the chart is first loaded.
However, Widget Constructor has many different parameters to manage.
You can find the full list in the [`ChartingLibraryWidgetOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions) interface.

## Next steps
At this stage, you have set up Widget Constructor.
Next, you will implement your own datafeed and methods.
## Complete code
Click the following sections to reveal the complete code for the examples at this stage of the tutorial.

`index.html````
<!DOCTYPE HTML>
<html>
    <head>
        <title>TradingView Advanced Charts example</title>

        <!-- The script that loads the library -->
        <script
            type="text/javascript"
            src="charting_library_cloned_data/charting_library/charting_library.js">
        </script>

        <!-- Custom datafeed module -->
        <script type="module" src="src/main.js"></script>
    </head>

    <body style="margin:0px;">
        <!-- A container for the the library widget -->
        <div id="tv_chart_container">
        </div>
    </body>
</html>

```
`main.js````
// Datafeed implementation that you will add later
import Datafeed from './datafeed.js';

window.tvWidget = new TradingView.widget({
    symbol: 'BTC/EUR',                     // Default symbol pair
    interval: '1D',                        // Default interval
    fullscreen: true,                      // Displays the chart in the fullscreen mode
    container: 'tv_chart_container',       // Reference to the attribute of the DOM element
    datafeed: Datafeed,
    library_path: '../charting_library_cloned_data/charting_library/',
});

```