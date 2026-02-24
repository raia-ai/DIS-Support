---
title: "Error Message/AGCO Orders Don’t Display on AGCO Side - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Error Message/AGCO Orders Don’t Display on AGCO Side - AG Internal."
long_description: "This document provides internal system administration information about Error Message/AGCO Orders Don’t Display on AGCO Side - AG Internal."
---

_Error Message/AGCO Orders Don’t Display on AGCO Side - AG Internal_

Issue 

 Orders placed through AGCO communications show orders were successful when looked at through ECC & ECM logs, but the order does not show on the AGCO side 

  

 Solution 

 This issue may be a result of AGCO installing AGCO Solutions online and/or the path being set as C:\AGCO\PARTDATA\ORDERSTABLES. 

 The path MUST be set to C:\AGCO\PARTDATA\ORDERS in Interface manager or Agco solutions | tools | Parts orders | Miscellaneous | Location of order files) on the PC. The IM and AGCO solutions must be pointing to that path in order for the order to be successful.