---
description: "Learn more about: ODD"
title: "ODD function (DAX) | Microsoft Docs"
ms.service: powerbi 
ms.subservice: dax 
ms.date: 08/04/2020
ms.reviewer: owend
ms.topic: reference
author: minewiskan
ms.author: owend 
recommendations: false

---
# ODD

Returns number rounded up to the nearest odd integer.  
  
## Syntax  
  
```js
ODD(number)  
```
  
### Parameters  
  
|Term|Definition|  
|--------|--------------|  
|number|Required. The value to round.|  
  
## Return value

Returns number rounded up to the nearest odd integer.  
  
## Remarks

- If number is nonnumeric, ODD returns the #VALUE! error value.  
  
- Regardless of the sign of number, a value is rounded up when adjusted away from zero. If number is an odd integer, no rounding occurs.  

- [!INCLUDE [function-not-supported-in-directquery-mode](includes/function-not-supported-in-directquery-mode.md)]

## Example  
  
|Formula|Description|Result|  
|-----------|---------------|----------|  
|= ODD(1.5)|Rounds 1.5 up to the nearest odd integer.|3|  
|= ODD(3)|Rounds 3 up to the nearest odd integer.|3|  
|= ODD(2)|Rounds 2 up to the nearest odd integer.|3|  
|= ODD(-1)|Rounds -1 up to the nearest odd integer.|-1|  
|= ODD(-2)|Rounds -2 up (away from 0) to the nearest odd integer.|-3|  
