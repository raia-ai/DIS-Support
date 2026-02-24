---
title: "Setup and Enable Direct Deposit - Keystone (Ag Internal)"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Setup and Enable Direct Deposit - Keystone (Ag Internal)."
long_description: "This document provides internal system administration information about Setup and Enable Direct Deposit - Keystone (Ag Internal)."
---

_Setup and Enable Direct Deposit - Keystone (AG Internal)_

Introduction 


  

 Before You Begin 


 Select Laser Forms Configuration (Security |Laser Forms Configuration) . 


 Type the laser printer ID in the Default Printer field (P1 for instance). 

  

 To Setup Direct Deposit 






 Type the bank name the employee will use for direct deposit in the Bank Name field. 

 Type the routing number for the employee’s bank account in the routing number field. 

 Type the bank account number to be used for direct deposit in the bank account field. 

 Select Checking or Savings to designate the account type for direct deposit. 

  

 Additional Information Regarding Direct Deposit 




  

 Direct Deposit Upload File 

 During processing, Direct Deposit records are added to a CSV (comma separated value) data file named  X13_DIR_DEP.csv, which will be copied to the AS/400 IFS in the following path:  \\Keystone\Keystone\Export\ "as400 user signon" \.  If the file already exists, it will be overwritten during the next direct deposit batch. 

 WARNING: The CSV file is not secured. It must be manually copied from the IFS to your local PC. As soon as possible, it must be deleted manually from the IFS directory to ensure that no unauthorized person will have access to the file.  This can be done through Windows Explorer. 

 The clerk will then be able to log onto the Internet portal provided by the ACH (Automated Clearing House) such as FreedomWare. After the file is uploaded, the information will be processed to create and transfer the direct deposit transactions from the dealership's bank account to each employee's bank account. You will be able to review a log of transactions on the ACH's internet portal. The ACH will furnish all the information you need to be successful. 

  

 Verification Reports 

 The dealership will receive a verification report indicating the transactions that have been made for direct deposit. In addition, it receives a list of the employees whose transactions could not be processed or verified because of incorrect routing or account numbers. 

 If there are accounts that could not be verified, FreedomWare will notify the dealership by email. If there aren't any errors in the batch, a report will not be generated.  

 If the bank rejected the transaction, it may be due to issues with the account numbers on the .CSV file. See Troubleshoot Direct Deposit Rejection by Bank   for more information.