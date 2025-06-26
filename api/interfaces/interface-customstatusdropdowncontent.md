---
title: "Interface: CustomStatusDropDownContent | Advanced Charts Documentation"
url: "https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CustomStatusDropDownContent"
extracted_at: "2025-06-22T09:35:41.474Z"
---

- [](/charting-library-docs/)- Interfaces- CustomStatusDropDownContentOn this page# Interface: CustomStatusDropDownContent[Charting Library](https://www.tradingview.com/charting-library-docs/latest/api/modules/Charting_Library).CustomStatusDropDownContent

Specifies the content to be displayed within a section of
the pop-up tooltip which is displayed when a user clicks on
the symbol status items.
The pop-up tooltip should be used to display additional
information related to the status item.
## Properties[​](#properties)
### action[​](#action)
• `Optional` action: [`CustomStatusDropDownAction`](https://www.tradingview.com/charting-library-docs/latest/api/interfaces/Charting_Library.CustomStatusDropDownAction)

Optional action link to be displayed at the bottom of
the status section.

### color[​](#color)
• `Optional` color: `string`

Color to be used for the icon and title. If unspecified
then the color from the status item will be used.

### content[​](#content)
• content: `string`[]

Content to the displayed within this section of the
pop-up tooltip.
It is essential to protect the content you provide
against cross-site scripting (XSS) attacks, as these
strings will be interpreted as HTML markup.

### icon[​](#icon)
• `Optional` icon: `string`

Icon to be displayed next to the title for this section
of the pop-up tooltip. If unspecified then the icon from
the status item will be used.

### title[​](#title)
• title: `string`

Title to be displayed next to the icon for this section
of the pop-up tooltip.- [Properties](#properties)[action](#action)- [color](#color)- [content](#content)- [icon](#icon)- [title](#title)