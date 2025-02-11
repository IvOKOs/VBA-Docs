---
title: OLEDBConnection.RobustConnect property (Excel)
keywords: vbaxl10.chm794088
f1_keywords:
- vbaxl10.chm794088
ms.prod: excel
api_name:
- Excel.OLEDBConnection.RobustConnect
ms.assetid: 47ca146c-54ba-b2d5-6d16-15571daf08f3
ms.date: 05/02/2019
ms.localizationpriority: medium
---


# OLEDBConnection.RobustConnect property (Excel)

Returns or sets how an OLE DB connection connects to its data source. Read/write **[XlRobustConnect](Excel.XlRobustConnect.md)**.


## Syntax

_expression_.**RobustConnect**

_expression_ A variable that represents an **[OLEDBConnection](Excel.OLEDBConnection.md)** object.


## Remarks

If you use robust connectivity, when Microsoft Excel is unable to establish a connection by using the workbook connection information, Excel will check if the workbook connection has a path to an external connection file. If it does, Excel will open the external connection file and try to connect by using the information contained in the external connection file. If a connection can be established after using the external connection file, Excel will then update the workbook's connection object. 

This provides robust connectivity in scenarios where an information technology department maintains and updates connections in a central place, permitting a user's workbook to automatically fetch those updates whenever the previous version of the connection (cached within the workbook) fails. 

> [!NOTE] 
> Robust connectivity isn't secure. If you create a connection on your computer and use it in a workbook and then send someone the workbook, that person will be able to see the path to the connection file on your computer. It is a good idea to remove the connection file information from the workbook before you send the workbook to someone else.



[!include[Support and feedback](~/includes/feedback-boilerplate.md)]