---
title: CustomControl.Cancel property (Access)
keywords: vbaac10.chm12046
f1_keywords:
- vbaac10.chm12046
ms.prod: access
api_name:
- Access.CustomControl.Cancel
ms.assetid: 013feb6d-44e9-dbdf-0342-c07ff743f747
ms.date: 03/05/2019
ms.localizationpriority: medium
---


# CustomControl.Cancel property (Access)

Use the **Cancel** property to specify whether a command button is also the **Cancel** button on a form. Read/write **Boolean**.


## Syntax

_expression_.**Cancel**

_expression_ A variable that represents a **[CustomControl](Access.CustomControl.md)** object.


## Remarks

The **Cancel** property uses the following settings.

|Setting|Visual Basic|Description|
|:-----|:-----|:-----|
|Yes|**True**|The command button is the **Cancel** button.|
|No|**False**|(Default) The command button isn't the **Cancel** button.|

Setting the **Cancel** property to Yes makes the command button the **Cancel** button in the form. However, you must still write the macro or Visual Basic event procedure that performs whatever action or actions you want the **Cancel** button to carry out (for example, closing the form without saving any changes to it). Set the command button's **OnClick** event property to the name of the macro or event procedure.

When a command button's **Cancel** property setting is Yes and the Form window is active, the user can choose the command button by pressing Esc, by pressing Enter when the command button has the focus, or by choosing the command button.

> [!NOTE] 
> If a text box has the focus when the user presses Esc, any changes made to the data in the text box will be lost, and the original data will be restored.

When the **Cancel** property is set to Yes for one command button on a form, it is automatically set to No for all other command buttons on the form.

For a form that supports irreversible operations, such as deletions, it's a good idea to make the **Cancel** button the default command button. To do this, set both the **Cancel** property and the **Default** property to Yes.




[!include[Support and feedback](~/includes/feedback-boilerplate.md)]