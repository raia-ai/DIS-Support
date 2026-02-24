---
title: "CNH Credit Card Timing Out - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about CNH Credit Card Timing Out - Ag Internal."
long_description: "This document provides internal system administration information about CNH Credit Card Timing Out - Ag Internal."
---

_CNH Credit Card Timing Out - AG Internal_

Issue 

 

 When performing a CNH credit card promo lookup the following message is received: 

 Timeout-Stop/Start ECC on transmitting PC 

 If this process completes for other tickets, the issue may be due to the process not being able to finish within the default 2 minute time out setting because of the size of the work order. 

 This issue can be resolved by adjusting the CNH credit card time out value. 

  

 Solution 

 Open a command line, type CHGTIMOUT (F4), and click OK . 

 

 The default is 120 seconds. You can change it to 300 seconds to extend the window to 5 minutes. After the promo lookup completes, set the timeout value back to 120 to ensure proper timeout if ECC is actually down. 

  

 T imeout values for Century, Gravity, CSPS and Polaris may be adjusted through this menu as well.