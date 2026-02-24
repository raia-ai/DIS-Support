---
title: "Force Sales Ranking Job to Run Immediately - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Force Sales Ranking Job to Run Immediately - Ag Internal."
long_description: "This document provides internal system administration information about Force Sales Ranking Job to Run Immediately - Ag Internal."
---

Issue 

 Customer has changed their Sales Ranking Configuration and wants the changes to be made / run the report immediately. 

  

 Solution: Force the Sales Ranking Job to Run Immediately 

 The following process updates the Sales Ranking report, M360 Parts Contribution, M360 Service Contribution, and the C360 overall ranking. Complete the following steps instead of waiting for the 7pm job to fire off to recalculate everything.  

 Select AS/400 Command Line (System | AS/400 Command Line). 

 

 Type CHGDTAARA DISFILES/XQCLP00602 in the Command Line and click OK . 

 

 Type 19:00:00 I in the New Value field and click Enter to save. 

 Select AS/400 Command Line (System | AS/400 Command Line). 

 

 Type WRKACTJOB SBS(QSYSWRK) in the Command Line and click OK . 

 

 Select the QDISXQRNK job under that subsystem and click End to stop the job. 

 

 Click Enter to confirm that you want to end the job. 

 Sign off your session, then sign back on. The job runs immediately. 

 Open a Command Line, type DSPDTAARA DISFILES/XQCLP00602 , and click OK to see the current value of the Sales Ranking configuration.