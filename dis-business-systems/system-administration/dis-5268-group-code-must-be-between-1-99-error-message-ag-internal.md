---
title: "DIS-5268 Group Code must be between 1-99 Error Message – Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about DIS-5268 Group Code must be between 1-99 Error Message – Ag Internal."
long_description: "This document provides internal system administration information about DIS-5268 Group Code must be between 1-99 Error Message – Ag Internal."
---

Issue 

 Received a DIS-5268 Group Code must be between 1-99 error message when on the Sold To screen and are locked in the invoice. 

 This is likely because the group code field is missing a character. For example, just 0 instead of 01. 

  

 Resolution 

 Update the u.SAM header record for the invoice and change position 95 to a 1.