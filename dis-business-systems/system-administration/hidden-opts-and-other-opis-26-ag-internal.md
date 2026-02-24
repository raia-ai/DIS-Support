---
title: "Hidden OPTs and other OPIs #26 – AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Hidden OPTs and other OPIs #26 – AG Internal."
long_description: "This document provides internal system administration information about Hidden OPTs and other OPIs #26 – AG Internal."
---

_Hidden OPTs and other OPIs #26 – AG Internal_

Introduction

 This is one of many articles providing Hidden OPTs and other OPIs. They are listed in alphabetical order by Option.

 Important! If a Hidden OPT created for a specific customer is applied to another customer, ensure the new customer knows that there will NOT BE any further modifications to the OPT.

  

 
 Option 

 
 Version 

 
 Set-By 

 
 OPT 

 
 Definition of Switch Setting 

 
 
 PYRLPURC

 
 V7L3

 
 Tape

 
 0

 

 
       
 1

 

 
           
 
 PYVACCHK

 
 V7L3

 
 Menu

 
 0

 

 
       
 1

 

 
       
 2

 

 
           
 
 QM360UIE

 
 future

 
 phone

 
 0

 
 include both ‘F’ status and ‘R’ status units in M360 Unit Inventory KPI

 
 
  

     
 1

 
 include ‘F’ status but exclude ‘R’ status units in M360 Unit Inventory KPI

 
       
 2

 
 exclude ‘F’ status but include ‘R’ status units in M360 Unit Inventory KPI

 
       
 3

 
 exclude both ‘F’ status and ‘R’ status units in M360 Unit Inventory KPI

 
           
 
 QM360GBU

 
 future

 
 phone

 
 0

 
 full monthly budget, annual budget cut off as of end of the month in M360 GL KPI

 
       
 1

 
 full monthly budget, full annual budget in M360 GL KPI

 
       
 2

 
 prorated monthly budget, prorated annual budget in M360 GL KPI

 
           
 
 QUEBECPR

 
 future

 
 Phone

 
 0

 

 
       
 1

 

 
           
 
 RECAGECR

 
 10801

 
 Menu

 
 0

 
 Do not Age Credits.

 
       
 1

 
 Age Credits.

 
           
 
 RECAGEIN

 
 2.2

 
 Menu

 
 0

 
 Age interest transactons

 
       
 1

 
 Keep interest transactions current

 
           
 
 RECAGEOD

 
 10801

 
 Menu

 
 0

 
 Do not Calculate Aging on Day in Advance at EOD.

 
       
 1

 
 Calculate Aging on Day in Advance at EOD.

 
           
 
 RECBFD

 
 2.2

 
 Menu

 
 0

 
 Do not Automatically Distribute Payments to Balance Forword Customers

 
       
 1

 
 Automatically Distribute Payments to BFD Cust.

 
           
 
 RECCRP

 
 10801

 
 Menu

 
 0

 
 Receivables Corporate Address Functions Inactive

 
       
 1

 
 Receivables Corporate Address Functions Active

 
           
 
 RECCU11A

 
 2.3

 
 Menu

 
 0

 
 Age non-printed transactions normally

 
       
 1

 
 Always treat non-printed transactions as current

 
           
 
 RECDEPRP

 
 10801

 
 Menu

 
 0

 
 Print Both A.R. Payments and G/L Transaction Reports.

 
       
 1

 
 Print only A.R. Payments Report.

 
       
 2

 
 Print only G/L Transaction Report.

 
           
 
 RECDTFMT

 
 10801

 
 Menu

 
 0

 
 Receivables Statement Date Format = MMDDYY.

 
       
 1

 
 Receivables Statement Date Format = YYMMDD.

 
       
 2

 
 Receivables Statement Date Format = DDMMYY.

 
           
 
 RECDVROL

 
 2.3

 
 Menu

 
 0

 
 Receivables Rolodex is not restricted by division

 
       
 1

 
 Receivables Rolodex is restricted to divisional

 
           
 
 RECFUTUR

 
 2.2

 
 Menu

 
 0

 
 Do not future age receivable transactions with delayed interest

 
       
 1

 
 Future age receivable transactions with delayed interest

 
     
 phone

 
 2

 
 Avenue Farm Custom Aging Rules

 
           
 
 RECINTPR

 
 10801

 
 Menu

 
 0

 
 Print Total Outstanding Interest.

 
       
 1

 
 Print Current Interest.

 
           
 
 RECPDEDE

 
 10801

 
 Menu

 
 0

 
 Do not Display Description from Preceeding Payment

 
       
 1

 
 Display Description from Preceeding Payment.

 
           
 
 RECPDNDE

 
 10801

 
 Menu

 
 0

 
 Do not Display Document # from Preceeding Payment

 
       
 1

 
 Display Document # from Preceeding Payment.

 
           
 
 RECPMTDT

 
 10801

 
 Menu

 
 0

 
 Print Payment Detail on Inquiry Print.

 
       
 1

 
 Do not Print Payment Detail on Inquiry Print.

 
           
 
 RECRDEDE

 
 10801

 
 Menu

 
 0

 
 Do not Display Description from Preceeding Receipt.

 
       
 1

 
 Display Description from Preceeding Receipt.

 
           
 
 RECRDNDE

 
 10801

 
 Menu

 
 0

 
 Do not Display Document # from Preceeding Receipt

 
       
 1

 
 Display Document # from Preceeding Receipt.

 
           
 
 RECSALMN

 
 future

 
 Menu

 
 0

 
 Do not display Salesman from REM in X111 or X112

 
       
 1

 
 Display Salesman from REM in X111 and X112

 
           
 
 RECZROTR

 
 10801

 
 Menu

 
 0

 
 Do not Post Zero Transactions to Receivables.

 
       
 1

 
 Post Zero Transactions to Receivables.

 
           
 
 REQUISIT

 
 2.2

 
 Phone

 
 0

 
 Requisitions (from Orton's C.C.) is off.

 
       
 1

 
 Requisitions (from Orton's C.C.) is on.

 
           
 
 RESEFILL

 
 V8L3

 
 Menu

 
 0

 
 All reservations get a fill priority of ' 1' and they are therefore filled in date/time order.

 
       
 1

 
 All Customer reservations get a ' 2' fill priority.

 
         
 All Warranty reservations get a ' 3' fill priority.

 
         
 All Internal reservations get a ' 4' fill priority.

 
   
 V8L5

   
 2

 
 All reservations with a 'P' priority code get a ' 1' fill priority.

 
         
 All reservations with an 'S' priority code get a ' 2' fill priority.

 
           
   
 V8L5

   
 3

 
 Customer reservations with a 'P' priority code get a ' 1' fill priority.

 
         
 Warranty reservations with a 'P' priority code get a ' 2' fill priority.

 
         
 Internal reservations with a 'P' priority code get a ' 3' fill priority.

 
         
 Customer reservations with a 'S' priority code get a ' 4' fill priority.

 
         
 Warranty reservations with a 'S' priority code get a ' 5' fill priority.

 
         
 Internal reservations with a 'S' priority code get a ' 6' fill priority.

 
           
   
 V8L5

   
 4

 
 Customer reservations with a 'P' priority code get a ' 1' fill priority.

 
         
 Customer reservations with a 'S' priority code get a ' 2' fill priority.

 
         
 Warranty reservations with a 'P' priority code get a ' 3' fill priority.

 
         
 Warranty reservations with a 'S' priority code get a ' 4' fill priority.

 
         
 Internal reservations with a 'P' priority code get a ' 5' fill priority.

 
         
 Internal reservations with a 'S' priority code get a ' 6' fill priority.