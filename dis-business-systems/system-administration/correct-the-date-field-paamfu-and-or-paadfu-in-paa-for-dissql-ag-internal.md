---
title: "Correct the date field PAAMFU and/or PAADFU in PAA for DISSQL - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Correct the date field PAAMFU and/or PAADFU in PAA for DISSQL - Ag Internal."
long_description: "This document provides internal system administration information about Correct the date field PAAMFU and/or PAADFU in PAA for DISSQL - Ag Internal."
---

_How to correct the date field PAAMFU and/or PAADFU in PAA for DISSQL - Ag Internal_

Issue:
 If a DISSQL will not run when trying to select or update the PAAMFU field,
it could be because some of the records have 404040404040 instead of the   
number 0 on the unmerged records.                                          
To correct, the DISMFU fields need to be initialized to 0 on the records   
which have not been merged.                                                
There is the same problem with the merge date field, PAADFU.      
  
 Solution:
 Run this SQL to correct to correct the merge month field, PAAMFU on the 
records which are 404040404040 instead of 0.                            
     DISSQL REQUEST('UPDATE PAA SET PAAMFU = 0 WHERE                    
     HEX(PAAMFU) = ''404040404040''')       
  
 Run this SQL to correct to correct the merge date field, PAADFU on the
records which are 4040404404004040 instead of 0.                      
     DISSQL REQUEST('UPDATE PAA SET PAADFU = 0 WHERE                  
     HEX(PAADFU) = ''4040404040404040''')                                       
  
      
 SC400 A03413