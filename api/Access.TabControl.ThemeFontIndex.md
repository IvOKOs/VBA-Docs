---
title: TabControl.ThemeFontIndex property (Access)
keywords: vbaac10.chm14610
f1_keywords:
- vbaac10.chm14610
ms.prod: access
api_name:
- Access.TabControl.ThemeFontIndex
ms.assetid: b3de7b94-dd76-82ee-dfe5-7c2b7e956a34
ms.date: 03/02/2019
ms.localizationpriority: medium
---


# TabControl.ThemeFontIndex property (Access)

Gets or sets the font index that represents a font in the applied theme associated with the **FontName** property of the specified object. Read/write **Long**.


## Syntax

_expression_.**ThemeFontIndex**

_expression_ A variable that represents a **[TabControl](Access.TabControl.md)** object.


## Remarks

The **ThemeFontIndex** property uses one of the values listed in the following table.

|Value|Description|
|:-----|:-----|
|0|Header font|
|1 (Default)|Detail font|

If no theme is applied, the **ThemeFontIndex** property contains -1.

This property is not surfaced in the property sheet.



[!include[Support and feedback](~/includes/feedback-boilerplate.md)]