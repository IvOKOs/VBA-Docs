---
title: DataLabels.AutoText property (Excel)
keywords: vbaxl10.chm584092
f1_keywords:
- vbaxl10.chm584092
ms.prod: excel
api_name:
- Excel.DataLabels.AutoText
ms.assetid: 3155a424-b25d-8f0c-f252-d371203f52fa
ms.date: 04/23/2019
ms.localizationpriority: medium
---


# DataLabels.AutoText property (Excel)

**True** if the object automatically generates appropriate text based on context. Read/write **Boolean**.


## Syntax

_expression_.**AutoText**

_expression_ A variable that represents a **[DataLabels](Excel.DataLabels(object).md)** object.


## Example

This example sets the data labels for series one on Chart1 to automatically generate appropriate text.

```vb
Charts("Chart1").SeriesCollection(1).DataLabels.AutoText = True
```

> [!NOTE] 
> If you run `ActiveChart.SeriesCollection(1).DataLabels.AutoText` in the Immediate window, you will receive the following:
> - Excel 2003: Returns nothing.
> - Excel 2007 and later: Returns **True** only when all **DataLabels** have **AutoText** = **True**, returns **False** if all **DataLabels** have **AutoText** = **False** or some **DataLabels** have **AutoText** = **False**.




[!include[Support and feedback](~/includes/feedback-boilerplate.md)]