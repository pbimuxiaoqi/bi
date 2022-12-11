---
description: "Learn more about: NORM.DIST"
title: "NORM.DIST function (DAX) | Microsoft Docs"
ms.service: powerbi 
ms.subservice: dax 
ms.date: 07/08/2020
ms.reviewer: owend
ms.topic: reference
author: minewiskan
ms.author: owend 
recommendations: false

---
# NORM.DIST

Returns the normal distribution for the specified mean and standard deviation. 

## Syntax  
  
```js
NORM.DIST(X, Mean, Standard_dev, Cumulative)  
```
  
### Parameters  
  
|Term|Definition|  
|--------|--------------|  
|X|The value for which you want the distribution.|  
|Mean |The arithmetic mean of the distribution.|
|Standard_dev|The standard deviation of the distribution.|
|Cumulative*|A logical value that determines the form of the function. If cumulative is TRUE, NORM.DIST returns the cumulative distribution function; if FALSE, it returns the probability density function.|
  
## Return value

The normal distribution for the specified mean and standard deviation.  

## Remarks

[!INCLUDE [function-not-supported-in-directquery-mode](includes/function-not-supported-in-directquery-mode.md)]

## Example  
  
```js
EVALUATE { NORM.DIST(42, 40, 1.5, TRUE) }
```

Returns

|[Value]  |
|---------|
|0.908788780274132     |


## See also  

[NORM.S.DIST function](norm-s-dist-dax.md)  
[NORM.INV function](norm-inv-dax.md)  
[NORM.S.INV](norm-s-inv-dax.md)  
