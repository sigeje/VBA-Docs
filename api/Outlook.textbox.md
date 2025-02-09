---
title: TextBox object (Outlook Forms Script)
keywords: olfm10.chm2000670
f1_keywords:
- olfm10.chm2000670
ms.prod: outlook
ms.assetid: 4a0e4a3d-beca-9f94-7e27-469c4bafe250
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# TextBox object (Outlook Forms Script)

Displays information from a user or from an organized set of data.


## Remarks

A **TextBox** is the control most commonly used to display information entered by a user. Also, it can display a set of data, such as a table, query, worksheet, or a calculation result. If a **TextBox** is bound to a data source, then changing the contents of the **TextBox** also changes the value of the bound data source.

Formatting applied to any piece of text in a **TextBox** will affect all text in the control. For example, if you change the font or point size of any character in the control, the change will affect all characters in the control.

The default property for a **TextBox** is the **[Value](Outlook.textbox.value.md)** property.


## Tips on using text boxes

The **TextBox** is a flexible control governed by the following properties: **[Text](Outlook.textbox.text.md)**, **[MultiLine](Outlook.textbox.multiline.md)**, **[WordWrap](Outlook.textbox.wordwrap.md)**, and **[AutoSize](Outlook.textbox.autosize.md)**.

**Text** contains the text that's displayed in the text box.

**MultiLine** controls whether the **TextBox** can display text as a single line or as multiple lines. Newline characters identify where one line ends and another begins. If **MultiLine** is **False** (the default value), the text is truncated instead of wrapped.

**WordWrap** allows the **TextBox** to wrap lines of text that are longer than the width of the **TextBox** into shorter lines that fit. The default value is **True**.

If you do not use **WordWrap**, the **TextBox** starts a new line of text when it encounters a newline character in the text. If **WordWrap** is turned off, you can have text lines that do not fit completely in the **TextBox**. The **TextBox** displays the portions of text that fit inside its width and truncates the portions of text that do not fit. **WordWrap** is not applicable unless **MultiLine** is **True**.

**AutoSize** controls whether the **TextBox** adjusts to display all of the text. When using **AutoSize** with a **TextBox**, the width of the **TextBox** shrinks or expands according to the amount of text in the **TextBox** and the font size used to display the text. The default value is **False**.

**AutoSize** works well in the following situations:

- Displaying a caption of one or more lines.
    
- Displaying the contents of a single-line **TextBox**.
    
- Displaying the contents of a multiline **TextBox** that is read-only to the user.
    
Avoid using **AutoSize** with an empty **TextBox** that also uses the **MultiLine** and **WordWrap** properties. When the user enters text into a **TextBox** with these properties, the **TextBox** automatically sizes to a long narrow box one character wide and as long as the line of text.


## Methods

|Name|Description|
|:-----|:-----|
| [Copy](Outlook.textbox.copy.md)|Copies the contents of an object to the Clipboard.|
| [Cut](Outlook.textbox.cut.md)|Removes selected information from an object and transfers it to the Clipboard.|
| [Paste](Outlook.textbox.paste.md)|Transfers the contents of the Clipboard to an object.|


## Properties

