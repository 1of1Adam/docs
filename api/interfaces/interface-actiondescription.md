---
title: "Interface: ActionDescription | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.ActionDescription"
extracted_at: "2025-06-22T09:53:17.505Z"
---

- [](/charting-library-docs/)- Interfaces- ActionDescriptionOn this page# Interface: ActionDescription[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).ActionDescription

## Hierarchy[​](#hierarchy)

`ActionDescription`

↳ [`ActionDescriptionWithCallback`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.ActionDescriptionWithCallback)

↳ [`MenuSeparator`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.MenuSeparator)

## Properties[​](#properties)
### checkable[​](#checkable)
• `Optional` checkable: `boolean`

Whether menu action represents a checkbox state. Set it to true if you need a checkbox.

### checked[​](#checked)
• `Optional` checked: `boolean`

Value of the checkbox.

### checkedStateSource[​](#checkedstatesource)
• `Optional` checkedStateSource: () => `boolean`

Getter to retrieve the current checkbox value.

#### Type declaration[​](#type-declaration)
▸ (): `boolean`

Returns[​](#returns)
`boolean`

### enabled[​](#enabled)
• `Optional` enabled: `boolean`

Whether the action is enabled. Set to false to disabled the action.

### externalLink[​](#externallink)
• `Optional` externalLink: `boolean`

External link (url) which will be opened upon clicking the menu item.

### icon[​](#icon)
• `Optional` icon: `string`

A string of SVG icon for an action. A string should be a string representation of SVG (not a path/URL).

### separator[​](#separator)
• `Optional` separator: `boolean`

Is a menu separator

### shortcut[​](#shortcut)
• `Optional` shortcut: `string`

Keyboard shortcut for the action. Displayed as hint text.

### text[​](#text)
• `Optional` text: `string`

Displayed text for action

### tooltip[​](#tooltip)
• `Optional` tooltip: `string`

Tooltip text to be displayed when hovering over the action item.

- [Hierarchy](#hierarchy)- [Properties](#properties)[checkable](#checkable)- [checked](#checked)- [checkedStateSource](#checkedstatesource)- [enabled](#enabled)- [externalLink](#externallink)- [icon](#icon)- [separator](#separator)- [shortcut](#shortcut)- [text](#text)- [tooltip](#tooltip)