---
title: "Interface: CreateMultipointShapeOptions<TOverrides> | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateMultipointShapeOptions"
extracted_at: "2025-06-22T09:34:56.911Z"
---

- [](/charting-library-docs/)- Interfaces- CreateMultipointShapeOptionsOn this page# Interface: CreateMultipointShapeOptions<TOverrides>[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).CreateMultipointShapeOptions

Options for creating a multipoint drawing.

## Type parameters[​](#type-parameters)
NameType`TOverrides`extends `object`
## Hierarchy[​](#hierarchy)

[`CreateShapeOptionsBase`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateShapeOptionsBase)<`TOverrides`>

↳ `CreateMultipointShapeOptions`

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

The ID of an indicator that the drawing is attached to. For more information, refer to the [Attach drawing to indicator](https://www.tradingview.com/charting-library-docs/latest/ui_elements/drawings/drawings-api#attach-drawing-to-indicator) section.

#### Inherited from[​](#inherited-from-7)
[CreateShapeOptionsBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateShapeOptionsBase).[ownerStudyId](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateShapeOptionsBase#ownerstudyid)

### shape[​](#shape)
• `Optional` shape: `"emoji"` | `"triangle"` | `"curve"` | `"table"` | `"circle"` | `"ellipse"` | `"path"` | `"polyline"` | `"text"` | `"icon"` | `"extended"` | `"anchored_text"` | `"anchored_note"` | `"note"` | `"signpost"` | `"double_curve"` | `"arc"` | `"sticker"` | `"arrow_up"` | `"arrow_down"` | `"arrow_left"` | `"arrow_right"` | `"price_label"` | `"price_note"` | `"arrow_marker"` | `"flag"` | `"vertical_line"` | `"horizontal_line"` | `"cross_line"` | `"horizontal_ray"` | `"trend_line"` | `"info_line"` | `"trend_angle"` | `"arrow"` | `"ray"` | `"parallel_channel"` | `"disjoint_angle"` | `"flat_bottom"` | `"anchored_vwap"` | `"pitchfork"` | `"schiff_pitchfork_modified"` | `"schiff_pitchfork"` | `"balloon"` | `"comment"` | `"inside_pitchfork"` | `"pitchfan"` | `"gannbox"` | `"gannbox_square"` | `"gannbox_fixed"` | `"gannbox_fan"` | `"fib_retracement"` | `"fib_trend_ext"` | `"fib_speed_resist_fan"` | `"fib_timezone"` | `"fib_trend_time"` | `"fib_circles"` | `"fib_spiral"` | `"fib_speed_resist_arcs"` | `"fib_channel"` | `"xabcd_pattern"` | `"cypher_pattern"` | `"abcd_pattern"` | `"callout"` | `"text_note"` | `"triangle_pattern"` | `"3divers_pattern"` | `"head_and_shoulders"` | `"fib_wedge"` | `"elliott_impulse_wave"` | `"elliott_triangle_wave"` | `"elliott_triple_combo"` | `"elliott_correction"` | `"elliott_double_combo"` | `"cyclic_lines"` | `"time_cycles"` | `"sine_line"` | `"long_position"` | `"short_position"` | `"forecast"` | `"date_range"` | `"price_range"` | `"date_and_price_range"` | `"bars_pattern"` | `"ghost_feed"` | `"projection"` | `"rectangle"` | `"rotated_rectangle"` | `"brush"` | `"highlighter"` | `"regression_trend"` | `"fixed_range_volume_profile"`

A drawing to create.

### showInObjectsTree[​](#showinobjectstree)
• `Optional` showInObjectsTree: `boolean`

Enable/disable showing the drawing in the objects tree.

#### Inherited from[​](#inherited-from-8)
[CreateShapeOptionsBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateShapeOptionsBase).[showInObjectsTree](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateShapeOptionsBase#showinobjectstree)

### text[​](#text)
• `Optional` text: `string`

Text for drawing

#### Inherited from[​](#inherited-from-9)
[CreateShapeOptionsBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateShapeOptionsBase).[text](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateShapeOptionsBase#text)

### zOrder[​](#zorder)
• `Optional` zOrder: `"top"` | `"bottom"`

Create the drawing in front of all other drawings, or behind all other drawings.

#### Inherited from[​](#inherited-from-10)
[CreateShapeOptionsBase](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateShapeOptionsBase).[zOrder](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CreateShapeOptionsBase#zorder)

- [Type parameters](#type-parameters)- [Hierarchy](#hierarchy)- [Properties](#properties)[disableSave](#disablesave)- [disableSelection](#disableselection)- [disableUndo](#disableundo)- [filled](#filled)- [icon](#icon)- [lock](#lock)- [overrides](#overrides)- [ownerStudyId](#ownerstudyid)- [shape](#shape)- [showInObjectsTree](#showinobjectstree)- [text](#text)- [zOrder](#zorder)