---
description: "Learn more about: MOD"
title: "MOD function (DAX) | Microsoft Docs"
ms.service: powerbi 
ms.subservice: dax 
ms.date: 12/10/2018
ms.reviewer: owend
ms.topic: reference
author: minewiskan
ms.author: owend 
recommendations: false

---
# MOD

Returns the remainder after a number is divided by a divisor. The result always has the same sign as the divisor.  
  
## Syntax  
  
```js
MOD(<number>, <divisor>)  
```
  
### Parameters  
  
|Term|Definition|  
|--------|--------------|  
|number|The number for which you want to find the remainder after the division is performed.|  
|divisor|The number by which you want to divide.|  
  
## Return value

A whole number.  
  
## Remarks

- If the divisor is 0 (zero), MOD returns an error. You cannot divide by 0.  
  
- The MOD function can be expressed in terms of the INT function: MOD(n, d) = n - d*INT(n/d)  
  
## Example 1

The following formula returns 1, the remainder of 3 divided by 2.  
  
```js
= MOD(3,2)  
```
  
## Example 2

The following formula returns -1, the remainder of 3 divided by 2. Note that the sign is always the same as the sign of the divisor.  
  
```js
= MOD(-3,-2)  
```
  
## See also

[Math and Trig functions](math-and-trig-functions-dax.md)  
[ROUND function](round-function-dax.md)  
[ROUNDUP function](roundup-function-dax.md)  
[ROUNDDOWN function](rounddown-function-dax.md)  
[MROUND function](mround-function-dax.md)  
[INT function](int-function-dax.md)  
