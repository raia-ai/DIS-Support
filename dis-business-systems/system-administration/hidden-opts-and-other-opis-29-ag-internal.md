---
title: "Hidden OPTs and other OPIs #29 – Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Hidden OPTs and other OPIs #29 – Ag Internal."
long_description: "This document provides internal system administration information about Hidden OPTs and other OPIs #29 – Ag Internal."
---

_Hidden OPTs and other OPIs #29 – AG Internal_

Introduction

 This is one of many articles providing Hidden OPTs and other OPIs. They are listed in alphabetical order by Option.

 Important! If a Hidden OPT created for a specific customer is applied to another customer, ensure the new customer knows that there will NOT BE any further modifications to the OPT.

  

 
 Option 

 
 Version 

 
 Set-By 

 
 OPT 

 
 Definition of Switch Setting 

 
 
 TKDLR

 
 V8L5

 
 Menu

 
 0

 
 Dlr is not a Thermo King Dealer.

 
       
 1

 
 Dlr is a Thermo King Dealer.

 
           
 
 TKDLRCAN

 
 10800

 
 Menu

 
 0

 
 Dlr is not a Canadian Thermo King Dealer.

 
       
 1

 
 TK Canadian dealer using part category to build landed cost.

 
       
 2

 
 TK Canadian dealer using part class to build landed cost.

 
           
 
 TKNODASH

 
 future

 
 phone

 
 0

 
 Normal reformatting of TK price books to include a dash

 
       
 1

 
 Do not reformat with TK price book to include a dash

 
           
 
 TKPKGUPD

 
 future

 
 phone

 
 0

 
 X37-8 Allow Pkg Qty to be updated

 
       
 1

 
 X37-8 Ignore Pkg Qty during update

 
           
 
 TKSVC

 
 11.0

 
 Menu

 
 0

 
 Thermo King SVC Interface is not installed

 
       
 1

 
 Thermo King SVC Interface is installed

 
           
 
 TKSVCUPL

 
 11.0

 
 Phone

 
 0

 
 Do not ask for types of lines (Customer or Internal) to upload to TK SVC Interface

 
       
 1

 
 Ask for types of lines (Customer or Internal) to upload to TK SVC Interface

 
           
 
 TKUPRC

 
 10.2V6

 
 Phone

 
 0

 
 Old style Thermo King price files and folders are used

 
       
 1

 
 New style Thermo King price files and folders are used

 
           
 
 TMCLK-01

 
 2.1

 
 Phone

 
 0

 
 Time Clock is has not been purchased.

 
       
 1

 
 Time Clock has been purchased.

 
       
 2

 
 Time Clock: all TC features available; POS is allowed to make changes in labor lines

 
         
 (2 is set by POS procs based on Time Clock config. where access is granted by user-id.)

 
           
 
 TMCLK24H

   
 Menu

 
 0

 
 Technicians using Time Clock must punch IN every day before punching OUT

 
       
 1

 
 Technicians using Time Clock can work through midnight and not punch IN again

 
           
 
 TRICRENT

 
 1.4

 
 Phone

 
 0

 
 Trico Custom Rentals Option is off

 
       
 1

 
 Trico Custom Rentals Option is on

 
           
 
 TRNSHIST

 
 V8L0

 
 Menu

 
 0

 
 POS- Update history when transferring parts

 
       
 1

 
 POS- Do not update history when transferring parts

 
           
 
 TXCUSTOM

 
 1.4

 
 Phone

 
 0

 
 DIS Internal Custom Tax Maintenance is not installed

 
       
 1

 
 DIS Internal Custom Tax Maintenance is installed

 
           
 
 TXREPORT

 
 1.4

 
 Phone

 
 0

 
 DIS Internal Custom Tax Report is not installed.

 
       
 1

 
 DIS Internal Custom Tax Report is installed.

 
           
 
 TXREPQRY

 
 1.4

 
 Phone

 
 0

 
 DIS Internal Custom Tax File is not installed

 
       
 1

 
 DIS Internal Custom Tax File is installed

 
           
 
 UNITDUDT

 
 1.4

 
 Menu

 
 0

 
 Update Flooring Due Date when unit is sold.

 
       
 1

 
 Do not update Flooring Due Date when unit is sold.

 
           
 
 UNITNU

 
 future

 
 phone

 
 0

 
 New/Used flag must be blank, N, or U.

 
       
 1

 
 New/Used flag must be N or U.

 
       
 2

 
 New/Used flag must be N or U, and if U, Traded on field must be present.

 
 
  

         
 
 UNITOVER

 
 future

 
 Menu

 
 0

 
 Does not perform automatic unit overallowance adjustments

 
       
 1

 
 Automatically adjust unit overalloweances against the selling price of the outgoing unit

 
       
 2

 
 Automatically adjust unit overalloweances against the cost of sale of the outgoing unit

 
 
  

         
 
 UNITRES

 
 future

 
 Menu

 
 0

 
 Update Unit Reservations from Point of Sale

 
       
 1

 
 Do not update Unit Reservations from Point of Sale

 
           
 
 UNITTYPE

 
 1.4

 
 Phone

 
 0

 
 Carpenter & Chapman Custom Adv Rentals option is: OFF

 
       
 1

 
 Adv Rentals: "For Unit Group and For Unit Type" added to upper right corner of screen

 
           
 
 UPDMETR

 
 11.2

 
 Menu

 
 0

 
 Do not synchronizeunit hour meter fields

 
       
 1

 
 Synchronize unit hour meter fields

 
           
 
 VENSELMV

 
 future

 
 Menu

 
 0

 
 show records for all vendors in vendor select

 
       
 1

 
 only show records for the specified vendor in vendor select

 
         
  

 
 
 VOIDAFT

 
 11.1

 
 Phone

 
 0

 
 MICR checks "Void over $" verbiage prints as is

 
       
 1

 
 MICR checks void verbiage is configurable

 
           
 
 VOLMMI

 
 11.1

 
 Phone

 
 0

 
 Volvo MMI is not installed

 
       
 1

 
 Volvo MMI is installed

 
           
 
 VOLMMId

 
 11.1

 
 Phone

 
 1

 
 Divisional download option to download comprehensive parts list (Mass Load)

 
       
 2

 
 Divisional download option to download changed parts (Daily)

 
           
 
 VOLMMIAG

 
 11.1

 
 Phone

 
 0

 
 Send maximum of 13 months of history to the aggrivated demand file

 
       
 1

 
 Send maximum of 25 months of history to the aggrivated demand file

 
           
 
 W2PRNT

 
 V8L1

 
 Menu

 
 0

 
 Printer will double strike W-2/T4 forms

 
       
 1

 
 Printer will single strike W-2/T4 forms

 
           
 
 WIPZERO

 
 future

 
 phone

 
 0

 
 Don't include any $0 WO's on the Service WIP

 
       
 1

 
 Include $0 Customer WO's on the Service WIP

 
       
 2

 
 Include $0 Customer and Internal WO's on the Service WIP

 
       
 3

 
 Include $0 Customer and Warranty WO's on the Service WIP

 
       
 4

 
 Include All $0 WO's on the Service WIP