---
title: "Interface: CustomComboBoxMetaInfo | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomComboBoxMetaInfo"
extracted_at: "2025-06-22T09:53:47.186Z"
---

- [](/charting-library-docs/)- Interfaces- CustomComboBoxMetaInfoOn this page# Interface: CustomComboBoxMetaInfo[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).CustomComboBoxMetaInfo

## Hierarchy[​](#hierarchy)

[`CustomInputFieldMetaInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldMetaInfo)

↳ `CustomComboBoxMetaInfo`

## Properties[​](#properties)
### customInfo[​](#custominfo)
• `Optional` customInfo: `any`

Additional custom information

#### Inherited from[​](#inherited-from)
[CustomInputFieldMetaInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldMetaInfo).[customInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldMetaInfo#custominfo)

### id[​](#id)
• id: `string`

Input field ID

#### Inherited from[​](#inherited-from-1)
[CustomInputFieldMetaInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldMetaInfo).[id](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldMetaInfo#id)

### inputType[​](#inputtype)
• inputType: `"ComboBox"`

Type of the input field

#### Overrides[​](#overrides)
[CustomInputFieldMetaInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldMetaInfo).[inputType](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldMetaInfo#inputtype)

### items[​](#items)
• items: [`CustomComboBoxItem`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomComboBoxItem)[]

Items for the combo box input field

### placeHolder[​](#placeholder)
• `Optional` placeHolder: `string`

Placeholder string for the field

#### Inherited from[​](#inherited-from-2)
[CustomInputFieldMetaInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldMetaInfo).[placeHolder](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldMetaInfo#placeholder)

### preventModify[​](#preventmodify)
• `Optional` preventModify: `boolean`

Prevent modification

#### Inherited from[​](#inherited-from-3)
[CustomInputFieldMetaInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldMetaInfo).[preventModify](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldMetaInfo#preventmodify)

### saveToSettings[​](#savetosettings)
• `Optional` saveToSettings: `boolean`

Should the input field value be saved to settings

#### Inherited from[​](#inherited-from-4)
[CustomInputFieldMetaInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldMetaInfo).[saveToSettings](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldMetaInfo#savetosettings)

### title[​](#title)
• title: `string`

Title for the input field

#### Inherited from[​](#inherited-from-5)
[CustomInputFieldMetaInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldMetaInfo).[title](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldMetaInfo#title)

### validator[​](#validator)
• `Optional` validator: [`InputFieldValidator`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#inputfieldvalidator)

Validator function for the field

#### Inherited from[​](#inherited-from-6)
[CustomInputFieldMetaInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldMetaInfo).[validator](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldMetaInfo#validator)

### value[​](#value)
• `Optional` value: `any`

Value of the field

#### Inherited from[​](#inherited-from-7)
[CustomInputFieldMetaInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldMetaInfo).[value](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldMetaInfo#value)

- [Hierarchy](#hierarchy)- [Properties](#properties)[customInfo](#custominfo)- [id](#id)- [inputType](#inputtype)- [items](#items)- [placeHolder](#placeholder)- [preventModify](#preventmodify)- [saveToSettings](#savetosettings)- [title](#title)- [validator](#validator)- [value](#value)