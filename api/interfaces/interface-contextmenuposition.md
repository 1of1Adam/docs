---
title: "Interface: ContextMenuPosition | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ContextMenuPosition"
extracted_at: "2025-06-22T09:34:43.701Z"
---

- [](/charting-library-docs/)- Interfaces- ContextMenuPositionOn this page# Interface: ContextMenuPosition[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).ContextMenuPosition

## Properties[​](#properties)
### attachToXBy[​](#attachtoxby)
• `Optional` attachToXBy: `"auto"` | `"left"` | `"right"`

Tells what side of the context menu widget should be used to "attach" to a provided x coordinate.
If the value is `undefined`, then you may treat it based on whether it is rtl or not (e.g. `'right'` for rtl and `'left'` otherwise).
The value `'auto'` behaves as `undefined` but additionally checks if there is enough space to place the menu and if it's not then the result value is inverted.

### attachToYBy[​](#attachtoyby)
• `Optional` attachToYBy: `"auto"` | `"top"` | `"bottom"` | `"auto-strict"`

Tells what side of the context menu widget should be used to "attach" to a provided y coordinate:

- `'auto'` means similar to `'top'` but the menu could be expanded above the coordinate if needed (if there is no enough space to place it below)
- `'auto-strict'` means `'top'` if the whole menu fits the space below the coordinate and `'bottom'` otherwise (see [box](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ContextMenuPosition#box))
- `'top'` means that the menu should be placed to the bottom of y coordinate (the menu should be attached by its bottom to y coordinate)
- `'bottom'` means that the menu should be placed above y coordinate (the menu should be attached by its top to y coordinate)

You may treat `undefined` as `'auto'`.

### box[​](#box)
• `Optional` box: `Object`

The optional structure that helps to more accurate calculate a position of the menu (see [attachToYBy](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.ContextMenuPosition#attachtoyby)).

#### Type declaration[​](#type-declaration)
NameTypeDescription`h``number`menu height`overlapX?``boolean`x coordinate overlaps`w``number`menu width`x``number`menu x coordinate`y``number`menu y coordinate

### clientX[​](#clientx)
• clientX: `number`

X (horizontal) coordinate (in pixels) at which the mouse event occurred, relative to the left edge of the applications viewport.

### clientY[​](#clienty)
• clientY: `number`

Y (vertical) coordinate (in pixels) at which the mouse event occurred, relative to the left edge of the applications viewport.

### marginX[​](#marginx)
• `Optional` marginX: `number`

Additional horizontal margin.

### marginY[​](#marginy)
• `Optional` marginY: `number`

Additional vertical margin.

### touches[​](#touches)
• `Optional` touches: readonly { `clientX`: `number` ; `clientY`: `number`  }[]

Touch positions

- [Properties](#properties)[attachToXBy](#attachtoxby)- [attachToYBy](#attachtoyby)- [box](#box)- [clientX](#clientx)- [clientY](#clienty)- [marginX](#marginx)- [marginY](#marginy)- [touches](#touches)