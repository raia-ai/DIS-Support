---
title: "Import Parts Update in Parts Posting & Maintenance - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Import Parts Update in Parts Posting & Maintenance - Ag Internal."
long_description: "This document provides internal system administration information about Import Parts Update in Parts Posting & Maintenance - Ag Internal."
---

Click here   to view the customer facing document. 

  

 Part Information Import (X3-2): A new part information import feature in Parts Posting and Maintenance (PP&M) allows users to update part information en masse via a CSV file. 

 The option can be accessed from both the Transaction and Information pages of PP&M. Additionally, there is a template CSV file available within the feature to help users format their import file correctly. 

 Enter X00081 PARTIMPT,1 in a command line to turn this feature on. 

 Program name associated with change from this application = X32007 

 Notes from QU-3682 where this feature was rolled in. (Internal use only) 

 Note that this feature can be used to clear part information out by leaving the field blank. Use case could be if the part descriptions were accidently entered in another language. This feature could be used to clear those out and then descriptions in the correct language could be populated from the price book. 

  

 The following fields can be updated using the import feature: 

 
 Class 
 Description 
 Bin Location 1 
 Bin Location 2 
 Quick Code 
 Long Description 
 Supersession Quantity 
 Supersession Vendor 
 Supersession Part Number 
 Supersession Code 
 Core Code 
 Part Category 
 Stock Code 
 Order Code 
 Return Code 
 Tax Code Override 
 Protect 
 Force ROB 

 
 Print Barcode Label Minimum 
 Maximum 
 Quantity Required 
 APR Code 
 APR Source 
 APR Season Code 
 APR Quantity Required 
 Weight 
 Discount 
 Package 
 Last Receipt Quantity 
 Dealer Order Number 
 Last Receipt Date 
 Dealer List Price 
 Suggested List Price 
 Internal Price 
 Dealer Net Price 

 
 
 Fields Below CANNOT BE UPDATED 

 
 
 Average Cost 

 
 Bases