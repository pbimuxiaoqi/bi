---
description: "Learn more about: SUMX"
title: "SUMX function (DAX) | Microsoft Docs"
ms.service: powerbi 
ms.subservice: dax 
ms.date: 06/07/2022
ms.reviewer: owend
ms.topic: reference
author: minewiskan
ms.author: owend 
recommendations: false

---
# SUMX

Returns the sum of an expression evaluated for each row in a table.  
  
## Syntax  
  
```js
SUMX(<table>, <expression>)  
```
  
### Parameters  
  
|Term|Definition|  
|--------|--------------|  
|table|The table containing the rows for which the expression will be evaluated.|  
|expression|The expression to be evaluated for each row of the table.|  
  
## Return value

A decimal number.  
  
## Remarks

- The SUMX function takes as its first argument a table, or an expression that returns a table. The second argument is a column that contains the numbers you want to sum, or an expression that evaluates to a column.  
  
- Only the numbers in the column are counted. Blanks, logical values, and text are ignored.  
  
- For more complex examples of SUMX in formulas, see [ALL](all-function-dax.md) and [CALCULATETABLE](calculatetable-function-dax.md).  

- [!INCLUDE [function-not-supported-in-directquery-mode](includes/function-not-supported-in-directquery-mode.md)]

## Example

The following example first filters the table, InternetSales, on the expression, 'InternetSales[SalesTerritoryID] = 5`, and then returns the sum of all values in the Freight column. In other words, the expression returns the sum of freight charges for only the specified sales area.  
  
```js
= SUMX(FILTER(InternetSales, InternetSales[SalesTerritoryID]=5),[Freight])  
```

If you do not need to filter the column, use the SUM function. The SUM function is similar to the Excel function of the same name, except that it takes a column as a reference.  
  
## See also

[SUM](sum-function-dax.md)  
[Statistical functions](statistical-functions-dax.md)  