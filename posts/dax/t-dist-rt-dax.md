---
description: "Learn more about: T.DIST.RT"
title: "T.DIST.RT function (DAX) | Microsoft Docs"
ms.service: powerbi 
ms.subservice: dax 
ms.date: 07/10/2020
ms.reviewer: owend
ms.topic: reference
author: minewiskan
ms.author: owend 
recommendations: false

---
# T.DIST.RT

Returns the right-tailed Student's t-distribution.

## Syntax  
  
```js
T.DIST.RT(X,Deg_freedom)
```
  
### Parameters  
  
|Term|Definition|  
|--------|--------------|  
|X|The numeric value at which to evaluate the distribution.|  
|Deg_freedom |An integer indicating the number of degrees of freedom.|
  
## Return value

The right-tailed Student's t-distribution.

## Remarks

[!INCLUDE [function-not-supported-in-directquery-mode](includes/function-not-supported-in-directquery-mode.md)]

## Example  
  
```js
EVALUATE { T.DIST.RT(1.959999998, 60) }
```

Returns

|[Value]  |
|---------|
|0.0273224649879605     |

## See also  

[T.DIST](t-dist-dax.md)  
[T.DIST.2T](t-dist-2t-dax.md)  
[T.INV](t-inv-dax.md)  
[T.INV.2t](t-inv-2t-dax.md)  
