---
title: "How to: Create Payment Slips"
ms.custom: na
ms.date: "06-05-2016"
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "payment slips"
  - "payment files"
ms.assetid: e1d42533-6e6c-4ee2-9d25-53eac831ca50
caps.latest.revision: 34
ms.author: "edupont"
manager: "terryaus"
translation.priority.ht: 
  - "fr-fr"
---
# How to: Create Payment Slips
You can create payments slips to manage vendor and customer payments. Before you create payment slips, you must set up payment classes. For more information, see [How to: Set Up Payment Classes](../../LocalFunctionalityForMicrosoftDynamicsNav2016/France/how-to-set-up-payment-classes.md).  
  
 The following procedure describes how to create payment slips for vendor payments, but the same steps also apply to creating payment slips for customer payments.  
  
### To create a payment slip for vendors  
  
1.  In the **Search** box, enter **Payment Slips**, and then choose the relevant link.  
  
2.  On the **Home** tab, choose **New**.  
  
3.  In the **Payment Slip** window, choose a field to open the **Payment Class List** window.  
  
4.  Select a payment class, and then choose the **OK** button.  
  
5.  On the **General** FastTab, fill in the fields as described in the following table.  
  
    |[!INCLUDE[bp_tablefield](../../ApplicationDesign/includes/bp_tablefield_md.md)]|[!INCLUDE[bp_tabledescription](../../ApplicationDesign/includes/bp_tabledescription_md.md)]|  
    |---------------------------------|---------------------------------------|  
    |**Currency Code**|Specify the currency code to be used for the payment lines.|  
    |**Posting Date**|Specify the posting date.|  
    |**Document Date**|Specify the document date.|  
    |**Amount \(LCY\)**|The total amount from the payment lines. This field is updated automatically when the net line amounts are changed.<br /><br /> [!INCLUDE[bp_fieldnoneditable](../../Finance/includes/bp_fieldnoneditable_md.md)]|  
  
6.  On the **Lines** FastTab, fill in the fields as described in the following table.  
  
    |[!INCLUDE[bp_tablefield](../../ApplicationDesign/includes/bp_tablefield_md.md)]|[!INCLUDE[bp_tabledescription](../../ApplicationDesign/includes/bp_tabledescription_md.md)]|  
    |---------------------------------|---------------------------------------|  
    |**Account Type**|The account type to which the payment line is posted.|  
    |**Account No.**|The unique identification number for the account to which the entry will be posted.|  
  
7.  In the **Bank Account Code** field, select a bank name from the list, and then choose **Advanced**.  
  
8.  Optionally, for SEPA, in the **Select – Vendor Account List** window, on the **Home** tab, in the **Manage** Group, choose **Edit**.  
  
     Fill in the following fields if needed:  
  
    -   **Country\/Region Code**. In the list, choose **Advanced**, and make sure that the **SEPA Allowed** check box is selected for the code that you select.  
  
    -   **Swift Code**  
  
    -   **IBAN**  
  
     Choose the **OK** button to close the window.  
  
9. Optionally, for SEPA, on the **Navigate** tab, choose **Header RIB**. Select the **Bank Country\/Region Code** field, and then choose **Advanced**. Make sure the **SEPA Allowed** check box is selected. Also make sure that the **IBAN** and **SWIFT Code** fields are filled in.  
  
10. On the **Home** tab, in the **Process** group, choose **Suggest Vendor Payments**.  
  
    > [!NOTE]  
    >  You can also manually fill in the payment lines.  
  
11. In the **Suggest Vendor Payments** batch job, on the **Options** FastTab, fill in the fields as described in the following table.  
  
    |[!INCLUDE[bp_tablefield](../../ApplicationDesign/includes/bp_tablefield_md.md)]|[!INCLUDE[bp_tabledescription](../../ApplicationDesign/includes/bp_tabledescription_md.md)]|  
    |---------------------------------|---------------------------------------|  
    |**Last Payment Date**|The last payment date for the vendor ledger entries that are to be included in the batch job.|  
    |**Find Payment Discounts**|Select to include vendor ledger entries for which you can receive a payment discount.|  
    |**Summarize per**|The criteria for summarizing the payment line.|  
    |**Use Vendor Priority**|Select to sort the suggested payments based on the value in the **Priority** field on the vendor cards. For more information, see [Priority](../Topic/\($%20T_23_46%20Priority%20$\).md).|  
    |**Available Amount \(LCY\)**|The maximum amount that is available for payments in local currency.|  
    |**Currency Filter**|The code for the currency to be included in the batch job.|  
  
