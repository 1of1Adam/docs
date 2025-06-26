---
title: "Interface: CreateShapeOptionsBase<TOverrides> | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateShapeOptionsBase"
extracted_at: "2025-06-22T09:35:00.071Z"
---

- [](/charting-library-docs/)- Interfaces- CreateShapeOptionsBaseOn this page# Interface: CreateShapeOptionsBase<TOverrides>[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).CreateShapeOptionsBase

Options for creating a drawing.

## Type parameters[​](#type-parameters)
NameType`TOverrides`extends `object`
## Hierarchy[​](#hierarchy)

`CreateShapeOptionsBase`

↳ [`CreateAnchoredShapeOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateAnchoredShapeOptions)

↳ [`CreateMultipointShapeOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateMultipointShapeOptions)

↳ [`CreateShapeOptions`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateShapeOptions)

## Properties[​](#properties)
### disableSave[​](#disablesave)
• `Optional` disableSave: `boolean`

Disable/enable saving the drawing.

### disableSelection[​](#disableselection)
• `Optional` disableSelection: `boolean`

Disable/enable selecting the drawing.

### disableUndo[​](#disableundo)
• `Optional` disableUndo: `boolean`

If `true`, users cannot cancel the drawing creation in the UI. However, users can still click the Undo button to cancel previous actions.

### filled[​](#filled)
• `Optional` filled: `boolean`

Enable/disable filling the drawing with color (if the drawing supports filling).

### icon[​](#icon)
• `Optional` icon: `number`

Specify an icon to render. Only icons from the [Drawings list](https://www.tradingview.com/charting-library-docs/latest/ui_elements/drawings/Drawings-List#icons) are supported.
Note that the value should be a hex number, not a string.

### lock[​](#lock)
• `Optional` lock: `boolean`

Should drawing be locked

### overrides[​](#overrides)
• `Optional` overrides: `TOverrides`

Drawing properties overrides. Refer to [Drawing Overrides](https://www.tradingview.com/charting-library-docs/latest/customization/overrides/Drawings-Overrides) for more information.

### ownerStudyId[​](#ownerstudyid)
• `Optional` ownerStudyId: [`EntityId`](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library#entityid)

The ID of an indicator that the drawing is attached to. For more information, refer to the [Attach drawing to indicator](https://www.tradingview.com/charting-library-docs/latest/ui_elements/drawings/drawings-api#attach-drawing-to-indicator) section.

### showInObjectsTree[​](#showinobjectstree)
• `Optional` showInObjectsTree: `boolean`

Enable/disable showing the drawing in the objects tree.

### text[​](#text)
• `Optional` text: `string`

Text for drawing

### zOrder[​](#zorder)
• `Optional` zOrder: `"top"` | `"bottom"`

Create the drawing in front of all other drawings, or behind all other drawings.

- [Type parameters](#type-parameters)- [Hierarchy](#hierarchy)- [Properties](#properties)[disableSave](#disablesave)- [disableSelection](#disableselection)- [disableUndo](#disableundo)- [filled](#filled)- [icon](#icon)- [lock](#lock)- [overrides](#overrides)- [ownerStudyId](#ownerstudyid)- [showInObjectsTree](#showinobjectstree)- [text](#text)- [zOrder](#zorder)