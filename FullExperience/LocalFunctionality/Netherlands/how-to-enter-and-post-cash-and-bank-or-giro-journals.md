---
title: "How to: Enter and Post Cash and Bank or Giro Journals"
ms.custom: na
ms.date: "06-05-2016"
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "bank journals, posting"
  - "giro, journals"
  - "bank journals, entering"
  - "bank/giro, posting"
  - "cash journals"
  - "bank/giro, journals"
ms.assetid: 39540a57-c740-443c-ad9d-50b694f68a98
caps.latest.revision: 24
ms.author: "edupont"
manager: "terryaus"
translation.priority.ht: 
  - "nl-nl"
---
# How to: Enter and Post Cash and Bank or Giro Journals
In [!INCLUDE[navnow](../../ApplicationDesign/includes/navnow_md.md)], you can use the cash and bank journals to enter the transactions that affect the cash and bank accounts by using **Cash Book** and **Bank Book**.  
  
 You can enter increases or decreases to the cash account in the **Cash Journals**. For example, you can use this journal for paying out petty cash or receiving transfers from a different bank account.  
  
 The **Bank\/Giro Journal** records the inflow or outflow of the cash to a specific bank account. This journal forms the basis for bank reconciliation. The layout of this journal resembles the paper bank statement, so you can transpose the required fields from the paper statement to the journal, or you can import an electronic bank statement file. The transactions can be customer payments or vendor payments.  
  
 You can apply the payments from customers to the open invoices from Accounts Receivables. You can also enter general ledger transactions to capture miscellaneous amounts, such as bank charges or interest income. VAT codes can also be applied to these transaction lines. You can define a journal for every bank account.  
  
### To post cash journals  
  
1.  In the **Search** box, enter **Cash Journal**, and then choose the related link.  
  
2.  On the **Home** tab, choose **New**.  
  
3.  In the **Cash Journal** window, on the **Lines** FastTab, fill in the required fields as described in the following table.  
  
    |[!INCLUDE[bp_tablefield](../../ApplicationDesign/includes/bp_tablefield_md.md)]|[!INCLUDE[bp_tabledescription](../../ApplicationDesign/includes/bp_tabledescription_md.md)]|  
    |---------------------------------|---------------------------------------|  
    |**Date**|The journal entry date.|  
    |**Document No.**|The document number for which journal entry is created.|  
    |**Account Type**|The account type to which the entry is to be posted.|  
    |**Account No.**|The account number to which the entry is to be posted.|  
    |**Description**|The description of the entry. This field automatically populates the description of the account number selected in the **Account No.** field.|  
    |**VAT Prod. Posting Group**|The VAT product posting group code used to post the entry. You can select a code in this field only if the **Account Type** is **G\/L Account**. For more information, see [VAT Product Posting Groups](assetId:///fec65dff-74eb-4151-bdf2-c2981a718b58).|  
    |**Amount**|The total amount that the statement line consists of. You must enter the debit amount without a plus or minus sign and the credit amount with a minus sign.<br /><br /> If this amount includes the VAT amount, then select the **Amount incl. VAT** check box.|  
  
4.  On the **Home** tab, in the **Process** group, choose **Post**.  
  
    > [!NOTE]  
    >  If there is a difference between the opening balance and the closing balance, you must change the closing balance before posting the entry.  
  
     The entries are posted to the general ledger. For more information, see [General Ledger Entries](assetId:///7634ea31-5577-42dc-9076-78cffea19ef4).  
  
### To post bank or giro journals  
  
1.  In the **Search** box, enter **Bank\/Giro Journal**, and then choose the related link.  
  
2.  On the **Home** tab, choose **New**.  
  
3.  Select the relevant journal template, and then choose the **OK** button.  
  
4.  In the **Bank\/Giro Journal** window, fill in the fields as described in the following table.  
  
    |[!INCLUDE[bp_tablefield](../../ApplicationDesign/includes/bp_tablefield_md.md)]|[!INCLUDE[bp_tabledescription](../../ApplicationDesign/includes/bp_tabledescription_md.md)]|  
    |---------------------------------|---------------------------------------|  
    |**Opening Balance**|The current balance of the bank or giro account. It equals the closing balance of previously posted entries for the journal.|  
    |**Closing Balance**|The new closing balance of the journal.|  
  
5.  On the **Lines** FastTab, fill in the required fields as described in the following table.  
  
    |[!INCLUDE[bp_tablefield](../../ApplicationDesign/includes/bp_tablefield_md.md)]|[!INCLUDE[bp_tabledescription](../../ApplicationDesign/includes/bp_tabledescription_md.md)]|  
    |---------------------------------|---------------------------------------|  
    |**Date**|The journal entry date.|  
    |**Account Type**|The account type to which the journal entry is to be posted.|  
    |**Account No.**|The account number to which the journal entry is to be posted.|  
    |**Identification**|The identification number that links the statement line to a payment history line.|  
    |**Description**|The description of the entry.|  
    |**VAT Prod. Posting Group**|The VAT product posting group code that will be used when you post the entry on the statement line.|  
    |**Amount**|The total amount that the statement line consists of. You must enter the debit amount without a plus or minus sign and the credit amount with a minus sign.<br /><br /> If this amount includes the VAT amount, then select the **Amount incl. VAT** check box.|  
  
6.  On the **Home** tab, in the **Process** group, choose **Post**.  
  
    > [!NOTE]  
    >  If there is a difference between the opening balance and the closing balance, you must change the closing balance before posting the entry.  
  
     The entries are posted to the general ledger. For more information, see [General Ledger Entries](assetId:///7634ea31-5577-42dc-9076-78cffea19ef4).  
  
## See Also  
 [How to: Print the Test Reports for Cash and Bank or Giro Journals](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Netherlands/how-to-print-the-test-reports-for-cash-and-bank-or-giro-journals.md)   
 [VAT Product Posting Groups](assetId:///fec65dff-74eb-4151-bdf2-c2981a718b58)   
 [General Ledger Entries](assetId:///7634ea31-5577-42dc-9076-78cffea19ef4)