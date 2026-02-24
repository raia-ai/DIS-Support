---
title: "Display and Search System Operator Messages – AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Display and Search System Operator Messages – AG Internal."
long_description: "This document provides internal system administration information about Display and Search System Operator Messages – AG Internal."
---

Introduction 

 Specific message(s) can be found in the System Operator Message queue by displaying and searching the System Operator Messages – not physically printing them. 

  

 Set Printer 

 The report is sent to the printer specified as the ‘System Printer’ in the IBM System Values: 

 DSPSYSVAL QPRTDEV (enter): 

 

 In this instance the writer for PRT01 needs to be ended: 

 ENDWTR PRT01 (enter). 

  

 Generate the Report 

 Type DSPMSG QSYSOPR and press F4 . Fill out the screen as shown below: 

 

 The Output field defaults to be an * to display it on the screen. Change the Output field to *Print and press Enter .   

 The report is called: QPDSPMSG 

 You can search that file using D P (My Printer Output). 

 In D P, display the QPDSPMSG job.  Enter the text you want to search on in the Find field and Press F16 ( shift + F4 ). 

 For instance, to search for a Load Forms message type the word Load in the Find field and press F16 .  The first search result on the search criteria will be listed near the top of the list as shown below: 

 

 Note : The Find field is Case Sensitive.  You may have to try a few different ways of entering your search data. 

 For example, in searching for a Load Forms message a search on LOAD found nothing, then FORMS , still nothing, then load , again nothing, and then finally Load to find the desired info. 

 Press F16 again to find the next matching result on the search criteria: 

 

 The purpose of this was to quickly find out how the Load Forms message was being answered. 

 In the above example the user printed Statements to A9 at 14:43 and answered the message with a ‘G’.   This tells the system that this type of paper has been loaded. 

 Then at 15:00 a report or invoice (form type *STD) was sent to A9.  Because the load forms message for Statements was answered with a ‘G’, they must answer the message for *STD forms. 

 This is a great way of showing the customer the sequence of the messages and the results of how they’re answered. 

 If they’re printing Statements on plain paper (so, not changing the paper in the printer), they could answer the load forms message for statements with an ‘I’, and they would not have to answer a 2 nd message when a report or invoice is sent.