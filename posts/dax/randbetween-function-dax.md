---
description: "Learn more about: RANDBETWEEN"
title: "RANDBETWEEN function (DAX) | Microsoft Docs"
ms.service: powerbi 
ms.subservice: dax 
ms.date: 07/10/2020
ms.reviewer: owend
ms.topic: reference
author: minewiskan
ms.author: owend 
recommendations: false

---
# RANDBETWEEN

Returns a random number in the range between two numbers you specify.  
  
## Syntax  
  
```dax
RANDBETWEEN(<bottom>,<top>)  
```
  
### Parameters  
  
|Term|Definition|  
|--------|--------------|  
|Bottom|The smallest integer the function will return.|  
|Top|The largest integer the function will return.|  
  
## Return value

A whole number.  
  
## Remarks

[!INCLUDE [function-not-supported-in-directquery-mode](includes/function-not-supported-in-directquery-mode.md)]
  
## Example

The following formula returns a random number between 1 and 10.  
  
```dax
= RANDBETWEEN(1,10)  
```
  
## See also

[Math and Trig functions](math-and-trig-functions-dax.md)  
[Statistical functions](statistical-functions-dax.md)  
