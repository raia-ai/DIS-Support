---
title: "Fixed Asset Screen Fields and Description - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Fixed Asset Screen Fields and Description - Ag Internal."
long_description: "This document provides internal system administration information about Fixed Asset Screen Fields and Description - Ag Internal."
---

Fixed Asset Screen Fields and Descriptions 

 
 
 Start Date 

 
 Date (mm/dd/yy). Date on which unit becomes a fixed asset and depreciation begins. 

 
 
 Starting Cost 

 
 9.2 digits. The original cost of the unit prior to depreciation (9999999.99). Must be a positive number. 

 
 
 Method 

 
 3 characters. Depreciation method. 

 ACR = ACRS (Accelerated Cost Recovery System) Depreciation calculations for ACRS on units placed into service before 12/31/86 are different than for units placed into service after that date. 
 SLN = Straight Line 
 MAN = Manual. No depreciation is calculated by the system. Debits and credits for depreciation must be posted in Create Source Documents (X1-7). 
 3 digits = Declining Balance. Example: 200 = 200%.     

   

 See solution record A03138. This is generally referred to as a double declining method.  Essentially what it does is calculate the same rate as SLN (straight line) and then apply this factor.  What that means is that if SLN would have calculated $1000 for the month and my method was 200, depreciation would be $2000 for the month.   However, there is one key additional difference in that past depreciation is subtracted during the calculation. 

 
 
 Invest Credit 

 
 9.2 digits. Amount of investment credit claimed. This field is not valid if Start Date is greater than December 31, 1986 

 
 
 Life 

 
 3 digits. Life of the unit in years (99.9). Must be a positive number. 

 
 
 Past Depr 

 
 9.2 digits. Amount of depreciation taken in previous years. Should not include the depreciation to be in the Frst Yr/179 Depr field. 

 
 
 Vehicle Flag 

 
 1 character. Y = Yes, N = No. “Y” indicates that the fixed asset is a vehicle. 

 When the system encounters a “Y” in this field, NEW ACRS is examined. There is a yearly ceiling on depreciation on vehicles defined as Luxury Vehicles by the IRS. The Life for Luxury Vehicles must be 5 years. Depreciation may extend beyond 5 years. Depreciation will be calculated until the depreciation amount equals the starting cost. 

 
 
 Expense Account 

 
 8 characters. General Ledger account number debited for depreciation expense on the unit. 

 
 
 Frst Yr/179 Depr 

 
 9.2 digits. Amount of depreciation taken on this unit during its first year 

 
 

  

 See also SC400 solution records: 

 A02008 - HOW DOES 179 DEDUCTION EFFECT DEPRECIATION? 

 A03128 - HOW DOES DOUBLE DECLINING BALANCE DEPRECIATION WORK A03249 - DETAILED INFORMATION ON UNIT DEPRECIATION