---
description: "Learn more about: HASONEFILTER"
title: "HASONEFILTER function (DAX) | Microsoft Docs"
ms.service: powerbi 
ms.subservice: dax 
ms.date: 07/08/2020
ms.reviewer: owend
ms.topic: reference
author: minewiskan
ms.author: owend 
recommendations: false

---
# HASONEFILTER

Returns **TRUE** when the number of directly filtered values on *columnName* is one; otherwise returns **FALSE**.  
  
## Syntax  
  
```js
HASONEFILTER(<columnName>)  
```
  
### Parameters  

|Term|Definition|  
|--------|--------------|  
| columnName   |  The name of an existing column, using standard DAX syntax. It cannot be an expression.  |  
  
## Return value

**TRUE** when the number of directly filtered values on *columnName* is one; otherwise returns **FALSE**.  
  
## Remarks  
  
- This function is similar to HASONEVALUE() with the difference that HASONEVALUE() works based on cross-filters while HASONEFILTER() works by a direct filter.  

- [!INCLUDE [function-not-supported-in-directquery-mode](includes/function-not-supported-in-directquery-mode.md)]

## Example

The following example shows how to use HASONEFILTER() to return the filter for   ResellerSales_USD[ProductKey]) if there is one filter, or to return BLANK if there are no filters or more than one filter on ResellerSales_USD[ProductKey]).  
  
```js
= IF(HASONEFILTER(ResellerSales_USD[ProductKey]),FILTERS(ResellerSales_USD[ProductKey]),BLANK())  
```
