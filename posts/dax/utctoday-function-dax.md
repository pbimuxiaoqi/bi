---
description: "Learn more about: UTCTODAY"
title: "UTCTODAY function (DAX) | Microsoft Docs"
ms.service: powerbi 
ms.subservice: dax 
ms.date: 01/06/2021
ms.reviewer: owend
ms.topic: reference
author: minewiskan
ms.author: owend 
recommendations: false

---
# UTCTODAY

Returns the current UTC date.

## Syntax  
  
```js
UTCTODAY()  
```
  
## Return value

A date.  
  
## Remarks  

- UTCTODAY returns the time value 12:00:00 PM for all dates.

- The UTCNOW function is similar but returns the exact time and date.
  
## Example

The following:
  
```js
EVALUATE { FORMAT(UTCTODAY(), "General Date") }
```

Returns:

|[Value]  |
|---------|
|2/2/2018    |

## See also

[NOW function](now-function-dax.md)  
[UTCNOW function](utcnow-function-dax.md)  
