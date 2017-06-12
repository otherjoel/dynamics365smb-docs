---
title: "How to: Download CODA Files from an Isabel Server"
ms.custom: na
ms.date: "06-05-2016"
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "CODA, downloading files"
ms.assetid: c32c7977-ae51-4ea8-a607-a432b270ade9
caps.latest.revision: 2
ms.author: "edupont"
translation.priority.ht: 
  - "fr-be"
  - "nl-be"
---
# How to: Download CODA Files from an Isabel Server
CODA files can be downloaded manually or in attended mode.  
  
 To manually download CODA files, log  on to the Isabel server and select the files that you want to download. The downloaded files can then be imported from the **Bank Account** table. For more information, see [How to: Import CODA Statements](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Belgium/how-to-import-coda-statements.md).  
  
### To download CODA files in attended mode  
  
1.  In the **Search** box, enter **IBS Logs**, and then choose the related link.  
  
2.  On the **Home** tab, in the **Process** group, choose **Download**.  
  
3.  In the **IBS Download Request Options** window, fill in the fields as described in the following table.  
  
    |[!INCLUDE[bp_tablefield](../../ApplicationDesign/includes/bp_tablefield_md.md)]|[!INCLUDE[bp_tabledescription](../../ApplicationDesign/includes/bp_tabledescription_md.md)]|  
    |---------------------------------|---------------------------------------|  
    |**From Date**|Specify the start date of the download.|  
    |**To Date**|Specify the end date of the download.|  
    |**File Format**|Select **Coda** as the file format.|  
    |**File Status**|Select the file status of the download. File statuses include **Not Downloaded**, **Downloaded**, and **All**. Typically you will select **Not Downloaded**, because you are downloading the CODA files that have not been downloaded to your system.|  
  
4.  Choose the **OK** button.  
  
    > [!NOTE]  
    >  You cannot delete any files from the Isabel server by using the **IBS Download Request Options** window. You must manually delete the files by logging on to the Isabel server.  
  
     After the CODA files have been downloaded, the **Process Status** field will display **Created** in the **IBS Logs** window. You can log on to the Isabel server to manually retrieve the files. For more information, see [How to: Import CODA Statements](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Belgium/how-to-import-coda-statements.md).  
  
## See Also  
 [IBS Download Request Options](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Belgium/-$-n_2000012-ibs-download-request-options-$-.md)   
 [Import CODA Statement](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Belgium/-$-b_2000030-import-coda-statement-$-.md)   
 [IBS Logs](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Belgium/-$-n_2000010-ibs-logs-$-.md)