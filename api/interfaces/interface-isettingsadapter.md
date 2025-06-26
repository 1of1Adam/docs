---
title: "Interface: ISettingsAdapter | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ISettingsAdapter"
extracted_at: "2025-06-22T09:39:38.463Z"
---

- [](/charting-library-docs/)- Interfaces- ISettingsAdapterOn this page# Interface: ISettingsAdapter[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).ISettingsAdapter

Properties of the [ChartingLibraryWidgetOptions.settings_adapter](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ChartingLibraryWidgetOptions#settings_adapter) property that allows saving [user settings](https://www.tradingview.com/charting-library-docs/latest/saving_loading/user-settings) to your preferred storage, including server-side.

## Properties[​](#properties)
### initialSettings[​](#initialsettings)
• `Optional` initialSettings: [`InitialSettingsMap`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.InitialSettingsMap)

Initial settings the chart should be initiated with.

## Methods[​](#methods)
### removeValue[​](#removevalue)
▸ removeValue(`key`): `void`

Remove a value for a setting.

#### Parameters[​](#parameters)
NameType`key``string`
#### Returns[​](#returns)
`void`

### setValue[​](#setvalue)
▸ setValue(`key`, `value`): `void`

Set a value for a setting.

#### Parameters[​](#parameters-1)
NameType`key``string``value``string`
#### Returns[​](#returns-1)
`void`

- [Properties](#properties)[initialSettings](#initialsettings)- [Methods](#methods)[removeValue](#removevalue)- [setValue](#setvalue)