---
title: View.Save method (Outlook)
keywords: vbaol11.chm2488
f1_keywords:
- vbaol11.chm2488
ms.prod: outlook
api_name:
- Outlook.View.Save
ms.assetid: effc4046-2e9c-3898-e37f-c4de817ddde7
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# View.Save method (Outlook)

Saves the view, or saves the changes to a view.


## Syntax

_expression_.**Save**

_expression_ A variable that represents a [View](Outlook.View.md) object.


## Remarks

Always use  **Save** to save a view after you change any property of the view.


## Example

The following VBA example creates a new view called New Table and applies it.


```vb
Sub CreateView() 
 
 'Creates a new view 
 
 Dim objName As Outlook.NameSpace 
 
 Dim objViews As Outlook.Views 
 
 Dim objNewView As Outlook.View 
 
 
 
 Set objName = Application.GetNamespace("MAPI") 
 
 Set objViews = objName.GetDefaultFolder(olFolderInbox).Views 
 
 Set objNewView = objViews.Add(Name:="New Table", _ 
 
 ViewType:=olTableView) 
 
 objNewView.Save 
 
 objNewView.Apply 
 
End Sub
```


## See also


[View Object](Outlook.View.md)

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]