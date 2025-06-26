---
title: "Interface: IOrderLineAdapter | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IOrderLineAdapter"
extracted_at: "2025-06-22T09:39:21.636Z"
---

- [](/charting-library-docs/)- Interfaces- IOrderLineAdapterOn this page# Interface: IOrderLineAdapter[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).IOrderLineAdapter

An API object used to control order lines.

## Methods[​](#methods)
### getBodyBackgroundColor[​](#getbodybackgroundcolor)
▸ getBodyBackgroundColor(): `string`

Get the body background color of the order line.

#### Returns[​](#returns)
`string`

### getBodyBorderColor[​](#getbodybordercolor)
▸ getBodyBorderColor(): `string`

Get the body border color of the order line.

#### Returns[​](#returns-1)
`string`

### getBodyFont[​](#getbodyfont)
▸ getBodyFont(): `string`

Get the body font of the order line.

#### Returns[​](#returns-2)
`string`

### getBodyTextColor[​](#getbodytextcolor)
▸ getBodyTextColor(): `string`

Get the body text color of the order line.

#### Returns[​](#returns-3)
`string`

### getCancelButtonBackgroundColor[​](#getcancelbuttonbackgroundcolor)
▸ getCancelButtonBackgroundColor(): `string`

Get the cancel button background color of the order line.

#### Returns[​](#returns-4)
`string`

### getCancelButtonBorderColor[​](#getcancelbuttonbordercolor)
▸ getCancelButtonBorderColor(): `string`

Get the cancel button border color of the order line.

#### Returns[​](#returns-5)
`string`

### getCancelButtonIconColor[​](#getcancelbuttoniconcolor)
▸ getCancelButtonIconColor(): `string`

Get the cancel button icon color of the order line.

#### Returns[​](#returns-6)
`string`

### getCancelTooltip[​](#getcanceltooltip)
▸ getCancelTooltip(): `string`

Get the cancel tooltip of the order line.

#### Returns[​](#returns-7)
`string`

### getCancellable[​](#getcancellable)
▸ getCancellable(): `boolean`

Get the cancellable flag value of the order line.

#### Returns[​](#returns-8)
`boolean`

### getEditable[​](#geteditable)
▸ getEditable(): `boolean`

Get the editable flag value of the order line.

#### Returns[​](#returns-9)
`boolean`

### getExtendLeft[​](#getextendleft)
▸ getExtendLeft(): `boolean`

Get the extend left flag value of the order line.

#### Returns[​](#returns-10)
`boolean`

### getLineColor[​](#getlinecolor)
▸ getLineColor(): `string`

Get the line color of the order line.

#### Returns[​](#returns-11)
`string`

### getLineLength[​](#getlinelength)
▸ getLineLength(): `number`

Get the line length of the order line.

#### Returns[​](#returns-12)
`number`

