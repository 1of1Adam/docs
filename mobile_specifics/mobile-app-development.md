---
title: "Mobile app development | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/mobile_specifics/"
extracted_at: "2025-06-22T09:16:16.866Z"
---

# Mobile app development## Overview
Advanced Charts and [Trading Platform](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/) are compatible with mobile devices.

The chart layout adapts to the device type and screen size by resizing/hiding elements.
This means that the following features **may not be supported** on smaller devices:

- The right widget bar that includes [Watchlist](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/Watch-List), [Details](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/#details), [News](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/news), and Data Window widgets.
- [Marks](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Marks#marks-on-the-time-scale) on the time scale.
- The [Account Manager](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/account-manager/) at the bottom bar. Instead, the Account Manager will be available through the *Broker* button () in the [legend](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Legend). You can disable this button by adding the [`broker_button`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#broker_button) featureset to the [`disabled_features`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#disabled_features) array.

The library supports mouse and touch-based inputs and recognizes single and multi-touch gestures.
It is available on all major browsers such as Google Chrome, Firefox, Safari, Opera, and Microsoft Edge, including their mobile versions.
### Mobile specifics
You should be aware of the following mobile specifics:

- The chart legend shows a close price and percentage change. Open, high, and low prices and indicator values are displayed in tracking mode only. To activate this mode, a user should long tap on the bar and make a single tap on the chart to exit.
You should implement the [`getQuotes`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IDatafeedQuotesApi#getquotes) and [`subscribeQuotes`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IDatafeedQuotesApi#subscribequotes) methods to display data in the [legend](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Legend) if you use Trading Platform.
Otherwise, [NaN values](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Legend#nan-values-in-legend) will appear in the legend instead of the expected data.
- The percentage change of the price is calculated based on intraday quotes, not the previous bar.
- Only one price scale can be displayed on the chart.

The following [featuresets](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets) affect chart behavior on mobile devices:

- `show_zoom_and_move_buttons_on_touch` enables zoom in/out and scroll left/right buttons.
- `horz_touch_drag_scroll` and `vert_touch_drag_scroll` enable horizontal/vertical page scroll.
- `pinch_scale` enables scaling using pinch gestures.

### Gestures

- **Single tap** allows you to drag the chart left or right, as well as to adjust the [price](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Price-Scale) and [time](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Time-Scale) scales by dragging.
**Long press**

- Opens a context menu for [price](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Price-Scale) and [time](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Time-Scale) scales.
- Enables crosshair mode on the chart, allowing for detailed data visualization in the [legend](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Legend).

- **Double tap** activates line movement mode: double-click a line, then drag it vertically to adjust its position.

## Mobile applications
You can embed Advanced Charts and Trading Platform inside a mobile application using a web view. Native wrappers for iOS or Android are not provided. Consider the following integration examples:

- [TradingView Advanced Charts Android Integration Example](https://github.com/tradingview/charting-library-examples/tree/master/android)
- [TradingView Advanced Charts iOS (Swift version) Integration Example](https://github.com/tradingview/charting-library-examples/tree/master/ios-swift)
- [TradingView Advanced Charts React-Native Integration Example](https://github.com/tradingview/charting-library-examples/tree/master/react-native)

We do not have an example of integrating the library with Flutter currently. You can consider the [How to Build a Native Communication Bridge in Flutter with WebView and JavaScript](https://www.freecodecamp.org/news/how-to-build-a-native-communication-bridge-in-flutter-with-webview-and-javascript/) article.

### Frequently Asked Questions
#### The library Android Integration Example demonstrates a white screen. How to fix it?
Make sure that the WebView version installed on your device supports ES6. We recommend you update to the latest WebView version to avoid potential issues. For more information, refer to the [WebView for Android](https://developer.chrome.com/docs/multidevice/webview/) article.

#### What is the minimum Android version required for the library?
The minimum Android version for the library is Android 5.0 (Lollipop). Starting from this version, you can update WebView separately to the Android platform. For more information, refer to the [WebView for Android](https://developer.chrome.com/docs/multidevice/webview/) article.

#### How to check the library for errors?

- For Android applications, use Chrome DevTools. Refer to the [Remote debug Android devices](https://developer.chrome.com/docs/devtools/remote-debugging/) and [Remote debugging WebViews](https://developer.chrome.com/docs/devtools/remote-debugging/webviews/) articles for more information.
- For iOS applications, use [Safari Web Inspector](https://developer.apple.com/library/archive/documentation/AppleApplications/Conceptual/Safari_Developer_Guide/Introduction/Introduction.html). Refer to the [Enabling Web Inspector](https://webkit.org/web-inspector/enabling-web-inspector/) article for more information.

#### How to transfer data from native code to JavaScript code?
You should use a mechanism that allows the execution of arbitrary code. Refer to the following articles for more information:

- [evaluateJavascript](https://developer.android.com/reference/android/webkit/WebView#evaluateJavascript(java.lang.String,%20android.webkit.ValueCallback%3Cjava.lang.String%3E)) for Android
- [evaluateJavaScript](https://developer.apple.com/documentation/webkit/wkwebview/1415017-evaluatejavascript?changes=_8) for iOS

You can consider the following projects as examples of interaction between the native code and JavaScript library:

- [Android Lightweight Charts](https://github.com/tradingview/lightweight-charts-android)
- [LightweightChartsIOS](https://github.com/tradingview/LightweightChartsIOS)

#### How to open links in the built-in mobile browser instead of the web view on Android?
You can use the [`shouldOverrideUrlLoading`](https://developer.android.com/reference/android/webkit/WebViewClient#shouldOverrideUrlLoading(android.webkit.WebView,%20android.webkit.WebResourceRequest)) method to implement custom logic for loading URLs. To open a built-in web browser, you should use [`Intent`](https://developer.android.com/reference/android/content/Intent) with the `ACTION_VIEW` parameter.

- Java- Kotlin```
Intent browserIntent = new Intent(Intent.ACTION_VIEW, Uri.parse("https://www.tradingview.com/"));
startActivity(browserIntent);

``````
val browserIntent = Intent(Intent.ACTION_VIEW, Uri.parse("https://www.tradingview.com/"))
startActivity(browserIntent)

```
You can also open links in Google Chrome Custom Tabs. Refer to [Implementation guide](https://developer.chrome.com/docs/android/custom-tabs/integration-guide/) for more information.

#### How to resolve a truncated price and time scales issue?
This issue occurs only when emulating a mobile device on a Chrome-based browser.
However, when using the charts on an actual mobile device, both the price and time scales will display correctly.