---
title: "Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.TextWithCheckboxFieldMetaInfo"
extracted_at: "2025-06-22T09:56:33.903Z"
---

- [](/charting-library-docs/)- Interfaces- TextWithCheckboxFieldMetaInfoOn this page# Interface: TextWithCheckboxFieldMetaInfo[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).TextWithCheckboxFieldMetaInfo

## Hierarchy[​](#hierarchy)

[`CustomInputFieldMetaInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldMetaInfo)

↳ `TextWithCheckboxFieldMetaInfo`

## Properties[​](#properties)
### customInfo[​](#custominfo)
• customInfo: [`TextWithCheckboxFieldCustomInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.TextWithCheckboxFieldCustomInfo)

Additional custom information

#### Overrides[​](#overrides)
[CustomInputFieldMetaInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldMetaInfo).[customInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldMetaInfo#custominfo)

### id[​](#id)
• id: `string`

Input field ID

#### Inherited from[​](#inherited-from)
[CustomInputFieldMetaInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldMetaInfo).[id](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldMetaInfo#id)

### inputType[​](#inputtype)
• inputType: `"TextWithCheckBox"`

Type of the input field

#### Overrides[​](#overrides-1)
[CustomInputFieldMetaInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldMetaInfo).[inputType](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldMetaInfo#inputtype)

### placeHolder[​](#placeholder)
• `Optional` placeHolder: `string`

Placeholder string for the field

#### Inherited from[​](#inherited-from-1)
[CustomInputFieldMetaInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldMetaInfo).[placeHolder](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldMetaInfo#placeholder)

### preventModify[​](#preventmodify)
• `Optional` preventModify: `boolean`

Prevent modification

#### Inherited from[​](#inherited-from-2)
[CustomInputFieldMetaInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldMetaInfo).[preventModify](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldMetaInfo#preventmodify)

### saveToSettings[​](#savetosettings)
• `Optional` saveToSettings: `boolean`

Should the input field value be saved to settings

#### Inherited from[​](#inherited-from-3)
[CustomInputFieldMetaInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldMetaInfo).[saveToSettings](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldMetaInfo#savetosettings)

### title[​](#title)
• title: `string`

Title for the input field

#### Inherited from[​](#inherited-from-4)
[CustomInputFieldMetaInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldMetaInfo).[title](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldMetaInfo#title)

### validator[​](#validator)
• `Optional` validator: [`TextInputFieldValidator`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#textinputfieldvalidator)

Validator function for the field

#### Overrides[​](#overrides-2)
[CustomInputFieldMetaInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldMetaInfo).[validator](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldMetaInfo#validator)

### value[​](#value)
• value: [`TextWithCheckboxValue`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.TextWithCheckboxValue)

Value of the field

#### Overrides[​](#overrides-3)
[CustomInputFieldMetaInfo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldMetaInfo).[value](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldMetaInfo#value)

- [Hierarchy](#hierarchy)- [Properties](#properties)[customInfo](#custominfo)- [id](#id)- [inputType](#inputtype)- [placeHolder](#placeholder)- [preventModify](#preventmodify)- [saveToSettings](#savetosettings)- [title](#title)- [validator](#validator)- [value](#value)