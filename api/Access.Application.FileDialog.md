---
title: Application.FileDialog property (Access)
keywords: vbaac10.chm12592
f1_keywords:
- vbaac10.chm12592
ms.prod: access
api_name:
- Access.Application.FileDialog
ms.assetid: 8589e1de-e6e7-f85c-0138-0690781d5ed5
ms.date: 02/05/2019
ms.localizationpriority: medium
---


# Application.FileDialog property (Access)

Returns a **FileDialog** object that represents a single instance of a file dialog box. Read-only.


## Syntax

_expression_.**FileDialog** (_dialogType_)

_expression_ A variable that represents an **[Application](Access.Application.md)** object.


## Parameters

|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
| _dialogType_|Required|**[MsoFileDialogType](Office.MsoFileDialogType.md)**|An **MsoFileDialogType** constant that represents the type of dialog box.|

## Remarks

The **msoFileDialogOpen** and **msoFileDialogSaveAs** constants are not supported in Microsoft Access.


## Example

This example illustrates how to use the **FileDialog** object to display a dialog box that allows the user to select one or more files. The selected files are then added to a listbox named **FileList**.


```vb
Private Sub cmdFileDialog_Click() 
  
   ' Requires reference to Microsoft Office 11.0 Object Library. 
 
   Dim fDialog As Office.FileDialog 
   Dim varFile As Variant 
 
   ' Clear listbox contents. 
   Me.FileList.RowSource = "" 
 
   ' Set up the File Dialog. 
   Set fDialog = Application.FileDialog(msoFileDialogFilePicker) 
 
   With fDialog 
 
      ' Allow user to make multiple selections in dialog box 
      .AllowMultiSelect = True 
             
      ' Set the title of the dialog box. 
      .Title = "Please select one or more files" 
 
      ' Clear out the current filters, and add our own. 
      .Filters.Clear 
      .Filters.Add "Access Databases", "*.MDB" 
      .Filters.Add "Access Projects", "*.ADP" 
      .Filters.Add "All Files", "*.*" 
 
      ' Show the dialog box. If the .Show method returns True, the 
      ' user picked at least one file. If the .Show method returns 
      ' False, the user clicked Cancel. 
      If .Show = True Then 
 
         'Loop through each file selected and add it to our list box. 
         For Each varFile In .SelectedItems 
            Me.FileList.AddItem varFile 
         Next 
 
      Else 
         MsgBox "You clicked Cancel in the file dialog box." 
      End If 
   End With 
End Sub
```




[!include[Support and feedback](~/includes/feedback-boilerplate.md)]
