---
title: "Payables Out of Balance SQL - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Payables Out of Balance SQL - Ag Internal."
long_description: "This document provides internal system administration information about Payables Out of Balance SQL - Ag Internal."
---

_Payables Out of Balance SQL - AG Internal_

Payables Out of Balances are often caused by merge issues.  Here are steps to find the check number causing the issue 

  

 First run this                                                              
 DISSQL REQUEST('SELECT PAACHK, SUM(PAAAMT) FROM PAA WHERE PAACHK <> '' ''   
 GROUP BY PAACHK ORDER BY PAACHK') OUTPUT(*OUTFILE) OUTFILE(QS36F/PAATMP)    
 --                                                                          
 Then this:                                                              
 DISSQL REQUEST('select * from paatmp where SEL1 <> 0')                      
 --                                                                          
 With any luck, the problem transactions will be exposed.                     
                      
 *** Modification ideas***                                                   
 To look at a specific GL account.                                           
 Call QCMD  (enter)                                                          
 DISSQL REQUEST('SELECT PAACHK, SUM(PAAAMT) FROM PAA WHERE PAACHK <> '' ''   
  AND PAAACT = ''A20000'' GROUP BY PAACHK ORDER BY PAACHK')                  
 OUTPUT(*OUTFILE) OUTFILE(QS36F/PAATMP)                                      
 --then                                                                      

 DISSQL REQUEST('select * from paatmp where SEL1 <> 0')                         
 --                                                                             
 How to look at details of one check number.                                    
 DISSQL REQUEST('select * from paa where PAACHK = ''1234567890''')              
 be careful of spacing on the check number.  Checks created in the system often 
 have spaces before and after the check number.  ex: '   12345  ' for check     
 number 12345 written by the system.                                            
 --                                                                             
                                                                                

 SC400: A03323