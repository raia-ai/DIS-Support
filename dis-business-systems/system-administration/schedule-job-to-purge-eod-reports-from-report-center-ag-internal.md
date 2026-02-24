---
title: "Schedule Job to Purge EOD Reports from Report Center - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Schedule Job to Purge EOD Reports from Report Center - Ag Internal."
long_description: "This document provides internal system administration information about Schedule Job to Purge EOD Reports from Report Center - Ag Internal."
---

_Schedule Job to Purge EOD Reports from Report Center - AG Internal_

Issue 

 The End of Day reports generated from the Accounting and Parts End of Day jobs are automatically sent to the report center where they are accumulating and tying up the report center. 

  

 Solution 

 
The DLTEODDSPLF job can be scheduled to automatically purge these reports. 

 Open a command line ( ALT + A keys), type WRKJOBSCDE , and click OK . The Work with Schedule Entries screen displays. 

 Press F6 on your keyboard. The Add Job Schedule Entry screen displays. Configure the job as shown below. 

   

 Enter the Command DLTSPLF FILE(*SELECT) SELECT(DISBACK P NP ) in the Command box changing  the P to the File Set and NP to the default printer assigned to the reports. 

 Set the job to run *Weekly on *Sun at 06:00:00.