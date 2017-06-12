---
title: "How to: Manage Company Configuration in a Worksheet"
ms.custom: na
ms.date: "03-03-2017"
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "configuration worksheets"
  - "RapidStart Services, using configuration worksheets"
ms.assetid: 3a47122e-e2d7-4ebc-b6a7-acdbe99b122b
caps.latest.revision: 19
ms.author: "edupont"
manager: "terryaus"
translation.priority.ht: 
  - "da-dk"
  - "de-at"
  - "de-ch"
  - "de-de"
  - "en-au"
  - "en-ca"
  - "en-gb"
  - "en-in"
  - "en-nz"
  - "es-es"
  - "es-mx"
  - "fi-fi"
  - "fr-be"
  - "fr-ca"
  - "fr-ch"
  - "fr-fr"
  - "is-is"
  - "it-ch"
  - "it-it"
  - "nb-no"
  - "nl-be"
  - "nl-nl"
  - "ru-ru"
  - "sv-se"
---
# How to: Manage Company Configuration in a Worksheet
The configuration worksheet is the central location in which you can plan, track, and perform your configuration work. You can create a worksheet for each company that you are working with or create a standard configuration worksheet that can be used for configuring multiple identical companies.  
  
 Before you start, make sure that you are on the [!INCLUDE[rim](../Roles/includes/rim_md.md)] Role Center page. It provides the correct context for your configuration work. To change your Role Center home page, see [How to: Change Role Centers](../GettingStarted/how-to-change-role-centers.md). Choose the RapidStart Profile ID.  
  
 The first step in preparing a configuration package is to select a company that you have already set up and modified to suit most of your solution needs. This company serves as the baseline for your configuration work on new companies. In the worksheet, you designate the tables that you want your configuration to control and handle. Since most tables in [!INCLUDE[navnow](../ApplicationDesign/includes/navnow_md.md)] have relationships and dependencies on other tables, you should also include those related tables as necessary. Together, these tables will then serve as the structure around which you will build a new company. Subsequent steps help you package and then deploy your configuration.  
  
 To aide you in tracking and reviewing your work, use the **Config. Package Table** FactBox to see information about records. Use the **Config. Related Tables** FactBox to monitor table relationships.  
  
 The following procedures demonstrate how to add and customize table information for your configuration.  
  
### To open the configuration worksheet  
  
1.  In the [!INCLUDE[nav_windows](../BusinessFunctionality/IntegratingWithMicrosoftOffice/includes/nav_windows_md.md)], open the company that is the baseline for configuration, and then open its Role Center Home page for [!INCLUDE[rim](../Roles/includes/rim_md.md)].  
  
2.  In the **Search** box, enter **Configuration Worksheet**, and then choose the related link.  
  
 The worksheet window opens.  
  
### To add one table to the worksheet  
  
1.  On the **Home** tab, in the **Manage** group, choose **Edit List**.  
  
2.  In the configuration worksheet, select the first line.  
  
3.  In the **Line Type** field, choose **Table**.  
  
4.  In the **Table ID** field, select the table that you want to add to your configuration.  
  
5.  In the **Page ID** field, enter the page ID associated with the table. For standard [!INCLUDE[navnow](../ApplicationDesign/includes/navnow_md.md)] tables, this value is automatically filled in. For custom tables, you have to provide the ID.  
  
6.  In the **Reference** field, enter a url of a page that provides best practice information or instructions for how to set up the table.  
  
7.  To add related tables, on the **Actions** tab, in the **Functions** group, choose **Get Related Tables**.  
  
    > [!NOTE]  
    >  Related tables will not be added with the **Get Related Tables** action if either of the following is true:  
    >   
    >  -   The relation is conditional.  
    >   
    >      Example: If you get related tables for table 18 \(**Customer**\), then table 14 \(**Location**\) will not be added, since it is only conditionally related to table 18, namely if the **Location Code** field in table 18 is filled.  
    > -   The related table is filtered.  
    >   
    >      Example: A field in the related table has a WHERE clause.  
    >   
    >  The reason for this is that the involved relations information is stored in the **Field** system table, which is not fully accessible to the application.  
    >   
    >  You must add such types of tables manually by following step 4 in this procedure.  
  
8.  To modify the resulting list of tables, select a table that you want to remove, and on the **Home** tab, choose **Delete**.  
  
9. Repeat the step for each table that you want to add to the configuration.  
  
10. To remove duplicate table information, which can result from the **Get Related Tables** action, on the **Actions** tab, in the **Functions** group, choose **Delete Duplicate Lines**. This will remove duplicate tables that have the same package code.  
  
### To add multiple tables to the configuration worksheet  
  
1.  On the **Actions** tab, in the **Functions** group, choose **Get Tables**. The **Get Config. Tables** batch job window opens.  
  
     On the **Options** FastTab, specify the types of tables that you want to add to the configuration. The following table describes the options.  
  
    |[!INCLUDE[bp_tableoption](../ApplicationDesign/includes/bp_tableoption_md.md)]|[!INCLUDE[bp_tabledescription](../ApplicationDesign/includes/bp_tabledescription_md.md)]|  
    |----------------------------------|---------------------------------------|  
    |**Include with Data Only**|Select the check box to include only those tables that contain data. For example, you may want to include a table that already defines the typical payment terms that your solution supports.|  
    |**Include Related Tables**|Select the check box to include all related tables. To add a subset of related tables, see step 3 in this procedure.|  
    |**Include Dimension Tables**|Select the check box to include dimension tables.|  
    |**Include Licensed Tables Only**|Select the check box to include only those tables for which the license under which you are creating the worksheet allows you access.|  
  
