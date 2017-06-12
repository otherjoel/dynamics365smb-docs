---
title: "Currency Exchange Rates"
ms.custom: na
ms.date: "06-05-2016"
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "currency exchange rates"
  - "BilMoG"
ms.assetid: 573e5260-bddf-4040-9a4b-51341a91aa41
caps.latest.revision: 9
ms.author: "edupont"
manager: "terryaus"
translation.priority.ht: 
  - "de-de"
---
# Currency Exchange Rates
At the end of the fiscal year, you must adjust currency exchange rates for payables and receivables so that they are valued correctly in the annual balance. The **Adjust Exchange Rates** batch job supports different valuation methods in order to meet legal requirements in Germany.  
  
## Valuation Methods  
 According to the Bilanz Modernisierungs Gesetz \(BilMoG\), payables and receivables are valued differently depending on the difference between the reference date and the due date. This is managed by the **Adjust Exchange Rates** batch job where you can specify which valuation method to use. If the due date is less than one year after the reference date, the **Adjust Exchange Rates** batch job must be run using the lowest value valuation method.  
  
 The following table describes the valuation methods.  
  
|Valuation method|[!INCLUDE[bp_tabledescription](../../ApplicationDesign/includes/bp_tabledescription_md.md)]|  
|----------------------|---------------------------------------|  
|BilMoG \(Germany\)|Beginning in 2010, each ledger entry is adjusted as follows:<br /><br /> -   If the due date is less than one year after the reference date, payable\/receivable transactions are valued at the actual exchange rate.<br />-   If the due date is more than one year after the reference date, payable\/receivable transactions are valued at the lowest value, with the possibility of appreciation in value \(Wertaufholung\) up to the initial value. **Note:**  Ledger entries must contain a due date. An entry that does not have a due date is treated as a long term liability.|  
|Lowest value|Exchange rates are adjusted by using the lowest value of the two exchange rates. Currency losses are always calculated and posted. Currency gains are only calculated and posted up to the original local currency value of the transaction.<br /><br /> This ensures that receivables are not valued above their original posting amounts, and that payables are not valued below their original posting amounts.|  
|Standard|Exchange rates are adjusted according to standard valuation principles. Full unrealized gains and losses are calculated and posted. If the transaction is partially applied, only the remaining amount is included in the adjustment. For more information, see [Adjust Exchange Rates](../Topic/\($%20B_595%20Adjust%20Exchange%20Rates%20$\).md).|  
  
 German companies must use the **BilMoG \(Germany\)** option when they run the **Adjust Exchange Rates** batch job. This ensures that each transaction is adjusted using the appropriate valuation method as required in Germany. This also enables two fields in the request window, where you can specify the two dates that must be used to calculate the adjustment. The following table describes the fields.  
  
|[!INCLUDE[bp_tablefield](../../ApplicationDesign/includes/bp_tablefield_md.md)]|[!INCLUDE[bp_tabledescription](../../ApplicationDesign/includes/bp_tabledescription_md.md)]|  
|---------------------------------|---------------------------------------|  
|**Valuation Reference Date**|Specifies the base date that is used to calculate which entries are short\-term entries.|  
|**Short term liabilities until**|Specifies the date that separates short\-term entries from long\-term entries. Short\-term entries have a due date that is before or on this date. The default value is the value of the **Valuation Reference Date** field plus one year.|  
  
## See Also  
 [Adjust Exchange Rates](../Topic/\($%20B_595%20Adjust%20Exchange%20Rates%20$\).md)   
 [Currencies](assetId:///c41486d9-65f9-416a-b138-8de3ded8333b)   
 [Currency Exchange Rates](assetId:///ecc75eeb-2b22-4316-8204-fd0940c11c68)