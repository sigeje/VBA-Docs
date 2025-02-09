---
title: Report.ScaleTop property (Access)
keywords: vbaac10.chm13746
f1_keywords:
- vbaac10.chm13746
ms.prod: access
api_name:
- Access.Report.ScaleTop
ms.assetid: 2f148587-6da0-a6d3-414a-82f97d94a615
ms.date: 03/20/2019
ms.localizationpriority: medium
---


# Report.ScaleTop property (Access)

You can use the **ScaleTop** property to specify the units for the vertical coordinates that describe the location of the top edge of a page when the **[Circle](Access.Report.Circle.md)**, **[Line](Access.Report.Line.md)**, **[Pset](Access.Report.PSet.md)**, or **[Print](Access.Report.Print.md)** method is used while a report is printed or previewed, or its output is saved to a file. Read/write **Single**.


## Syntax

_expression_.**ScaleTop**

_expression_ A variable that represents a **[Report](Access.Report.md)** object.


## Remarks

You can set the **ScaleTop** property by using a macro or a [Visual Basic](../access/Concepts/Settings/set-properties-by-using-visual-basic.md) event procedure specified by a section's **OnPrint** property setting.

By using these properties and the related **ScaleHeight** and **ScaleWidth** properties, you can set up a custom coordinate system with both positive and negative coordinates. All four of these Scale properties interact with the **[ScaleMode](Access.Report.ScaleMode.md)** property in the following ways:

- Setting any other Scale property to any value automatically sets the **ScaleMode** property to 0.
    
- Setting the **ScaleMode** property to a number greater than 0 changes the **ScaleHeight** and **ScaleWidth** property settings to the new unit of measurement and sets the **ScaleLeft** and **ScaleTop** properties to 0. Also, the **[CurrentX](Access.Report.CurrentX.md)** and **[CurrentY](Access.Report.CurrentY.md)** property settings change to reflect the new coordinates of the current point.
    
You can also use the **Scale** method to set the **ScaleHeight**, **ScaleWidth**, **ScaleLeft**, and **ScaleTop** properties in one statement.

> [!NOTE] 
> The **ScaleTop** property isn't the same as the **Top** property.


## Example

The following example uses the **Circle** method to draw a circle and create a pie slice within the circle. It then uses the **FillColor** and **FillStyle** properties to color the pie slice red. It also draws a line from the upper-left to the center of the circle.

To try this example in Microsoft Access, create a new report. Set the **OnPrint** property of the Detail section to [Event Procedure]. Enter the following code in the report's module, and then switch to Print Preview.

```vb
Private Sub Detail_Print(Cancel As Integer, PrintCount As Integer) 
 
 Const conPI = 3.14159265359 
 
 Dim sngHCtr As Single 
 Dim sngVCtr As Single 
 Dim sngRadius As Single 
 Dim sngStart As Single 
 Dim sngEnd As Single 
 
 sngHCtr = Me.ScaleWidth / 2 ' Horizontal center. 
 sngVCtr = Me.ScaleHeight / 2 ' Vertical center. 
 sngRadius = Me.ScaleHeight / 3 ' Circle radius. 
 Me.Circle (sngHCtr, sngVCtr), sngRadius ' Draw circle. 
 sngStart = -0.00000001 ' Start of pie slice. 
 
 sngEnd = -2 * conPI / 3 ' End of pie slice. 
 Me.FillColor = RGB(255, 0, 0) ' Color pie slice red. 
 Me.FillStyle = 0 ' Fill pie slice. 
 
 ' Draw Pie slice within circle 
 Me.Circle (sngHCtr, sngVCtr), sngRadius, , sngStart, sngEnd 
 
 ' Draw line to center of circle. 
 Dim intColor As Integer 
 Dim sngTop As Single, sngLeft As Single 
 Dim sngWidth As Single, sngHeight As Single 
 
 Me.ScaleMode = 3 ' Set scale to pixels. 
 sngTop = Me.ScaleTop ' Top inside edge. 
 sngLeft = Me.ScaleLeft ' Left inside edge. 
 sngWidth = Me.ScaleWidth / 2 ' Width inside edge. 
 sngHeight = Me.ScaleHeight / 2 ' Height inside edge. 
 intColor = RGB(255, 0, 0) ' Make color red. 
 
 ' Draw line. 
 Me.Line (sngTop, sngLeft)-(sngWidth, sngHeight), intColor 
 
End Sub
```



[!include[Support and feedback](~/includes/feedback-boilerplate.md)]