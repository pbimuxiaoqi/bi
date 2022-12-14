---
description: "Learn more about: REPT"
title: "REPT function (DAX) | Microsoft Docs"
ms.service: powerbi 
ms.subservice: dax 
ms.date: 07/10/2020
ms.reviewer: owend
ms.topic: reference
author: minewiskan
ms.author: owend 
recommendations: false

---
# REPT

Repeats text a given number of times. Use REPT to fill a cell with a number of instances of a text string.  
  
## Syntax  
  
```js
REPT(<text>, <num_times>)  
```
  
### Parameters  
  
|Term|Definition|  
|--------|--------------|  
|text|The text you want to repeat.|  
|num_times|A positive number specifying the number of times to repeat text.|  
  
## Return value

A string containing the changes.  
  
## Remarks

- If **number_times** is 0 (zero), REPT returns a blank.  
  
- If **number_times** is not an integer, it is truncated.  
  
- The result of the REPT function cannot be longer than 32,767 characters, or REPT returns an error.  

## Example: Repeating Literal Strings  

The following example returns the string, 85, repeated three times.  
  
```js
= REPT("85",3)  
```
  
## Example: Repeating Column Values  
  
The following example returns the string in the column, [MyText], repeated for the number of times in the column, [MyNumber]. Because the formula extends for the entire column, the resulting string depends on the text and number value in each row.  
  
```js
= REPT([MyText],[MyNumber])  
```
  
|MyText|MyNumber|CalculatedColumn1|  
|----------|------------|---------------------|  
|Text|2|TextText|  
|Number|0||  
|85|3|858585|  
  
## See also

[Text functions](text-functions-dax.md)  
