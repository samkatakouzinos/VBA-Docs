---
title: BoundObjectFrame.SourceDoc property (Access)
keywords: vbaac10.chm10913
f1_keywords:
- vbaac10.chm10913
ms.prod: access
api_name:
- Access.BoundObjectFrame.SourceDoc
ms.assetid: 5b0e6b68-6528-5a35-e31d-b93d119897cc
ms.date: 02/08/2019
ms.localizationpriority: medium
---


# BoundObjectFrame.SourceDoc property (Access)

Use the **SourceDoc** property to specify the file to create a link to or to embed when you create a linked object or embedded object by using the **Action** property in Visual Basic. Read/write **String**.


## Syntax

_expression_.**SourceDoc**

_expression_ A variable that represents a **[BoundObjectFrame](Access.BoundObjectFrame.md)** object.


## Remarks

For an embedded object, enter the full path and file name for the file that you want to use as a template and set the **Action** property to **acOLECreateEmbed**.

For a linked object, enter the full path and file name of the file to create a link to and set the **Action** property to **acOLECreateLink**.

While this property appears in the property sheet, it takes effect only after the **Action** property is set in a macro or by using Visual Basic.

Use the **SourceDoc** property to specify the file to create a link to, and the control's **SourceItem** property to specify the data within that file. If you want to create a link to the entire object, leave the **SourceItem** property blank.

When a linked unbound object is created, the control's **SourceItem** property setting is concatenated with its **SourceItem** property setting. In Form view, Datasheet view, and Print Preview, the control's **SourceItem** property setting is a zero-length string (`" "`), and its **SourceDoc** property setting is the full path to the linked file, followed by an exclamation point (`!`) or a backslash (`\`) and the **SourceItem** property setting, as in the following example.

```vb
"C:\Work\Qtr1\Revenue.xls!R1C1:R30C15"
```


## Example

The following example creates a linked OLE object by using an unbound object frame named **OLE1**, and sizes the control to display the object's entire contents when the user clicks a command button.


```vb
Sub Command1_Click 
 OLE1.Class = "Excel.Sheet" ' Set class name. 
 ' Specify type of object. 
 OLE1.OLETypeAllowed = acOLELinked 
 ' Specify source file. 
 OLE1.SourceDoc = "C:\Excel\Oletext.xls" 
 ' Specify data to create link to. 
 OLE1.SourceItem = "R1C1:R5C5" 
 ' Create linked object. 
 OLE1.Action = acOLECreateLink 
 ' Adjust control size. 
 OLE1.SizeMode = acOLESizeZoom 
End Sub
```




[!include[Support and feedback](~/includes/feedback-boilerplate.md)]