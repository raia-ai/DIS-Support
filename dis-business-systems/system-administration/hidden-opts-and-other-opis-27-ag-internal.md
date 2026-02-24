---
title: "Hidden OPTs and other OPIs #27 – Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Hidden OPTs and other OPIs #27 – Ag Internal."
long_description: "This document provides internal system administration information about Hidden OPTs and other OPIs #27 – Ag Internal."
---

_Hidden OPTs and other OPIs #27 – AG Internal_

Introduction

 This is one of many articles providing Hidden OPTs and other OPIs. They are listed in alphabetical order by Option.

 Important! If a Hidden OPT created for a specific customer is applied to another customer, ensure the new customer knows that there will NOT BE any further modifications to the OPT.

  

 
 Option 

 
 Version 

 
 Set-By 

 
 OPT 

 
 Definition of Switch Setting 

 
 
 RESMATCH

 
 future

 
 Menu

 
 0

 
 Reservations are filled as they always have been according to the priorities above.

 
       
 1

 
 Reservations are filled directly from the orders that they were originally placed on.

 
           
 
 REVUNTSL

 
 future

 
 Menu

 
 0

 
 Any debit to a unit sale acct must be exact amt as orig sale

 
       
 1

 
 Unit sale reversal debit can be for any amount

 
           
 
 RNTCONT

 
 V8L5A

 
 Menu

 
 0

 
 Processing of contracts not allowed from Dispatching.

 
     
 X9

 
 1

 
 Processing of contracts allowed, default to 'N'.

 
       
 2

 
 Processing of contracts allowed, default to 'Y'.

 
           
 
 RENTRSRV

 
 future

 
 Menu

 
 0

 
 Do not restrict units pending sale

 
       
 1

 
 Restrict units pending sale with a soft warning message at POS and Equipment Rentals

 
       
 2

 
 Restrict units pending sale with a hard warning message at POS and Equipment Rentals

 
           
 
 RNTRTNd

 
 V8L5A

 
 Menu

 
 0

 
 Set unit to 'WL' when returned from rent.

 
     
 X9

 
 1

 
 Set unit to 'AV' when returned from rent.

 
         
 (The small d in the switch name indicates division, so the switch can be divisional.   Programs

 
         
  must concatenate the switch name with the division and then check the switch setting.)

 
           
 
 S360SCG1

 
 future

 
 Phone

 
 0

 
 S360 Sales Calls KPI Bar Graph 1 time frame is set to Today

 
       
 1

 
 S360 Sales Calls KPI Bar Graph 1 time frame is set to Yesterday

 
       
 2

 
 S360 Sales Calls KPI Bar Graph 1 time frame is set to Week-to-Date

 
       
 3

 
 S360 Sales Calls KPI Bar Graph 1 time frame is set to Last Week

 
       
 4

 
 S360 Sales Calls KPI Bar Graph 1 time frame is set to Month-to-Date

 
       
 5

 
 S360 Sales Calls KPI Bar Graph 1 time frame is set to Last Month

 
 
  

     
 6

 
 S360 Sales Calls KPI Bar Graph 1 time frame is set to 2 Months Ago

 
 
  

     
 7

 
 S360 Sales Calls KPI Bar Graph 1 time frame is set to Year-to-Date

 
           
 
 S360SCG2

 
 future

 
 Phone

 
 0

 
 S360 Sales Calls KPI Bar Graph 2 time frame is set to Today

 
       
 1

 
 S360 Sales Calls KPI Bar Graph 2 time frame is set to Yesterday

 
       
 2

 
 S360 Sales Calls KPI Bar Graph 2 time frame is set to Week-to-Date

 
       
 3

 
 S360 Sales Calls KPI Bar Graph 2 time frame is set to Last Week

 
       
 4

 
 S360 Sales Calls KPI Bar Graph 2 time frame is set to Month-to-Date

 
       
 5

 
 S360 Sales Calls KPI Bar Graph 2 time frame is set to Last Month

 
 
  

     
 6

 
 S360 Sales Calls KPI Bar Graph 2 time frame is set to 2 Months Ago

 
 
  

     
 7

 
 S360 Sales Calls KPI Bar Graph 2 time frame is set to Year-to-Date

 
           
 
 S360SCG3

 
 future

 
 Phone

 
 0

 
 S360 Sales Calls KPI Bar Graph 3 time frame is set to Today

 
       
 1

 
 S360 Sales Calls KPI Bar Graph 3 time frame is set to Yesterday

 
       
 2

 
 S360 Sales Calls KPI Bar Graph 3 time frame is set to Week-to-Date

 
       
 3

 
 S360 Sales Calls KPI Bar Graph 3 time frame is set to Last Week

 
       
 4

 
 S360 Sales Calls KPI Bar Graph 3 time frame is set to Month-to-Date

 
       
 5

 
 S360 Sales Calls KPI Bar Graph 3 time frame is set to Last Month

 
 
  

     
 6

 
 S360 Sales Calls KPI Bar Graph 3 time frame is set to 2 Months Ago

 
 
  

     
 7

 
 S360 Sales Calls KPI Bar Graph 3 time frame is set to Year-to-Date

 
           
 
 S360SCG4

 
 future

 
 Phone

 
 0

 
 S360 Sales Calls KPI Bar Graph 4 time frame is set to Today

 
       
 1

 
 S360 Sales Calls KPI Bar Graph 4 time frame is set to Yesterday

 
       
 2

 
 S360 Sales Calls KPI Bar Graph 4 time frame is set to Week-to-Date

 
       
 3

 
 S360 Sales Calls KPI Bar Graph 4 time frame is set to Last Week

 
       
 4

 
 S360 Sales Calls KPI Bar Graph 4 time frame is set to Month-to-Date

 
       
 5

 
 S360 Sales Calls KPI Bar Graph 4 time frame is set to Last Month

 
 
  

     
 6

 
 S360 Sales Calls KPI Bar Graph 4 time frame is set to 2 Months Ago

 
 
  

     
 7

 
 S360 Sales Calls KPI Bar Graph 4 time frame is set to Year-to-Date

 
           
 
 S360TAXC

 
 future

 
 Phone

 
 0

 
 Do not show the tax code description of a customer on the S360 Contacts landing page

 
       
 1

 
 Show the tax code description of a customer on the S360 Contacts landing page

 
           
 
 SCCLOSE

 
 future

 
 Menu

 
 0

 
 Do not prompt to close sales call when exiting

 
       
 1

 
 Prompt to close sales call when exiting

 
           
 
 SELLRNTL

 
 10800

 
 Menu

 
 0

 
 Do not restrict sale of units with 'RE' status

 
       
 1

 
 Restrict sale of RE status rental units at posting

 
       
 2

 
 Restrict sale of RE status rental units at posting and issue a soft warning at POS

 
       
 3

 
 Restrict sale of RE status rental units at posting and issue a hard warning at POS

 
         
 (NOTE:  When using Equipment Rentals opt setting 0 is not available.  Opt setting 1 is the default with 2 & 3 available)

 
           
 
 SERVHALL

 
 Future 

 
 Phone

 
 0

 
 Service History Report is for 1 division only.

 
       
 1

 
 Can request Service History Report for ALL divisions.

 
           
 
 SFISRV

 
 future

 
 phone

 
 0

 
 SFI Survey is not installed

 
       
 1

 
 SFI Survey is installed

 
           
 
 SHIPADDR

 
 10809

 
 Menu

 
 0

 
 Multiple Ship-To Addresses is not enabled.

 
       
 1

 
 Multiple Ship-To Addresses is enabled.

 
           
 
 SHIPREQ

 
 future

 
 menu

 
 0

 
 Shipto address is  optional

 
       
 1

 
 Shipto address if supplied must be established Ship-to location

 
       
 2

 
 Shipto address is required on ALL docs

 
       
 3

 
 Shipto address required and must be Ship-to location (established Ship-to location setup in Addr/Recv maint.

 
           
 
 SIGCAP

 
 11.2

 
  

 
 0

 
 Signature Capture Code has not been installed

 
       
 1

 
 Signature Capture Code has been installed

 
           
 
 SMSJMG

 
 V8L4A

 
 Menu

 
 0

 
 InquireUpdate Service Units:  When adding additional jobs do not use the model as the group code.

 
       
 1

 
 Inquire/Update Service Units: When adding additional jobs use the model as the group code.

 
           
 
 SNDUNTIF

 
 future

 
 phone

 
 0

 
 DISNET - Send unit information to DIS

 
       
 1

 
 DISNET - Do not send unit information to DIS