---
title: Range.ShowDependents method (Excel)
keywords: vbaxl10.chm144195
f1_keywords:
- vbaxl10.chm144195
ms.prod: excel
api_name:
- Excel.Range.ShowDependents
ms.assetid: f2e062b2-733b-d0e5-b5ed-9587b104bbc7
ms.date: 05/11/2019
ms.localizationpriority: medium
---


# Range.ShowDependents method (Excel)

Draws tracer arrows to the direct dependents of the range.


## Syntax

_expression_.**ShowDependents** (_Remove_)

_expression_ A variable that represents a **[Range](excel.range(object).md)** object.


## Parameters

|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
| _Remove_|Optional| **Variant**| **True** to remove one level of tracer arrows to direct dependents. **False** to expand one level of tracer arrows. The default value is **False**.|

## Return value

Variant


## Example

This example draws tracer arrows to dependents of the active cell on Sheet1.

```vb
Worksheets("Sheet1").Activate 
ActiveCell.ShowDependents
```

<br/>

This example removes the tracer arrow for one level of dependents of the active cell on Sheet1.

```vb
Worksheets("Sheet1").Activate 
ActiveCell.ShowDependents Remove:=True
```




[!include[Support and feedback](~/includes/feedback-boilerplate.md)]