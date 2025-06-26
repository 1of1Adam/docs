---
title: "Interface: IPositionLineAdapter | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IPositionLineAdapter"
extracted_at: "2025-06-22T09:39:25.165Z"
---

- [](/charting-library-docs/)- Interfaces- IPositionLineAdapterOn this page# Interface: IPositionLineAdapter[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).IPositionLineAdapter

An API object used to control position lines.

## Methods[​](#methods)
### getBodyBackgroundColor[​](#getbodybackgroundcolor)
▸ getBodyBackgroundColor(): `string`

Get the body font of the position line.

#### Returns[​](#returns)
`string`

### getBodyBorderColor[​](#getbodybordercolor)
▸ getBodyBorderColor(): `string`

Get the body border color of the position line.

#### Returns[​](#returns-1)
`string`

### getBodyFont[​](#getbodyfont)
▸ getBodyFont(): `string`

Get the body font of the position line.

#### Returns[​](#returns-2)
`string`

### getBodyTextColor[​](#getbodytextcolor)
▸ getBodyTextColor(): `string`

Get the body text color of the position line.

#### Returns[​](#returns-3)
`string`

### getCloseButtonBackgroundColor[​](#getclosebuttonbackgroundcolor)
▸ getCloseButtonBackgroundColor(): `string`

Get the close button background color of the position line.

#### Returns[​](#returns-4)
`string`

### getCloseButtonBorderColor[​](#getclosebuttonbordercolor)
▸ getCloseButtonBorderColor(): `string`

Get the close button border color of the position line.

#### Returns[​](#returns-5)
`string`

### getCloseButtonIconColor[​](#getclosebuttoniconcolor)
▸ getCloseButtonIconColor(): `string`

Get the close button icon color of the position line.

#### Returns[​](#returns-6)
`string`

### getCloseTooltip[​](#getclosetooltip)
▸ getCloseTooltip(): `string`

Get the close tooltip of the position line.

#### Returns[​](#returns-7)
`string`

### getExtendLeft[​](#getextendleft)
▸ getExtendLeft(): `boolean`

Get the extend left flag value of the position line.

#### Returns[​](#returns-8)
`boolean`

### getLineColor[​](#getlinecolor)
▸ getLineColor(): `string`

Get the line color of the position line.

#### Returns[​](#returns-9)
`string`

### getLineLength[​](#getlinelength)
▸ getLineLength(): `number`

Get the line length of the position line.

#### Returns[​](#returns-10)
`number`

