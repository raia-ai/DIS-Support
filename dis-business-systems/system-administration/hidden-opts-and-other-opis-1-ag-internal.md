---
title: "Hidden OPTs and other OPIs #1 – AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Hidden OPTs and other OPIs #1 – AG Internal."
long_description: "This document provides internal system administration information about Hidden OPTs and other OPIs #1 – AG Internal."
---

_Hidden OPTs and other OPIs #1 – AG Internal_

Introduction 

 This is one of many articles providing Hidden OPTs and other OPIs. They are listed in alphabetical order by option through all of the Hidden OPT articles. 

 Important! If a Hidden OPT created for a specific customer is applied to another customer, ensure the new customer knows that there will NOT BE any further modifications to the OPT. 

  

 
 Option 

 
 Version 

 
 Set-By 

 
 OPT 

 
 Definition for Switch Setting 

 
 
 ADMDEL 

 
 future 

 
 phone 

 
 0 

 
 Do not allow Employees and Time Clock Technicians to be renamed by PFX687 

 
       
 1 

 
 Allow Employees and Time Clock Technicians to be renamed by PFX687 

 
           
 
 ADMTOCON 

 
 11.1 

 
 Menu 

 
 0 

 
 Default the Track as Contact prompt to Y 

 
       
 1 

 
 Default the Track as Contact prompt to N 

 
           
 
 ADVRCANC 

 
 1.4 

 
 Menu 

 
 0 

 
 Cancelled documents are not printed 

 
     
 X9 

 
 1 

 
 Cancelled documents are printed 

 
           
 
 ADVRCCHK 

 
 Future 

 
 Menu 

 
 0 

 
 Determine Over Credit Limit by Receivables Balances Only. 

 
       
 1 

 
 Include Unposted Invoices by Division in Credit Limit Check 

 
       
 2 

 
 Include Unposted Invoices in All Divisions in Credit Limit Check 

 
           
 
 ADVRCOLR 

 
 future 

 
 Menu 

 
 0 

 
 Do not print Color on the rental contract 

 
     
 X9 

 
 1 

 
 Print Color on the rental contract 

 
           
 
 ADVRCPOS 

 
 1.4 

 
 Menu 

 
 0 

 
 'Continue to POS' prompt defaults to 'N' 

 
     
 X9 

 
 1 

 
 'Continue to POS' prompt defautls to 'Y' 

 
           
 
 ADVRCMYC 

 
 10.1 

 
 Menu 

 
 0 

 
 Do not print other unit information on the rental contract 

 
     
 X9 

 
 1 

 
 Print other unit information on the rental contract 

 
           
 
 ADVRENT 

 
 V8L5 

 
 Tape 

 
 0 

 
 Advanced rentals is not installed 

 
       
 1 

 
 Advanced rentals is installed 

 
           
 
 ADVRENTX 

 
 Future 

 
 Phone 

 
 0 

 
 POS will not modify Rental Status if ADVRENT is installed 

 
       
 1 

 
 POS will modify Rental Status even if ADVRENT is installed 

 
           
 
 ADVRFORM 

 
 V8L5 

 
 Menu 

 
 0 

 
 Regular contract 

 
     
 X9 

 
 1 

 
 POS form 

 
           
 
 ADVRPRER 

 
 10.1 

 
 Menu 

 
 0 

 
 Do not print rental rates on the rental contract 

 
     
 X9 

 
 1 

 
 Print rental rates on the rental contract 

 
           
 
 ADVRFRCP 

 
 V8L5 

 
 Menu 

 
 0 

 
 Rental contract length is 88 lines. Header lines = 12 / Footer lines = 28 

 
     
 X9 

 
 1 

 
 Rental contract length is 112 lines.  Header lines = 12 / Footer lines = 28 

 
           
 
 ADVROLIN 

 
 V8L5 

 
 Menu 

 
 0 

 
 Other lines will not print 

 
     
 X9 

 
 1 

 
 Other lines will print 

 
           
 
 ADVRPDIR 

 
 V8L5 

 
 Menu 

 
 0 

 
 Job site directions do not print 

 
     
 X9 

 
 1 

 
 Job site directions print. 

 
           
 
 ADVRTLIN 

 
 V8L5 

 
 Menu 

 
 0 

 
 Total lines will not print 

 
     
 X9 

 
 1 

 
 Total lines will print 

 
 
 Rental Contract Print Total Lines 

 (ADVRTLIN) Above

       
 When the OPT is SET, the contract prints a line total for each rental line and the subtotal of all rental lines as well as the tax and final Total dollar amount as shown in the first screen shot below. See Print Total Lines on Rental Contract (Hidden OPT ADVRTLIN) for more details.