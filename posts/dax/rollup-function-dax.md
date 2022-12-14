---
description: "Learn more about: ROLLUP"
title: "ROLLUP function (DAX) | Microsoft Docs"
ms.service: powerbi 
ms.subservice: dax 
ms.date: 09/01/2020
ms.reviewer: owend
ms.topic: reference
author: minewiskan
ms.author: owend 
recommendations: false

---
# ROLLUP

Modifies the behavior of the [SUMMARIZE](summarize-function-dax.md) function by adding rollup rows to the result on columns defined by the groupBy_columnName parameter. This function can only be used within a [SUMMARIZE](summarize-function-dax.md) expression.
  
## Syntax

```js
ROLLUP ( <groupBy_columnName> [, <groupBy_columnName> [, … ] ] )
```

With SUMMARIZE,

```js
SUMMARIZE(<table>, <groupBy_columnName>[, <groupBy_columnName>]…[, ROLLUP(<groupBy_columnName>[,< groupBy_columnName>…])][, <name>, <expression>]…)  
```
  
### Parameters  

|Term|Definition|  
|--------|--------------|  
| groupBy_columnName | The qualified name of an existing column or ROLLUPGROUP function to be used to create summary groups based on the values found in it. This parameter cannot be an expression.  |

## Return value

This function does not return a value. It only specifies the set of columns to be subtotaled.
  
## Remarks  
  
This function can only be used within a [SUMMARIZE](summarize-function-dax.md) expression.

## Example

See [SUMMARIZE](summarize-function-dax.md).
