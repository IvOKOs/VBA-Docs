---
title: Report.CloseButton property (Access)
keywords: vbaac10.chm13803
f1_keywords:
- vbaac10.chm13803
ms.prod: access
api_name:
- Access.Report.CloseButton
ms.assetid: dad15f66-4787-a4eb-dbbe-d698faaa0917
ms.date: 03/15/2019
ms.localizationpriority: medium
---


# Report.CloseButton property (Access)

Specifies whether the **Close** button on a form is enabled. Read/write **Boolean**.


## Syntax

_expression_.**CloseButton**

_expression_ A variable that represents a **[Report](Access.Report.md)** object.


## Remarks

The **CloseButton** property uses the following settings.

|Setting|Visual Basic|Description|
|:-----|:-----|:-----|
|Yes|**True**|(Default) The **Close** button is enabled.|
|No|**False**|The **Close** button is disabled, and the **Close** command isn't available on the **Control** menu.|

You can set the **CloseButton** property only in form Design view.

If you set the **CloseButton** property to No, the **Close** button remains visible but appears dimmed (grayed), and you must provide some other way to close the form; for example, a command button or custom menu command that runs a macro or event procedure that closes the form.

You can also close the form by pressing Alt+F4.




[!include[Support and feedback](~/includes/feedback-boilerplate.md)]