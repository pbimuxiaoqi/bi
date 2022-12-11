---
description: "Learn more about: EXACT"
title: "EXACT function (DAX) | Microsoft Docs"
ms.service: powerbi 
ms.subservice: dax 
ms.date: 03/16/2022
ms.reviewer: owend
ms.topic: reference
author: minewiskan
ms.author: owend 
recommendations: false

---
# EXACT

Compares two text strings and returns TRUE if they are exactly the same, otherwise returns FALSE. EXACT is case-sensitive but ignores formatting differences. EXACT is case-sensitive
  
## Syntax  
  
```js
EXACT(<text1>,<text2>)  
```
  
### Parameters  
  
|Term|Definition|  
|--------|--------------|  
|text1|The first text string or column that contains text.|  
|text2|The second text string or column that contains text.|  
  
## Return value

True or False. (Boolean)  
  
## Example

The following formula used in a calculated column in the Product table checks the value of Product for the current row against the value of Model for the current row, and returns True if they are the same, and returns False if they are different.  

[!INCLUDE [power-bi-dax-sample-model](includes/power-bi-dax-sample-model.md)]

```js
= EXACT([Product], [Model])  
```
  
## See also

[Text functions](text-functions-dax.md)  
