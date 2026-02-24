---
title: "Change ECC Workstation Names on the Server with SQL Command - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Change ECC Workstation Names on the Server with SQL Command - AG Internal."
long_description: "This document provides internal system administration information about Change ECC Workstation Names on the Server with SQL Command - AG Internal."
---

Issue 

 Customer wants to transfer ECC settings from one PC to another PC.

 We get requests from time to time to change ECC on a PC that died to another PC and then back again.  Changing the name for every transaction in every division can be time consuming.

  

 Solution 

 Use the SQL command below to change the workstation name globally.  Note this is system wide. Copy and paste into notepad.  Make the change.  Copy and paste on the 2 nd line in DISSQL

 DISSQL (F4)                                                            

 update disfiles/mfgparmd set CTPDEV='newdevice' where CTPDEV='olddevice' 

   

 Example 

 DISSQL (F4)                                                             

 Update disfiles/mfgparmd set CTPDEV='DCQUI622' where CTPDEV='DCNH1892'

 This example is for the actual PC name which may be what you need to do. The most common, these days, is changing the workstation name to CSPS. Just substitute CTPDEV=’CSPS’