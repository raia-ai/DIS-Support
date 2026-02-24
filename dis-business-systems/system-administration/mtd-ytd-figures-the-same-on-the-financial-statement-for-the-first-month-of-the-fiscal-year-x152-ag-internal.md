---
title: "MTD & YTD figures the same on the financial statement for the first month of the fiscal year X152 - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about MTD & YTD figures the same on the financial statement for the first month of the fiscal year X152 - Ag Internal."
long_description: "This document provides internal system administration information about MTD & YTD figures the same on the financial statement for the first month of the fiscal year X152 - Ag Internal."
---

_MTD & YTD figures the same on the financial statement for the first month of the fiscal year X152 - Ag Internal_

Issue 

 There is a lot of confusion regarding the financial statement for the first month of the 
 fiscal year.  There is not a set rule for what is displayed but the rules are  
 in the solution text.  Note, these apply to the financial statement only and   
 should not be applied to other financial reports.                              

  

 Solution 

 The MTD is arbitrarily set to the YTD value if:                              
 The report is for the first month of the fiscal year AND that same month     
 is either the oldest open or is closed.  In other words, even though the     
 report is for the first month of the fiscal year, if the month is still open 
 but it is not the OLDEST open for that division then the MTD will not be     
 adjusted.                                                                    
 In the situation where they have closed the last month of their fiscal year  
 but have not run eoy, mtd & ytd will be equal and both be 13 months worth of 
 information.                                                                 

  

 From SC400 A02499