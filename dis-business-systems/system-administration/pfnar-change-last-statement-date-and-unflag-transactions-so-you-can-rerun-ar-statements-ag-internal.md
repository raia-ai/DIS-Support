---
title: "PFNAR - Change Last Statement Date and Unflag transactions so you can rerun AR Statements - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about PFNAR - Change Last Statement Date and Unflag transactions so you can rerun AR Statements - Ag Internal."
long_description: "This document provides internal system administration information about PFNAR - Change Last Statement Date and Unflag transactions so you can rerun AR Statements - Ag Internal."
---

_PFNAR - Change Last Statement Date and Unflag transactions so you can rerun AR Statements - AG Internal_

Change Last Statement Date & unflag transactions- PFNAR 
  
 Introduction 
 The PFNAR procedure changes Receivables Last Statement date, unflags previously printed transactions and allows you to run statements again from a previous date.   
   
 PFNAR is a divisional job. 
 It does not require a dedicated system. 
 It prints a report of all the transactions it unflags. 

   
 Steps to run PFNAR 
 Type PFNAR [Enter] at an AS/400 Command line 
 Enter the date in YYMMDD format 

 NOTE: Typically you would use the date of the last statement run for the prior month.  
 You can look in archiving to try to determine the date statements were ran.