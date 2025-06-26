---
title: "Snapshots | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/ui_elements/Snapshots"
extracted_at: "2025-06-22T09:14:59.614Z"
---

# SnapshotsThe library allows users to take chart snapshots.
The *Take a snapshot* button is located on the top toolbar.
By clicking the button, users can select one of the available options.
![Take snapshot menu](https://www.tradingview.com/charting-library-docs/assets/images/take-snapshot-90b84d9a7be10beed65838b52be1de34.gif)
If you want snapshots to include orders, positions, and executions, enable the [`snapshot_trading_drawings`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#snapshot_trading_drawings) featureset.

## Snapshot storage
All snapshots are stored on the TradingView servers.
The data storage period is not limited in time.
If you want to save snapshots on your server, use the [`snapshot_url`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#snapshot_url) property of the [Widget Constructor](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Widget-Constructor).
Your server should have an endpoint that accepts POST requests and returns saved image URLs to the library.
## Hide button
Disable the [`header_screenshot`](https://www.tradingview.com/charting-library-docs/latest/customization/Featuresets#header_screenshot) featureset to hide the snapshot button.

## Remove button options
When users click *Take a snapshot*, the menu with several options appears.
If you want to hide some options, use custom CSS defined within the [`custom_css_url`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#custom_css_url) property of the [Widget Constructor](https://www.tradingview.com/charting-library-docs/latest/core_concepts/Widget-Constructor).
The example below shows how to keep only two options in the menu: *Download image* and *Copy image*.
See the Pen 
UI. Remove options from Snapshots menu by TradingView ([@tradingview](https://codepen.io/tradingview))
on [CodePen](https://codepen.io).
## Implement your logic
If you want to implement your logic for taking snapshots, use the [`takeClientScreenshot`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#takeclientscreenshot) method.
This method creates a snapshot of the chart and returns it as a canvas.
You can then take the canvas element and create an image from it.
The code sample below saves a snapshot as a PNG.
```
async function saveChartToPNG() {
  const screenshotCanvas = await widget.takeClientScreenshot();
  const linkElement = document.createElement('a');
  linkElement.download = 'screenshot';
  linkElement.href = screenshotCanvas.toDataURL(); // Alternatively, use `toBlob` which is a better API
  linkElement.dataset.downloadurl = ['image/png', linkElement.download, linkElement.href].join(':');
  document.body.appendChild(linkElement);
  linkElement.click();
  document.body.removeChild(linkElement);
}
saveChartToPNG(); // Call the screenshot function

```
Additionally, you can configure snapshot parameters listed in [`ClientSnapshotOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ClientSnapshotOptions). To do this, specify the desired parameters and pass them to [`takeClientScreenshot`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#takeclientscreenshot).
For example, you can hide indicators from the legend with `hideStudiesFromLegend`:
```
const screenshotCanvas = await widget.takeClientScreenshot({ hideStudiesFromLegend: true });

```