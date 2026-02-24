---
title: "Hidden OPTs and other OPIs #5 – Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Hidden OPTs and other OPIs #5 – Ag Internal."
long_description: "This document provides internal system administration information about Hidden OPTs and other OPIs #5 – Ag Internal."
---

_Hidden OPTs and other OPIs #5 – AG Internal_

Introduction

 This is one of many articles providing Hidden OPTs and other OPIs. They are listed in alphabetical order by Option.

 Important! If a Hidden OPT created for a specific customer is applied to another customer, ensure the new customer knows that there will NOT BE any further modifications to the OPT.

  

 
 Option 

 
 Version 

 
 Set-By 

 
 OPT 

 
 Definition of Switch Setting 

 
 
   

 
   

 
   

 
   

 
   

 
 
 CCTOTAL

 
 2.2

 
 Menu

 
 0

 
 If credit card completely pays invoice total the invoice total will print at the bottom of the invoice

 
       
 1

 
 If credit card completely pays invoice, the final amount printed at the bottom of the invoice will be 0.

 
       
 2

 
 Invoice total will be 0 if paid by credit card or ROA

 
           
 
 CKBYPASS

 
 1.4

 
 Phone

 
 0

 
 DIS Internal Custom DON'T ignore first check number is not installed.

 
       
 1

 
 DIS Internal Custom DON'T ignore first check number is installed.

 
           
 
 CLAPIMTP

 
 future

 
 phone

 
 0

 
 Send CLAAS PIM files to Test server

 
       
 1

 
 Send CLAAS PIM files to Production server

 
           
 
 CONADDCA

 
 future

 
 Menu

 
 0

 
 Do not prompt to Add as Cash Cust when adding a new Contact

 
       
 1

 
 Prompt to Add as Cash Cust when adding a new Contact

 
           
 
 CONSECUR 

 
 obsolete 

 
 removed 

 
 0 

 
 Changing Contact information that is kept in sync with ADM does not require a security gate 

 
   
 security project 

   
 1 

 
 Changing Contact information that is kept in sync with ADM requires a security gate 

 
           
 
 CONTOADM

 
 11.1

 
 Menu

 
 0

 
 Default the Track as a Business System Address to Y

 
       
 1

 
 Default the Track as a Business System Address to N

 
           
 
 COREPRC

 
 2.3

 
 Menu

 
 0

 
 Core price will be referenced from the Pricebook

 
       
 1

 
 Core price will be referenced from Dealer list, if the part is in inventory, otherwise from Pricebook.

 
           
 
 COREPRT

 
 2.3

 
 Menu

 
 0

 
 POS documents will print two lines when a Reman part is sold.  The Reman# and the Core#.

 
       
 1

 
 POS documents will only print the Reman part line when sold. (Fully priced)

 
           
 
 CORPLIMT

 
 Future

 
 Menu

 
 0

 
 Corporate Account Credit Limit is not used

 
       
 1

 
 Corporate Account Credit Limit is used in POS Lockout programs

 
       
 2

 
 Corporate account credit limit is used in POS lockout programs and total balance includes unposted invoices

 
           
 
 COST0001

 
 V8L5

 
 Menu

 
 0

 
 X21 Display transactions even w/o the security code entered at the security gate

 
       
 1

 
 X21 Do not display transactions w/o the security code entered at the security gate

 
   
 obsolete w/ sec proj---> 

   
 2 

 
 X21 Display trans and cost w/o the security code entered at the security gate 

 
           
 
 COWIDPTM

 
 future

 
 Menu

 
 0

 
 Prompt to copy to other divisions at PTM defaults to ‘Y’

 
       
 1

 
 Prompt to copy to other divisions at PTM defaults to ‘N’

 
           
 
 CREOPT

 
 1.4

 
 Phone

 
 0

 
 Pioneer Custom credit code check is not installed

 
       
 1

 
 Pioneer Custom credit code check is installed

 
           
 
 CSDIMPOR

 
 future

 
 Phone

 
 0

 
 Import function from CSD Recurrent Trans is not valid

 
       
 1

 
 Import function from CSD Recurrent Trans is valid

 
           
 
 CSPSPWC

 
 future

 
 Phone

 
 0

 
 auto password change will occur for CSPS when last change date is greater than 54 days

 
       
 1

 
 auto password change is disabled for CSPS

 
           
 
 CUST0001

 
 Avail.

   
 0

   
           
 
 CUST0002

 
 V8L4B

 
 Phone

 
 0

 
 Merge payables immediately as enter is pressed

 
       
 1

 
 Merge payables after Cmd1 to end program is pressed so job is evoked.

 
           
 
 CUST0003

 
 V8L4B

 
 Phone

 
 0

 
 legacy bar code features are not installed – see the BAR1 project report

 
       
 1

 
 legacy bar code features are installed – see the BAR1 project report