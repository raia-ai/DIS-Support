---
title: "Force Posting of a Out of Balance CSD Batch - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Force Posting of a Out of Balance CSD Batch - Ag Internal."
long_description: "This document provides internal system administration information about Force Posting of a Out of Balance CSD Batch - Ag Internal."
---

_Force Posting of a Out of Balance CSD Batch - AG Internal_

Introduction 

 This article contains the steps required to post an out of balance create source documents batch when the balance sheet is out of balance. This should only be done if you determine that a previously posted batch was truly out of balance, such as when the general ledger is out of balance due to a structural issue like orphaned cost of sale accounts. 

  

  

 To Force Posting 

 Create source documents using the GL month the out of balance occurred enter the missing debit or credit and enter the line up.
 Click Check for Errors , then click Enter on the Check for Errors screen.
 Make sure The debit and credit totals on above document do not balance is the only error returned.
 Click Check for Errors .
 Click End Job With Printed Edit List .
 Click Return to Menu .
 Open a command line (Alt + A), type MENU X171 , and click OK .
 Select Post Source Documents .
 Verify the batch has posted by running a financial statement.

 one sided post  

 one sided entry