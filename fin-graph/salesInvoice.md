---
title: salesInvoice resource type | Microsoft Docs
description: A sales invoice.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen

ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 02/03/2017
ms.author: solsen
---

# salesInvoice resource type

## Methods

| Method       | Return Type  |Description|
|:---------------|:--------|:----------|
|GET Sales Invoice|Sales Invoice|Get Sales Invoice object|
|POST Sales Invoice|Sales Invoice|Create Sales Invoice object|
|PATCH Sales Invoice|Sales Invoice|Update Sales Invoice object|
|DELETE Sales Invoice|none|Delete Sales Invoice object|

## Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|id|GUID|The invoice id.|
|number|string|The invoice number.|
|invoiceDate|date|The invoice Date|
|customerPurchaseOrderReference|string|The customer purchase order reference for the invoice|
|dueDate|date|The date the invoice is due.|
|customerNumber|string|The customer number for the invoice.|
|customerId|GUID|The id of the invoice customer.|
|customerName|string|The full name of the customer.|
|currencyCode|string|The currency code for the invoice.|
|status|string|The invoice status. Can be one of:  ,Draft,In Review,Open,Paid,Canceled or Corrective|
|discountAmount|numeric|The invoice discount amount|
|discountAppliedBeforeTax|boolean|Specifies whether the discount is applied before tax.|
|totalAmountExcludingTax|numeric|The total amount excluding tax.|
|totalTaxAmount|numeric|The total tax amount for the invoice.|
|totalAmountIncludingTax|numeric|The total amount for the invoice, including tax.|
|billingPostalAddress|complex|The billing postal address for the invoice.|  
|paymentTerms|string|The payment terms of the invoice.|
|shipmentMethod|string|The shipment method of the invoice.|
|salesperson|string|The salesperson code for the invoice.|
|lastModifiedDateTime|datetime|The last datetime the account was modified.|


## Relationships
None

## JSON representation

Here is a JSON representation of the resource.


```json
{
      "id": "GUID",
      "number": "String",
      "invoiceDate": "Date",
      "dueDate": "Date",
      "customerPurchaseOrderReference": "String",
      "customerId": "GUID",
      "customerNumber": "String",
      "customerName": "String",
      "currencyCode": "String",
      "status": "String",
      "discountAmount": decimal,
      "discountAppliedBeforeTax": boolean,
      "totalAmountExcludingTax": decimal,
      "totalTaxAmount": decimal,
      "totalAmountIncludingTax": decimal,
      "billingPostalAddress": {NAV.PostalAddress},
      "paymentTerms": "String",
      "shipmentMethod": "String",
      "salesperson": "String",
      "lastModifiedDateTime": "DateTime"
}

```
## See Also
[Graph Reference](graph-reference.md)  