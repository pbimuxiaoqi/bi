---
description: "Learn more about: ISNUMBER"
title: "ISNUMBER function (DAX) | Microsoft Docs"
ms.service: powerbi 
ms.subservice: dax 
ms.date: 12/10/2018
ms.reviewer: owend
ms.topic: reference
author: minewiskan
ms.author: owend 
recommendations: false

---
# ISNUMBER

Checks whether a value is a number, and returns TRUE or FALSE.  
  
## Syntax  
  
```js
ISNUMBER(<value>)  
```
  
### Parameters  
  
|Term|Definition|  
|--------|--------------|  
|value|The value you want to test.|  
  
## Return value

TRUE if the value is numeric; otherwise FALSE.  

## Remarks

[!INCLUDE [function-not-supported-in-directquery-mode](includes/function-not-supported-in-directquery-mode.md)]

## Example

The following three samples show the behavior of ISNUMBER.  
  
```js
//RETURNS: Is number  
= IF(ISNUMBER(0), "Is number", "Is Not number")  
  
//RETURNS: Is number  
= IF(ISNUMBER(3.1E-1),"Is number", "Is Not number")  
  
//RETURNS: Is Not number  
= IF(ISNUMBER("123"), "Is number", "Is Not number")  
```
  
## See also

[Information functions](information-functions-dax.md)  
