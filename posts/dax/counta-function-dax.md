---
description: "Learn more about: COUNTA"
title: "COUNTA function (DAX) | Microsoft Docs"
ms.service: powerbi 
ms.subservice: dax 
ms.date: 06/07/2022
ms.reviewer: owend
ms.topic: reference
author: minewiskan
ms.author: owend 
recommendations: false

---
# COUNTA

Counts the number of rows in the specified column that contain non-blank values.
  
## Syntax  
  
```js
COUNTA(<column>)  
```
  
### Parameters
  
|Term|Definition|  
|--------|--------------|  
|column|The column that contains the values to be counted.|  
  
## Return value

A whole number.  
  
## Remarks  
  
- When the function does not find any rows to count, the function returns a blank.
- Unlike [COUNT](count-function-dax.md), COUNTA supports Boolean data type.

- [!INCLUDE [function-not-supported-in-directquery-mode](includes/function-not-supported-in-directquery-mode.md)]
  
## Example

The following example returns all rows in the `Reseller` table that have any kind of value in the column that stores phone numbers. 
  
```js
= COUNTA(Reseller[Phone])  
```
  
## See also

[COUNT function](count-function-dax.md)  
[COUNTAX function](countax-function-dax.md)  
[COUNTX function](countx-function-dax.md)  
[Statistical functions](statistical-functions-dax.md)  
