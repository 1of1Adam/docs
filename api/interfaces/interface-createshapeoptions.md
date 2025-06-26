---
title: "Interface: CreateShapeOptions<TOverrides> | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateShapeOptions"
extracted_at: "2025-06-22T09:34:58.288Z"
---

- [](/charting-library-docs/)- Interfaces- CreateShapeOptionsOn this page# Interface: CreateShapeOptions<TOverrides>[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).CreateShapeOptions

Options for creating a drawing.

## Type parameters[​](#type-parameters)
NameType`TOverrides`extends `object`
## Hierarchy[​](#hierarchy)

[`CreateShapeOptionsBase`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateShapeOptionsBase)<`TOverrides`>

↳ `CreateShapeOptions`

## Properties[​](#properties)
### disableSave[​](#disablesave)
• `Optional` disableSave: `boolean`

Disable/enable saving the drawing.

#### Inherited from[​](#inherited-from)
[CreateShapeOptionsBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateShapeOptionsBase).[disableSave](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateShapeOptionsBase#disablesave)

### disableSelection[​](#disableselection)
• `Optional` disableSelection: `boolean`

Disable/enable selecting the drawing.

#### Inherited from[​](#inherited-from-1)
[CreateShapeOptionsBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateShapeOptionsBase).[disableSelection](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateShapeOptionsBase#disableselection)

### disableUndo[​](#disableundo)
• `Optional` disableUndo: `boolean`

If `true`, users cannot cancel the drawing creation in the UI. However, users can still click the Undo button to cancel previous actions.

#### Inherited from[​](#inherited-from-2)
[CreateShapeOptionsBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateShapeOptionsBase).[disableUndo](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateShapeOptionsBase#disableundo)

### filled[​](#filled)
• `Optional` filled: `boolean`

Enable/disable filling the drawing with color (if the drawing supports filling).

#### Inherited from[​](#inherited-from-3)
[CreateShapeOptionsBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateShapeOptionsBase).[filled](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateShapeOptionsBase#filled)

### icon[​](#icon)
• `Optional` icon: `number`

Specify an icon to render. Only icons from the [Drawings list](https://www.tradingview.com/charting-library-docs/latest/ui_elements/drawings/Drawings-List#icons) are supported.
Note that the value should be a hex number, not a string.
#### Inherited from[​](#inherited-from-4)
[CreateShapeOptionsBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateShapeOptionsBase).[icon](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateShapeOptionsBase#icon)

### lock[​](#lock)
• `Optional` lock: `boolean`

Should drawing be locked

#### Inherited from[​](#inherited-from-5)
[CreateShapeOptionsBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateShapeOptionsBase).[lock](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateShapeOptionsBase#lock)

### overrides[​](#overrides)
• `Optional` overrides: `TOverrides`

Drawing properties overrides. Refer to [Drawing Overrides](https://www.tradingview.com/charting-library-docs/latest/customization/overrides/Drawings-Overrides) for more information.

#### Inherited from[​](#inherited-from-6)
[CreateShapeOptionsBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateShapeOptionsBase).[overrides](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateShapeOptionsBase#overrides)

### ownerStudyId[​](#ownerstudyid)
• `Optional` ownerStudyId: [`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)

The ID of an indicator that the drawing is attached to.
For more information, refer to the [Attach drawing to indicator](https://www.tradingview.com/charting-library-docs/latest/ui_elements/drawings/drawings-api#attach-drawing-to-indicator) section.
#### Overrides[​](#overrides-1)
[CreateShapeOptionsBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateShapeOptionsBase).[ownerStudyId](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateShapeOptionsBase#ownerstudyid)

### shape[​](#shape)
• `Optional` shape: `"emoji"` | `"text"` | `"icon"` | `"anchored_text"` | `"anchored_note"` | `"note"` | `"sticker"` | `"arrow_up"` | `"arrow_down"` | `"flag"` | `"vertical_line"` | `"horizontal_line"` | `"long_position"` | `"short_position"`

A drawing to create.

### showInObjectsTree[​](#showinobjectstree)
• `Optional` showInObjectsTree: `boolean`

Enable/disable showing the drawing in the objects tree.

#### Inherited from[​](#inherited-from-7)
[CreateShapeOptionsBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateShapeOptionsBase).[showInObjectsTree](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateShapeOptionsBase#showinobjectstree)

### text[​](#text)
• `Optional` text: `string`

Text for drawing

#### Inherited from[​](#inherited-from-8)
[CreateShapeOptionsBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateShapeOptionsBase).[text](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateShapeOptionsBase#text)

### zOrder[​](#zorder)
• `Optional` zOrder: `"top"` | `"bottom"`

Create the drawing in front of all other drawings, or behind all other drawings.

#### Inherited from[​](#inherited-from-9)
[CreateShapeOptionsBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateShapeOptionsBase).[zOrder](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateShapeOptionsBase#zorder)

- [Type parameters](#type-parameters)- [Hierarchy](#hierarchy)- [Properties](#properties)[disableSave](#disablesave)- [disableSelection](#disableselection)- [disableUndo](#disableundo)- [filled](#filled)- [icon](#icon)- [lock](#lock)- [overrides](#overrides)- [ownerStudyId](#ownerstudyid)- [shape](#shape)- [showInObjectsTree](#showinobjectstree)- [text](#text)- [zOrder](#zorder)