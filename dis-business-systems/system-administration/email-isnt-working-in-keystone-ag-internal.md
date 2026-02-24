---
title: "Email Isn't Working in Keystone - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Email Isn't Working in Keystone - AG Internal."
long_description: "This document provides internal system administration information about Email Isn't Working in Keystone - AG Internal."
---

_Email Isn't Working in Keystone - AG Internal_

Issue 

 User can't Email from Keystone. They're Receiving iSeries cannot install pending reboot message and are unable to install iSeries access (client access). 

  

 Tried 

 Disabled Windows firewalls and set Outlook to run as administrator.  Client Access isn't installed - downloaded DIS component file - installation fails keeps requesting a reboot. Checked for the IBM folder & WOW folder - not installed - rebooted several times - no go. 

  

 Solution 

 Delete the pending reboot files in 

 "HKLM\SYSTEM\CurrentControlSet\Control\Session Manager" "PendingFileRenameOperations" 

 Install Iseries access 

 Set Keystone to run as administrator 

 Install EasyFile