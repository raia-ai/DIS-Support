---
title: "Thermo King Web Interface Install – Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Thermo King Web Interface Install – Ag Internal."
long_description: "This document provides internal system administration information about Thermo King Web Interface Install – Ag Internal."
---

_Thermo King Web Interface Install – Ag Internal_

Introduction 

 The Themo King Web Interface is no longer set from the Manufacturers OPT page. 

 

 Verify the OPT is set to #6  and the Thermo King SVC Interface is NOT installed (X63B-7). 

   

   

 To Install TK Web Interface 

 Access a Command Line. 

 

 Enter INSTALL_KI and click OK . 

 

 Type 0008 in the Item to be installed field and click Enter . 

 

 Provide the Lock & Key Information and click OK . 

 You will now see three TK Interface Buttons under the Unit Info tab on the Sold By screen in Invoicing as shown below. 

   

 You can view the install information on the Additional Products Lock screen. 

 CALL X000B6RP 

 

 The Thermo King Web interface uses ECM transactions HST for TK History and TK SVC & WTY for TK Warranty.