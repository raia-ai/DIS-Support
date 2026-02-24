---
title: "Issue Sending EFT and/or Parts Daily Transfer Emails from Business System - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Issue Sending EFT and/or Parts Daily Transfer Emails from Business System - Ag Internal."
long_description: "This document provides internal system administration information about Issue Sending EFT and/or Parts Daily Transfer Emails from Business System - Ag Internal."
---

_Issue Sending EFT and/or Parts Daily Transfer Emails from Business System - AG Internal_

Issue 
 Problem sending EFT and/or Parts Daily Transfer emails from the business system. Email provider needs to know what SPF record to put in to be allowed to send out emails. 
  
 Solution 
 Have the customer/email provider update their SPF record to allow any emails originating from our public network 216.57.222.128/25  or  216.57.222.128/255.255.255.128 . This is the simplest way to allow this type of traffic.