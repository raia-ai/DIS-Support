---
title: "How to pull a list of all customers with a credit card on file - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about How to pull a list of all customers with a credit card on file - Ag Internal."
long_description: "This document provides internal system administration information about How to pull a list of all customers with a credit card on file - Ag Internal."
---

_How to pull a list of all customers with a credit card on file - AG Internal_

How to pull a list of all customers with a credit card on file 

 
You can use this SQL to get a list of all customers with a credit card saved on their account.

 CALL QCMD                                                                     
F11 and then copy/paste each line separately:                                        

 DISSQL REQUEST('SELECT ABB7TX, F0AQCD, F0O3CD, ABBPTX, ABBRTX, ABBTTX,       

 ABBUTX FROM RCC, ADM WHERE F0O3CD  = ''CC'' and ABB7TX = ''E'' AND F0AQCD =  

  ABAQCD ORDER BY F0AQCD') OUTPUT(*PRINT)                                     

 -                                                                            

 note:                                                                 
F0O3CD  = ''CC''        (credit card code)                                         
ABB7TX = ''E''          (division)                                           

 -                                                                             

 Here is another option that prints the expiration date too.                

 DISSQL REQUEST('SELECT ABB7TX, F0AQCD, F0O3CD, F0S9NB, ABBPTX, ABBRTX, ABB  
TTX, ABBUTX FROM RCC, ADM WHERE F0O3CD  = ''CC'' AND ABB7TX = ''A'' AND F0AQCD 
= ABAQCD ORDER BY F0AQCD') OUTPUT(*PRINT) PRTFILWID(150)