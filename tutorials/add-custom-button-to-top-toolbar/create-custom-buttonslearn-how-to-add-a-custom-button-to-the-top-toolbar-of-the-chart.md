---
title: "How to add custom button to top toolbar | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/tutorials/add-custom-button-to-top-toolbar/"
extracted_at: "2025-06-22T09:29:32.896Z"
---

# How to add custom button to top toolbarThis guide shows how to add buttons to the [top toolbar](https://www.tradingview.com/charting-library-docs/latest/ui_elements/#top-toolbar) using the following methods:

- `createDropdown` — creates a [dropdown menu](#add-a-dropdown-button).
- `createButton` — creates a [customizable button](#add-a-custom-button).

See the Pen 
[WIP] Add custom button to top toolbar by TradingView ([@tradingview](https://codepen.io/tradingview))
on [CodePen](https://codepen.io).
## Before you start
Consider taking the following steps before proceeding with the guide:

- Set up the Widget Constructor and run the library. Refer to the [First run](https://www.tradingview.com/charting-library-docs/latest/tutorials/First-Run-Tutorial) tutorial for more information.
- Connect data to the library. Refer to the [Connecting data](https://www.tradingview.com/charting-library-docs/latest/tutorials/implement_datafeed_tutorial/) tutorial for more information.

## Add a dropdown button

Call the widget's [`headerReady`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#headerready) method that ensures the toolbar is fully loaded before adding custom elements.
The method returns a promise that will be resolved once the chart’s top toolbar is available for customization.
```
widget.headerReady().then(function () {});

```

Use the widget's [`createDropdown`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#createdropdown) method to add a dropdown button to the top toolbar.
This button will [set a symbol](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartWidgetApi#setsymbol) with a specific resolution to the chart.
```
widget.headerReady().then(function () {
    var dropdown = widget.createDropdown({
    title: "Select symbol",
    tooltip: "Select one of the symbols to load the chart with",
    items: [
        {
            title: "MSFT (1M)",
            onSelect: () => {
                widget.setSymbol("MSFT", "1M");
            }
        },
        {
            title: "IBM (1D)",
            onSelect: () => {
                widget.setSymbol("IBM", "1D");
            }
        }
    ]
    });
});

```

## Add a custom button

Call the widget's [`headerReady`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#headerready) method that ensures the toolbar is fully loaded before adding custom elements.
The method returns a promise that will be resolved once the chart’s top toolbar is available for customization.
```
widget.headerReady().then(function () {});

```

Use the widget's [`createButton`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#createbutton) method to add a button that triggers a confirmation dialog when clicked.
The widget's [`showConfirmDialog`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#showconfirmdialog) method displays a dialog box with a title, body text, and two buttons: *Yes* and *No*.
```
widget.headerReady().then(function () {
    var button = widget.createButton();
    button.textContent = "Show dialog";
    button.addEventListener("click", function () {
        widget.showConfirmDialog({
            title: "Accept Terms and Conditions",
            body: "By selecting Yes, you agree to the terms of use. Otherwise, select No to cancel.",
            callback(result) {
                result ? console.log("The terms are accepted.") : console.log("The terms are not accepted.");
            }
        });
    });
});

```

**(Optional)** If you're a [Trading Platform](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/) user, you can alternatively use the [`showConfirmDialog`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost#showconfirmdialog) method within the [`IBrokerConnectionAdapterHost`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IBrokerConnectionAdapterHost) interface.

Use the widget's [`createButton`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#createbutton) method to add a button that triggers a confirmation dialog when clicked.

```
widget.headerReady().then(function () {
    var buttonTwo = widget.createButton(); // Create a button
    buttonTwo.textContent = "Show dialog 2"; // Add the button title
    buttonTwo.addEventListener("click", function () {
        window.broker.showDialog(); // Trigger a custom dialog on click
    });
});

```

Define the `showDialog` method in the constructor of your [Broker API](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/trading-concepts/#broker-api) class.

```
async showDialog() {
    const actionConfirmed = await this.host.showConfirmDialog(
        "Confirm action", // Dialog title
        [
        "This action cannot be undone. Please confirm to continue.",
        "Otherwise, you may close this dialog to retain the current settings."
        ], // Dialog content
        "Confirm", // Text for the button that returns true
        "Dismiss"  // Text for the button that returns false
    );
    if (actionConfirmed) {
        console.log("Action was confirmed.");
    } else {
        console.log("Action was not confirmed.");
    }
}

```

## What's next?
If you want to dive deeper into how to customize the chart, we recommend checking the following documentation articles:

- [Customization overview](https://www.tradingview.com/charting-library-docs/latest/customization/)
- [UI elements overview](https://www.tradingview.com/charting-library-docs/latest/ui_elements/)