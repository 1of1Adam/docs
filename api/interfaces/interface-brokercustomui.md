---
title: "Interface: BrokerCustomUI | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.BrokerCustomUI"
extracted_at: "2025-06-22T09:53:28.271Z"
---

- [](/charting-library-docs/)- Interfaces- BrokerCustomUIOn this page# Interface: BrokerCustomUI[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).BrokerCustomUI

## Properties[​](#properties)
### showCancelOrderDialog[​](#showcancelorderdialog)
• `Optional` showCancelOrderDialog: (`order`: [`Order`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#order)) => `Promise`<`boolean`>

Shows a confirmation dialog and executes handler if YES/OK is pressed.

#### Type declaration[​](#type-declaration)
▸ (`order`): `Promise`<`boolean`>

Parameters[​](#parameters)
NameTypeDescription`order`[`Order`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#order)order to be cancelled
Returns[​](#returns)
`Promise`<`boolean`>

### showClosePositionDialog[​](#showclosepositiondialog)
• `Optional` showClosePositionDialog: (`position`: [`Position`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.Position) | [`IndividualPosition`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IndividualPosition)) => `Promise`<`boolean`>

Shows the Close Position Dialog.

#### Type declaration[​](#type-declaration-1)
▸ (`position`): `Promise`<`boolean`>

Parameters[​](#parameters-1)
NameTypeDescription`position`[`Position`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.Position) | [`IndividualPosition`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IndividualPosition)position to be closed
Returns[​](#returns-1)
`Promise`<`boolean`>

### showOrderDialog[​](#showorderdialog)
• `Optional` showOrderDialog: (`order`: [`OrderTemplate`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderTemplate) | [`Order`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#order), `focus?`: [`OrderTicketFocusControl`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.OrderTicketFocusControl)) => `Promise`<`boolean`>

Shows Order Ticket to create or modify an order and executes handler if Buy/Sell/Modify is pressed.

#### Type declaration[​](#type-declaration-2)
▸ (`order`, `focus?`): `Promise`<`boolean`>

Parameters[​](#parameters-2)
NameTypeDescription`order`[`OrderTemplate`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.OrderTemplate) | [`Order`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#order)order to be placed or modified`focus?`[`OrderTicketFocusControl`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.OrderTicketFocusControl)Control to focus on when dialog is opened
Returns[​](#returns-2)
`Promise`<`boolean`>

### showPositionDialog[​](#showpositiondialog)
• `Optional` showPositionDialog: (`position`: [`Position`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.Position) | [`IndividualPosition`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IndividualPosition), `brackets`: [`Brackets`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.Brackets), `focus?`: [`OrderTicketFocusControl`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.OrderTicketFocusControl)) => `Promise`<`boolean`>

Shows the Position Dialog

#### Type declaration[​](#type-declaration-3)
▸ (`position`, `brackets`, `focus?`): `Promise`<`boolean`>

Parameters[​](#parameters-3)
NameTypeDescription`position`[`Position`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.Position) | [`IndividualPosition`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.IndividualPosition)position to be placed or modified`brackets`[`Brackets`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.Brackets)brackets for the position`focus?`[`OrderTicketFocusControl`](https://www.tradingview.com/charting-library-docs/latest/api/enums/Broker.OrderTicketFocusControl)Control to focus on when dialog is opened
Returns[​](#returns-3)
`Promise`<`boolean`>

- [Properties](#properties)[showCancelOrderDialog](#showcancelorderdialog)- [showClosePositionDialog](#showclosepositiondialog)- [showOrderDialog](#showorderdialog)- [showPositionDialog](#showpositiondialog)