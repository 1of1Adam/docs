---
title: "Keyboard shortcuts | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/getting_started/Shortcuts"
extracted_at: "2025-06-22T09:14:05.971Z"
---

# Keyboard shortcuts
## Overview
This article lists shortcuts built in Advanced Charts and Trading Platform. It also [explains](#manage-shortcuts) how to override the default shortcuts and specify custom ones.

> **Info:** The shortcut dialog that can be seen on [tradingview.com](https://www.tradingview.com/chart/) is not available in the libraries. Therefore, you need to implement a custom dialog if necessary.

## Advanced Charts shortcuts
The shortcuts below are available in Advanced Charts and Trading Platform.

> **Tip:** On macOS, you can use ⌘/⌥/⇧ instead of Ctrl/Alt/Shift.

### Chart
You can use the following shortcuts to interact with the [chart](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Chart).

 **|Action** | **Shortcut** ||
| Open Quick Search | Ctrl + K ||
| Open indicators | / ||
| Load chart layout | . ||
| Save chart layout | Ctrl + S ||
| Undo | Ctrl + Z ||
| Redo | Ctrl + Y ||
| Change symbol | Start typing a symbol name ||
| Change interval | Digit or , ||
| Move chart 1 bar to the left | ← ||
| Move chart 1 bar to the right | → ||
| Move chart to the left/right | Shift + Mouse wheel ||
| Zoom in | Ctrl + ↑ ||
| Zoom out | Ctrl + ↓ ||
| Move further to the left | Ctrl + ← ||
| Move further to the right | Ctrl + → ||
| Toggle maximize pane | Double-click the pane ||
| Toggle collapse pane | Ctrl + Double-click the pane ||
| Go to date | Alt + G ||
| Take snapshot, saving URL to clipboard | Alt + S ||
| Reset chart | Alt + R ||
| Invert series scale | Alt + I ||
| Enable/disable logarithmic series scale | Alt + L ||
| Enable/disable percent series scale | Alt + P ||
| Zoom in focused area | Ctrl + Mouse wheel ||
| Start keyboard navigation | Alt + Z 
 Tab if [`accessible_keyboard_shortcuts`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#accessible_keyboard_shortcuts) is enabled ||

### Indicators and drawings
You can use the following shortcuts to interact with [indicators](https://www.tradingview.com/charting-library-docs/latest/ui_elements/indicators/) and [drawings](https://www.tradingview.com/charting-library-docs/latest/ui_elements/drawings/).

 **|Action** | **Shortcut** ||
| Partially erase drawing | *Eraser* + Ctrl ||
| Enable Gann box fixed increments | Hold Shift ||
| Enable measure tool | Hold Shift + Click ||
| Copy selected object | Ctrl + C ||
| Paste object | Ctrl + V ||
| Temporary turn on/off magnet mode | Ctrl  + Move a point ||
| Hide all drawings | Ctrl  + Alt + H ||
| Clone a drawing | Ctrl  + Drag ||
| Select multiple drawings | Hold Ctrl  + Click ||
| Move a drawing horizontally or vertically | Drag + Shift ||
| Move selected drawing left | ← ||
| Move selected drawing right | → ||
| Move selected drawing up | ↑ ||
| Move selected drawing down | ↓ ||
| Draw *Trend line* | Alt + T ||
| Draw *Horizontal line* | Alt + H ||
| Draw *Vertical line* | Alt + V ||
| Draw *Cross line* | Alt + C ||
| Draw *Fib retracement* | Alt + F ||
| Draw *Rectangle* | Alt + Shift + R ||
| Draw *Square* | *Rectangle* + Shift ||
| Draw *Circle* | *Ellipse* + Shift ||
| Draw 45 degrees angle or horizontal | *Trend line* or *Channel* + Shift ||

## Trading Platform shortcuts
The shorcuts below are available in [Trading Platform](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/) only.

### Chart
You can use the following shortcuts to interact with the [chart](https://www.tradingview.com/charting-library-docs/latest/ui_elements/Chart).

 **|Action** | **Shortcut** ||
| Switch between charts | Tab 
 Shift + → if [`accessible_keyboard_shortcuts`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#accessible_keyboard_shortcuts) is enabled ||
| Switch between charts in reverse order | Shift + Tab 
 Shift + ← if [`accessible_keyboard_shortcuts`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#accessible_keyboard_shortcuts) is enabled ||
| Toggle maximize chart | Alt + Enter or Alt + Click ||
| Add symbol to watchlist | Alt + W ||

### Watchlist
You can use the following shortcuts to interact with [watchlist](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/Watch-List).

 **|Action** | **Shortcut** ||
| Switch to next symbol | ↓ or Space ||
| Switch to previous symbol | ↑ or Shift + Space ||
| Select all symbols | Ctrl + A ||
| Select next symbol | Shift + ↓ ||
| Select previous symbol | Shift + ↑ ||

### Trading
You can use the following shortcuts to trade.

 **|Action** | **Shortcut** ||
| Place market order to buy | Shift + B ||
| Place market order to sell | Shift + S ||
| Place limit order | Click the [Depth of Market](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/depth-of-market) (DOM) cell ||
| Place limit order to buy | Shift + Alt + B ||
| Place limit order to sell | Shift + Alt + S ||
| Place stop order | Ctrl  + Click the [DOM](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/depth-of-market) cell ||
| Center [DOM](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/depth-of-market) data | Shift + Alt + C ||

## Manage shortcuts
### Override shortcuts
The [`onShortcut`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#onshortcut) method allows you to override the built‑in shortcuts or specify custom ones. To do this, pass a keyboard shortcut and a callback function as parameters. The `shortCut` parameter depends on the key types:

If a shortcut consists of a modifier and alphabet keys, you should pass a string and use `+` as a separator.

```
widget.onShortcut("alt+q", function() {
  widget.chart().executeActionById("symbolSearch");
});

```

If a shortcut consists of a non-alphabet key, you should pass the key code. You can refer to the [keycode.info](https://keycode.info) page to find out a key code.

```
// F1
widget.onShortcut(112, function() {
  widget.chart().executeActionById("symbolSearch");
});

```

If a shortcut consists of modifier and non-alphabet keys, you should pass an array that contains strings and key codes.

```
// Ctrl+Shift+\
widget.onShortcut(['ctrl', 'shift', 220], function() {
    widget.chart().executeActionById("symbolSearch");
});

```

### Disable shortcuts
The shortcuts listed below can be disabled using the corresponding [featureset](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets):

- *Open indicators* using [`insert_indicator_dialog_shortcut`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#insert_indicator_dialog_shortcut)
- *Save chart layout* using [`save_shortcut`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#save_shortcut)