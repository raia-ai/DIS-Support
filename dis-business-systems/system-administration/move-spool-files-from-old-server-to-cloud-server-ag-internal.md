---
title: "Move Spool Files From Old Server To Cloud Server - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Move Spool Files From Old Server To Cloud Server - Ag Internal."
long_description: "This document provides internal system administration information about Move Spool Files From Old Server To Cloud Server - Ag Internal."
---

_Move Spool Files From Old Server To Cloud Server - AG Internal_

Introduction 

 This article provides a general outline of the process required to move spool files from an existing server to a cloud server. 

  

 To Move Spool Files 

 Start System i Navigator,   (Under the IBM i Access Menu) there may be a connection to Keystone, not sure that one will go to the old server, deleted it. 

 Create a new connection to the old Server by using the I.P. address: (Bottom Right Section). 

   

 Fill out the System field using the I.P. This is the only field that needs to be filled. 

   

 Click Next , the next screen displays prompting for a user ID. 

   

 Fill in the Default user ID on this screen and click Next . 

   

 Click Finish . 

 Repeat this process using Keystone as the System.  This will create 2 entries under My Connections. 

   

 Yours will have one that says Keystone and one with the old server IP from the earlier step. 

 Click on old server IP. A screen similar to the following displays: 

   

 Enter your Keystone password and click OK .  Updates occur and a menu tree similar to the following displays: 

   

 Click on the  next to Basic Operations to reveal additional options. 

   

 Click Printer Output , this opens all the printer output on the old server with the user I.D. you signed on with above. 

   

 Repeat the steps above on the Keystone connection until you reach the last step. 

 Click on the  next to Printers. DO NOT CLICK ON A PRINTER . 

 The right screen should still have the list of printouts in it. 

 Click on the first one you want to move, and then hold the shift key and click on a few (NO MORE THEN 20) down the list to highlight them. 

 Click and hold, on the last one that is highlighted, and drag it to the printer on the left screen. If you select a real printer, they will print, so it’s best to use a No Print printer. 

 Repeat the steps above, until you have moved all the printouts.