---
title: "Rental Billing Options in Periodic Invoices - Quantum - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Rental Billing Options in Periodic Invoices - Quantum - AG Internal."
long_description: "This document provides internal system administration information about Rental Billing Options in Periodic Invoices - Quantum - AG Internal."
---

Introduction 

 This document explains how different billing options work with periodic invoicing specifically for the Monthly period. 

 To ensure accurate and timely periodic invoicing, verify the key contract and system settings that determine how billing cycles are calculated and processed. 

 Key Items to Confirm 

 Number of days defined in your monthly billing period . 
 Billing method selected on the contract (Pre-bill, Post-bill, or Rent-to-Sell: 
 Pre-Bill : Pre-Bill creates the first invoice immediately when you convert the reservation to a contract. Every additional invoice appears in Periodic Invoicing only after a full rental period has passed. Billing always happens at the beginning of the rental period, and early invoicing is not supported. Pre-Bill follows your standard rental-period setup and works with Post-Bill settings if needed. 

 
 Post-Bill : Post-Bill generates the first invoice at the end of the first rental period, with all future invoices appearing in Periodic Invoicing at the end of each rental period. This option supports early billing when enabled in Options (Equipment Rental |Maintenance | Options), allowing invoices to be created earlier if the Monthly rate threshold is met before period end. Post-Bill bills after the rental usage are complete. 
 Rent to Sell : Rent to Sell billing is based strictly on the On Rent Date. Each billing period runs from the On Rent Date to the same date in the following month (e.g., 09/23–10/22, 10/23–11/22, and so on). Invoices for each new period appear in Periodic Invoicing one day after the new period starts.
 Important : Rent to Sell can only be used with Pre-Bill and does not support Post-Bill or early invoicing. 

 Determine the time your Scheduled Job runs to review active contracts and add any items that are due to Periodic Invoicing. 

   

 View Number of Days Defined in Monthly Billing Period                 

 To View Number of Days Defined in Your Monthly Billing Period: 

 Click Work with Rates ( Equipment Rental | Maintenance | Work with Rate ). 

 

 Click the Periods button and the Maintain Rental Periods screen opens. 

 

 Review the M Rental Period.  For example, the rental period in the image below is calculated as hours in period divided by 24 hours in a day i.e. 672/24 that gives the monthly rental period of 28 days.  

 

   

 Review Billing Methods 

 To review billing methods: 

 Click Options ( Equipment Rental | Maintenance | Options ). 

 

 Click the Enter button and the Customer Billing option appears. 

 

 In the screenshot below, the system would bill on the 25 th day for the full 28 days.  

 

  

 Review Scheduled Job 

 To Check the Scheduled Job: 

 From the command line, type WRKJOBSCDE and press Enter . 
 Scroll through the list of scheduled jobs until you locate the job named X90000u . 

 Important : The final letter in the job name indicates your specific file set. 

 In the screenshot below, the scheduled job is for the D file set and runs each day at 6:00AM. 

 

 To change the scheduled job, click Schedule Automatic Periodic Invoicing Job ( Equipment Rental | Maintenance | Schedule Automatic Periodic Invoicing Job ). 
 Change the time and click the green check mark.