|Name|Description|
|:-----|:-----|
| [AutoSize](Outlook.textbox.autosize.md)|Returns or sets a **Boolean** that specifies whether an object automatically resizes to display its entire contents. Read/write.|
| [AutoTab](Outlook.textbox.autotab.md)|Returns or sets a **Boolean** that specifies whether an automatic tab occurs when a user enters the maximum allowable number of characters into a [TextBox](Outlook.textbox.md). Read/write.|
| [AutoWordSelect](Outlook.textbox.autowordselect.md)|Returns or sets a **Boolean** that specifies whether the basic unit used to extend a selection is a word or a single character. Read/write.|
| [BackColor](Outlook.textbox.backcolor.md)|Returns or sets a **Long** that specifies the background color of the object. Read/write.|
| [BackStyle](Outlook.textbox.backstyle.md)|Returns or sets an **Integer** that specifies the background style for an object. Read/write.|
| [BorderColor](Outlook.textbox.bordercolor.md)|Returns or sets a **Long** that specifies the border color of an object. Read/write.|
| [BorderStyle](Outlook.textbox.borderstyle.md)|Returns or sets an **Integer** that specifies the type of border of the control. Read/write.|
| [CanPaste](Outlook.textbox.canpaste.md)|Returns a **Boolean** that specifies whether the Clipboard contains data that the object supports. Read-only.|
| [CurLine](Outlook.textbox.curline.md)|Returns or sets a **Long** that represents the current line of a control. Read/write.|
| [CurTargetX](Outlook.textbox.curtargetx.md)|Returns a **Long** that represents the preferred horizontal position of the insertion point in a multiline **TextBox**. Read-only.|
| [CurX](Outlook.textbox.curx.md)|Returns or sets a **Long** that represents the current horizontal position of the insertion point in a multiline **TextBox**. Read/write.|
| [DragBehavior](Outlook.textbox.dragbehavior.md)|Returns or sets an **Integer** that specifies whether the system enables the drag-and-drop feature for the control. Read/write.|
| [Enabled](Outlook.textbox.enabled.md)|Returns or sets a **Boolean** that specifies whether a control can receive the focus and respond to user-generated events. Read/write.|
| [EnterFieldBehavior](Outlook.textbox.enterfieldbehavior.md)|Returns or sets an **Integer** that specifies the selection behavior when entering a **TextBox**. Read/write.|
| [EnterKeyBehavior](Outlook.textbox.enterkeybehavior.md)|Returns or sets a **Boolean** that defines the effect of pressing **ENTER** in a **TextBox**. Read/write.|
| [ForeColor](Outlook.textbox.forecolor.md)|Returns or sets a **Long** that specifies the foreground color of an object. Read/write.|
| [HideSelection](Outlook.textbox.hideselection.md)|Returns or sets a **Boolean** that specifies whether selected text remains highlighted when a control does not have the focus. Read/write.|
| [IMEMode](Outlook.textbox.imemode.md)|Returns or sets an **Integer** that specifies the default run-time mode of the Input Method Editor (IME) for a control. Read/write.|
| [IntegralHeight](Outlook.textbox.integralheight.md)|Returns or sets a **Boolean** that specifies whether a **TextBox** displays full lines of text or partial lines. Read/write.|
| [LineCount](Outlook.textbox.linecount.md)|Returns a **Long** that specifies the number of text lines in a **TextBox**. Read-only.|
| [Locked](Outlook.textbox.locked.md)|Returns or sets a **Boolean** that specifies whether a control can be edited. Read/write.|
| [MaxLength](Outlook.textbox.maxlength.md)|Returns or sets a **Long** that specifies the maximum number of characters a user can enter in a **TextBox**. Read/write.|
| [MouseIcon](Outlook.textbox.mouseicon.md)|Returns a **String** that represents the full path name of a custom icon that is to be assigned to the control. Read-only.|
| [MousePointer](Outlook.textbox.mousepointer.md)|Returns or sets an **Integer** that specifies the type of pointer displayed when the user positions the mouse over a particular object. Read/write.|
| [MultiLine](Outlook.textbox.multiline.md)|Returns or sets a **Boolean** that specifies whether a control can accept and display multiple lines of text. Read/write.|
| [PasswordChar](Outlook.textbox.passwordchar.md)|Returns or sets a **String** that specifies a placeholder character to be displayed instead of the characters actually entered in a **TextBox**. Read/write.|
| [ScrollBars](Outlook.textbox.scrollbars.md)|Returns or sets an **Integer** that specifies whether a control has vertical scroll bars, horizontal scroll bars, or both. Read/write.|
| [SelectionMargin](Outlook.textbox.selectionmargin.md)|Returns or sets a **Boolean** that specifies whether the user can select a line of text by clicking in the region to the left of the text. Read/write.|
| [SelLength](Outlook.textbox.sellength.md)|Returns or sets a **Long** that represents the number of characters selected in a **TextBox**. Read/write.|
| [SelStart](Outlook.textbox.selstart.md)|Returns or sets a **Long** that represents the starting point of selected text, or the insertion point if no text is selected. Read/write.|
| [SelText](Outlook.textbox.seltext.md)|Returns or sets a **String** that represents the selected text of a control. Read/write.|
| [SpecialEffect](Outlook.textbox.specialeffect.md)|Returns or sets an **Integer** that specifies the visual appearance of an object. Read/write.|
| [TabKeyBehavior](Outlook.textbox.tabkeybehavior.md)|Returns or sets a **Boolean** that specifies whether tabs are allowed in the edit region. Read/write.|
| [Text](Outlook.textbox.text.md)|Returns or sets a **String** that specifies text in the control. Read/write.|
| [TextAlign](Outlook.textbox.textalign.md)|Returns or sets an **Integer** that specifies how text is aligned in a control. Read/write.|
| [TextLength](Outlook.textbox.textlength.md)|Returns a **Long** that represents the length, in number of characters, of text in the edit region of a **TextBox**. Read-only.|
| [Value](Outlook.textbox.value.md)|Returns or sets a **Variant** that specifies text in the edit region. Read/write.|
| [WordWrap](Outlook.textbox.wordwrap.md)|Returns or sets a **Boolean** that specifies whether the contents of a control automatically wrap at the end of a line and the control expands to fit the text. Read/write.|

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]