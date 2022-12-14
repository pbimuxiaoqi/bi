---
description: "Learn more about: LN"
title: "LN function (DAX) | Microsoft Docs"
ms.service: powerbi 
ms.subservice: dax 
ms.date: 07/08/2020
ms.reviewer: owend
ms.topic: reference
author: minewiskan
ms.author: owend 
recommendations: false

---
# LN

Returns the natural logarithm of a number. Natural logarithms are based on the constant e (2.71828182845904).  
  
## Syntax  
  
```js
LN(<number>)  
```
  
### Parameters  
  
|Term|Definition|  
|--------|--------------|  
|number|The positive number for which you want the natural logarithm.|  
  
## Return value

A decimal number.  
  
## Remarks

LN is the inverse of the EXP function.  
  
## Example

The following example returns the natural logarithm of the number in the column, `[Values]`.  
  
```js
= LN([Values])  
```
  
## See also

[Math and Trig functions](math-and-trig-functions-dax.md)  
[EXP function](exp-function-dax.md)  
