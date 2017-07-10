---
title: "AsToken Method"
ms.author: solsen
ms.custom: na
ms.date: 06/29/2017
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.prod: "dynamics-nav-2017"
ms.assetid: 620f0e32-eadc-43e9-8f6e-8fc0b12c3aaf
caps.latest.revision: 9
manager: edupont
author: SusanneWindfeldPedersen
---

[!INCLUDE[newdev_dev_preview](../includes/newdev_dev_preview.md)]

# AsToken Method
Converts the value in a JsonArray to a JsonToken data type.

```
JsonToken := JsonArray.AsToken
```

### Parameters
*JsonArray*   
&emsp;Type: JsonArray

## Return Value
*JsonToken*  
Type: JsonToken

## Remarks
The returned JsonToken contains the same data as the JsonArray, but allows for treating the data in a generic manner.

## See Also
[Getting Started](../devenv-get-started.md)  
[Developing Extensions](../devenv-dev-overview.md)