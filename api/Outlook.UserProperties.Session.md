---
title: UserProperties.Session property (Outlook)
keywords: vbaol11.chm205
f1_keywords:
- vbaol11.chm205
ms.prod: outlook
api_name:
- Outlook.UserProperties.Session
ms.assetid: 0cd76318-80c6-4cfc-3aca-32e385ff6b88
ms.date: 06/08/2017
ms.localizationpriority: medium
---


# UserProperties.Session property (Outlook)

Returns the  **[NameSpace](Outlook.NameSpace.md)** object for the current session. Read-only.


## Syntax

_expression_.**Session**

_expression_ A variable that represents a [UserProperties](Outlook.UserProperties.md) object.


## Remarks

The **Session** property and the **[GetNamespace](Outlook.Application.GetNamespace.md)** method can be used interchangeably to obtain the **NameSpace** object for the current session. Both members serve the same purpose. For example, the following statements do the same function:


```vb
Set objNamespace = Application.GetNamespace("MAPI") 
```


```vb
Set objSession = Application.Session
```


## See also


[UserProperties Object](Outlook.UserProperties.md)

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]