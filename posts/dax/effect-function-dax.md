---
description: "Learn more about: EFFECT"
title: "EFFECT function (DAX) | Microsoft Docs"
ms.service: powerbi 
ms.subservice: dax
ms.date: 07/02/2020
ms.reviewer: owend
ms.topic: reference
author: jajin7
ms.author: owend 
recommendations: false

---

# EFFECT

Returns the effective annual interest rate, given the nominal annual interest rate and the number of compounding periods per year.

## Syntax

```js
EFFECT(<nominal_rate>, <npery>)
```

### Parameters

|Term|Definition|  
|--------|--------------|  
|nominal_rate|The nominal interest rate.|
|npery|The number of compounding periods per year.|

## Return Value

The effective annual interest rate.

## Remarks

- EFFECT is calculated as follows:

    $$\text{EFFECT} = \bigg( 1 + \frac{\text{nominal\_rate}}{\text{npery}} \bigg)^{\text{npery}} - 1$$

- npery is rounded to the nearest integer.

- An error is returned if:
  - nominal_rate ≤ 0.
  - npery < 1.

- [!INCLUDE [function-not-supported-in-directquery-mode](includes/function-not-supported-in-directquery-mode.md)]

## Example

| **Data** | **Description**                        |
| -------- | -------------------------------------- |
| 5.25%    | Nominal interest rate                  |
| 4        | Number of compounding periods per year |

The following DAX query:

```js
EVALUATE
{
  EFFECT(0.0525, 4)
}
```

Returns the effective interest rate using the terms specified above.

| **[Value]**      |
| ------------------ |
| 0.0535426673707584 |
