---
title: "DIS-5057 – The Sales Code Entered is not Valid - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about DIS-5057 – The Sales Code Entered is not Valid - AG Internal."
long_description: "This document provides internal system administration information about DIS-5057 – The Sales Code Entered is not Valid - AG Internal."
---

_DIS-5057 – The Sales Code Entered is not Valid - AG Internal_

Issue 

 A POS document can’t be accessed and an error stating the sales code is invalid displays. 

  

 Solution 

 Sometimes a sales code will be listed with just one character. If it’s not obvious what the sales code with the error message is, you will need to cross reference it to their list of sales codes. 

   

 When the incorrect sales code is identified, DSPPFM u.SAM and find and make not of all records with that sales code. 

 Use DISFU to update those records. This is most easily done in Green Screen. 

 DISFU 

   

 u.SAM 

   

 QS36F 

   

 Enter through the last prompt. 

   

 Put the record number in and press Enter . 

   

 Find where the sales code is listed and change the hex code underneath to the correct code for the symbol by typing over the yellow characters in line underneath the symbol that needs to be changed (as soon as you press enter on this screen anything that you have changed will be permanently updated, if you think you have made a mistake make sure to exit before entering). 

   

 Hex Code Guide