---
title: Manage, delete, or compress documents 
description: Keep your historical data or delete it.
author: edupont04

ms.prod: "dynamics-nav-2018"
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords:
ms.date: 09/01/2017
ms.author: edupont

---
# Manage Documents
A central role, such as the application administrator, must regularly deal with accumulating historic documents by deleting or compressing them.  

## Delete Documents
In certain situations, you may need to delete invoiced purchase orders that have not been deleted. [!INCLUDE[d365fin](includes/d365fin_md.md)] checks that you have fully invoiced the deleted purchase orders. You cannot delete orders that you have not fully invoiced and received.  

Return orders are usually deleted after they are invoiced. When you post an invoice, it is transferred to the **Posted Purchase Credit Memo** window. If you selected the **Return Shipment on Credit Memo** check box in the **Purchases & Payable Setup** window, then the invoice is transferred to the **Posted Return Shipment** window. You can delete the documents using the **Delete Invd Purch. Ret. Orders** batch job. Before deleting, the batch job checks if the purchase return orders are fully shipped and invoiced.  

Blanket purchase orders are not deleted after you have processed and invoiced all the related purchase orders. You can delete blanket orders with the **Delete Invoiced Blanket Purchase Orders** batch job.  

Invoiced service orders are usually deleted automatically after having been fully invoiced. When an invoice is posted, a corresponding entry is created in the **Posted Service Invoices** window. The posted document can be viewed in the **Posted Service Invoice** window.  

Service orders are not deleted automatically, however, if the total quantity on the order has been posted not from the service order itself, but from the **Service Invoice** window. Then you may need to delete invoiced orders that were not deleted. You can do this by running the **Delete Invoiced Service Orders** batch job.  

## See Also
[Dynamics 365 Business Central](https://docs.microsoft.com/dynamics365/business-central/)  
[Setup and Administration in Dynamics NAV](admin-setup-and-administration.md)  
