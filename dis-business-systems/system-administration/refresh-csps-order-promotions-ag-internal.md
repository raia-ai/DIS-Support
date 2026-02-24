---
title: "Refresh CSPS Order Promotions - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Refresh CSPS Order Promotions - Ag Internal."
long_description: "This document provides internal system administration information about Refresh CSPS Order Promotions - Ag Internal."
---

_Refresh CSPS Order Promotions - AG Internal_

Refresh CSPS Order Promotions  

 All of the CSPS Configuration Data such as Warehouses, Order Types etc. can be refreshed or updated on-the-fly by going to Manufacturers Menu > CNH Communications Menu > Refresh Configuration Data. Select a category and then click CNH Update. 

  

 CSPS Promotions take a long time to update so they are not updated this way. Instead they are updated by a scheduled job that runs every Saturday at 4AM Typically Promotions take effect the 1st if the month. So, depending on how the first Saturday of the month falls, you may be a need to update Promos before the scheduled job runs. 

  

 There are two ways to update CSPS Promos: 

  

 The first way is from a command line. Type CALL CSPSPROUPD. This command will update the promotions file (SUPPORT or QSECOFR only). This is an interactive job. It will tie up a session and can take hours to run. Also, if VPN drops you’ll have to start over. 
 The second way is by updating the CSPS_NXTUP data area. This data area controls when the weekly update of the promo codes runs. 

  

 To update it type WRKDTAARA CSPS_NXTUP and take a 2 to Change. 

     

 The data area value is CCYYMMDDHHMMSS, so for example, you would change it to ‘20210204040000’ to have it run at 4AM on 2/4/2021. 

   

 Press enter, then F3 to exit back to the menu.