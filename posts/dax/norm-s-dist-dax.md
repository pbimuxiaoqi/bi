---
description: "Learn more about: NORM.S.DIST"
title: "NORM.S.DIST function (DAX) | Microsoft Docs"
ms.service: powerbi 
ms.subservice: dax 
ms.date: 07/08/2020
ms.reviewer: owend
ms.topic: reference
author: minewiskan
ms.author: owend 
recommendations: false

---
# NORM.S.DIST

Returns the standard normal distribution (has a mean of zero and a standard deviation of one).

## Syntax  
  
```js
NORM.S.DIST(Z, Cumulative)
```
  
### Parameters  
  
|Term|Definition|  
|--------|--------------|  
|Z|The value for which you want the distribution.|  
|Cumulative|Cumulative is a logical value that determines the form of the function. If cumulative is TRUE, NORM.S.DIST returns the cumulative distribution function; if FALSE, it returns the probability density function.|
  
## Return value

The standard normal distribution (has a mean of zero and a standard deviation of one.

## Remarks

[!INCLUDE [function-not-supported-in-directquery-mode](includes/function-not-supported-in-directquery-mode.md)]

## Example  
  
```js
EVALUATE { NORM.S.DIST(1.333333, TRUE) }
```

Returns

|[Value]  |
|---------|
|0.908788725604095    |

## See also  

[NORM.INV function](norm-inv-dax.md)  
[NORM.DIST function](norm-dist-dax.md)  
[NORM.S.INV](norm-s-inv-dax.md)  
