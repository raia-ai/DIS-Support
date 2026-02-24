---
title: "Prework and Considerations before Changing Fiscal Start Month - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Prework and Considerations before Changing Fiscal Start Month - Ag Internal."
long_description: "This document provides internal system administration information about Prework and Considerations before Changing Fiscal Start Month - Ag Internal."
---

Introduction 

 This document provides prework to complete before changing the fiscal start month as well as aspects that should be considered. 

  

 Prework and Considerations 

 If there is more than one division and combined financial statements are needed, all divisions need to change the fiscal start. 
 If Budgeting is used, then the information needs to be re-entered. Save a copy of everything needed in Excel BEFORE changing the fiscal start. 
 Run all the old financials that are needed BEFORE changing the fiscal start.  Once changed, all financials (old and new) will use the new fiscal start to format the year. Run the same reports run for Accounting EOY . 
 Run financial Data Mines for all previous years BEFORE changing the fiscal start. 

 Contact the DIS Support Team to have Data Mine synced to your financials and ensure information from previous years are resynced. 
 Internal SUPPORT Note : To reorg Data Mine financials DMGLFIX- Before reconverting Datamine files, please make copies of DMGLDET and DMGLSUM.  The reason this needs to be done- The fiscal periods will be different in the DMGLSUM file. The best thing would be to not recalculate so a full recalculate and just do the last 25 months in +current in DMGLSUM.  So just run DMGLFIX, not PFDMCNV. 

 Comparative income statements will not be available for a year after changing fiscal month. 
 Considering the timing of the new fiscal start in the calendar year, determine whether it will be a long year or a short year.