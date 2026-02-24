---
title: "CNH BMS Financial Report Sum of Aging Amounts Error - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about CNH BMS Financial Report Sum of Aging Amounts Error - Ag Internal."
long_description: "This document provides internal system administration information about CNH BMS Financial Report Sum of Aging Amounts Error - Ag Internal."
---

_CNH BMS Financial Report Sum of Aging Amounts Error - AG Internal_

Introduction 

 When submitting the CNH BMS Report, 5 aging screens require some input based on figures gathered from specific general ledger accounts. If an accident is made and the sum of the amounts provided on the Aging screen do not equal the total, the report may display a Warning stating Sum of aging amounts must equal Total. CNH will reject this statement . 

   

 The message is referring to the accounts listed above the message. 

  

 To Resolve Error 

 The Aging entry or entries will need to be adjusted to equal the total. (362,633.25 in the screenshot above.) 

   

 The figures listed in the aging category fields on the Accts Payable Schedule screen need to total the amount on the report. 

 Note : CNH rounds up to the nearest dollar. As a result, the DIS Report can show errors when the CNH Portal does not. 

 For Example : In the following scenario: 

                240                     362.633.25            (Report Generates from mapped accounts) 

                240A                   362,633.24             (User typed in on Aging Screen) 

 DIS Report would have an error while the CNH portal would not.