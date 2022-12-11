---
description: "Learn more about: NOT"
title: "NOT function (DAX) | Microsoft Docs"
ms.service: powerbi 
ms.subservice: dax 
ms.date: 08/04/2020
ms.reviewer: owend
ms.topic: reference
author: minewiskan
ms.author: owend 
recommendations: false

---
# NOT

Changes FALSE to TRUE, or TRUE to FALSE.  
  
## Syntax  
  
```js
NOT(<logical>)  
```
  
### Parameters  
  
|Term|Definition|  
|--------|--------------|  
|logical|A value or expression that can be evaluated to TRUE or FALSE.|  
  
## Return value

TRUE OR FALSE.  
  
## Example

The following example retrieves values from the calculated column that was created to illustrate the IF function. For that example, the calculated column was named using the default name, **Calculated Column1**, and contains the following formula: `= IF([Orders]<300,"true","false")`  
  
The formula checks the value in the column, [Orders], and returns "true" if the number of orders is under 300.  
  
Now create a new calculated column, **Calculated Column2**, and type the following formula.  
  
```js
= NOT([CalculatedColumn1])  
```

For each row in **Calculated Column1**, the values "true" and "false" are interpreted as the logical values TRUE or FALSE, and the NOT function returns the logical opposite of that value.  
  
## See also

[TRUE function](true-function-dax.md)  
[FALSE function](false-function-dax.md)  
[IF function](if-function-dax.md)  
