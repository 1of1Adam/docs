---
title: "Interface: MenuSeparator | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.MenuSeparator"
extracted_at: "2025-06-22T09:55:21.502Z"
---

- [](/charting-library-docs/)- Interfaces- MenuSeparatorOn this page# Interface: MenuSeparator[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).MenuSeparator

Separator for a dropdown or context menu

## Hierarchy[​](#hierarchy)

[`ActionDescription`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.ActionDescription)

↳ `MenuSeparator`

## Properties[​](#properties)
### checkable[​](#checkable)
• `Optional` checkable: `boolean`

Whether menu action represents a checkbox state. Set it to true if you need a checkbox.

#### Inherited from[​](#inherited-from)
[ActionDescription](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.ActionDescription).[checkable](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.ActionDescription#checkable)

### checked[​](#checked)
• `Optional` checked: `boolean`

Value of the checkbox.

#### Inherited from[​](#inherited-from-1)
[ActionDescription](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.ActionDescription).[checked](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.ActionDescription#checked)

### checkedStateSource[​](#checkedstatesource)
• `Optional` checkedStateSource: () => `boolean`

Getter to retrieve the current checkbox value.

#### Type declaration[​](#type-declaration)
▸ (): `boolean`

Returns[​](#returns)
`boolean`

#### Inherited from[​](#inherited-from-2)
[ActionDescription](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.ActionDescription).[checkedStateSource](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.ActionDescription#checkedstatesource)

### enabled[​](#enabled)
• `Optional` enabled: `boolean`

Whether the action is enabled. Set to false to disabled the action.

#### Inherited from[​](#inherited-from-3)
[ActionDescription](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.ActionDescription).[enabled](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.ActionDescription#enabled)

### externalLink[​](#externallink)
• `Optional` externalLink: `boolean`

External link (url) which will be opened upon clicking the menu item.

#### Inherited from[​](#inherited-from-4)
[ActionDescription](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.ActionDescription).[externalLink](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.ActionDescription#externallink)

### icon[​](#icon)
• `Optional` icon: `string`

A string of SVG icon for an action. A string should be a string representation of SVG (not a path/URL).

#### Inherited from[​](#inherited-from-5)
[ActionDescription](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.ActionDescription).[icon](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.ActionDescription#icon)

### separator[​](#separator)
• separator: `boolean`

Is a menu separator

#### Overrides[​](#overrides)
[ActionDescription](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.ActionDescription).[separator](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.ActionDescription#separator)

### shortcut[​](#shortcut)
• `Optional` shortcut: `string`

Keyboard shortcut for the action. Displayed as hint text.

#### Inherited from[​](#inherited-from-6)
[ActionDescription](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.ActionDescription).[shortcut](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.ActionDescription#shortcut)

### text[​](#text)
• `Optional` text: `string`

Displayed text for action

#### Inherited from[​](#inherited-from-7)
[ActionDescription](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.ActionDescription).[text](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.ActionDescription#text)

### tooltip[​](#tooltip)
• `Optional` tooltip: `string`

Tooltip text to be displayed when hovering over the action item.

#### Inherited from[​](#inherited-from-8)
[ActionDescription](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.ActionDescription).[tooltip](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.ActionDescription#tooltip)

- [Hierarchy](#hierarchy)- [Properties](#properties)[checkable](#checkable)- [checked](#checked)- [checkedStateSource](#checkedstatesource)- [enabled](#enabled)- [externalLink](#externallink)- [icon](#icon)- [separator](#separator)- [shortcut](#shortcut)- [text](#text)- [tooltip](#tooltip)