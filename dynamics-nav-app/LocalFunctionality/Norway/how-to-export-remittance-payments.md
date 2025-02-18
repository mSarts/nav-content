---
    title: How to Export Remittance Payments
    description: You can use the export remittance payments process to export the payments file to your computer.

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
# How to: Export Remittance Payments
You can use the export remittance payments process to export the payments file to your computer. You can then transfer the remittance payments to the bank.  

> [!IMPORTANT]  
>  Before you can export a remittance payment, you must select a payment format in the **Payment Export Format** field in the **Bank Account Card** window.  

You export payments to a bank file by choosing the **Export Payments** button in the **Payment Journal** window. The process may be different, depending on the export format that you select:  

- Payments using the SEPA payment standard are directly exported to a file when you choose the **Export Payments** button. For more information, see [Making Payments](../../payables-make-payments.md).  

- Payments using local payment standards, such as **Telepay**, are exported with either the **Remittance - export (bank)** or the **Remittance - export (BBS)** report, which automatically opens when you choose the **Export Payments** button.  

The procedure for exporting payments using the **Remittance – Export** batch job is described in this topic.  

## To export remittance payments using the Remittance - Export batch jobs  

1.  Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Journals**, and then choose the related link.  
2.  Prepare to export the payments from the journal. For more information, see [How to: Export Payments to a Bank File](../../payables-how-export-payments-bank-file.md).  
3.  Choose the **Export Payments** action.  
4.  In the report window that opens, choose the **Options** FastTab, and fill in the fields as described in the following table.  

    |Field|Description|  
    |---------------------------------|---------------------------------------|  
    |**Remittance agreement code**|Specify the code for the agreement.|  
    |**Operator**|Specify the operator number.|  
    |**Password**|Specify the password for the payments.|  
    |**Division**|Specify the division that is paying remittance.|  
    |**Current note**|Specify a note for the payment.|  
    |**Filename**|Specify the name and directory of the payment file.|  

5.  Choose the **OK** button.  

The payment information is exported to the file that is set up in the remittance agreement.  

The payment journal is deleted and the transactions are transferred to the waiting journal.  

## See Also
[Dynamics 365 Business Central](https://docs.microsoft.com/dynamics365/business-central/)  
[Electronic Payments to Vendors in Norway](electronic-payments-to-vendors-in-norway.md)   
 [How to: Set Up Remittance Agreements](how-to-set-up-remittance-agreements.md)   
 [How to: Create Remittance Accounts](how-to-create-remittance-accounts.md)   
 [How to: Set Up Vendors for Remittance](how-to-set-up-vendors-for-remittance.md)   
 [Recipient Reference Codes](recipient-reference-codes.md)   
 [How to: Create Remittance Suggestions](how-to-create-remittance-suggestions.md)   
 [How to: Create Manual Remittance Payments](how-to-create-manual-remittance-payments.md)   
 [How to: Set Up Payment Line Information](how-to-set-up-payment-line-information.md)   
 [How to: Test Remittance Payments](how-to-test-remittance-payments.md)   
 [Types of Payment Returns Files](types-of-payment-returns-files.md)   
 [How to: Import Payment Return Data](how-to-import-payment-return-data.md)   
 [How to: Delete Remittance Payment Orders](how-to-delete-remittance-payment-orders.md)   
 [Remittance Errors](remittance-errors.md)   
 [How to: View Remittance Error Codes](how-to-view-remittance-error-codes.md)   
 [How to: Cancel Payments](how-to-cancel-payments.md)
