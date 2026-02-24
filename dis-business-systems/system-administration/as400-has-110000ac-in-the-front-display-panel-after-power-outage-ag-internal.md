---
title: "AS400 has 110000AC in the front display panel after power outage - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about AS400 has 110000AC in the front display panel after power outage - AG Internal."
long_description: "This document provides internal system administration information about AS400 has 110000AC in the front display panel after power outage - AG Internal."
---

_AS400 has 110000AC in the front display panel after power outage - AG Internal_

Issue 

 AS400 has a flashing on and off green light, an exclamation point and 110000AC in the front display. 

  

 Solution 

 Press and hold the white power button on the front of the AS400 for 4 seconds, then let go.  

 This will start an IPL.  

  

 You should see C###'s on the front panel as the IPL is happening.  This process will take about 15 minutes to complete.  

  

 When IPL is complete you should see 01 BN in the front panel and the green light will be solid. 

  

 Note : Thinks will be a little slow once the system is backup as the AS400 will still be starting things up in the background.