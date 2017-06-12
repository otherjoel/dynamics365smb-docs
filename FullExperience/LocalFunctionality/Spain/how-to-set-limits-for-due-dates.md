---
title: "How to: Set Limits for Due Dates"
ms.custom: na
ms.date: "06-05-2016"
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "payments, setting legal limits"
  - "due dates, setting limits"
ms.assetid: c4abb260-c121-4443-8d8f-f19c13ba1b15
caps.latest.revision: 9
ms.author: "edupont"
manager: "terryaus"
translation.priority.ht: 
  - "es-es"
---
# How to: Set Limits for Due Dates
You can modify payment terms to have limits for the maximum number of days that can be between a delivery and the corresponding payment.  
  
 Legal limits for the gap between delivery and payment determine how due dates are calculated. For example, if you create a payment term that will be used for sales to the public sector, the **Max. No. of Days till Due Date** field for that payment term must be set to 30 days.  
  
### To set limits for due dates on payment terms  
  
1.  In the **Search** box, enter **Payment Terms**, and then choose the related link.  
  
2.  Select the payment term that you want to modify, and then, in the **Max. No. of Days till Due Date** field, specify the number of calendar days to allow between delivery and payment.  
  
 Next, you must make sure that you specify the appropriate payment terms for your public and private customers and vendors. When you create a document for that customer or vendor, the due date for the payment is calculated from the day that the customer received the items or services. Then, you must update the **Document Date** field for the document with the date of the receipt. For example, if you update a sales invoice when you are informed of delivery, the due date is calculated based on the new document date that you specified. The calculated due date cannot be further away than the limit that you specified for the payment term.  
  
> [!IMPORTANT]  
>  You cannot post a document that creates a bill where one or more installments have a due date that is later than the limit that is specified in the **Max. No. of Days till Due Date** field.  
  
## See Also  
 [Calculating Due Dates](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Spain/calculating-due-dates.md)   
 [How to: Set Up Payment Terms](../../Finance/how-to-set-up-payment-terms.md)