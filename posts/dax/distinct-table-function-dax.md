---
description: "Learn more about: DISTINCT (table)"
title: "DISTINCT (table) function (DAX) | Microsoft Docs"
ms.service: powerbi 
ms.subservice: dax 
ms.date: 07/05/2020
ms.reviewer: owend
ms.topic: reference
author: minewiskan
ms.author: owend 
recommendations: false

---
# DISTINCT (table)

Returns a table by removing duplicate rows from another table or expression.
  
## Syntax  
  
```js
DISTINCT(<table>)  
```
  
### Parameters  
  
|Term|Definition|  
|--------|--------------|  
|table|The table from which unique rows are to be returned. The table can also be an expression that results in a table.|  
  
## Return value

A table containing only distinct rows.  
  
## Related functions

There is another version of the DISTINCT function, [DISTINCT (column)](distinct-function-dax.md), that takes a column name as input parameter.
  
## Example  

The following query:

```js
EVALUATE DISTINCT( { (1, "A"), (2, "B"), (1, "A") } )
```

Returns table:

|[Value1]    |[Value2]  |
|---------|---------|
|1    |     A    |
|2    |     B    |

## See also

[Filter functions](filter-functions-dax.md)  
[DISTINCT (column)](distinct-function-dax.md)  
[FILTER function](filter-function-dax.md)  
[RELATED function](related-function-dax.md)  
[VALUES function](values-function-dax.md)  
