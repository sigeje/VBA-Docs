---
title: FillFormat.Creator property (Word)
keywords: vbawd10.chm164103145
f1_keywords:
- vbawd10.chm164103145
ms.prod: word
api_name:
- Word.FillFormat.Creator
ms.assetid: 1bb9d3ad-ab28-f109-f449-624c61be3746
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# FillFormat.Creator property (Word)

Returns a 32-bit integer that indicates the application in which the specified object was created. Read-only  **Long**.


## Syntax

_expression_.**Creator**

_expression_ Required. A variable that represents a **[FillFormat](word.fillformat.md)** object.


## Remarks

If the object was created in Microsoft Word, the **Creator** property returns the hexadecimal number 4D535744, which represents the string "MSWD." This property was primarily designed to be used on the Macintosh, where each application has a four-character creator code. For example, Microsoft Word has the creator code MSWD. For additional information about this property, consult the language reference Help included with Microsoft Office Macintosh Edition.


## See also


[FillFormat Object](Word.FillFormat.md)

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]