---
title: "An Array index is out of range (C G D F) error in Group Inventory Adjustment (X33-6) - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about An Array index is out of range (C G D F) error in Group Inventory Adjustment (X33-6) - Ag Internal."
long_description: "This document provides internal system administration information about An Array index is out of range (C G D F) error in Group Inventory Adjustment (X33-6) - Ag Internal."
---

_An Array index is out of range (C G D F) error in Group Inventory Adjustment (X33-6) - AG Internal_

Issue 

 The customer went to Parts | Part Inventory Adjustment | Group Inventory Adjustment

 or X33-6 in green screen. 

  

 Then typed in the Group, Vendor and Part number and hit enter.

 The following error came up on their screen. 

  

 An Array index is out of range (C G D F) 

  

 If you put your cursor in the line of the error and hit F1/help you can get additional text about the error. This can also be seen if you look at the job log for this session.

  

  

 

  

 If you take a C to this error, you will receive the following error. 

  

 X33600  

 Application error.  MCH0603 unmonitored by X33601 at statement 0000000842, 

 instruction X'0000;. 

  

 SYS7373 OPtions (  23) 

 Unexpected error CCE9901 rec eived by program X33601. 

  

 Resolution 

 You most likely are working with a segmented Parts vendor and there are parts in the group inventory list that are not segmented properly. 

 NOTE: The part number they type into the screen above is not necessarily the part with an issue. 

  

 Go to Parts | Parts Configuration |  Configure Vendor / Class 

 Type in they vendor they were trying to use when they got the error and look at the segmentation sizes to see if they are using multiple segments.  Here is an example of a vendor using multiple segments. 

 

  

 Run a Parts Pad Summary to get a secondary report with a list of Parts with segmentation errors. 

  

 Go to Parts | Part Reports | Parts Inventory Report. 

 You can run this for all vendors or just one it doesn't matter. Click the forward arrow. 

 Uncheck the Print Detail field and click the forward arrow. 

 Select "No delay"

  

 This will put 2 reports in the print spool.  We are interested in the parts on the Segmentation Error Report. 

 Here is a sample of the report. 

 

  

 These parts do not match the segmentation of the vendor setup and needs to be fixed by the customer. 

  

 To fix, resegment the part in Parts Posting & Maintenance.

 In this case, here is how the part needed to be resegmented.   NOTE: The customer will need to know how their segments and part number related. 

 Press enter once the screen has been filled out as follows.  

 

  

 All parts(or at least all parts for the vendor the customer is working on) on the report will need to be fixed prior to going back in to 

 Parts | Part Inventory Adjustment | Group Inventory Adjustment to begin work on the the physical inventory again. 

  

  

 Note: A customer could also decide not to use segmentation on the vendor moving forward. 

 If they wanted to move in this direction, they would change the vendor configuration to have 18 characters in the first segment.  This would affect ALL divisions so if they decide to go this route make sure all divisions are on board for this change. If everyone is onboard and the vendor configuration has been changed, we do have utility to resegment all parts in a given vendor to 1 segment.  There is not an "undo" to this is they change their mind. 

 X336