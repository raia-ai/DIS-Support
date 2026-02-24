---
title: "Push DBST Update to a Dealer - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Push DBST Update to a Dealer - Ag Internal."
long_description: "This document provides internal system administration information about Push DBST Update to a Dealer - Ag Internal."
---

_Push DBST Update to a Dealer - AG Internal_

Issue 

 A dealer is having difficulties downloading the monthly DBST update or the automatic update during backup is not working (assuming the option is enabled). 

   

 Solution 

 Navigate to ASAP, where uncompressed DBST files are stored in the IFS. 
 Click the Windows button. 

 

 Type \\172.16.16.80.  Access the Keystone folder, then navigate to the DBST folder. 

  

 Retrieve the dealer's IP address from vLink and follow the same steps as mentioned in step 2 . 

 

  

 Click the Windows button, type the dealer's IP, and access the Keystone folder, then the DBST folder. Drag and drop the file from ASAP to the dealer’s IFS. 

 

 Once you can view the file in the IFS, verify it in Quantum. 

 

 Select Tax Code Maintenance (POS | Table Maintenance | Tax Configuration | Tax Code Maintenance). You'll notice the pending update. 

 Note that it will update during backup. Applying it on-the-fly is not possible. If the dealer has multiple file sets, performing this process once is sufficient, as all file sets will update accordingly.