2.  On the **Object** FastTab, set filters as appropriate to specify the types of tables you want to include or exclude.  
  
3.  Choose the **OK** button. [!INCLUDE[navnow](../ApplicationDesign/includes/navnow_md.md)] tables are added to the worksheet. Each entry in the list has a line type of **Table**.  
  
4.  To remove duplicate table information, which can result from the **Get Tables** action, on the **Actions** tab, in the **Functions** group, choose **Delete Duplicate Lines**. This will remove duplicate tables that have the same package code.  
  
5.  You can add tables to the worksheet that are related to a table you have selected. Review the information in the **Related Tables** FactBox to see whether there are missing tables. To add related tables for a specific table, select the table in the list, and on the **Actions** tab, in the **Functions** group, choose **Get Related Tables**.  
  
    > [!NOTE]  
    >  Related tables will not be added with the **Get Related Tables** function if either of the following is true:  
    >   
    >  -   The relation is conditional.  
    >   
    >      Example: If you get related tables for table 18 \(**Customer**\), then table 14 \(**Location**\) will not be added, since it is only conditionally related to table 18, namely if the **Location Code** field in table 18 is filled.  
    > -   The related table is filtered.  
    >   
    >      Example: A field in the related table has a WHERE clause.  
    >   
    >  The reason for this is that the involved relations information is stored in the **Field** virtual table and is not available in windows such as the configuration worksheet for performance reasons.  
    >   
    >  You must add related tables with such complex relationships manually by following step 4 in the "To add one table to the worksheet" section.  
  
6.  You can also remove tables. To modify the resulting list of tables, select a table to remove, and on the **Home** tab, choose **Delete**.  
  
 Use the next procedure to specify which table fields to include. After you make this specification, you can export the table into Excel, and use the table structure as a template for gathering customer data. For more information, see [How to: Create a Configuration Template](../SetupAndAdministration/how-to-create-a-configuration-template.md).  
  
### To specify a set of fields and records for a configuration table  
  
1.  Select a table in the list of configuration tables, and on the **Home** tab, in the **Manage** group, chose **Edit List**.  
  
2.  Select a table for which you want to specify field information, and on the **Actions** tab, in the **Show** group, choose **Fields**.  
  
     To select just the fields you want to include, on the **Home** tab, in the **Process** group, choose **Clear Included**. To add all fields, choose **Set Included**.  
  
     To specify that the field data should not be validated, clear the **Validate Field** check box for the field.  
  
     Choose the **OK** button.  
  
3.  To filter to a certain set of records to include in the configuration worksheet, on the **Actions** tab, in the **Show** group, choose **Filters**. Specify the appropriate filter values.  
  
     [!INCLUDE[bp_fieldhelp]()]  
  
 You can create areas of functionality and groups of tables in the worksheet in order to put similar functionality together. For example, in setting up the chart of accounts for your configuration, you may decide to create a group of posting tables. Typically, areas are used to group a set of tables that correspond to a functional area. Each area can contain groups. A group can be used to arrange tables that have a common meaning together.  
  
 The following procedure describes how to add area and group designations, after you have created the initial list of tables. After you have added these categories, you can continue to add and modify your list of tables.  
  
### To categorize and group functionality in the worksheet  
  
1.  At the beginning of an area, insert a new line into the worksheet.  
  
2.  In the **Line Type** field, choose **Area**. In the **Name** field, enter a name for the area.  
  
3.  At the beginning of a grouping of tables, insert a new line into the worksheet.  
  
4.  In the **Line Type** field, choose **Group**. In the **Name** field, enter a name for the area. The group name is automatically indented.  
  
5.  To move tables to the appropriate category, on the **Actions** tab, in the **Functions** group, select a table to move. Choose **Move Up** or **Move Down**. Alternatively, you can delete a worksheet line and insert the table again in the required location.  
  
 For more information about how to use categories effectively, see [Line Type](../Topic/\($%20T_8622_2%20Line%20Type%20$\).md).  
  
 Some [!INCLUDE[navnow](../ApplicationDesign/includes/navnow_md.md)] tables are standard and the data in them is not likely to change from implementation to implementation. Consequently, to help your customer focus, you can remove these tables from the worksheet after you have included them in the configuration package. Once added, the tables remain part of the configuration package.  
  
### To remove a standard table in the worksheet  
  
1.  After you have added all necessary tables to a configuration package, determine which tables will not require customer attention.  
  
2.  Select the tables, and then delete them.  
  
    > [!NOTE]  
    >  The tables remain in the package.  
  
## See Also  
 [Config. Worksheet](../Topic/\($%20N_8632%20Config.%20Worksheet%20$\).md)   
 [Get Config. Tables](../Topic/\($%20B_8614%20Get%20Config.%20Tables%20$\).md)   
 [How to: Create a Configuration Package](../SetupAndAdministration/how-to-create-a-configuration-package.md)