---
title: "Change Invoice Credit Card from Manually Authorized to Charge - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Change Invoice Credit Card from Manually Authorized to Charge - Ag Internal."
long_description: "This document provides internal system administration information about Change Invoice Credit Card from Manually Authorized to Charge - Ag Internal."
---

_Accidently manually authorized CC used for invoice and need to charge a card._

Issue 

 User accidentally selects Allow bypass and manually authorizes an invoice they meant to charge to a credit card. They are being prompted for an authorization code but actually want to go back and process the invoice with the credit card. 

 

  

 Solution 

 Use DISFU to update the record for the invoice in the SCC file and change position 72 to M.