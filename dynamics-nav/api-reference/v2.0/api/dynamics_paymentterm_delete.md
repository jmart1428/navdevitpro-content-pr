---
title: DELETE paymentTerms | Microsoft Docs
description: Deletes paymentTerm  in Dynamics 365 Business Central.
author: SusanneWindfeldPedersen
ms.service: "dynamics365-business-central"
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: solsen
---

# Delete paymentTerms
Delete a payment terms object from [!INCLUDE[d365fin_long_md](../../includes/d365fin_long_md.md)].

## HTTP request
Replace the URL prefix for [!INCLUDE[d365fin_long_md](../../includes/d365fin_long_md.md)] depending on environment following the [guideline](../../v2.0/endpoints-apis-for-dynamics.md).
```
DELETE businesscentralPrefix/companies({id})/paymentTerms({id})
```

## Request headers

|Header         |Value                     |
|---------------|--------------------------|
|Authorization  |Bearer {token}. Required. |
|If-Match       |Required. When this request header is included and the eTag provided does not match the current tag on the **paymentTerms**, the **paymentTerms** will not be updated. |

## Request body
Do not supply a request body for this method.

## Response
If successful, this method returns ```204 No Content``` response code. It does not return anything in the response body.

## Example

**Request**

Here is an example of the request.

```json
DELETE https://{businesscentralPrefix}/api/v2.0/companies({id})/paymentTerms({id})
```

**Response** 

Here is an example of the response. 

```json
HTTP/1.1 204 No Content
```


## See also
[Tips for working with the APIs](/dynamics365/business-central/dev-itpro/developer/devenv-connect-apps-tips)    
[paymentterm](../resources/dynamics_paymentterm.md)    
[Get paymentterm](../api/dynamics_paymentterm_Get.md)    
[Create paymentterm](../api/dynamics_paymentterm_Create.md)    
[Update paymentterm](../api/dynamics_paymentterm_Update.md)    