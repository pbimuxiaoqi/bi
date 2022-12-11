---
description: "Learn more about: COT"
title: "COT function (DAX) | Microsoft Docs"
ms.service: powerbi 
ms.subservice: dax 
ms.date: 07/05/2020
ms.reviewer: owend
ms.topic: reference
author: minewiskan
ms.author: owend 
recommendations: false

---
# COT

Returns the cotangent of an angle specified in radians.  
  
## Syntax  
  
```js
COT (<number>)
```
  
### Parameters
  
|Term|Definition|  
|--------|--------------|  
|number|The angle in radians for which you want the cotangent.|  
  
## Return value

The cotangent of the given angle.  
  
## Remarks

- The absolute value of number must be less than 2^27 and cannot be 0.

- If number is outside its constraints, an error is returned.

- If number is a non-numeric value, an error is returned.

## Example  
  
The following DAX query,
  
```js
EVALUATE { COT(30) }
```

Returns

|[Value] |
|---------|
|-0.156119952161659    |
