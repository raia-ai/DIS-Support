---
title: "Configure Payables EFT - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Configure Payables EFT - Ag Internal."
long_description: "This document provides internal system administration information about Configure Payables EFT - Ag Internal."
---

_Configure Payables EFT - AG Internal_

Introduction 

 This is a quick sheet for Dealership EFT Configuration 

  

 To Enable EFT 

 Before beginning you will need to do the following: 

 Ensure dealer has Archiving, EasyFile, and Laser Form products on their account inventory. They will need to be listed on their inventory record. 

 To turn on EasyFile - on a command line, type INSTALL_EF – lock/key 

 To turn on EFT - on a command line, type X127EFT – lock/key 

 Dealer can configure EFT through Vendor Maintenance  They can add an Email address to verify the vendor is active and enabled. See the Complete a Payables Checks Electronic Fund Transfer Article for Dealer instructions. 

 Keystone is Ticket here . Quantum is here . 

  

 To Disable EFT 

 At a menu type: CALL X000B6RP and press enter. 

 Highlight Payables EFT Checks and click Remove . 

 

  

 Note: Turning the product off will not remove email address from payables vendor or unmark them as verified.   

 If it is important for the customer to NOT have this information they should remove it prior to us turning off the product. 

  

 This information is held in the PEFTP file.