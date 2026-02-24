---
title: "SQL For Finding Future Dated Punches in Time Clock - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about SQL For Finding Future Dated Punches in Time Clock - AG Internal."
long_description: "This document provides internal system administration information about SQL For Finding Future Dated Punches in Time Clock - AG Internal."
---

_SQL For Finding Future Dated Punches in Time Clock - AG Internal_

Issue 

 User receives the following error when exiting out of the TCLOCK user ID 

 X5B101 has an index error in array DYS or future punches indicated on the Payroll Audit Report . 

  

 Solution 

 Run this SQL to find the punch creating the issue: 

 DISSQL REQUEST('select * from tcd where tcddat > ''YYYYMMDD''') replacing the YYYYMMDD with the current date.