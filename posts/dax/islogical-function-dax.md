---
description: "Learn more about: ISLOGICAL"
title: "ISLOGICAL function (DAX) | Microsoft Docs"
ms.service: powerbi 
ms.subservice: dax 
ms.date: 07/08/2020
ms.reviewer: owend
ms.topic: reference
author: minewiskan
ms.author: owend 
recommendations: false

---
# ISLOGICAL

Checks whether a value is a logical value, (TRUE or FALSE), and returns TRUE or FALSE.  
  
## Syntax  
  
```js
ISLOGICAL(<value>)  
```
  
### Parameters  
  
|Term|Definition|  
|--------|--------------|  
|value|The value that you want to test.|  
  
## Return value

TRUE if the value is a logical value; FALSE if any value other than TRUE OR FALSE.  

## Remarks

[!INCLUDE [function-not-supported-in-directquery-mode](includes/function-not-supported-in-directquery-mode.md)]

## Example

The following three samples show the behavior of ISLOGICAL.  
  
```js
//RETURNS: Is Boolean type or Logical  
= IF(ISLOGICAL(true), "Is Boolean type or Logical", "Is different type")  
  
//RETURNS: Is Boolean type or Logical  
= IF(ISLOGICAL(false), "Is Boolean type or Logical", "Is different type")  
  
//RETURNS: Is different type  
= IF(ISLOGICAL(25), "Is Boolean type or Logical", "Is different type")  
```
  
## See also

[Information functions](information-functions-dax.md)  
