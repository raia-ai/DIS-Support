---
title: "GL Periods Wrapped and Transactions Appear to be Posted to Future GL Period - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about GL Periods Wrapped and Transactions Appear to be Posted to Future GL Period - Ag Internal."
long_description: "This document provides internal system administration information about GL Periods Wrapped and Transactions Appear to be Posted to Future GL Period - Ag Internal."
---

_GL Periods Wrapped and Transactions Appear to be Posted to Future GL Period - AG Internal_

Issue 

 The user posted transactions to GL Period 12/2021, but the transactions were posted on 01/04/2022 with 01/21 still open . Posting anything with more than twelve open months can cause data issues such as transactions showing a future GL year. 

 

 In the example above, Receivable Invoice BM0014724 was posted to 12/2021 on 01/2022 but 01/2021 was still open. The result is the transaction shows a GL period of 12/22. 

  

 Solution 

 This is a data issue that needs to be corrected with a series of SQL statements. 

 The files to consider are: 

 REA (REAGLM and REAMGM) 
 PAA(PAADGL and PAAMFU) 
 TAXHIST(TXHGL) 
 WHT(WHTSL1) 
 RPD(RPDGLM). 

 Data Mine also needs to be recalculated.