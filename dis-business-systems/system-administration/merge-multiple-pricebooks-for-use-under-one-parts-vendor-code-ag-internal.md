---
title: "Merge Multiple Pricebooks for use under one Parts Vendor Code - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Merge Multiple Pricebooks for use under one Parts Vendor Code - Ag Internal."
long_description: "This document provides internal system administration information about Merge Multiple Pricebooks for use under one Parts Vendor Code - Ag Internal."
---

_Merge Multiple Pricebooks for use under one Parts Vendor Code - Ag Internal_

Merge Multiple Pricebooks for use under one Parts Vendor Code 

  

 This is useful to do when you have multiple parts under one vendor that are updated in separate books. This is a multi-step process. Doing this breaks the link of Automatic Updates and causes dealers to have to re-merge + update pricing each time a new book is released. 

  

 Look at vendor configuration, note the book configured currently (making sure it’s the most current book); this will be the “master” book 

 Go to Parts > Price Update / Parts List > Display / Print / Change Pricebook, take note of the name of the book you wish to merge under the “master” book 

  

 On a command line, type CPYF, hit Enter 

  

 In the following page that opens, you’ll need to fill out the following: 

 From File: the book you’ll be merging into the master pricefile 

 Library: QS36F 

 To File: the “master” pricefile, the book that’s already configured to the vendor 

 Library: QS36F 

 Replace or add: *ADD 

 Hit Enter once each field is completed 

  

 

  

 After you hit enter, the system will take you back to the main menu and a blue notification will display across the bottom, and there will be a spinning wheel in the upper right corner – the system will cycle through a few messages but when completed you’ll see one like this: 

  

 

  

 Next, find a part that exists only in the pricefile you merged (not the master book), then search for that part in the master book ( Parts | Price Update / Parts List | Display / Print / Change Pricebook).   Highlight master book  click  Display and  search for the part. 
 The part should be found in the book when it previously had not. 

  

 Lastly, you’ll need to rerun prices using the Automatic Price Update from Price Book menu option for the vendor with newly merged books. NOTE: You may want to run Parts Pad Summary before and after to get the change in value that happened due to the pricebook update.  

  

 Note: When there’s a new book of either of the merged books, the whole process of merging / applying must be done again.