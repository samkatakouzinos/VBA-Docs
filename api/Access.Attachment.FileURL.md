---
title: Attachment.FileURL property (Access)
keywords: vbaac10.chm13983
f1_keywords:
- vbaac10.chm13983
ms.prod: access
api_name:
- Access.Attachment.FileURL
ms.assetid: 661ce36f-77f8-be34-845f-a3c450b878bf
ms.date: 02/07/2019
ms.localizationpriority: medium
---


# Attachment.FileURL property (Access)

Returns the Uniform Resource Locator (URL) of the specified attachment. Read-only **String**.


## Syntax

_expression_.**FileURL** (_var_)

_expression_ A variable that represents an **[Attachment](Access.Attachment.md)** object.


## Parameters

|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
| _var_|Optional|**Variant**|An expression that specifies the position of a member of the collection referred to by the _expression_ argument. If a numeric expression, the _index_ argument must be a number from 0 to the value of the collection's **Count** property minus 1. If a string expression, the _index_ argument must be the name of a member of the collection.|

## Remarks

The **FileURL** property returns an empty string if the table that contains the attachments is not linked to a SharePoint list.




[!include[Support and feedback](~/includes/feedback-boilerplate.md)]