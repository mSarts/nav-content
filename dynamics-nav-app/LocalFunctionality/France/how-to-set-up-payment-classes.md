---
    title: How to Set Up Payment Classes
    description: To use payment management, you must set up payment classes to define operation types, such as bills of exchange, electronic payments, or checks.

    documentationcenter: ''
    author: SorenGP

    ms.prod: "dynamics-nav-2018"
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 07/01/2017
    ms.author: edupont

---
# How to: Set Up Payment Classes
To use payment management, you must set up payment classes to define operation types, such as bills of exchange, electronic payments, or checks.  

## To set up a payment class  

1.  Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Slip Setup**, and then choose the relevant link.  
2.  In the **Payment Class** window, choose the **New** action.  
3.  Fill in the fields as described in the following table.  

    |Field|Description|  
    |---------------------------------|---------------------------------------|  
    |**Enable**|Select to enable usage of the payment class.|  
    |**Code**|The unique identification code for the payment class.|  
    |**Name**|The payment class description.|  
    |**Header No. Series**|The number series code for the payment slip header.|  
    |**Line No. Series**|The number series code for the payment slip lines. If you leave this field blank, the number for each payment line is created based on the payment header number.|  
    |**Suggestions**|The type of payment proposals that can be created automatically on a payment slip.|  
    |**Unrealized VAT Reversal**|Specify the method to handle unrealized VAT.<br /><br /> If you select **Application**, VAT will be realized when you post the invoice application and payment application.<br /><br /> If you select **Delayed**, you must define the payment step during which VAT must be realized, by selecting the **Realize VAT** field in the **Payment Step Card** window. For more information, see Realize VAT and Payment Step.|  
    |**SEPA Transfer Type**|Specify the SEPA export format, either **Credit Transfer** or **Direct Debit**.|  

4.  Choose the **OK** button.  

## See Also
[Dynamics 365 Business Central](https://docs.microsoft.com/dynamics365/business-central/)  
[Payment Management](payment-management.md)   
 [How to: Set Up Payment Statuses](how-to-set-up-payment-statuses.md)   
 [How to: Set Up Payment Steps](how-to-set-up-payment-steps.md)   
 [How to: Set Up Payment Addresses](how-to-set-up-payment-addresses.md)   
 [How to: Export or Import Payment Management Setup Parameters](how-to-export-or-import-payment-management-setup-parameters.md)   
 [How to: Create Payment Slips](how-to-create-payment-slips.md)   
 [How to: Post Payment Slips](how-to-post-payment-slips.md)   
 [How to: Archive Payment Slips](how-to-archive-payment-slips.md)
