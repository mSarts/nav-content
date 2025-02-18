---
    title: How to Remove and Reapply Item Entries
    description: You can view and manually change certain item application entries that are created automatically during inventory transactions.

    documentationcenter: ''
    author: SorenGP

    ms.prod: "dynamics-nav-2018"
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 08/10/2018
    ms.author: edupont

---
# How to: Remove and Reapply Item Ledger Entries
In the **Application Worksheet** window, you can view and manually change certain item application entries that are created automatically during inventory transactions.  

When you post a transaction where items are moved in or out of inventory, an item application is created between each inventory increase and inventory decrease. These applications determine the flow of costs from the goods that are received in inventory to the cost of goods going out of inventory. Because of the way the unit cost is calculated, an incorrect item application could lead to a skewed average cost and a skewed unit cost. For more information, see [Design Details: Item Application](design-details-item-application.md).

The following scenarios might require that you undo an application or reapply item ledger entries:

- You have forgotten to make a fixed application.
- You have made an incorrect fixed application.
- You have to return an item to which a sale has already been applied.

If possible, use a document to reapply an item ledger entry. For example, if you must make a purchase return of an item to which a sale has already been applied, you can reapply by creating and posting the purchase return document by using the correct application in the **Appl.-to Item Entry** field on the purchase return line. You can use the **Get Posted Document Lines to Reverse** function or the **Copy Document** function in the purchase return document to make this easier. When you post the document, the item ledger entry is automatically reapplied. For more information, see [How to: Process Purchase Returns or Cancellations](purchasing-how-process-purchase-returns-cancellations.md).

If you cannot use a document to reapply, such as when you have to correct a fixed application, then use the **Application Worksheet** window to correct an application.

> [!Warning]
> The following are important considerations to remember when you are working with the application worksheet:
>     - You should not leave application entries unapplied for long periods of time because other users cannot process the items until you reapply the application entries or close the **Application Worksheet** window. Users who try to perform actions that involve a manually unapplied application entry receive the following error message: “You cannot perform this action because entries for item XXX are unapplied in the Application Worksheet by user XXX.”
>     - You should only reapply item ledger entries during nonworking hours to avoid conflicts with other users who are posting transactions with the same items.
>     - When you close the application worksheet, [!INCLUDE[d365fin](includes/d365fin_md.md)] performs a check to make sure that all entries are applied. For example, if you remove a quantity application but do not create a new application, and then you close the application worksheet, a new application is created. This helps keep the cost intact. However, if you remove a fixed application, a new fixed application is not automatically created when you close the worksheet. You must do this manually by creating a new application in the worksheet.
>     - It is possible to remove applications from more than one entry at a time in the application worksheet. However, because applying entries affects the set of entries that are available for application, you cannot create an application for more than one entry at a time.
>     - The application worksheet cannot make an application in the following situation: If there is not enough quantity on stock to apply, the application worksheet cannot make an application when you are trying to apply an inventory decrease entry without item tracking information to an inventory increase entry with item tracking information.

## To remove an item application by using the Application Worksheet  
1. Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Application Worksheet**, and then choose the related link.  
2. The **Application Worksheet** window opens displaying existing item ledger entries for all items.  
3. Enter filters on the **General** FastTab to make it easier to find the item ledger entry for which you want to change the application.  
4. Select the item ledger entry, and then choose the **Applied Entries** action. The **View Applied Entries – Applied Entries** window opens to show the item ledger entry or entries that are currently applied to the selected entry.  
5. Select the item ledger entry for which you want to remove the application.  
6. Choose the **Remove Application** action. This removes the item application entry that links the two item ledger entries and moves it to the **View Applied Entries – Unapplied Entries** window.  
7. Close the **View Applied Entries – Applied Entries** window.  

   The **Remaining Quantity** field of the two item ledger entries are increased by the quantity that has been unapplied. The removed item ledger entry is now available for reapplication in the **View Applied Entries – Unapplied Entries** window.  

> [!IMPORTANT]  
>  You should not leave application entries unapplied for longer periods of time because other users cannot process the affected items until you reapply the application entries or close the **Application Worksheet** window. The following error message is displayed if you try to perform actions that involve a manually unapplied application entry:  
>   
>  **You cannot perform this action because entries for item <item> are unapplied in the Application Worksheet by user <user>.**  

## To reapply an item application by using the Application Worksheet  
1.  Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Application Worksheet**, and then choose the related link.  
2.  The **Application Worksheet** window opens displaying existing item ledger entries for all items.  
3.  To reapply entries that were removed since the worksheet was opened, select the item ledger entry that you want to reapply. On the **Actions** tab, in the **Functions** group, choose **Reapply**.  

    > [!NOTE]  
    >  This reapplication to the original balance also occurs automatically when you close the **Application Worksheet** window.  
4.  To apply an available open item ledger entry to another entry, select the item ledger entry that you want to apply. Choose the **Unapplied Entries** action. The **View Applied Entries – Unapplied Entries** window opens.  
5.  Select one or more item ledger entries that you want to apply to the entry selected in the **Application Worksheet** window, and then choose the **OK** button.  

     An item application entry is created between the two item ledger entries. The **Remaining Quantity** fields of the two entries are reduced by the applied quantity.  

    > [!NOTE]  
    >  If you have chosen to make an application that would create an infinite loop in the cost adjustment process, then the application that you proposed is not made. This can occur when the original entries created negative stock. The application is not made. Therefore, you must select a different entry for the application.  
6.  If the **Automatic Cost Adjustment** field in the **Inventory Setup** is set to **Always**, then the cost adjustment batch job is automatically run after you make a reapplication. Otherwise, run the **Adjust Cost - Item Entries** batch job to make sure that all costs are up to date.  

## See Also
[Dynamics 365 Business Central](https://docs.microsoft.com/dynamics365/business-central/)  
[How to: Close Open Item Ledger Entries Resulting from Fixed Application in the Item Journal](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)  
 [How to: Process Purchase Returns or Cancellations](purchasing-how-process-purchase-returns-cancellations.md)  
 [Managing Inventory Costs](finance-manage-inventory-costs.md)   
 [Design Details: Item Application](design-details-item-application.md)  
 [Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
