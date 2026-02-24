---
title: "Cursor Position on Parts Lines in Point of Sale ( Parts Number vs Quantity field) - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Cursor Position on Parts Lines in Point of Sale ( Parts Number vs Quantity field) - Ag Internal."
long_description: "This document provides internal system administration information about Cursor Position on Parts Lines in Point of Sale ( Parts Number vs Quantity field) - Ag Internal."
---

_Cursor Position on Parts Lines in Point of Sale ( Parts Number vs Quantity field) - AG Internal_

Option Settings 
 The starting cursor position on Point of Sale parts lines is controlled by custom opt CUST0003. This is a barcoding opt. 
   
 Introduction 
 This switch was designed for POS scanners. When reading a bar code in POS the part number is passed to the field onscreen and <enter> is then passed.  This causes the part to be automatically added as a new line onto the POS detail screen without requiring the user to manually press the <enter> key. 
   
 The choices are: 
 X00081 CUST0003,1 : The cursor position starts in the Part Number Field. 
 
 X00081 CUST0003,0 : The cursor position starts in the Quantity Field.