### getLineLengthUnit[​](#getlinelengthunit)
▸ getLineLengthUnit(): [`OrderLineLengthUnit`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#orderlinelengthunit)

Get the unit of length specified for the line length of the order line.

#### Returns[​](#returns-13)
[`OrderLineLengthUnit`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#orderlinelengthunit)

### getLineStyle[​](#getlinestyle)
▸ getLineStyle(): `number`

Get the line style of the order line.

#### Returns[​](#returns-14)
`number`

### getLineWidth[​](#getlinewidth)
▸ getLineWidth(): `number`

Get the line width of the order line.

#### Returns[​](#returns-15)
`number`

### getModifyTooltip[​](#getmodifytooltip)
▸ getModifyTooltip(): `string`

Get the modify tooltip of the order line.

#### Returns[​](#returns-16)
`string`

### getPrice[​](#getprice)
▸ getPrice(): `number`

Get the price of the order line.

#### Returns[​](#returns-17)
`number`

### getQuantity[​](#getquantity)
▸ getQuantity(): `string`

Get the quantity of the order line.

#### Returns[​](#returns-18)
`string`

### getQuantityBackgroundColor[​](#getquantitybackgroundcolor)
▸ getQuantityBackgroundColor(): `string`

Get the quantity background color of the order line.

#### Returns[​](#returns-19)
`string`

### getQuantityBorderColor[​](#getquantitybordercolor)
▸ getQuantityBorderColor(): `string`

Get the quantity border color of the order line.

#### Returns[​](#returns-20)
`string`

### getQuantityFont[​](#getquantityfont)
▸ getQuantityFont(): `string`

Get the quantity font of the order line.

#### Returns[​](#returns-21)
`string`

### getQuantityTextColor[​](#getquantitytextcolor)
▸ getQuantityTextColor(): `string`

Get the quantity text color of the order line.

#### Returns[​](#returns-22)
`string`

### getText[​](#gettext)
▸ getText(): `string`

Get the text of the order line.

#### Returns[​](#returns-23)
`string`

### getTooltip[​](#gettooltip)
▸ getTooltip(): `string`

Get the tooltip of the order line.

#### Returns[​](#returns-24)
`string`

### onCancel[​](#oncancel)
▸ onCancel(`callback`): `this`

Attach a callback to be executed when the order line is cancelled.

#### Parameters[​](#parameters)
NameTypeDescription`callback`() => `void`Callback to be executed when the order line is cancelled.
#### Returns[​](#returns-25)
`this`

▸ onCancel<`T`>(`data`, `callback`): `this`

Attach a callback to be executed when the order line is cancelled.

#### Type parameters[​](#type-parameters)
Name`T`
#### Parameters[​](#parameters-1)
NameTypeDescription`data``T`Data to be passed to the callback.`callback`(`data`: `T`) => `void`Callback to be executed when the order line is cancelled.
#### Returns[​](#returns-26)
`this`

### onModify[​](#onmodify)
▸ onModify(`callback`): `this`

Attach a callback to be executed when the order line is modified.

#### Parameters[​](#parameters-2)
NameTypeDescription`callback`() => `void`Callback to be executed when the order line is modified.
#### Returns[​](#returns-27)
`this`

▸ onModify<`T`>(`data`, `callback`): `this`

Attach a callback to be executed when the order line is modified.

#### Type parameters[​](#type-parameters-1)
Name`T`
#### Parameters[​](#parameters-3)
NameTypeDescription`data``T`Data to be passed to the callback.`callback`(`data`: `T`) => `void`Callback to be executed when the order line is modified.
#### Returns[​](#returns-28)
`this`

### onMove[​](#onmove)
▸ onMove(`callback`): `this`

Attach a callback to be executed when the order line is moved.

#### Parameters[​](#parameters-4)
NameTypeDescription`callback`() => `void`Callback to be executed when the order line is moved.
#### Returns[​](#returns-29)
`this`

▸ onMove<`T`>(`data`, `callback`): `this`

Attach a callback to be executed when the order line is moved.

#### Type parameters[​](#type-parameters-2)
Name`T`
#### Parameters[​](#parameters-5)
NameTypeDescription`data``T`Data to be passed to the callback.`callback`(`data`: `T`) => `void`Callback to be executed when the order line is moved.
#### Returns[​](#returns-30)
`this`

### onMoving[​](#onmoving)
▸ onMoving(`callback`): `this`

Attach a callback to be executed while the order line is being moved.

#### Parameters[​](#parameters-6)
NameTypeDescription`callback`() => `void`Callback to be executed while the order line is being moved.
#### Returns[​](#returns-31)
`this`

▸ onMoving<`T`>(`data`, `callback`): `this`

Attach a callback to be executed while the order line is being moved.

#### Type parameters[​](#type-parameters-3)
Name`T`
#### Parameters[​](#parameters-7)
NameTypeDescription`data``T`Data to be passed to the callback.`callback`(`data`: `T`) => `void`Callback to be executed while the order line is being moved.
#### Returns[​](#returns-32)
`this`

### remove[​](#remove)
▸ remove(): `void`

Remove the order line. This API object cannot be used after this call.

#### Returns[​](#returns-33)
`void`

### setBodyBackgroundColor[​](#setbodybackgroundcolor)
▸ setBodyBackgroundColor(`value`): `this`

Set the body background color of the order line.

#### Parameters[​](#parameters-8)
NameTypeDescription`value``string`The new body background color.
#### Returns[​](#returns-34)
`this`

### setBodyBorderColor[​](#setbodybordercolor)
▸ setBodyBorderColor(`value`): `this`

Set the body border color of the order line.

#### Parameters[​](#parameters-9)
NameTypeDescription`value``string`The new body border color.
#### Returns[​](#returns-35)
`this`

### setBodyFont[​](#setbodyfont)
▸ setBodyFont(`value`): `this`

Set the body font of the order line.

Example

```
orderLine.setPrice(170).setBodyFont("bold 12px Verdana")
```
#### Parameters[​](#parameters-10)
NameTypeDescription`value``string`The new body font.
#### Returns[​](#returns-36)
`this`

### setBodyTextColor[​](#setbodytextcolor)
▸ setBodyTextColor(`value`): `this`

Set the body text color of the order line.

#### Parameters[​](#parameters-11)
NameTypeDescription`value``string`The new body text color.
#### Returns[​](#returns-37)
`this`

### setCancelButtonBackgroundColor[​](#setcancelbuttonbackgroundcolor)
▸ setCancelButtonBackgroundColor(`value`): `this`

Set the cancel button background color of the order line.

#### Parameters[​](#parameters-12)
NameTypeDescription`value``string`The new cancel button background color.
#### Returns[​](#returns-38)
`this`

### setCancelButtonBorderColor[​](#setcancelbuttonbordercolor)
▸ setCancelButtonBorderColor(`value`): `this`

Set the cancel button border color of the order line.

#### Parameters[​](#parameters-13)
NameTypeDescription`value``string`The new cancel button border color.
#### Returns[​](#returns-39)
`this`

### setCancelButtonIconColor[​](#setcancelbuttoniconcolor)
▸ setCancelButtonIconColor(`value`): `this`

Set the cancel button icon color of the order line.

#### Parameters[​](#parameters-14)
NameTypeDescription`value``string`The new cancel button icon color.
#### Returns[​](#returns-40)
`this`

### setCancelTooltip[​](#setcanceltooltip)
▸ setCancelTooltip(`value`): `this`

Set the cancel tooltip of the order line.

#### Parameters[​](#parameters-15)
NameTypeDescription`value``string`The new cancel tooltip
#### Returns[​](#returns-41)
`this`

### setCancellable[​](#setcancellable)
▸ setCancellable(`value`): `this`

Set the cancellable flag value of the order line.

#### Parameters[​](#parameters-16)
NameTypeDescription`value``boolean`The new cancellable flag value.
#### Returns[​](#returns-42)
`this`

### setEditable[​](#seteditable)
▸ setEditable(`value`): `this`

Set the editable of the order line.

#### Parameters[​](#parameters-17)
NameTypeDescription`value``boolean`The new editable.
#### Returns[​](#returns-43)
`this`

### setExtendLeft[​](#setextendleft)
▸ setExtendLeft(`value`): `this`

Set the extend left flag value of the order line.

#### Parameters[​](#parameters-18)
NameTypeDescription`value``boolean`The new extend left flag value.
#### Returns[​](#returns-44)
`this`

### setLineColor[​](#setlinecolor)
▸ setLineColor(`value`): `this`

Set the line color of the order line.

#### Parameters[​](#parameters-19)
NameTypeDescription`value``string`The new line color.
#### Returns[​](#returns-45)
`this`

### setLineLength[​](#setlinelength)
▸ setLineLength(`value`, `unit?`): `this`

Set the line length of the order line.

If negative number is provided for the value and the unit is 'pixel' then
the position will be relative to the left edge of the chart.
#### Parameters[​](#parameters-20)
NameTypeDescription`value``number`The new line length.`unit?`[`OrderLineLengthUnit`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#orderlinelengthunit)unit for the line length, defaults to 'percentage'.
#### Returns[​](#returns-46)
`this`

### setLineStyle[​](#setlinestyle)
▸ setLineStyle(`value`): `this`

Set the line style of the order line.

#### Parameters[​](#parameters-21)
NameTypeDescription`value``number`The new line style.
#### Returns[​](#returns-47)
`this`

### setLineWidth[​](#setlinewidth)
▸ setLineWidth(`value`): `this`

Set the line width of the order line.

#### Parameters[​](#parameters-22)
NameTypeDescription`value``number`The new line width.
#### Returns[​](#returns-48)
`this`

### setModifyTooltip[​](#setmodifytooltip)
▸ setModifyTooltip(`value`): `this`

Set the modify tooltip of the order line.

#### Parameters[​](#parameters-23)
NameTypeDescription`value``string`The new modify tooltip
#### Returns[​](#returns-49)
`this`

### setPrice[​](#setprice)
▸ setPrice(`value`): `this`

Set the price of the order line.

#### Parameters[​](#parameters-24)
NameTypeDescription`value``number`The new price
#### Returns[​](#returns-50)
`this`

### setQuantity[​](#setquantity)
▸ setQuantity(`value`): `this`

Set the quantity of the order line.

#### Parameters[​](#parameters-25)
NameTypeDescription`value``string`The new quantity.
#### Returns[​](#returns-51)
`this`

### setQuantityBackgroundColor[​](#setquantitybackgroundcolor)
▸ setQuantityBackgroundColor(`value`): `this`

Set the quantity background color of the order line.

#### Parameters[​](#parameters-26)
NameTypeDescription`value``string`The new quantity background color.
#### Returns[​](#returns-52)
`this`

### setQuantityBorderColor[​](#setquantitybordercolor)
▸ setQuantityBorderColor(`value`): `this`

Set the quantity border color of the order line.

#### Parameters[​](#parameters-27)
NameTypeDescription`value``string`The new quantity border color.
#### Returns[​](#returns-53)
`this`

### setQuantityFont[​](#setquantityfont)
▸ setQuantityFont(`value`): `this`

Set the quantity font of the order line.

Example

```
orderLine.setPrice(170).setQuantityFont("bold 12px Verdana")
```
#### Parameters[​](#parameters-28)
NameTypeDescription`value``string`The new quantity font.
#### Returns[​](#returns-54)
`this`

### setQuantityTextColor[​](#setquantitytextcolor)
▸ setQuantityTextColor(`value`): `this`

Set the quantity text color of the order line.

#### Parameters[​](#parameters-29)
NameTypeDescription`value``string`The new quantity text color.
#### Returns[​](#returns-55)
`this`

### setText[​](#settext)
▸ setText(`value`): `this`

Set the text of the order line.

#### Parameters[​](#parameters-30)
NameTypeDescription`value``string`The new text
#### Returns[​](#returns-56)
`this`

### setTooltip[​](#settooltip)
▸ setTooltip(`value`): `this`

Set the tooltip of the order line.

#### Parameters[​](#parameters-31)
NameTypeDescription`value``string`The new tooltip
#### Returns[​](#returns-57)
`this`

- [Methods](#methods)[getBodyBackgroundColor](#getbodybackgroundcolor)- [getBodyBorderColor](#getbodybordercolor)- [getBodyFont](#getbodyfont)- [getBodyTextColor](#getbodytextcolor)- [getCancelButtonBackgroundColor](#getcancelbuttonbackgroundcolor)- [getCancelButtonBorderColor](#getcancelbuttonbordercolor)- [getCancelButtonIconColor](#getcancelbuttoniconcolor)- [getCancelTooltip](#getcanceltooltip)- [getCancellable](#getcancellable)- [getEditable](#geteditable)- [getExtendLeft](#getextendleft)- [getLineColor](#getlinecolor)- [getLineLength](#getlinelength)- [getLineLengthUnit](#getlinelengthunit)- [getLineStyle](#getlinestyle)- [getLineWidth](#getlinewidth)- [getModifyTooltip](#getmodifytooltip)- [getPrice](#getprice)- [getQuantity](#getquantity)- [getQuantityBackgroundColor](#getquantitybackgroundcolor)- [getQuantityBorderColor](#getquantitybordercolor)- [getQuantityFont](#getquantityfont)- [getQuantityTextColor](#getquantitytextcolor)- [getText](#gettext)- [getTooltip](#gettooltip)- [onCancel](#oncancel)- [onModify](#onmodify)- [onMove](#onmove)- [onMoving](#onmoving)- [remove](#remove)- [setBodyBackgroundColor](#setbodybackgroundcolor)- [setBodyBorderColor](#setbodybordercolor)- [setBodyFont](#setbodyfont)- [setBodyTextColor](#setbodytextcolor)- [setCancelButtonBackgroundColor](#setcancelbuttonbackgroundcolor)- [setCancelButtonBorderColor](#setcancelbuttonbordercolor)- [setCancelButtonIconColor](#setcancelbuttoniconcolor)- [setCancelTooltip](#setcanceltooltip)- [setCancellable](#setcancellable)- [setEditable](#seteditable)- [setExtendLeft](#setextendleft)- [setLineColor](#setlinecolor)- [setLineLength](#setlinelength)- [setLineStyle](#setlinestyle)- [setLineWidth](#setlinewidth)- [setModifyTooltip](#setmodifytooltip)- [setPrice](#setprice)- [setQuantity](#setquantity)- [setQuantityBackgroundColor](#setquantitybackgroundcolor)- [setQuantityBorderColor](#setquantitybordercolor)- [setQuantityFont](#setquantityfont)- [setQuantityTextColor](#setquantitytextcolor)- [setText](#settext)- [setTooltip](#settooltip)