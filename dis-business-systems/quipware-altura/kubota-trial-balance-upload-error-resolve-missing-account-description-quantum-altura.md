---
title: "Kubota Trial Balance Upload Error: Resolve Missing Account Description - Quantum / Altura"
source: "salesforce_articles.md"
tags: ["Quipware", "Altura"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Kubota Trial Balance Upload Error: Resolve Missing Account Description - Quantum / Altura."
long_description: "This document provides information about Kubota Trial Balance Upload Error: Resolve Missing Account Description - Quantum / Altura from the DIS Salesforce Knowledge Base."
---

Introduction 

 If you encounter the following error when uploading trial balance information to Kubota, it may be caused by a general ledger account in your system not having a title: 

 Error encountered during ValidateSubmittedTrialBalance: Data is missing required Account Description. If you need assistance resolving this issue, please send an email to: your DBS provider. 

 

  

 Solution 

 Run a Chart of Accounts report and look for any accounts without a title. 

 

 Update these accounts with the correct titles and then resubmit your trial balance. 

 Once the account title has been added in DIS, resubmit your Kubota Trial Balance.