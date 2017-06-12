---
title: "How to: Create New Versions of Production BOMs"
ms.custom: na
ms.date: "03-03-2017"
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "production BOMs, creating"
  - "production BOMs, versions"
ms.assetid: e32013aa-924a-41c9-99ac-0b65d6891eaf
caps.latest.revision: 8
ms.author: "sgroespe"
manager: "terryaus"
translation.priority.ht: 
  - "da-dk"
---
# How to: Create New Versions of Production BOMs
New versions of production BOMs are used when, for example, an item is replaced by another item, or when a customer requires a special version of a product.  
  
### To create a new version of a production BOM  
  
1.  In the **Search** box, enter **Production BOM**, and then choose the related link.  
  
2.  Select the production BOM to be copied.  
  
3.  On the **Navigate** tab, in the **Prod. BOM** group, choose **Versions**.  
  
4.  On the **Home** tab, in the **New** group, choose **New**.  
  
5.  Fill in the fields of the new production BOM version for the BOM you selected. Enter a value in the **Version Code** field.  
  
     The newly created version is automatically assigned the status **New**.  
  
     The time validity of the version is specified by the **Starting Date** field.  
  
> [!NOTE]  
>  Select the **Item** option in the **Type** field to use an item from your item master data in the production BOM. If the item also has a production BOM, whereby the **Production BOM No.** field is filled in on the item card, this production BOM is also considered.  
>   
>  Select the **Production BOM** option if you want to use a phantom production BOM on the line.  
>   
>  Phantom production BOMs serve for structuring products. This production BOM type never leads to a finished product, but is used exclusively for determining the dependent demand. Phantom production BOMs do not have their own item master data.  
  
## See Also  
 [Concepts of Production BOMs](../DesignAndEngineering/concepts-of-production-boms.md)   
 [How to: Create Production BOMs](../DesignAndEngineering/how-to-create-production-boms.md)   
 [How to: Copy Versions of Production BOMs](../DesignAndEngineering/how-to-copy-versions-of-production-boms.md)   
 [How to: Compare Material Quantities in All Production BOM Versions](../DesignAndEngineering/how-to-compare-material-quantities-in-all-production-bom-versions.md)