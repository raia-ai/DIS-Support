---
title: "Push CNH Operation Codes to a Dealer - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Push CNH Operation Codes to a Dealer - Ag Internal."
long_description: "This document provides internal system administration information about Push CNH Operation Codes to a Dealer - Ag Internal."
---

_Push CNH Operation Codes to a Dealer - AG Internal_

Issue 

 When a dealer purchases CNH Operation codes, it is easier to get them started if they already have the Operation Codes in place. The easiest way to do that is to push the unzipped DISKSOCNH file over to the dealer’s IFS. 

  

 Solution  

 Download the file locally and \ drag and drop it into the dealer’s IFS. 

 Connect to ASAP and verify your hosts file is pointing to 172.16.16.80. 

   

 Important ! It’s critical the host file is pointing to 172.16.16.80. It the file unzips to the wrong IP it could load the codes at the wrong dealer or crash backup for an unsuspecting dealer. 

 Download the file from the WebLockers. 

   

 The file will unzip to \\keystone\keystone\Business_system_update. 

   

 Once the file unzips this window will close. 

 Open \\172.16.16.80\keystone\business_system_updates and open the same folder on the dealer’s IFS. 

   

 Drag and drop the file into the dealer’s IFS. 

 Verify the file transferred successfully in Apply Enhancements (X6-9). It will load with the next unattended backup. 

 Note : You do not need to queue or sequence the file. It will apply regardless. This is simply a window into the IFS. (If you are applying other code, queue it LAST as a rule.) 

   

 Verify the CNH Operation Codes loaded after the next unattended backup. Type call x00072cl in a command line and go into Inquire/Update Service Units (Service Management | Inquire/Update Service Units). 

 KSOCNH should be listed here. Alternatively, you can connect with Keystone or Quantum to see if the new CNH Operations button displays.