---
title: "Frequently Asked Questions | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/getting_started/Frequently-Asked-Questions"
extracted_at: "2025-06-22T09:13:51.424Z"
---

# Frequently Asked QuestionsIf your question is not outlined below, you can ask it on [GitHub Issues](https://github.com/tradingview/charting_library/issues) 🔐 (access is [restricted](https://www.tradingview.com/charting-library-docs/latest/getting_started/quick-start#getting-access)) or join the [Discord discussions](https://discord.gg/UC7cGkvn4U).

## Data Management
**1. How do I connect my data? How to add new symbols?**Refer to the following articles for information on how to connect data:

- [Connecting Data](https://www.tradingview.com/charting-library-docs/latest/connecting_data/)
- [Datafeed API](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/)
- [UDF](https://www.tradingview.com/charting-library-docs/latest/connecting_data/UDF)
Also, consider the [Datafeed: Common Issues](https://www.tradingview.com/charting-library-docs/latest/connecting_data/Datafeed-Issues) article to avoid typical errors when implementing the Datafeed API.

Use the [Demo Chart](https://charting-library.tradingview-widget.com) to investigate how the library processes data. Open the Network tab in a browser console and filter requests by `demo-feed` to see all data requests and responses.

**2. Do you have an example of the Datafeed API implementation?**You can consider [UDF Adapter](https://github.com/tradingview/charting_library/tree/master/datafeeds/udf) 🔐 (access is [restricted](https://www.tradingview.com/charting-library-docs/latest/getting_started/quick-start#getting-access)) as an example of the Datafeed API implementation.

If you need a step-by-step guide, refer to the [How to connect data via Datafeed API](https://www.tradingview.com/charting-library-docs/latest/tutorials/implement_datafeed_tutorial/) tutorial.

**3. Do you have an example of a WebSocket data transport?**The [How to connect data via Datafeed API](https://www.tradingview.com/charting-library-docs/latest/tutorials/implement_datafeed_tutorial/) tutorial shows how to stream data using WebSocket.

**4. Do you have an example of a backend datafeed in ASP.NET, Python, PHP, etc. ?**The only example of a backend datafeed that we have is written in JavaScript for Node.js. For more information, refer to the [yahoo_datafeed](https://github.com/tradingview/yahoo_datafeed) repository.

**5. How can I display data stored in a TXT/CSV/XLSX file?**The library is intended to display data from a server, not a file. You should also keep in mind that according to the license agreement you can use the library on public websites only. If you still want to use a file as a data source, complete the following steps:

Write an application using any server language (.NET, PHP, Node.js, Python, etc.). This application should read a file and transfer data from it in the [UDF](https://www.tradingview.com/charting-library-docs/latest/connecting_data/UDF) format over HTTP(S).

Note: You can provide data in another format or use a WebSocket to transfer it, but in this case you need a custom [Datafeed API](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/) implementation.

Make sure a browser can send requests to your server. For this, you should either have a static IP or register a domain.

Open `index.html` and replace `demo_feed.tradingview.com` with the URL to your server.

**6. Why my data is not displayed / displayed incorrectly / incorrectly fetched from the server?**The first thing you should do to debug any issue is to [enable console logs](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#debug). These logs contain the most important actions performed in the library. You can also refer to the [Datafeed: Common Issues](https://www.tradingview.com/charting-library-docs/latest/connecting_data/Datafeed-Issues) article that might answer your question.

Note that most data issues occur because symbol information is set incorrectly. To avoid these issues, consider [Symbology](https://www.tradingview.com/charting-library-docs/latest/connecting_data/Symbology).

**7. The library is constantly asking for data. How to tell it that the data is over?**To do this, you should use a flag that notifies the library that there is no more data on the server. Set the status code to `no_data` or the [`noData`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.HistoryMetadata#nodata) property to `true` if you use [UDF](https://www.tradingview.com/charting-library-docs/latest/connecting_data/UDF#bars) or [Datafeed API](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/required-methods#correct-amount-of-data), respectively.

**8. How to change the number of decimal places for prices on the chart?**The number of decimal places depends on the [`pricescale`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LibrarySymbolInfo#pricescale) value. For more information on the price format, refer to the [Symbology](https://www.tradingview.com/charting-library-docs/latest/connecting_data/Symbology#price-format) article.

**9. What if I have a single price for each timestamp?**Since the library is intended to display multiple data types like candles, bars, and histograms, you are supposed to provide Open, High, Low, Close, and optional Volume for each timestamp. If you have a single price for each timestamp, you can pass `Open = High = Low = Close = price`. For better data visualization, you can change the default chart style to “Line” (refer to the [GUI](#gui) section).

**10. Why is `unsubscribeBars` called with a delay?**This is intentional.

Refer to the [`unsubscribeBars`](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/required-methods#unsubscribebars) method for more information.

**11. How to specify time properties within the library?**All time properties should be [Unix timestamps](https://developer.mozilla.org/en-US/docs/Glossary/Unix_time) in **seconds** unless otherwise stated. For example, the code sample below specifies boundary values of a time range.

```
const from = Date.now() / 1000 - 500 * 24 * 3600; // 500 days ago
const to = Date.now() / 1000;

```
**12. Does the library support the FIX protocol?**Advanced Charts / Trading Platform is a browser-based client-side solution. You can implement your backend data connection with any instruments, including the FIX protocol, based on your requirements. However, the library does not provide any pre-made data integrations with the FIX protocol.

The diagram below illustrates the data connection layers. You should integrate the FIX protocol between your backend and the data provider.

[![Diagram illustrating data connection layers](https://www.tradingview.com/charting-library-docs/img/diagram-fix-protocol.svg)](/charting-library-docs/img/diagram-fix-protocol.svg)
## GUI
**1. How can I subscribe to chart events?**You can subscribe to chart events in two ways:

Subscribe to [general](https://www.tradingview.com/charting-library-docs/latest/core_concepts/widget-methods#subscribe--unsubscribe) events that are related to a whole chart layout, not a specific chart.

Subscribe to events that are related to a [single](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#methods) chart such as [`isSelectBarRequested`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#isselectbarrequested).

Some methods that expose events only allow a subscription to be created by passing a single callback function, others return a [Subscription](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.ISubscription) object that can be used to subscribe and unsubscribe.

**2. How to change the default bar style?**You can use the [`mainSeriesProperties.style`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartPropertiesOverrides#mainseriespropertiesstyle) property to customize bar style.
Refer to the [Chart Overrides](https://www.tradingview.com/charting-library-docs/latest/customization/overrides/chart-overrides#chart-styles) article for information.
**3. How to customize the chart style?**The library provides extensive customization options through multiple APIs.
Refer to the [Customization](https://www.tradingview.com/charting-library-docs/latest/customization/) section for more information.
**4. How can I change the list of resolutions (time intervals) on the chart / disable them?**Refer to the [Resolution](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Resolution#configure-resolutions-in-datafeed) article for more information.

**5. How to enable the resolution in seconds?**Refer to the [Resolution in seconds](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Resolution#resolution-in-seconds) section for more information.

**6. How to hide a GUI element (symbol, interval, button, etc.)?**Most of GUI elements can be hidden using [featuresets](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets). There are base elements that cannot be hidden, but if you still want to get rid of them, you can use [CSS customization](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#custom_css_url). Note that names, classes, and identifiers of the DOM elements may be changed in the next versions of the product without any notifications.

**7. Why do the Ask/Bid buttons not work?**Make sure you have implemented the [`getQuotes`](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/trading-platform-methods#getquotes) method.

**8. Can I add custom buttons to areas of the UI other than the top toolbar?**Custom buttons created with [`createButton`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#createbutton) and [`createDropdown`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#createdropdown) can only be added to the [top toolbar](https://www.tradingview.com/charting-library-docs/latest/ui_elements/#top-toolbar).
However, there are other ways to customize the UI: you can add extra buttons to the [context menu](https://www.tradingview.com/charting-library-docs/latest/ui_elements/context-menu) and [Order Ticket](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/order-ticket),
or [modify other elements](https://www.tradingview.com/charting-library-docs/latest/customization/) to tailor the interface to your needs.
**9. Why an indicator is not plotted when the resolution is changed?**Indicators, such as *VWAP* and *Pivot Points*, use extensive historical data to calculate their values and may need more bars than are visible on the chart.
These indicators are plotted only after the library gets all required data.The library does not prefetch all data to avoid excessive requests.
Therefore, when the resolution is changed, users need to scroll the chart for the indicator to appear.
## Localization
**1. What languages does the library support? How can I add the language that is not supported?**The library supports a variety of languages.
You can find the complete list in the [Localization](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Localization#supported-languages) article.
Note that it is impossible to add your own language support.
**2. Could you provide the list of all UI strings so I can translate them?**We cannot provide the list of UI strings.
However, if you want to add custom translations,
you can use the [`custom_translate_function`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#custom_translate_function) property of the [Widget Constructor](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Widget-Constructor).
## Other Questions
**1. What is the difference between Widget, Advanced Charts, and Trading Platform?**

[Widget](https://tradingview.com/widget/) is connected to the TradingView data. Perfect for websites, blogs, and forums where you need a fast & free solution.

Integration is simply copying & pasting pre-made iframe code. Widget has lots of display modes.

[Advanced Charts](https://www.tradingview.com/HTML5-stock-forex-bitcoin-charting-library/) is a chart with your data.

This is a standalone solution that you download, host on your servers, and connect your data to. You can use it in your site/app for free.

[Trading Platform](https://www.tradingview.com/HTML5-stock-forex-bitcoin-charting-library/?feature=charting-and-trading-platform) is a standalone product that is licensed to brokers.

It contains all features available in Advanced Charts and also includes trading functionality, multiple-chart layouts, watchlists, details, news widgets, and other advanced tools. Trading Platform has its own licensing fees associated with it.

**2. Does TradingView have access to any user data through the integration?**No, TradingView does not collect any user data.
Advanced Charts and Trading Platform are self-hosted solutions that run independently on your servers, ensuring there is no interaction with TradingView on user data.
**3. Is there a way to see detailed logs when working with the library?**Yes, you can enable debug modes that provide detailed logs for data connection and trading features.
For more information, refer to [How to enable debug mode](https://www.tradingview.com/charting-library-docs/latest/tutorials/enable-debug-mode).
**4. What should I do if I encounter a bug while using the library?**If you come across a bug or issue while using the library, we recommend taking the following steps:

**Check for updates**.
Ensure that you are using the latest version of the library.
Sometimes, bugs are resolved in newer releases.
If you are not using the most recent version, [update the library](https://www.tradingview.com/charting-library-docs/latest/releases/Update-Library) before proceeding further.
**Reproduce the bug**.
After updating to the latest version, attempt to replicate the bug.
This step helps determine whether the issue persists in the updated version.
**Report the issue**.
If the bug persists even after updating to the latest version,
report it in [GitHub issues](https://github.com/tradingview/charting_library/issues) 🔐 (access is [restricted](https://www.tradingview.com/charting-library-docs/latest/getting_started/quick-start#getting-access)).
Provide detailed information about the issue, including steps to reproduce it, the library version, console logs, and any error messages encountered.
This allows us to investigate and address the issue promptly.

**5. Is it possible to reduce the size of the library?**Yes. You can remove locales from the [bundle file](https://www.tradingview.com/charting-library-docs/latest/getting_started/Package-Content#package-content) if your app does not support them.

**6. How do I add a custom indicator?**Refer to [Custom indicators](https://www.tradingview.com/charting-library-docs/latest/custom_studies/) for more information.

**7. Does the library support Rocket Loader by Cloudflare?**No, it does not. Please avoid using Rocket Loader.

**8. Do you provide iOS or Android SDKs like you do for Lightweight Charts?**No, not currently.
However, we have a collection of [integration examples](https://www.tradingview.com/charting-library-docs/latest/tutorials/#framework-integrations) for frameworks commonly used with Advanced Charts and Trading Platform.
You can check the following examples:
- [iOS WKWebView in Swift](https://github.com/tradingview/charting-library-examples/tree/master/ios-swift)
- [Android WebView](https://github.com/tradingview/charting-library-examples/tree/master/android)
- [React Native for iOS and Android](https://github.com/tradingview/charting-library-examples/tree/master/react-native)

**9. How to integrate the library with Flutter?**We do not have an example for integrating the library with Flutter currently. You can consider the [How to Build a Native Communication Bridge in Flutter with WebView and JavaScript](https://www.freecodecamp.org/news/how-to-build-a-native-communication-bridge-in-flutter-with-webview-and-javascript/) article that explains how to use Flutter with WebView and JavaScript.

**10. How to switch from Advanced Charts to Trading Platform?**Refer to the [How to migrate from Advanced Charts](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/#how-to-migrate-from-advanced-charts) topic for more information.

**11. Is it possible to use Pine Script® for creating and editing indicators?**[Pine Script®](https://www.tradingview.com/pine-script-docs/) is not supported in Advanced Charts or Trading Platform. Alternatively, you can create your custom indicator using JavaScript. For more information, refer to [Custom indicators](https://www.tradingview.com/charting-library-docs/latest/custom_studies/).

**12. Does Advanced Charts / Trading Platform support Alerts, Range Bars, Bar Replay Tool, and patterns?**Some features that are available on [tradingview.com](https://www.tradingview.com/chart/) are not supported in the libraries, including Alerts, Range Bars, Bar Replay Tool, and patterns. Refer to the [Unsupported features](https://www.tradingview.com/charting-library-docs/latest/getting_started/Key-Features#unsupported-features) section for more information.

**13. Why do I get error messages mentioning CSP or blob? **Content Security Policy (CSP) is a web security standard that helps prevent various types of attacks.
CSP defines a policy specifying which domains are considered trusted sources for content such as scripts, images, fonts, and other resources.The error message may look like the following:

```
Refused to load the image <URL>' because it violates the following Content Security Policy directive: "img-src 'self' blob data

```Depending on your use cases, implementation, browser compatibility, or internal company policies, you may encounter issues with some library features. These could include displaying screenshots, logos, or using emojis/icons within the chart.

We encourage you to properly assess the situation and choose the appropriate solution by reading the [Content Security Policy](https://developer.mozilla.org/en-US/docs/Web/HTTP/CSP) article.

When changing CSP is not allowed, you can enable the [`iframe_loading_compatibility_mode`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#iframe_loading_compatibility_mode) featureset. This featureset will instead use `about:blank` as the source URL and build the iframe HTML using `document.write`.

The blob method is the preferred approach but this featureset offers a fallback for non-standard applications.

**14. Does the library set cookies?**The library does not set any cookies.

If necessary, you can add your own cookies via server responses and restrict access to specific files, pages, or content based on the cookies set in the user's request.