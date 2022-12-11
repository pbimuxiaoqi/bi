---
description: "Learn more about: VARX.S"
title: "VARX.S function (DAX) | Microsoft Docs"
ms.service: powerbi 
ms.subservice: dax 
ms.date: 07/13/2020
ms.reviewer: owend
ms.topic: reference
author: minewiskan
ms.author: owend 
recommendations: false

---
# VARX.S

Returns the variance of a sample population.  
  
## Syntax  
  
```js
VARX.S(<table>, <expression>)  
```
  
### Parameters  

|Term|Definition|  
|--------|--------------|  
|  table | Any DAX expression that returns a table of data. |  
| expression  |  Any DAX expression that returns a single scalar value, where the expression is to be evaluated multiple times (for each row/context).  |

## Return value

A number that represents the variance of a sample population.  

## Remarks  
  
- VARX.S evaluates *expression* for each row of *table* and returns the variance of *expression*; on the assumption that *table* refers to a sample of the population. If *table* represents the entire population, then you should compute the variance by using VARX.P.  
  
- VAR.S uses the following formula:  
  
    ∑(x - x̃)<sup>2</sup>/(n-1)  
  
    where x̃ is the average value of x for the sample population  
  
    and n is the population size  
  
- Blank rows are filtered out from *columnName* and not considered in the calculations.  
  
- An error is returned if *columnName* contains less than 2 non-blank rows.  
  
- [!INCLUDE [function-not-supported-in-directquery-mode](includes/function-not-supported-in-directquery-mode.md)]
  
## Example

The following example shows the formula for a calculated column that estimates the variance of the unit price per product for a sample population, when the formula is used in the Product table.  
  
```js
= VARX.S(InternetSales_USD, InternetSales_USD[UnitPrice_USD] – (InternetSales_USD[DiscountAmount_USD]/InternetSales_USD[OrderQuantity]))  
```
