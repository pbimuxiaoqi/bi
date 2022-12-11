---
description: "Learn more about: ROW function"
title: "ROW function (DAX) | Microsoft Docs"
ms.service: powerbi 
ms.subservice: dax 
ms.date: 07/10/2020
ms.reviewer: owend
ms.topic: reference
author: minewiskan
ms.author: owend 
recommendations: false

---
# ROW function

Returns a table with a single row containing values that result from the expressions given to each column.  
  
## Syntax  
  
```js
ROW(<name>, <expression>[[,<name>, <expression>]…])  
```
  
### Parameters  

|Term|Definition|  
|--------|--------------|  
|  name|  The name given to the column, enclosed in double quotes. |  
|  expression| Any DAX expression that returns a single scalar value to populate. *name*.  |

## Return value

A single row table  
  
## Remarks

- Arguments must always come in pairs of *name* and *expression*.

- [!INCLUDE [function-not-supported-in-directquery-mode](includes/function-not-supported-in-directquery-mode.md)]  
  
## Example

The following example returns a single row table with the total sales for internet and resellers channels.  
  
```js
ROW("Internet Total Sales (USD)", SUM(InternetSales_USD[SalesAmount_USD]),  
         "Resellers Total Sales (USD)", SUM(ResellerSales_USD[SalesAmount_USD]))  
```
