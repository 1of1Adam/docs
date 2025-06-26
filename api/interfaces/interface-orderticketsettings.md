---
title: "Interface: OrderTicketSettings | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderTicketSettings"
extracted_at: "2025-06-22T09:55:48.040Z"
---

- [](/charting-library-docs/)- Interfaces- OrderTicketSettingsOn this page# Interface: OrderTicketSettings[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).OrderTicketSettings

Settings for the ellipsis menu of the [Order Ticket](https://www.tradingview.com/charting-library-docs/latest/trading_terminal/order-ticket). You can read and adjust these settings using the
[IBrokerConnectionAdapterHost.getOrderTicketSetting](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerConnectionAdapterHost#getorderticketsetting) and
[IBrokerConnectionAdapterHost.setOrderTicketSetting](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IBrokerConnectionAdapterHost#setorderticketsetting) methods.
## Properties[​](#properties)
### showBracketsInCurrency[​](#showbracketsincurrency)
• showBracketsInCurrency: `boolean`

If true, the "Show TP/SL inputs in Money" setting is displayed.

### showBracketsInPercent[​](#showbracketsinpercent)
• showBracketsInPercent: `boolean`

If true, the "Show TP/SL inputs in %" setting is displayed.

### showCryptoBracketsInCurrency[​](#showcryptobracketsincurrency)
• `Optional` showCryptoBracketsInCurrency: `boolean`

If true, the "Money" field is displayed in the Order Ticket for crypto brackets.

### showCryptoBracketsInPercent[​](#showcryptobracketsinpercent)
• `Optional` showCryptoBracketsInPercent: `boolean`

If true, the "%" field is displayed in the Order Ticket for crypto brackets.

### showCurrencyRiskInQty[​](#showcurrencyriskinqty)
• showCurrencyRiskInQty: `boolean`

If true, the "Show Quantity in Money Risk" setting is displayed.

### showOrderPreview[​](#showorderpreview)
• showOrderPreview: `boolean`

If true, the "Show order confirmations" setting is displayed.

### showPercentRiskInQty[​](#showpercentriskinqty)
• showPercentRiskInQty: `boolean`

If true, the "Show Quantity in % Risk" setting is displayed.

### showRelativePriceControl[​](#showrelativepricecontrol)
• showRelativePriceControl: `boolean`

If true, the "Show Order Price in Ticks" setting is displayed.

- [Properties](#properties)[showBracketsInCurrency](#showbracketsincurrency)- [showBracketsInPercent](#showbracketsinpercent)- [showCryptoBracketsInCurrency](#showcryptobracketsincurrency)- [showCryptoBracketsInPercent](#showcryptobracketsinpercent)- [showCurrencyRiskInQty](#showcurrencyriskinqty)- [showOrderPreview](#showorderpreview)- [showPercentRiskInQty](#showpercentriskinqty)- [showRelativePriceControl](#showrelativepricecontrol)