---
title: "MyPortal Gravity Payments Installation and Overview - MyPortal"
source: "salesforce_articles.md"
tags: ["Quipware", "Altura"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about MyPortal Gravity Payments Installation and Overview - MyPortal."
long_description: "This document provides information about MyPortal Gravity Payments Installation and Overview - MyPortal from the DIS Salesforce Knowledge Base."
---

Introduction 

 This article details the process for installing Gravity Payments in Altura, so the option is enabled for your customers in MyPortal. It also details how to view and complete the associated tasks that are generated when your customers make invoice payments using Gravity Payments through MyPortal. 

  

 Configure Gravity Payments in Altura 

 Gravity must be configured in Altura before your customers can make payments through MyPortal. 

 Access Altura and select Applications (Altura | Admin Settings | Configurations | Applications). The Applications screen displays. 

 

 Click Payment Configuration .  The Payment Configuration fields display. 

 

 Click in the field and select Gravity from the drop-down. 

 

 Enable the Display Pay Online option and click the Save Changes button. The Pay Invoice button shown below does not display for your customers in MyPortal until you enable this option. 

 

 Your customer can now make online payments with Gravity Payments. 

 Post Customer Payment Notifications and Actions 

 When a customer makes an online payment, a task is created for them that allows them to track the progress of the payment.  An Invoice Related Request task is also created in Altura for the dealership, and designated dealership users are notified through the email that was entered when configured. 

 

 Select the All or Unassigned Invoice Related Request option. 

 

 Select the Task entry. A screen displays showing: 

 The status as Pending Dealer 
 A note that the invoice has been paid via credit 
 A confirmation number provided by Gravity 
 A Payment Details download option 
 Each invoice that was paid as a hyperlink so that invoice can be accessed and viewed 

 The payments also listed under Credit Transactions (Accounting | Payments | Credit Transactions) in Altura . 

 The status remains Paid In Progress until the invoice is closed and posted in the system and the status becomes Paid .