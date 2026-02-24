---
title: "SQL for credit card codes for specific addr#, division, credit card code and default fields - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about SQL for credit card codes for specific addr#, division, credit card code and default fields - AG Internal."
long_description: "This document provides internal system administration information about SQL for credit card codes for specific addr#, division, credit card code and default fields - AG Internal."
---

_SQL for credit card codes for specific addr#, division, credit card code and default fields - AG Internal_

There are a couple ways to do this dependent on if the customer want a division code included. 

  

 Addr#, Credit card code, default field 

  

 Go to a command line and paste each line in separately. 

  

 DISSQL REQUEST('select F0AQCD,F0O3CD,F0MUST from RCC where F0O3CD = ''FP'' ') OUTPUT(*PRINT)                                                         

  

  

  

 Division, Addr#, Credit card code, default field 

  

 CALL QCMD  enter

 Then paste each line below separately.

  

 DISSQL REQUEST('SELECT ADM.ABB7TX,RCC.F0AQCD,RCC.F0O3CD,RCC.F0MUST FROM 

 RCC INNER JOIN ADM ON RCC.F0AQCD = ADM.ABAQCD

 WHERE RCC.F0O3CD = ''CC''') OUTPUT(*PRINT)