---
title: "Summarizing Payment Lines and General Journal Lines"
ms.custom: na
ms.date: "06-05-2016"
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "invoices, lines with different descriptions"
  - "invoices, multiple lines"
ms.assetid: 1cbb20a1-89a3-4a98-9447-525bf4d818ec
caps.latest.revision: 2
ms.author: "edupont"
translation.priority.ht: 
  - "fr-be"
  - "nl-be"
---
# Summarizing Payment Lines and General Journal Lines
In [!INCLUDE[navnow](../../ApplicationDesign/includes/navnow_md.md)], you can post an invoice that has more than one line with the same general ledger account, but has different descriptions. A general ledger entry is created individually for each invoice line that is posted. The invoice line description will be copied to the general ledger account description in the general ledger entries. [!INCLUDE[navnow](../../ApplicationDesign/includes/navnow_md.md)] handles the following types of transactions in the same way:  
  
-   Domestic payments  
  
-   International payments  
  
-   SEPA payments  
  
-   Non\-euro SEPA payments  
  
## How Payment Journal Lines are Transferred to the General Journal  
 When you export the payment journal lines to a file, [!INCLUDE[navnow](../../ApplicationDesign/includes/navnow_md.md)] transfers the payment journal lines to the specified general journal. By default, a general journal line is created for each payment journal line.  
  
 The following two fields in the **Electronic Banking Setup** window affect how the payment lines are summarized:  
  
-   **Summarize Gen. Jnl. Lines**  
  
-   **Cut off Payment Message Texts**  
  
 If you have selected the **Summarize Gen. Jnl. Lines** check box in the **Electronic Banking Setup** window, [!INCLUDE[navnow](../../ApplicationDesign/includes/navnow_md.md)] summarizes all payment journal lines for a specific vendor into one general journal line. The general description "Payment %1," where %1 is the vendor number, is used for the summarized journal line description. A separate payment line and a separate general journal line are created to handle:  
  
-   Payment journal lines that contain partial payments, with both the **Partial Payment** and the **Separate Line** fields selected.  
  
-   Payment journal lines that contain a standard format message \(that is, passes the MOD97 test\), which sets **Standard Format Message** to True in the electronic banking journal.  
  
## Examples  
  
### Example 1  
 In this example, you export payment lines, and the **Summarize Gen. Jnl. Lines** check box is selected. [!INCLUDE[navnow](../../ApplicationDesign/includes/navnow_md.md)] creates:  
  
-   One combined payment line in a XML file that has a concatenated payment message. White space is the delimiter.  
  
-   One payment line in the general journal with a generic description that includes the vendor name.  
  
### Example 2  
 In this example, you export payment lines, and the **Summarize Gen. Jnl. Lines** check box is selected. The **Cut off Payment Message Texts** check box is cleared, and combined SEPA and non\-euro SEPA payment lines exceed 140 characters in payment message. [!INCLUDE[navnow](../../ApplicationDesign/includes/navnow_md.md)] creates:  
  
-   Two combined payment lines in a XML file. The first payment line contains the first concatenated payment messages. The second payment line contains the payment message from the third line.  
  
-   One payment line in the general journal with a generic description that includes the vendor name.  
  
### Example 3  
 In this example, you export payment lines, and the **Summarize Gen. Jnl. Lines** check box is selected. The **Cut off Payment Message Texts** check box is also selected and combined SEPA and non\-SEPA payment lines exceed 140 characters in payment message. [!INCLUDE[navnow](../../ApplicationDesign/includes/navnow_md.md)] creates:  
  
-   One combined payment line in a XML file that has two concatenated payment messages. An ellipsis \(…\) is used to indicate that the message is truncated.  
  
-   One payment line in the general journal with a generic description that includes the vendor name.  
  
 Based on the XML structure, the payments are summarized per account number and beneficiary bank account no and bank account no. The bank account filter can be empty.  
  
 The EndToEndId in the SEPA message is taken from the payment message and can be truncated to the maximum length of 45 characters.  
  
## See Also  
 [How to: Set Up Electronic Banking](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Belgium/how-to-set-up-electronic-banking.md)   
 [Summarize Gen. Jnl. Lines](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Belgium/-$-t_11306_2-summarize-gen.-jnl.-lines-$-.md)   
 [Cut off Payment Message Texts](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Belgium/-$-t_11306_3-cut-off-payment-message-texts-$-.md)   
 [Chart of Accounts](assetId:///fa407624-b670-44b6-8397-91aa606e4c39)   
 [How to: Set Up General Ledger Accounts in the Chart of Accounts Window](../../Finance/how-to-set-up-general-ledger-accounts-in-the-chart-of-accounts-window.md)   
 [Purchase Invoice](../Topic/\($%20N_51%20Purchase%20Invoice%20$\).md)   
 [How to: Post Purchase Invoices](../../Finance/how-to-post-purchase-invoices.md)   
 [Sales Invoice](../Topic/\($%20N_43%20Sales%20Invoice%20$\).md)