### getLineLengthUnit[​](#getlinelengthunit)
▸ getLineLengthUnit(): [`PositionLineLengthUnit`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#positionlinelengthunit)

Get the unit of length specified for the line length of the position line.

#### Returns[​](#returns-11)
[`PositionLineLengthUnit`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#positionlinelengthunit)

### getLineStyle[​](#getlinestyle)
▸ getLineStyle(): `number`

Get the line style of the position line.

#### Returns[​](#returns-12)
`number`

### getLineWidth[​](#getlinewidth)
▸ getLineWidth(): `number`

Get the line width of the position line.

#### Returns[​](#returns-13)
`number`

### getPrice[​](#getprice)
▸ getPrice(): `number`

Get the price of the position line.

#### Returns[​](#returns-14)
`number`

### getProtectTooltip[​](#getprotecttooltip)
▸ getProtectTooltip(): `string`

Get the protect tooltip of the position line.

#### Returns[​](#returns-15)
`string`

### getQuantity[​](#getquantity)
▸ getQuantity(): `string`

Get the quantity of the position line.

#### Returns[​](#returns-16)
`string`

### getQuantityBackgroundColor[​](#getquantitybackgroundcolor)
▸ getQuantityBackgroundColor(): `string`

Get the quantity background color of the position line.

#### Returns[​](#returns-17)
`string`

### getQuantityBorderColor[​](#getquantitybordercolor)
▸ getQuantityBorderColor(): `string`

Get the quantity border color of the position line.

#### Returns[​](#returns-18)
`string`

### getQuantityFont[​](#getquantityfont)
▸ getQuantityFont(): `string`

Get the quantity font of the position line.

#### Returns[​](#returns-19)
`string`

### getQuantityTextColor[​](#getquantitytextcolor)
▸ getQuantityTextColor(): `string`

Get the quantity text color of the position line.

#### Returns[​](#returns-20)
`string`

### getReverseButtonBackgroundColor[​](#getreversebuttonbackgroundcolor)
▸ getReverseButtonBackgroundColor(): `string`

Get the reverse button background color of the position line.

#### Returns[​](#returns-21)
`string`

### getReverseButtonBorderColor[​](#getreversebuttonbordercolor)
▸ getReverseButtonBorderColor(): `string`

Get the reverse button border color of the position line.

#### Returns[​](#returns-22)
`string`

### getReverseButtonIconColor[​](#getreversebuttoniconcolor)
▸ getReverseButtonIconColor(): `string`

Get the reverse button icon color of the position line.

#### Returns[​](#returns-23)
`string`

### getReverseTooltip[​](#getreversetooltip)
▸ getReverseTooltip(): `string`

Get the reverse tooltip of the position line.

#### Returns[​](#returns-24)
`string`

### getText[​](#gettext)
▸ getText(): `string`

Get the text of the position line.

#### Returns[​](#returns-25)
`string`

### getTooltip[​](#gettooltip)
▸ getTooltip(): `string`

Get the tooltip of the position line.

#### Returns[​](#returns-26)
`string`

### onClose[​](#onclose)
▸ onClose(`callback`): `this`

Attach a callback to be executed when the position line is closed.

#### Parameters[​](#parameters)
NameTypeDescription`callback`() => `void`Callback to be executed when the position line is closed.
#### Returns[​](#returns-27)
`this`

▸ onClose<`T`>(`data`, `callback`): `this`

Attach a callback to be executed when the position line is closed.

#### Type parameters[​](#type-parameters)
Name`T`
#### Parameters[​](#parameters-1)
NameTypeDescription`data``T`Data to be passed to the callback.`callback`(`data`: `T`) => `void`Callback to be executed when the position line is closed.
#### Returns[​](#returns-28)
`this`

### onModify[​](#onmodify)
▸ onModify(`callback`): `this`

Attach a callback to be executed when the position line is modified.

#### Parameters[​](#parameters-2)
NameTypeDescription`callback`() => `void`Callback to be executed when the position line is modified.
#### Returns[​](#returns-29)
`this`

▸ onModify<`T`>(`data`, `callback`): `this`

Attach a callback to be executed when the position line is modified.

#### Type parameters[​](#type-parameters-1)
Name`T`
#### Parameters[​](#parameters-3)
NameTypeDescription`data``T`Data to be passed to the callback.`callback`(`data`: `T`) => `void`Callback to be executed when the position line is modified.
#### Returns[​](#returns-30)
`this`

### onReverse[​](#onreverse)
▸ onReverse(`callback`): `this`

Attach a callback to be executed when the position line is reversed.

#### Parameters[​](#parameters-4)
NameTypeDescription`callback`() => `void`Callback to be executed when the position line is reversed.
#### Returns[​](#returns-31)
`this`

▸ onReverse<`T`>(`data`, `callback`): `this`

Attach a callback to be executed when the position line is reversed.

#### Type parameters[​](#type-parameters-2)
Name`T`
#### Parameters[​](#parameters-5)
NameTypeDescription`data``T`Data to be passed to the callback.`callback`(`data`: `T`) => `void`Callback to be executed when the position line is reversed.
#### Returns[​](#returns-32)
`this`

### remove[​](#remove)
▸ remove(): `void`

Remove the position line. This API object cannot be used after this call.

#### Returns[​](#returns-33)
`void`

### setBodyBackgroundColor[​](#setbodybackgroundcolor)
▸ setBodyBackgroundColor(`value`): `this`

Set the body font of the position line.

#### Parameters[​](#parameters-6)
NameTypeDescription`value``string`The new body font.
#### Returns[​](#returns-34)
`this`

### setBodyBorderColor[​](#setbodybordercolor)
▸ setBodyBorderColor(`value`): `this`

Set the body border color of the position line.

#### Parameters[​](#parameters-7)
NameTypeDescription`value``string`The new body border color.
#### Returns[​](#returns-35)
`this`

### setBodyFont[​](#setbodyfont)
▸ setBodyFont(`value`): `this`

Set the body font of the position line.

Example

```
positionLine.setPrice(170).setBodyFont("bold 12px Verdana")
```
#### Parameters[​](#parameters-8)
NameTypeDescription`value``string`The new body font.
#### Returns[​](#returns-36)
`this`

### setBodyTextColor[​](#setbodytextcolor)
▸ setBodyTextColor(`value`): `this`

Set the body text color of the position line.

#### Parameters[​](#parameters-9)
NameTypeDescription`value``string`The new body text color.
#### Returns[​](#returns-37)
`this`

### setCloseButtonBackgroundColor[​](#setclosebuttonbackgroundcolor)
▸ setCloseButtonBackgroundColor(`value`): `this`

Set the close button background color of the position line.

#### Parameters[​](#parameters-10)
NameTypeDescription`value``string`The new close button background color.
#### Returns[​](#returns-38)
`this`

### setCloseButtonBorderColor[​](#setclosebuttonbordercolor)
▸ setCloseButtonBorderColor(`value`): `this`

Set the close button border color of the position line.

#### Parameters[​](#parameters-11)
NameTypeDescription`value``string`The new close button border color.
#### Returns[​](#returns-39)
`this`

### setCloseButtonIconColor[​](#setclosebuttoniconcolor)
▸ setCloseButtonIconColor(`value`): `this`

Set the close button icon color of the position line.

#### Parameters[​](#parameters-12)
NameTypeDescription`value``string`The new close button icon color.
#### Returns[​](#returns-40)
`this`

### setCloseTooltip[​](#setclosetooltip)
▸ setCloseTooltip(`value`): `this`

Set the close tooltip of the position line.

#### Parameters[​](#parameters-13)
NameTypeDescription`value``string`The new close tooltip.
#### Returns[​](#returns-41)
`this`

### setExtendLeft[​](#setextendleft)
▸ setExtendLeft(`value`): `this`

Set the extend left flag value of the position line.

#### Parameters[​](#parameters-14)
NameTypeDescription`value``boolean`The new extend left flag value.
#### Returns[​](#returns-42)
`this`

### setLineColor[​](#setlinecolor)
▸ setLineColor(`value`): `this`

Set the line color of the position line.

#### Parameters[​](#parameters-15)
NameTypeDescription`value``string`The new line color.
#### Returns[​](#returns-43)
`this`

### setLineLength[​](#setlinelength)
▸ setLineLength(`value`, `unit?`): `this`

Set the line length of the position line.

If negative number is provided for the value and the unit is 'pixel' then
the position will be relative to the left edge of the chart.
#### Parameters[​](#parameters-16)
NameTypeDescription`value``number`The new line length.`unit?`[`PositionLineLengthUnit`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#positionlinelengthunit)unit for the line length, defaults to 'percentage'.
#### Returns[​](#returns-44)
`this`

### setLineStyle[​](#setlinestyle)
▸ setLineStyle(`value`): `this`

Set the line style of the position line.

#### Parameters[​](#parameters-17)
NameTypeDescription`value``number`The new line style.
#### Returns[​](#returns-45)
`this`

### setLineWidth[​](#setlinewidth)
▸ setLineWidth(`value`): `this`

Set the line width of the position line.

#### Parameters[​](#parameters-18)
NameTypeDescription`value``number`The new line width.
#### Returns[​](#returns-46)
`this`

### setPrice[​](#setprice)
▸ setPrice(`value`): `this`

Set the price of the position line.

#### Parameters[​](#parameters-19)
NameTypeDescription`value``number`The new price.
#### Returns[​](#returns-47)
`this`

### setProtectTooltip[​](#setprotecttooltip)
▸ setProtectTooltip(`value`): `this`

Set the protect tooltip of the position line.

#### Parameters[​](#parameters-20)
NameTypeDescription`value``string`The new protect tooltip.
#### Returns[​](#returns-48)
`this`

### setQuantity[​](#setquantity)
▸ setQuantity(`value`): `this`

Set the quantity of the position line.

#### Parameters[​](#parameters-21)
NameTypeDescription`value``string`The new quantity.
#### Returns[​](#returns-49)
`this`

### setQuantityBackgroundColor[​](#setquantitybackgroundcolor)
▸ setQuantityBackgroundColor(`value`): `this`

Set the quantity background color of the position line.

#### Parameters[​](#parameters-22)
NameTypeDescription`value``string`The new quantity background color.
#### Returns[​](#returns-50)
`this`

### setQuantityBorderColor[​](#setquantitybordercolor)
▸ setQuantityBorderColor(`value`): `this`

Set the quantity border color of the position line.

#### Parameters[​](#parameters-23)
NameTypeDescription`value``string`The new quantity border color.
#### Returns[​](#returns-51)
`this`

### setQuantityFont[​](#setquantityfont)
▸ setQuantityFont(`value`): `this`

Set the quantity font of the position line.

Example

```
positionLine.setPrice(170).setQuantityFont("bold 12px Verdana")
```
#### Parameters[​](#parameters-24)
NameTypeDescription`value``string`The new quantity font.
#### Returns[​](#returns-52)
`this`

### setQuantityTextColor[​](#setquantitytextcolor)
▸ setQuantityTextColor(`value`): `this`

Set the quantity text color of the position line.

#### Parameters[​](#parameters-25)
NameTypeDescription`value``string`The new quantity text color.
#### Returns[​](#returns-53)
`this`

### setReverseButtonBackgroundColor[​](#setreversebuttonbackgroundcolor)
▸ setReverseButtonBackgroundColor(`value`): `this`

Set the reverse button background color of the position line.

#### Parameters[​](#parameters-26)
NameTypeDescription`value``string`The new reverse button background color.
#### Returns[​](#returns-54)
`this`

### setReverseButtonBorderColor[​](#setreversebuttonbordercolor)
▸ setReverseButtonBorderColor(`value`): `this`

Set the reverse button border color of the position line.

#### Parameters[​](#parameters-27)
NameTypeDescription`value``string`The new reverse button border color.
#### Returns[​](#returns-55)
`this`

### setReverseButtonIconColor[​](#setreversebuttoniconcolor)
▸ setReverseButtonIconColor(`value`): `this`

Set the reverse button icon color of the position line.

#### Parameters[​](#parameters-28)
NameTypeDescription`value``string`The new reverse button icon color.
#### Returns[​](#returns-56)
`this`

### setReverseTooltip[​](#setreversetooltip)
▸ setReverseTooltip(`value`): `this`

Set the reverse tooltip of the position line.

#### Parameters[​](#parameters-29)
NameTypeDescription`value``string`The new reverse tooltip.
#### Returns[​](#returns-57)
`this`

### setText[​](#settext)
▸ setText(`value`): `this`

Set the text of the position line.

#### Parameters[​](#parameters-30)
NameTypeDescription`value``string`The new text.
#### Returns[​](#returns-58)
`this`

### setTooltip[​](#settooltip)
▸ setTooltip(`value`): `this`

Set the tooltip of the position line.

#### Parameters[​](#parameters-31)
NameTypeDescription`value``string`The new tooltip.
#### Returns[​](#returns-59)
`this`

- [Methods](#methods)[getBodyBackgroundColor](#getbodybackgroundcolor)- [getBodyBorderColor](#getbodybordercolor)- [getBodyFont](#getbodyfont)- [getBodyTextColor](#getbodytextcolor)- [getCloseButtonBackgroundColor](#getclosebuttonbackgroundcolor)- [getCloseButtonBorderColor](#getclosebuttonbordercolor)- [getCloseButtonIconColor](#getclosebuttoniconcolor)- [getCloseTooltip](#getclosetooltip)- [getExtendLeft](#getextendleft)- [getLineColor](#getlinecolor)- [getLineLength](#getlinelength)- [getLineLengthUnit](#getlinelengthunit)- [getLineStyle](#getlinestyle)- [getLineWidth](#getlinewidth)- [getPrice](#getprice)- [getProtectTooltip](#getprotecttooltip)- [getQuantity](#getquantity)- [getQuantityBackgroundColor](#getquantitybackgroundcolor)- [getQuantityBorderColor](#getquantitybordercolor)- [getQuantityFont](#getquantityfont)- [getQuantityTextColor](#getquantitytextcolor)- [getReverseButtonBackgroundColor](#getreversebuttonbackgroundcolor)- [getReverseButtonBorderColor](#getreversebuttonbordercolor)- [getReverseButtonIconColor](#getreversebuttoniconcolor)- [getReverseTooltip](#getreversetooltip)- [getText](#gettext)- [getTooltip](#gettooltip)- [onClose](#onclose)- [onModify](#onmodify)- [onReverse](#onreverse)- [remove](#remove)- [setBodyBackgroundColor](#setbodybackgroundcolor)- [setBodyBorderColor](#setbodybordercolor)- [setBodyFont](#setbodyfont)- [setBodyTextColor](#setbodytextcolor)- [setCloseButtonBackgroundColor](#setclosebuttonbackgroundcolor)- [setCloseButtonBorderColor](#setclosebuttonbordercolor)- [setCloseButtonIconColor](#setclosebuttoniconcolor)- [setCloseTooltip](#setclosetooltip)- [setExtendLeft](#setextendleft)- [setLineColor](#setlinecolor)- [setLineLength](#setlinelength)- [setLineStyle](#setlinestyle)- [setLineWidth](#setlinewidth)- [setPrice](#setprice)- [setProtectTooltip](#setprotecttooltip)- [setQuantity](#setquantity)- [setQuantityBackgroundColor](#setquantitybackgroundcolor)- [setQuantityBorderColor](#setquantitybordercolor)- [setQuantityFont](#setquantityfont)- [setQuantityTextColor](#setquantitytextcolor)- [setReverseButtonBackgroundColor](#setreversebuttonbackgroundcolor)- [setReverseButtonBorderColor](#setreversebuttonbordercolor)- [setReverseButtonIconColor](#setreversebuttoniconcolor)- [setReverseTooltip](#setreversetooltip)- [setText](#settext)- [setTooltip](#settooltip)