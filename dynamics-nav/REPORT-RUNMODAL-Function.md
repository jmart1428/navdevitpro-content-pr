---
title: "REPORT.RUNMODAL Function"
description: REPORT.RUNMODAL Function
ms.custom: na
ms.date: 06/05/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.prod: "dynamics-nav-2018"
ms.assetid: 0a1ffa1a-8b23-4ea4-9bd7-d7ea523b6e3a
caps.latest.revision: 16
manager: edupont
---
# REPORT.RUNMODAL Function
Loads and runs the report that you specify. The report is run modally.  
  
## Syntax  
  
```  
  
REPORT.RUNMODAL(Number [, ReqWindow] [, SystemPrinter] [, Record])  
```  
  
#### Parameters  
 *Number*  
 Type: Integer  
  
 The ID of the report that you want to run. To select the report from a list, on the **View** menu, choose **Symbols**.  
  
 If the report that you specify does not exist, then a run-time error occurs.  
  
 *ReqWindow*  
 Type: Boolean  
  
 Specifies whether the request window for the report will be displayed. The request window is part of the report object.  
  
 Specify **true**, which is the default value, to display the request window before you run the report. Specify **false** to run the report without displaying the request window.  
  
 This parameter overrides the setting of the [UseRequestPage Property](UseRequestPage-Property.md) of the report. If you do not provide a value for the *ReqWindow* parameter, then the setting of the UseRequestPage property is used.  
  
> [!IMPORTANT]  
>  Client-side printing is not supported by [!INCLUDE[nav_web](includes/nav_web_md.md)]. If you set this parameter to **false** and the report will be run on [!INCLUDE[nav_web](includes/nav_web_md.md)], you must set up the report to print from [!INCLUDE[nav_server](includes/nav_server_md.md)], otherwise an error occurs at runtime. For more information, see [How to: Specify Printer Selection for Reports](How-to--Specify-Printer-Selection-for-Reports.md) and [STARTSESSION Function \(Sessions\)](STARTSESSION-Function--Sessions-.md).  
  
 *SystemPrinter*  
 Type: Boolean  
  
 Specifies whether to use the default Windows printer or use table 78, Printer Selection, to find the correct printer for this report. For example, if the report prints on continuous forms, then you can set up an entry in the Printer Selection table to specify to always print this report on a specific printer.  
  
 Specify **true** to use the printer defined as the system printer. Specify **false**, which is the default value, to use the printer that is defined in the Printer Selection table.  
  
 *Record*  
 Type: Record  
  
 Specifies which record to use in the report. Any filters that are attached to the record that you specify are used.  
  
## Remarks  
 If you do not know the specific report that you want to run when you are designing your application, then use this function or the [REPORT.RUN Function](REPORT-RUN-Function.md). If you do know the specific report that you want to run, then you can use the [RUN Function \(Report\)](RUN-Function--Report-.md) or the [RUNMODAL Function \(Report\)](RUNMODAL-Function--Report-.md). When you use these functions the request page runs modally. However, when you choose **Preview** on the request page, the **Print Preview** page does not run modally.  
  
 The request page is run modally when you use this function.  
 
[!INCLUDE[multi_file_download_web_client](includes/multi_file_download_web_client.md)]
## Example 1 
 This example shows how to run a report. This example displays the request window and sends the report to the printer selected through the Printer Selection table.  
  
```  
REPORT.RUNMODAL(1001);  
```  
  
## Example 2 
 This example shows how to run a report. This example skips the request window, starts the report immediately, and sends the report to the printer that is selected in the Printer Selection table.  
  
```  
REPORT.RUNMODAL(1001, FALSE);  
```  
  
## Example 3 
 This example shows how to run a report. This example skips the request window and starts the report immediately. It sends the report to the system printer instead of the printer that is selected in the Printer Selection table.  
  
```  
REPORT.RUNMODAL(1001, FALSE, TRUE);  
```  
  
## See Also  
 [Report Data Type](Report-Data-Type.md)