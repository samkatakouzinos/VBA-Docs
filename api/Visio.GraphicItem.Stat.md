---
title: GraphicItem.Stat property (Visio)
keywords: vis_sdr.chm16914420
f1_keywords:
- vis_sdr.chm16914420
ms.prod: visio
api_name:
- Visio.GraphicItem.Stat
ms.assetid: 1136700d-35f6-3d8a-4d65-bbf39ec943ab
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# GraphicItem.Stat property (Visio)

Returns status information for an object. Read-only.


> [!NOTE] 
> This Visio object or member is available only to licensed users of Visio Professional 2013.


## Syntax

_expression_.**Stat**

_expression_ A variable that represents a **[GraphicItem](Visio.GraphicItem.md)** object.


## Return value

Integer


## Remarks

If an object is a reference to an entity in a document, and if that document closes, the **Stat** property returns a value in which the **visStatClosed** bit is set.

If an object is a reference to an entity that has been deleted, the **Stat** property returns a value in which the **visStatDeleted** bit is set.

A Component Object Model (COM) object, such as a Microsoft Visio **Document** object, lives as long as it is held (pointed to) by a client, even if the object is logically in a deleted or closed state.

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]