---
title: "Interface: CustomInputFieldMetaInfo | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomInputFieldMetaInfo"
extracted_at: "2025-06-22T09:53:56.138Z"
---

- [](/charting-library-docs/)- Interfaces- CustomInputFieldMetaInfoOn this page# Interface: CustomInputFieldMetaInfo[Broker](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker).CustomInputFieldMetaInfo

## Hierarchy[​](#hierarchy)

[`CustomFieldMetaInfoBase`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomFieldMetaInfoBase)

↳ `CustomInputFieldMetaInfo`

↳↳ [`CustomComboBoxMetaInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomComboBoxMetaInfo)

↳↳ [`TextFieldMetaInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.TextFieldMetaInfo)

↳↳ [`TextWithCheckboxFieldMetaInfo`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.TextWithCheckboxFieldMetaInfo)

## Properties[​](#properties)
### customInfo[​](#custominfo)
• `Optional` customInfo: `any`

Additional custom information

### id[​](#id)
• id: `string`

Input field ID

#### Inherited from[​](#inherited-from)
[CustomFieldMetaInfoBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomFieldMetaInfoBase).[id](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomFieldMetaInfoBase#id)

### inputType[​](#inputtype)
• inputType: `string`

Type of the input field

#### Inherited from[​](#inherited-from-1)
[CustomFieldMetaInfoBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomFieldMetaInfoBase).[inputType](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomFieldMetaInfoBase#inputtype)

### placeHolder[​](#placeholder)
• `Optional` placeHolder: `string`

Placeholder string for the field

### preventModify[​](#preventmodify)
• `Optional` preventModify: `boolean`

Prevent modification

### saveToSettings[​](#savetosettings)
• `Optional` saveToSettings: `boolean`

Should the input field value be saved to settings

#### Inherited from[​](#inherited-from-2)
[CustomFieldMetaInfoBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomFieldMetaInfoBase).[saveToSettings](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomFieldMetaInfoBase#savetosettings)

### title[​](#title)
• title: `string`

Title for the input field

#### Inherited from[​](#inherited-from-3)
[CustomFieldMetaInfoBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomFieldMetaInfoBase).[title](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomFieldMetaInfoBase#title)

### validator[​](#validator)
• `Optional` validator: [`InputFieldValidator`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Broker#inputfieldvalidator)

Validator function for the field

### value[​](#value)
• `Optional` value: `any`

Value of the field

#### Inherited from[​](#inherited-from-4)
[CustomFieldMetaInfoBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomFieldMetaInfoBase).[value](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Broker.CustomFieldMetaInfoBase#value)

- [Hierarchy](#hierarchy)- [Properties](#properties)[customInfo](#custominfo)- [id](#id)- [inputType](#inputtype)- [placeHolder](#placeholder)- [preventModify](#preventmodify)- [saveToSettings](#savetosettings)- [title](#title)- [validator](#validator)- [value](#value)