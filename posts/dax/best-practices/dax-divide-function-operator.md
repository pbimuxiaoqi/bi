---
title: "DIVIDE function vs divide operator (/) in DAX"
description: Best practices for using the DAX DIVIDE function.
author: peter-myers
ms.author: owend
ms.reviewer: owend
ms.service: powerbi 
ms.subservice: dax
ms.topic: conceptual
ms.date: 08/25/2021
recommendations: false
---

# DIVIDE function vs. divide operator (/)

As a data modeler, when you write a DAX expression to divide a numerator by a denominator, you can choose to use the [DIVIDE](../divide-function-dax.md) function or the divide operator (/ - forward slash).

When using the DIVIDE function, you must pass in numerator and denominator expressions. Optionally, you can pass in a value that represents an _alternate result_.

```dax
DIVIDE(<numerator>, <denominator> [,<alternateresult>])
```

The DIVIDE function was designed to automatically handle division by zero cases. If an alternate result is not passed in, and the denominator is zero or BLANK, the function returns BLANK. When an alternate result is passed in, it's returned instead of BLANK.

The DIVIDE function is convenient because it saves your expression from having to first test the denominator value. The function is also better optimized for testing the denominator value than the [IF](../if-function-dax.md) function. The performance gain is significant since checking for division by zero is expensive. Further using DIVIDE results in a more concise and elegant expression.

## Example

The following measure expression produces a safe division, but it involves using four DAX functions.

```dax
Profit Margin =
IF(
    OR(
        ISBLANK([Sales]),
        [Sales] == 0
    ),
    BLANK(),
    [Profit] / [Sales]
)
```

This measure expression achieves the same outcome, yet more efficiently and elegantly.

```dax
Profit Margin =
DIVIDE([Profit], [Sales])
```

## Recommendations

It's recommended that you use the DIVIDE function whenever the denominator is an expression that _could_ return zero or BLANK.

In the case that the denominator is a constant value, we recommend that you use the divide operator. In this case, the division is guaranteed to succeed, and your expression will perform better because it will avoid unnecessary testing.

Carefully consider whether the DIVIDE function should return an alternate value. For measures, it's usually a better design that they return BLANK. Returning BLANK is better because report visuals—by default—eliminate groupings when summarizations are BLANK. It allows the visual to focus attention on groups where data exists. When necessary, in Power BI, you can configure the visual to display all groups (that return values or BLANK) within the filter context by enabling the [Show items with no data](/power-bi/create-reports/desktop-show-items-no-data) option.

## See also

- Learning path: [Use DAX in Power BI Desktop](/training/paths/dax-power-bi/)
- Questions? [Try asking the Power BI Community](https://community.powerbi.com/)
- Suggestions? [Contribute ideas to improve Power BI](https://ideas.powerbi.com)
