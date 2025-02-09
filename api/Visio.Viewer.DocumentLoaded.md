---
title: Viewer.DocumentLoaded property (Visio Viewer)
ms.prod: visio
api_name:
- Visio.Viewer.DocumentLoaded
ms.assetid: 2d7c86fa-a154-dd8f-3a8c-6c433103d6a4
ms.date: 06/21/2019
ms.localizationpriority: medium
---


# Viewer.DocumentLoaded property (Visio Viewer)

Gets a value that indicates whether a document is loaded in Microsoft Visio Viewer. Read-only.


## Syntax

_expression_.**DocumentLoaded**

_expression_ An expression that returns a **[Viewer](Visio.Viewer.md)** object.


## Return value

**Boolean**


## Remarks

The default setting for the **DocumentLoaded** property value is **False**.


## Example

The following code gets a value that indicates whether a document is loaded in Visio Viewer.

```vb
Debug.Print vsoViewer.DocumentLoaded
```

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]