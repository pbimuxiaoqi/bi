---
description: "Learn more about: UPPER"
title: "UPPER function (DAX) | Microsoft Docs"
ms.service: powerbi 
ms.subservice: dax 
ms.date: 07/13/2020
ms.reviewer: owend
ms.topic: reference
author: minewiskan
ms.author: owend 
recommendations: false

---
# UPPER

Converts a text string to all uppercase letters.  
  
## Syntax  
  
```js
UPPER (<text>)  
```
  
### Parameters  
  
|Term|Definition|  
|--------|--------------|  
|text|The text you want converted to uppercase, or a reference to a column that contains text.|  
  
## Return value

Same text, in uppercase.  
  
## Example

The following formula converts the string in the column, [ProductCode], to all uppercase. Non-alphabetic characters are not affected.  
  
```js
= UPPER(['New Products'[Product Code])  
```
  
## See also

[Text functions](text-functions-dax.md)  
[LOWER function](lower-function-dax.md)  