12. On the **Vendor** FastTab, select the appropriate filters.  
  
13. Choose the **OK** button.  
  
     The payment lines are automatically created.  
  
14. In the **Payment Slip** window, on the **Posting** FastTab, fill in the fields as described in the following table.  
  
    |[!INCLUDE[bp_tablefield](../../ApplicationDesign/includes/bp_tablefield_md.md)]|[!INCLUDE[bp_tabledescription](../../ApplicationDesign/includes/bp_tabledescription_md.md)]|  
    |---------------------------------|---------------------------------------|  
    |**Source Code**|The source code for the payment slip.|  
    |**Department Code**|The relevant dimension code.|  
    |**Project Code**|The relevant dimension code.|  
    |**Account Type**|The account type to which or from which the payments will be transferred.|  
    |**Account No.**|The account number to which or from which the payments will be transferred.|  
  
15. Optionally, for SEPA, in the **Account No.** field, choose **Advanced**.  
  
     In the **Bank Account List** window, on the **Home** tab, choose **Edit**.  
  
     Fill in the following fields if needed:  
  
    -   **General** FastTab  
  
        -   **Country\/Region Code**  
  
    -   **Transfer**  FastTab  
  
        -   **Swift Code**  
  
        -   **IBAN**  
  
    -   **RIB** FastTab  
  
        -   **Payment Export Format**: SEPA  
  
        -   **SEPA CT Msg. ID No. Series**: Bank  
  
16. Choose the **OK** button.  
  
     After you create a payment slip, you can generate payment files and send them to the bank electronically.  
  
    > [!NOTE]  
    >  A payment file can be created if the payment slip displays **File** for the **Action Type** field. For more information, see [Action Type](../../LocalFunctionalityForMicrosoftDynamicsNav2016/France/-$-t_10862_6-action-type-$-.md).  
  
### To create a payment file  
  
1.  In the **Search** box, enter **Payment Slips**, and then choose the relevant link.  
  
2.  Select a payment slip, and then, on the **Home** tab, in the **Manage** group, choose **Edit**.  
  
3.  In the **Payment Slip** window, on the **Actions** tab, in the **Posting** group, choose **Generate file**.  
  
4.  Choose the **Yes** button, and then choose the **OK** button.  
  
     The payment file is generated and exported according to the export type that is specified in the **Payment Step** window.  
  
5.  In the case of error, review the errors listed in the **File Export Errors** FactBox, and take the appropriate action.  
  
## See Also  
 [Payment Management](../../LocalFunctionalityForMicrosoftDynamicsNav2016/France/payment-management.md)   
 [How to: Set Up Payment Classes](../../LocalFunctionalityForMicrosoftDynamicsNav2016/France/how-to-set-up-payment-classes.md)   
 [How to: Set Up Payment Statuses](../../LocalFunctionalityForMicrosoftDynamicsNav2016/France/how-to-set-up-payment-statuses.md)   
 [How to: Set Up Payment Steps](../../LocalFunctionalityForMicrosoftDynamicsNav2016/France/how-to-set-up-payment-steps.md)   
 [How to: Set Up Payment Addresses](../../LocalFunctionalityForMicrosoftDynamicsNav2016/France/how-to-set-up-payment-addresses.md)   
 [How to: Post Payment Slips](../../LocalFunctionalityForMicrosoftDynamicsNav2016/France/how-to-post-payment-slips.md)   
 [How to: Archive Payment Slips](../../LocalFunctionalityForMicrosoftDynamicsNav2016/France/how-to-archive-payment-slips.md)   
 [How to: Export or Import Payment Management Setup Parameters](../../LocalFunctionalityForMicrosoftDynamicsNav2016/France/how-to-export-or-import-payment-management-setup-parameters.md)   
 [Priority](../Topic/\($%20T_23_46%20Priority%20$\).md)   
 [Dimension Value](assetId:///abbe4b49-2198-452c-9fa0-108cf5e6d7af)