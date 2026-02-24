---
title: "MyAccount - Resending Data to Middle Tier - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about MyAccount - Resending Data to Middle Tier - Ag Internal."
long_description: "This document provides internal system administration information about MyAccount - Resending Data to Middle Tier - Ag Internal."
---

_My Account - Resending Data to Middle Tier - AG Internal_

If asked to resend data to the middle tier for a customer, for My Account,  here are the two commands that can be used while logged on the customers system.  

 The command used will depend on the kind of information that needs to be resent.  If you are not sure please ask.  Generally Ken Guy or Major Mally might be the ones asking for this type of action.   

  

 NOTE: It is important to select Initial load = Y if we do not want emails to be sent to the customers customer for each invoice being resent. 

  

  

 The commands related to this are: 

 MA_INVOICE then F4 (to pull up a specific customer and try to resend individual documents.) 

                 

 And 

 MA_RESEND then F4 (allows you to send all transactions for a specific customer or all or a number of days.)