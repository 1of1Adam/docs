---
title: "Interface: UndoRedoState | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.UndoRedoState"
extracted_at: "2025-06-22T09:49:48.971Z"
---

- [](/charting-library-docs/)- Interfaces- UndoRedoStateOn this page# Interface: UndoRedoState[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).UndoRedoState

State of the Undo/Redo stack. This object has the same structure as the result of [IChartingLibraryWidget.undoRedoState](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.IChartingLibraryWidget#undoredostate) method

## Properties[​](#properties)
### enableRedo[​](#enableredo)
• `Readonly` enableRedo: `boolean`

Redo is enabled

### enableUndo[​](#enableundo)
• `Readonly` enableUndo: `boolean`

Undo is enabled

### originalRedoText[​](#originalredotext)
• `Readonly` originalRedoText: `string`

Original text for redo action - without being translated

### originalUndoText[​](#originalundotext)
• `Readonly` originalUndoText: `string`

Original text for undo action - without being translated

### redoText[​](#redotext)
• `Readonly` redoText: `string`

Redo text

### undoText[​](#undotext)
• `Readonly` undoText: `string`

Undo text

- [Properties](#properties)[enableRedo](#enableredo)- [enableUndo](#enableundo)- [originalRedoText](#originalredotext)- [originalUndoText](#originalundotext)- [redoText](#redotext)- [undoText](#undotext)