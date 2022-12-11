---
description: "Learn more about: USERNAME"
title: "USERNAME function (DAX) | Microsoft Docs"
ms.service: powerbi 
ms.subservice: dax 
ms.date: 07/13/2020
ms.reviewer: owend
ms.topic: reference
author: minewiskan
ms.author: owend 
recommendations: false

---
# USERNAME

Returns the domain name and username from the credentials given to the system at connection time.  
  
## Syntax  
  
```js
USERNAME()  
```
  
### Parameters  

This expression has no parameters.
  
## Return value

The username from the credentials given to the system at connection time  
  
## Example

The following formula verifies if the user login is part of the UsersTable.  
  
```js
= IF(CONTAINS(UsersTable,UsersTable[login], USERNAME()), "Allowed", BLANK())  
```
