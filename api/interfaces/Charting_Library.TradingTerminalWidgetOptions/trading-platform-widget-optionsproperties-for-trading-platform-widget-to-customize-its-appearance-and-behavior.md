---
title: "Interface: TradingTerminalWidgetOptions | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.TradingTerminalWidgetOptions/"
extracted_at: "2025-06-22T09:29:51.977Z"
---

# Interface: TradingTerminalWidgetOptions[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).TradingTerminalWidgetOptions

## Hierarchy

`Omit`<[`ChartingLibraryWidgetOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions), `"enabled_features"` | `"disabled_features"` | `"favorites"`>

↳ **`TradingTerminalWidgetOptions`**

## Properties
### additional_symbol_info_fields
• `Optional` **additional_symbol_info_fields**: [`AdditionalSymbolInfoField`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.AdditionalSymbolInfoField)

An optional field containing an array of custom symbol info fields to be shown in the Security Info dialog.

Refer to [Symbology](https://www.tradingview.com/charting-library-docs/latest/connecting_data/Symbology) for more information about symbol info.

```
additional_symbol_info_fields: [
    { title: 'Ticker', propertyName: 'ticker' }
]

```
#### Inherited from
Omit.additional_symbol_info_fields

### auto_save_delay
• `Optional` **auto_save_delay**: `number`

A threshold delay in seconds that is used to reduce the number of `onAutoSaveNeeded` calls.

```
auto_save_delay: 5,

```
#### Inherited from
Omit.auto_save_delay

### autosize
• `Optional` **autosize**: `boolean`

Boolean value showing whether the chart should use all the available space in the container and resize when the container itself is resized.

**`Default`**

false

```
autosize: true,

```
#### Inherited from
Omit.autosize

### brokerConfig
• `Optional` **brokerConfig**: [`SingleBrokerMetaInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SingleBrokerMetaInfo)

**`Deprecated`**

Defines the [configuration flags](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/trading-features-configuration) for the Trading Platform.

### broker_config
• `Optional` **broker_config**: [`SingleBrokerMetaInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SingleBrokerMetaInfo)

Defines the [configuration flags](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/trading-features-configuration) for the Trading Platform.

### charts_storage_api_version
• `Optional` **charts_storage_api_version**: [`AvailableSaveloadVersions`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#availablesaveloadversions)

A version of your backend. Supported values are: `"1.0"` | `"1.1"`. Study Templates are supported starting from version `"1.1"`.

```
charts_storage_api_version: "1.1",

```
#### Inherited from
Omit.charts_storage_api_version

### charts_storage_url
• `Optional` **charts_storage_url**: `string`

Set the storage URL endpoint for use with the high-level saving/loading chart API.
Refer to [Save and load REST API](https://www.tradingview.com/charting-library-docs/latest/saving_loading/save-load-rest-api/) for more information.
```
charts_storage_url: 'http://storage.yourserver.com',

```
#### Inherited from
Omit.charts_storage_url

### client_id
• `Optional` **client_id**: `string`

Set the client ID for the high-level saving / loading charts API.
Refer to [Saving and Loading Charts](https://www.tradingview.com/charting-library-docs/latest/saving_loading/) for more information.
```
client_id: 'yourserver.com',

```
#### Inherited from
Omit.client_id

### compare_symbols
• `Optional` **compare_symbols**: [`CompareSymbol`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CompareSymbol)

an array of custom compare symbols for the Compare window.

Example:

```
compare_symbols: [
    { symbol: 'DAL', title: 'Delta Air Lines' },
    { symbol: 'VZ', title: 'Verizon' },
],

```
#### Inherited from
Omit.compare_symbols

### container
• **container**: `string` | `HTMLElement`

The `container` can either be a reference to an attribute of a DOM element inside which the iframe with the chart will be placed or the `HTMLElement` itself.

```
container: "tv_chart_container",

```
or

```
container: document.getElementById("tv_chart_container"),

```
#### Inherited from
Omit.container

### context_menu
• `Optional` **context_menu**: [`ContextMenuOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ContextMenuOptions)

