---
title: "Hide Part Numbers and Vendor Codes in POS Documents - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Hide Part Numbers and Vendor Codes in POS Documents - Ag Internal."
long_description: "This document provides internal system administration information about Hide Part Numbers and Vendor Codes in POS Documents - Ag Internal."
---

_Hide Part Numbers and Vendor Codes in POS Documents - Ag Internal_

Issue:
 There is an OPT that can be set to hide part numbers and vendor codes from POS documents.  Just the part description, quantities, and prices would show. 
 This was created because Lift truck dealers wanted a way  to change the printed appearance of part sale lines.  (Customize the appearance of printed POS part lines for Lift Parts dealers) 
  
 Solution:
 Open up a command line ( System | AS/400 Command Line ) 
 Put in this command: X00081 CUS331dc,2 The ‘d’ in that command is the “Division,” so put the division letter in there where you want this setting turned on.  So, if your division letter is A, put A in there. 
 The ‘c’ in the command is the “Document Classification,” so put the Document Classification code that you want to have this setting.  For example, if the Document Classification code for your quotes is Q, you’ll put Q in there. 

 

   
 This command is per division, per document classification .  This means it can be run multiple times for different document classifications and/or divisions.  This setting is all or nothing for those documents.  So, if you have quotes with a Document Classification code of Q and they’re in division A, and you run this command to have part numbers and vendor codes hidden on those documents in that division, it would affect ALL documents of that classification in that division.  You cannot decide “This quote will show the part numbers, but I’ll hide the part numbers in this other document.” 
   
 Once the command is run, it may not take effect until the next day once certain jobs are cleared. 
 If you put in the OPT X00081 CUS331dc,1 , then the part lines won’t print on the document at all.

This won’t work for older versions, like version 22v3, for example. 
  
 Summary of CUS331dc: 
 0 = the "normal" way 
 1 = the North Coast Lift Truck way (Part Lines do not print but there is still a subtotal)  Available in DIS_NR38 
 2 = the Total Lift way (Printed Vendor code and Part number omitted and Part description  aligned to the left where vendor code would have been) Available in DIS_NR53