---
title: "Add a State in Destination Based Sales Tax - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Add a State in Destination Based Sales Tax - Ag Internal."
long_description: "This document provides internal system administration information about Add a State in Destination Based Sales Tax - Ag Internal."
---

_How to a Add a State in Destination Based Sales Tax - AG Internal_

Introduction 

  

 If you are trying to update a tax code from a zip code and you get an error that there is an invalid tax code with no update, it is a sign that the state is not in Destination Based Sales Tax or DBST. 

 

 Check POS |Table Maintenance |Tax Configuration | Destination Base Tax Profile to be sure- if the state has not been loaded it will not show on that screen. 

  

 To ADD states to the DBST subscription 

 Add a GL Account for the state sales tax - this will be a liability account check to see where the other states GL accounts are, and follow the logic of the setup for those. 

 For this example, we created M31050 Georgia Sales Tax.  Enter in the Title, type L and 99 months to keep. 

 

 Add the account to the POS |Table Maintenance |Tax Configuration |Tax Account Assignments screen.  Click ADD. 

 

 Fill in all of the GL account information for each type of tax and Clicked OK when we finished. 

 

 Lock and Key setup:  Open sc400 type LOCK, then on command line from Dealer side, type X527SET 

 

 Enter in the permanent code and click OK. This opens the configuration window. 

 Enter the state and click Enter. Then you can exit. 

 

 Another windows pops up to see if you want to use Canada. Click Cancel. 

 

 The last step is to push over latest updates so it will load them at night. 

 Open to keystone sessions, one to ASAP \\172.16.16.80 and one to dealer keystone.  Check mocha for the IP. You will want to push the latest DBST file from ASAP over.  In this example we pushed February. 

 Slide from DBST over to DBST to copy. 

 

 Verify by Checking POS |Table Maintenance |Tax Configuration| Tax Code Maintenance 

   

 

 It will say Pending update at the top of the screen.  This will run with the end of day procedures so if you have more states to add on this same day you only need to  push once.