Use this property to override the [context menu](https://www.tradingview.com/charting-library-docs/latest/ui_elements/context-menu). You can also change the menu on the fly using the [IChartingLibraryWidget.onContextMenu](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#oncontextmenu) method.

#### Inherited from
Omit.context_menu

### custom_chart_description_function
• `Optional` **custom_chart_description_function**: [`ChartDescriptorFunction`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#chartdescriptorfunction)

Use this property to set your own chart description function. `context` will be passed to the function.

This description is read aloud by screen readers when a chart within the layout is selected via the `Tab` key.

The function should return either a string with a description or `null` to fallback to the default description.

```
custom_chart_description_function: (context) => {
    return Promise.resolve(`Chart ${context.chartIndex + 1} of ${context.chartCount}. ${context.chartTypeName} chart of ${context.symbol}.`);
}

```
#### Inherited from
Omit.custom_chart_description_function

### custom_css_url
• `Optional` **custom_css_url**: `string`

Adds your custom CSS to the chart. `url` should be an absolute or relative path to the `static` folder.

```
custom_css_url: 'css/style.css',

```
#### Inherited from
Omit.custom_css_url

### custom_font_family
• `Optional` **custom_font_family**: `string`

Changes the font family used on the chart including the [time scale](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Time-Scale), [price scale](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Price-Scale), and chart's pane.
If you want to customize fonts outside the chart, for example, within [Watchlist](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/Watch-List) or another widget,
you should use the [ChartingLibraryWidgetOptions.custom_css_url](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#custom_css_url) property to provide custom CSS styles.
Specify `custom_font_family` in [Widget Constructor](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Widget-Constructor) as follows:

```
custom_font_family: "'Inconsolata', monospace",

```
The `custom_font_family` value should have the same format as the `font-family` property in CSS.
To use a font that is not available by default on your system, you should first add this font to your [custom CSS](#custom_css_url).
For example, the code sample below imports a Google font into your custom CSS:
```
@import url('https://fonts.googleapis.com/css2?family=Inconsolata:wght@500&display=swap');

```
#### Inherited from
Omit.custom_font_family

### custom_formatters
• `Optional` **custom_formatters**: [`CustomFormatters`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CustomFormatters)

Custom formatters for adjusting the display format of price, date, and time values.

Example:

```
custom_formatters: {
timeFormatter: {
	format: (date) => {
		const _format_str = '%h:%m';
		return _format_str
			.replace('%h', date.getUTCHours(), 2)
			.replace('%m', date.getUTCMinutes(), 2)
			.replace('%s', date.getUTCSeconds(), 2);
	}
},
dateFormatter: {
	format: (date) => {
		return date.getUTCFullYear() + '/' + (date.getUTCMonth() + 1) + '/' + date.getUTCDate();
	}
},
tickMarkFormatter: (date, tickMarkType) => {
	switch (tickMarkType) {
		case 'Year':
			return 'Y' + date.getUTCFullYear();

		case 'Month':
			return 'M' + (date.getUTCMonth() + 1);

		case 'DayOfMonth':
			return 'D' + date.getUTCDate();

		case 'Time':
			return 'T' + date.getUTCHours() + ':' + date.getUTCMinutes();

		case 'TimeWithSeconds':
			return 'S' + date.getUTCHours() + ':' + date.getUTCMinutes() + ':' + date.getUTCSeconds();
	}

	throw new Error('unhandled tick mark type ' + tickMarkType);
},
priceFormatterFactory: (symbolInfo, minTick) => {
	if (symbolInfo?.fractional || minTick !== 'default' && minTick.split(',')[2] === 'true') {
		return {
			format: (price, signPositive) => {
				// return the appropriate format
			},
		};
	}
	return null; // this is to use default formatter;
},
studyFormatterFactory: (format, symbolInfo) => {
    if (format.type === 'price') {
        const numberFormat = new Intl.NumberFormat('en-US', { notation: 'scientific' });
        return {
            format: (value) => numberFormat.format(value)
        };
    }

    if (format.type === 'volume') {
        return {
            format: (value) => (value / 1e9).toPrecision(format?.precision || 2) + 'B'
        };
    }

    if (format.type === 'percent') {
        return {
            format: (value) => `${value.toPrecision(format?.precision || 4)} percent`
        };
    }

    return null; // this is to use default formatter;
},
}

```
**Remark**: `tickMarkFormatter` must display the UTC date, and not the date corresponding to your local timezone.

#### Inherited from
Omit.custom_formatters

### custom_indicators_getter
• `Optional` **custom_indicators_getter**: (`PineJS`: [`PineJS`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PineJS)) => `Promise`<readonly [`CustomIndicator`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CustomIndicator)>

Function that returns a Promise object with an array of your custom indicators.

`PineJS` variable will be passed as the first argument of this function and can be used inside your indicators to access internal helper functions.

Refer to [Custom indicators](https://www.tradingview.com/charting-library-docs/latest/custom_studies/) for more information.

```
custom_indicators_getter: function(PineJS) {
    return Promise.resolve([
        // *** your indicator object, created from the template ***
    ]);
},

```
#### Type declaration
▸ (`PineJS`): `Promise`<readonly [`CustomIndicator`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CustomIndicator)>

##### Parameters

 **|Name** | **Type** ||
| `PineJS` | [`PineJS`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.PineJS) ||

##### Returns
`Promise`<readonly [`CustomIndicator`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CustomIndicator)>

#### Inherited from
Omit.custom_indicators_getter

### custom_themes
• `Optional` **custom_themes**: [`CustomThemes`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CustomThemes)

Custom theme colors to override the default light and dark themes. For more information on custom themes, refer to the [Custom themes API](https://www.tradingview.com/charting-library-docs/latest/customization/styles/custom-themes) article.

#### Inherited from
Omit.custom_themes

### custom_timezones
• `Optional` **custom_timezones**: [`CustomAliasedTimezone`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CustomAliasedTimezone)

List of custom time zones.

Refer to [Timezones](https://www.tradingview.com/charting-library-docs/latest/ui_elements/timezones) for more information.

#### Inherited from
Omit.custom_timezones

### custom_translate_function
• `Optional` **custom_translate_function**: [`CustomTranslateFunction`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#customtranslatefunction)

Use this property to set a custom translation function for UI strings.
It accepts the original text, the singular form of the text, and the translated text as arguments.
The function should return a string with the new translation or `null` to fall back to the default translation.
The example below shows how to rename the "Trend Line" drawing to "Line Drawing".

```
custom_translate_function: (originalText, singularOriginalText, translatedText) => {
    if (originalText === "Trend Line") {
        return "Line Drawing";
    }
    return null;
}

```
#### Inherited from
Omit.custom_translate_function

### datafeed
• **datafeed**: [`IBasicDataFeed`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#ibasicdatafeed) | [`IDatafeedChartApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IDatafeedChartApi) & [`IExternalDatafeed`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IExternalDatafeed) & [`IDatafeedQuotesApi`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IDatafeedQuotesApi)

JavaScript object that implements the datafeed interface ([IBasicDataFeed](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#ibasicdatafeed)) to supply the chart with data. See [Connecting Data](https://www.tradingview.com/charting-library-docs/latest/connecting_data/) for more information on the JS API.

```
datafeed: new Datafeeds.UDFCompatibleDatafeed("https://demo_feed.tradingview.com")

```
#### Inherited from
Omit.datafeed

### debug
• `Optional` **debug**: `boolean`

Setting this property to `true` makes the library write detailed [Datafeed API](https://www.tradingview.com/charting-library-docs/latest/connecting_data/datafeed-api/) logs into the browser console.
Alternatively, you can use the [`charting_library_debug_mode`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#charting_library_debug_mode) featureset or the [IChartingLibraryWidget.setDebugMode](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#setdebugmode) method.
```
debug: true,

```
#### Inherited from
Omit.debug

### debug_broker
• `Optional` **debug_broker**: [`BrokerDebugMode`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#brokerdebugmode)

Setting this property makes the library write detailed [Broker API](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/#broker-api) and [Trading Host](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/#trading-host) logs into the browser console.

```
debug_broker: 'normal',

```
The logs include the calls and return values for methods invoked on the
host ([IBrokerConnectionAdapterHost](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost)) and broker ([IBrokerTerminal](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal)).
Since the method calls can be asynchronous, you can use the ID numbers in each message to match
the calls to responses.

### disabled_features
• `Optional` **disabled_features**: [`TradingTerminalFeatureset`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#tradingterminalfeatureset)

The array containing names of features that should be disabled by default. `Feature` means part of the functionality of the chart (part of the UI/UX). Supported features are listed in [Featuresets](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets).

Example:

```
disabled_features: ["header_widget", "left_toolbar"],

```

### drawings_access
• `Optional` **drawings_access**: [`AccessList`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.AccessList)

You can hide some drawings from the toolbar or add custom restrictions for applying them to the chart.

This property has the same structure as the `studies_access` argument. Use the same names as you see in the UI.

**Remark**: There is a special case for font-based drawings. Use the "Font Icons" name for them.
Those drawings cannot be enabled or disabled separately - the entire group will have to be either enabled or disabled.
**`Example`**

```
drawings_access: {
    type: 'black',
    tools: [
        {
            name: 'Trend Line',
            grayed: true
        },
    ]
},

```
#### Inherited from
Omit.drawings_access

### enabled_features
• `Optional` **enabled_features**: [`TradingTerminalFeatureset`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#tradingterminalfeatureset)

The array containing names of features that should be enabled by default. `Feature` means part of the functionality of the chart (part of the UI/UX). Supported features are listed in [Featuresets](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets).

Example:

```
enabled_features: ["move_logo_to_main_pane"],

```

### favorites
• `Optional` **favorites**: [`Favorites`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.Favorites)<[`TradingTerminalChartTypeFavorites`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#tradingterminalcharttypefavorites)>

See [ChartingLibraryWidgetOptions.favorites](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#favorites)

### fullscreen
• `Optional` **fullscreen**: `boolean`

Boolean value showing whether the chart should use all the available space in the window.

**`Default`**

false

```
fullscreen: true,

```
#### Inherited from
Omit.fullscreen

### header_widget_buttons_mode
• `Optional` **header_widget_buttons_mode**: [`HeaderWidgetButtonsMode`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#headerwidgetbuttonsmode)

An additional optional field to change the look and feel of buttons on the top toolbar.

By default (if option is omitted) header will be in adaptive mode (fullsize if the window width allows and icons on smaller windows).

Example:

```
header_widget_buttons_mode: 'fullsize',

```
#### Inherited from
Omit.header_widget_buttons_mode

### height
• `Optional` **height**: `number`

The desired height of a widget. Please make sure that there is enough space for the widget to be displayed correctly.

```
height: 600,

```
**Remark**: If you want the chart to use all the available space use the `fullscreen` parameter instead of setting it to '100%'.

#### Inherited from
Omit.height

### image_storage_adapter
• `Optional` **image_storage_adapter**: [`IImageStorageAdapter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IImageStorageAdapter)

EXPERIMENTAL. Customise the storage of image data for the image drawing tool.

By default images have no size limit and are saved in the chart layout which may not be suitable, depending on your chart storage implementation.

#### Inherited from
Omit.image_storage_adapter

### interval
• **interval**: [`ResolutionString`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#resolutionstring)

The default interval for the chart.

Example:

```
interval: '1D',

```
#### Inherited from
Omit.interval

### library_path
• `Optional` **library_path**: `string`

A path to a `static` folder.

```
library_path: "charting_library/",

```

- If you would like to host the library on a separate origin to the page containing the chart then please view the following guide: [Hosting the library on a separate origin](https://www.tradingview.com/charting-library-docs/latest/getting_started/Hosting-Library-Cross-Origin).

#### Inherited from
Omit.library_path

### load_last_chart
• `Optional` **load_last_chart**: `boolean`

Set this parameter to `true` if you want the library to load the last saved chart for a user. You should implement [save/load](https://www.tradingview.com/charting-library-docs/latest/saving_loading/) first to make it work.

Note that the [symbol](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#symbol) property takes precedence over `load_last_chart`. If `symbol` is specified, its value is displayed on the chart instead of the saved symbol. To avoid this issue, consider removing the `symbol` property when `load_last_chart` is enabled.

```
load_last_chart: true,

```
#### Inherited from
Omit.load_last_chart

### loading_screen
• `Optional` **loading_screen**: [`LoadingScreenOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.LoadingScreenOptions)

Customization of the loading spinner. Value is an object with the following possible keys:

- `backgroundColor`
- `foregroundColor`

Example:

```
loading_screen: { backgroundColor: "#000000" }

```
#### Inherited from
Omit.loading_screen

### locale
• **locale**: [`LanguageCode`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#languagecode)

Locale to be used by the library. See [Localization](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Localization) section for details.

```
locale: 'en',

```
#### Inherited from
Omit.locale

### news_provider
• `Optional` **news_provider**: [`GetNewsFunction`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#getnewsfunction)

Use this property to connect any custom news source to the *News* widget. To do this, you should specify [GetNewsFunction](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#getnewsfunction) that the library calls to request data for the widget.
In response, you should pass a [GetNewsResponse](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.GetNewsResponse) object to the callback function.
In this object, specify an array of [NewsItem](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.NewsItem) objects that contain data for each news item.
For more information, refer to the [News](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/news) article.
Note that if both [rss_news_feed](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.TradingTerminalWidgetOptions#rss_news_feed) and `news_provider` properties are specified, `rss_news_feed` is ignored.
Consider the following example. An API endpoint returns news items represented in JSON and the format matches the `NewsItem` interface.
In this case, you implement `GetNewsFunction` as follows:
```
const jsonNewsApiUrl = 'https://www.example.com';
new TradingView.widget({
    // ...
    news_provider: function getNews(symbol, callback) {
        const requestUrl = new URL('/news/', jsonNewsApiUrl);
        requestUrl.searchParams.append('symbol', symbol);
        fetch(requestUrl)
            .then(res => res.json())
            .then(json => {
                callback({
                    newsItems: json,
                });
            });
    }
});

```

### numeric_formatting
• `Optional` **numeric_formatting**: [`NumericFormattingParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.NumericFormattingParams)

The object containing formatting options for numbers. The only possible option is `decimal_sign` currently.

```
numeric_formatting: { decimal_sign: "," },

```
#### Inherited from
Omit.numeric_formatting

### overrides
• `Optional` **overrides**: `Partial`<[`WidgetOverrides`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#widgetoverrides)>

Override values for the default widget properties
You can override most of the properties (which also may be edited by user through UI)
using `overrides` parameter of Widget Constructor. `overrides` is supposed to be an object.
The keys of this object are the names of overridden properties.
The values of these keys are the new values of the properties.
Example:

```
overrides: {
    "mainSeriesProperties.style": 2
}

```
This code will change the default series style to "line".
All customizable properties are listed in [separate article](https://www.tradingview.com/charting-library-docs/latest/customization/overrides/).
#### Inherited from
Omit.overrides

### restConfig
• `Optional` **restConfig**: [`RestBrokerConnectionInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RestBrokerConnectionInfo)

Connection configuration settings for Rest Broker API

### rss_news_feed
• `Optional` **rss_news_feed**: [`RssNewsFeedParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RssNewsFeedParams)

Use this property to connect a RSS feed to the *News* widget. To do this, specify a [RssNewsFeedParams](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.RssNewsFeedParams) object that should contain at least the default RSS configuration.
You can specify a different RSS for each symbol type or use only one for all symbols. For more information, refer to the [News](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/news) article.
Note that if both `rss_news_feed` and [news_provider](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.TradingTerminalWidgetOptions#news_provider) properties are specified, `rss_news_feed` is ignored.
**`Example`**

```
rss_news_feed: {
    "default": {
        url: "https://articlefeeds.nasdaq.com/nasdaq/symbols?symbol={SYMBOL}",
        name: "NASDAQ"
    }
}

```

### rss_news_title
• `Optional` **rss_news_title**: `string`

Title for the News Widget

### save_load_adapter
• `Optional` **save_load_adapter**: [`IExternalSaveLoadAdapter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IExternalSaveLoadAdapter)

An object containing the save/load functions.
It is used to implement a custom save/load algorithm.
Refer to [API handlers](https://www.tradingview.com/charting-library-docs/latest/saving_loading/save-load-adapter) for more information.
#### Inherited from
Omit.save_load_adapter

### saved_data
• `Optional` **saved_data**: `object`

JS object containing saved chart content.
Use this parameter when creating the widget if you have a saved chart already.
If you want to load the chart content when the chart is initialized then use `load()` method ([IChartingLibraryWidget.load](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#load)) of the widget.
#### Inherited from
Omit.saved_data

### saved_data_meta_info
• `Optional` **saved_data_meta_info**: [`SavedStateMetaInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.SavedStateMetaInfo)

JS object containing saved chart content meta info.

#### Inherited from
Omit.saved_data_meta_info

### settings_adapter
• `Optional` **settings_adapter**: [`ISettingsAdapter`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISettingsAdapter)

An object that contains set/remove functions. Use it to save [user settings](https://www.tradingview.com/charting-library-docs/latest/saving_loading/user-settings) to your preferred storage, including the server-side one.

Example:

```
settings_adapter: {
    initialSettings: { ... },
    setValue: function(key, value) { ... },
    removeValue: function(key) { ... },
}

```
#### Inherited from
Omit.settings_adapter

### settings_overrides
• `Optional` **settings_overrides**: [`Overrides`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.Overrides)

The object that contains new values for values saved to the settings.
These overrides will replace any matching values from the settings, regardless of where the settings are loaded from (i.e. local storage or a custom settings adapter).
The object is similar to the [overrides](#overrides) object.
[overrides](#overrides) will not affect values that have been saved to settings so this option can be used instead.

```
settings_overrides: {
    "linetooltrendline.linecolor": "blue"
}

```
#### Inherited from
Omit.settings_overrides

### snapshot_url
• `Optional` **snapshot_url**: `string`

This URL is used to send a POST request with binary chart snapshots when a user presses the [snapshot](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Snapshots) button.
This POST request contains `multipart/form-data` with the field `preparedImage` that represents binary data of the snapshot image in `image/png` format.
This endpoint should return the full URL of the saved image in the response.

```
snapshot_url: "https://myserver.com/snapshot",

```
#### Inherited from
Omit.snapshot_url

### studies_access
• `Optional` **studies_access**: [`AccessList`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.AccessList)

You can hide some studies from the toolbar or add custom restrictions for applying them to the chart.

**`Example`**

```
studies_access: {
    type: "black" | "white",
    tools: [
        {
            name: "<study name>",
            grayed: true
        },
        < ... >
    ]
}

```
#### Inherited from
Omit.studies_access

### studies_overrides
• `Optional` **studies_overrides**: `Partial`<[`StudyOverrides`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyOverrides)>

Use this option to customize the style or inputs of the indicators.
You can also customize the styles and inputs of the `Compare` series using this argument.
Refer to [Indicator Overrides](https://www.tradingview.com/charting-library-docs/latest/customization/overrides/indicator-overrides#specify-default-properties) for more information.
Overrides for built-in indicators are listed in [StudyOverrides](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.StudyOverrides).
```
studies_overrides: {
    "volume.volume.color.0": "#00FFFF",
},

```
#### Inherited from
Omit.studies_overrides

### study_count_limit
• `Optional` **study_count_limit**: `number`

Maximum amount of studies allowed at one time within the layout. Minimum value is 2.

```
study_count_limit: 5,

```
#### Inherited from
Omit.study_count_limit

### symbol
• `Optional` **symbol**: `string`

The default symbol for the chart.

Example:

```
symbol: 'AAPL',

```
#### Inherited from
Omit.symbol

### symbol_search_complete
• `Optional` **symbol_search_complete**: [`SymbolSearchCompleteOverrideFunction`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#symbolsearchcompleteoverridefunction)

Use this property to set a function to override the symbol input from the [Symbol Search](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Symbol-Search).

For example, you may want to get additional input from the user before deciding which symbol should be resolved.

The function should take two parameters: a `string` of input from the Symbol Search and a optional search result item. It should return a `Promise` that resolves with a symbol ticker and a human-friendly symbol name.

**NOTE:** This override is not called when adding a symbol to the watchlist.

```
{
    // `SearchSymbolResultItem` is the same interface as for items returned to the Datafeed's searchSymbols result callback.
    symbol_search_complete: (symbol: string, searchResultItem?: SearchSymbolResultItem) => {
        return new Promise((resolve) => {
            let symbol = getNewSymbol(symbol, searchResultItem);
            let name = getHumanFriendlyName(symbol, searchResultItem)
            resolve({ symbol: symbol, name: name });
        });
    }
}

```
#### Inherited from
Omit.symbol_search_complete

### symbol_search_request_delay
• `Optional` **symbol_search_request_delay**: `number`

A threshold delay in milliseconds that is used to reduce the number of search requests when the user enters the symbol name in the [Symbol Search](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Symbol-Search).

```
symbol_search_request_delay: 1000,

```
#### Inherited from
Omit.symbol_search_request_delay

### theme
• `Optional` **theme**: [`ThemeName`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#themename)

Set predefined custom theme color for the chart. Supported values are: `"light"` | `"dark"`.

```
theme: "light",

```
#### Inherited from
Omit.theme

### time_frames
• `Optional` **time_frames**: [`TimeFrameItem`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.TimeFrameItem)

List of visible time frames that can be selected at the bottom of the chart. See [Time frame toolbar](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Time-Scale#time-frame-toolbar) for more information. Time frame is an object containing the following properties:

Example:

```
time_frames: [
    { text: "50y", resolution: "6M", description: "50 Years" },
    { text: "3y", resolution: "1W", description: "3 Years", title: "3yr" },
    { text: "8m", resolution: "1D", description: "8 Month" },
    { text: "3d", resolution: "5", description: "3 Days" },
    { text: "1000y", resolution: "1W", description: "All", title: "All" },
]

```
#### Inherited from
Omit.time_frames

### time_scale
• `Optional` **time_scale**: [`TimeScaleOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.TimeScaleOptions)

An additional optional field to add more bars on screen.

Example:

```
time_scale: {
    min_bar_spacing: 10,
}

```
#### Inherited from
Omit.time_scale

### timeframe
• `Optional` **timeframe**: [`TimeframeOption`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#timeframeoption)

Sets the default time frame of the chart.

The time frame can be relative to the current date, or a range.

A relative time frame is a number with a letter D for days and M for months:

```
timeframe: '3M',

```
A range is an object with to and from properties. The to and from properties should be UNIX timestamps:

```
timeframe: { from: 1640995200, to: 1643673600 } // from 2022-01-01 to 2022-02-01

```
**Note**:
When using a range the chart will still request data up to the current date. This is to enable scrolling forward in time once the chart has loaded.
#### Inherited from
Omit.timeframe

### timezone
• `Optional` **timezone**: `"exchange"` | [`Timezone`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#timezone)

Default time zone of the chart. The time on the timescale is displayed according to this time zone.
See the [list of supported time zones](https://www.tradingview.com/charting-library-docs/latest/ui_elements/timezones#supported-time-zones) for available values. Set it to `exchange` to use the exchange time zone. Use the [ChartingLibraryWidgetOptions.overrides](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#overrides) section if you wish to override the default value.
```
timezone: "America/New_York",

```
#### Inherited from
Omit.timezone

### toolbar_bg
• `Optional` **toolbar_bg**: `string`

Background color of the toolbars.

```
toolbar_bg: '#f4f7f9',

```
#### Inherited from
Omit.toolbar_bg

### trading_customization
• `Optional` **trading_customization**: [`TradingCustomization`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.TradingCustomization)

Overrides order and position lines created either using the [Broker API](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/#broker-api) or [IChartWidgetApi.createOrderLine](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#createorderline) and [IChartWidgetApi.createPositionLine](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#createpositionline) methods.

### user_id
• `Optional` **user_id**: `string`

Set the user ID for the high-level saving / loading charts API.
Refer to [Saving and Loading Charts](https://www.tradingview.com/charting-library-docs/latest/saving_loading/) for more information.
```
user_id: 'public_user_id',

```
#### Inherited from
Omit.user_id

### widgetbar
• `Optional` **widgetbar**: [`WidgetBarParams`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.WidgetBarParams)

Settings for the widget panel on the right side of the chart.
Watchlist, news, details and data window widgets on the right side of the chart can be enabled using the `widgetbar` field in Widget Constructor

### width
• `Optional` **width**: `number`

The desired width of a widget. Please make sure that there is enough space for the widget to be displayed correctly.

```
width: 300,

```
**Remark**: If you want the chart to use all the available space use the `fullscreen` parameter instead of setting it to '100%'.

#### Inherited from
Omit.width

## Methods
### broker_factory
▸ **broker_factory**(`host`): [`IBrokerTerminal`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal)

Use this field to pass the function that returns a new object which implements Broker API. This is a function that accepts the Trading Host ([IBrokerConnectionAdapterHost](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost)).

#### Parameters

 **|Name** | **Type** | **Description** ||
| `host` | [`IBrokerConnectionAdapterHost`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost) | Trading Host ||

#### Returns
[`IBrokerTerminal`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerTerminal)

**`Example`**

```
broker_factory: function(host) { ... }

```