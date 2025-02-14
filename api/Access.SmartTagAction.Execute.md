---
title: SmartTagAction.Execute method (Access)
keywords: vbaac10.chm13293
f1_keywords:
- vbaac10.chm13293
ms.prod: access
api_name:
- Access.SmartTagAction.Execute
ms.assetid: 0cc72e04-22aa-2d1c-707b-6b61868448ac
ms.date: 03/26/2019
ms.localizationpriority: medium
---


# SmartTagAction.Execute method (Access)

The **Execute** method performs the specified smart tag action.


## Syntax

_expression_.**Execute**

_expression_ A variable that represents a **[SmartTagAction](Access.SmartTagAction.md)** object.


## Remarks

Smart tag actions are processes that are programmed into smart tags that allow users to perform certain functions related to the smart tag. For example, one action for a smart tag might be to access a website, while another action inserts contact information from Microsoft Outlook, while yet another action displays a map and driving directions.

Calling the **Execute** method results in a run-time error if the smart tag is:

- Located on a report.
- Located on a form in Design view, PivotTable view, or PivotChart view.
    


[!include[Support and feedback](~/includes/feedback-boilerplate.md)]