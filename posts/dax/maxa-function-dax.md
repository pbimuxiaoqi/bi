---
description: "Learn more about: MAXA"
title: "MAXA function (DAX) | Microsoft Docs"
ms.service: powerbi 
ms.subservice: dax 
ms.date: 07/08/2020
ms.reviewer: owend
ms.topic: reference
author: minewiskan
ms.author: owend 
recommendations: false

---
# MAXA

Returns the largest value in a column.
  
## Syntax  
  
```js
MAXA(<column>)  
```
  
### Parameters
  
|Term|Definition|  
|--------|--------------|  
|column|The column in which you want to find the largest value.|  
  
## Return value

The largest value.  
  
## Remarks

- The MAXA function takes as argument a column, and looks for the largest value among the following types of values:  
  - Numbers  
  - Dates  
  
- Logical values, such as TRUE and FALSE. Rows that evaluate to TRUE count as 1; rows that evaluate to FALSE count as 0 (zero).  
  
- Empty cells are ignored. If the column contains no values that can be used, MAXA returns 0 (zero).  

- If you want to compare text values, use the MAX function.

- [!INCLUDE [function-not-supported-in-directquery-mode](includes/function-not-supported-in-directquery-mode.md)]

## Example 1

The following example returns the greatest value from a calculated column, named **ResellerMargin**, that computes the difference between list price and reseller price.  
  
```js
= MAXA([ResellerMargin])  
```
  
## Example 2

The following example returns the largest value from a column that contains dates and times. Therefore, this formula gets the most recent transaction date.  
  
```js
= MAXA([TransactionDate])  
```
  
## See also

[MAX function](max-function-dax.md)  
[MAXX function](maxx-function-dax.md)  
[Statistical functions](statistical-functions-dax.md)  
