---
title: Workbook.Signatures property (Excel)
keywords: vbaxl10.chm199237
f1_keywords:
- vbaxl10.chm199237
ms.prod: excel
api_name:
- Excel.Workbook.Signatures
ms.assetid: b45f8036-c2d7-6113-e95c-ff78ee6a1f46
ms.date: 05/29/2019
ms.localizationpriority: medium
---


# Workbook.Signatures property (Excel)

Returns the digital signatures for a workbook. Read-only.


## Syntax

_expression_.**Signatures**

_expression_ A variable that represents a **[Workbook](Excel.Workbook.md)** object.


## Remarks

To digitally sign Excel workbooks and verify other signatures in them, you will need the Microsoft CryptoAPI and a unique digital signature certificate. The CryptoAPI is installed with Microsoft Internet Explorer 4.01 or later. You can obtain a digital signature certificate from a certification authority.


## Example

```vb
Sub AddSignature() 
 ActiveWorkbook.Signatures.AddSignatureLine 
End Sub
```



[!include[Support and feedback](~/includes/feedback-boilerplate.md)]