---
title: "LPR Printer Start Command Produces Error Message - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about LPR Printer Start Command Produces Error Message - AG Internal."
long_description: "This document provides internal system administration information about LPR Printer Start Command Produces Error Message - AG Internal."
---

_LPR Printer Start Command Produces Error Message - AG Internal_

Issue 

 If the Start Command ( STRRMTWTR Px ) for an LPR printer results in the error message 

 Output queue Px has RMTSYS specified as *NONE 

 it is probably a result of the output queue Remote System value NOT being configured as an LPR device. 

 The Remote System must be *INTNETADR  for LPR devices. 
 For all other printer device descriptions, the Remote System is specified as *NONE . 

 This usually occurs when systems have been reloaded or a customer upgrades to LPAR (The Cloud). During the upgrade process, the device descriptions are copied over from the old system, but the output queues are not copied. The AS/400 then automatically creates an output queue for all the printer devices with the Remote System value specified as *NONE. For *LAN and KPS devices this isn’t an issue, but if LPR output queues aren’t assigned the *INTNETADR value, this error occurs when starting the remote writer. 

  

 Solution 

 Supposing P3 is the faulty printer: 

 Place any jobs in the P3 output queue on hold and move them to another output queue. Note which ones are moved as they will be moved back later in this process. 
 Delete the P3 device description. Because the print writer is not started and there are no jobs in the P3 output queue, both the device description and output queue will be de deleted. 
 Recreate P3 using the DISCRTLPR  command. 
 Move the jobs back to P3. 
 Release the jobs in the P3 output queue.