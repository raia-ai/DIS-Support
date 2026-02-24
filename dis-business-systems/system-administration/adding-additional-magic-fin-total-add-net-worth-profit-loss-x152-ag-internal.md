---
title: "Adding additional Magic FIN Total (Add NET WORTH & PROFIT/LOSS) X152 - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Adding additional Magic FIN Total (Add NET WORTH & PROFIT/LOSS) X152 - Ag Internal."
long_description: "This document provides internal system administration information about Adding additional Magic FIN Total (Add NET WORTH & PROFIT/LOSS) X152 - Ag Internal."
---

_Adding additional Magic FIN Total (Add NET WORTH & PROFIT/LOSS) X152 - Ag Internal_

Financial Reporting 

 This change affects X15-2, and X15-5.  (Financial Statement and Budget Review)

  

 A new optional subtotal is available on the balance sheet.  

 This new total will be coded in the FIN file as '99999  4' and, if used, will add together the        
"Net Worth" and the "Profit/Loss for Current Year" figures.  

 It does not matter what the subtotal level is for this new subtotal.  

 If used, this total will print after the "Profit/Loss Current Year" but before "Total Liabilities and Net Worth".  

 In order for this change to work the "Total Liabilities" subtotal must be a level 3 or 4

 and the "Net Worth" subtotal must be a level 1 or 2.            

  

 From SC400 A03038