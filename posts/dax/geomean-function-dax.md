---
description: "Learn more about: GEOMEAN"
title: "GEOMEAN function (DAX) | Microsoft Docs"
ms.service: powerbi 
ms.subservice: dax 
ms.date: 07/08/2020
ms.reviewer: owend
ms.topic: reference
author: minewiskan
ms.author: owend 
recommendations: false

---
# GEOMEAN
  
Returns the geometric mean of the numbers in a column.  
  
To return the geometric mean of an expression evaluated for each row in a table, use [GEOMEANX function](geomeanx-function-dax.md).  
  
## Syntax  
  
```js
GEOMEAN(<column>)  
```
  
### Parameters  
  
|Term|Definition|  
|--------|--------------|  
|column|The column that contains the numbers for which the geometric mean is to be computed.|  
  
## Return value

A decimal number.  
  
## Remarks

- Only the numbers in the column are counted. Blanks, logical values, and text are ignored.  
  
- GEOMEAN( Table[Column] ) is equivalent to GEOMEANX( Table, Table[Column] )  

- [!INCLUDE [function-not-supported-in-directquery-mode](includes/function-not-supported-in-directquery-mode.md)]

## Example

The following computes the geometric mean of the Return column in the Investment table:  
  
```js
= GEOMEAN( Investment[Return] )  
```
  
## See also

[GEOMEANX function](geomeanx-function-dax.md)  
