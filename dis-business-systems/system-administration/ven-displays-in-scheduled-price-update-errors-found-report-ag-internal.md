---
title: "VEN ??? Displays in Scheduled Price Update Errors Found Report - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about VEN ??? Displays in Scheduled Price Update Errors Found Report - AG Internal."
long_description: "This document provides internal system administration information about VEN ??? Displays in Scheduled Price Update Errors Found Report - AG Internal."
---

_VEN ??? Displays in Scheduled Price Update Errors Found Report - AG Internal_

Issue 

 Errors Found report in archiving shows ??? for Vendor entry as shown below. 

   

  

 Solutions 

 This can happen if: 

 It’s a new price book for the dealer and there aren’t any parts entered for the vendor. Run a parts pad summary for the vendor to confirm parts aren’t entered. If this is the case, no need for further action. 
 The dealership tried to download and process the price book from web locker themselves and the date in IEM file is earlier for the vendor than the previous book. 

 Steps to Reset: 

 Go into Configure Vendor/Class and assign the previous price book for the vendor. 

 Delete the newest price book for the vendor. 

 Go to Scheduled Price Updates, record the selected options for the vendor’s current configured price book, and delete it. 

   

 Select the vendor’s previous price book and click Change . On the screen that opens, apply the same options to this price book that were assigned to the one that was deleted. 

 Click Back up Options , then Manual Update .  This job will run for a few minutes. You can watch it on the user board until it finishes. 

   

 Once it’s finished, go back to Scheduled Price Updates and see if the new price book loaded and says EOD UPDT. If you want to ensure it loads properly, process it now rather than waiting by entering Call X37APPLY PARM( u ) where u = fileset. If they have more than one fileset, this command needs to be issued where the DIS vendor is set up in Electronic Commerce Configuration. 

 Check the archived reports. The Errors Found report typically has a list of parts that can’t be updated because they aren’t on the new price book. 

 If that doesn’t work, check the following: 

 Is the DISGL product key under the correct address? 

 Is the IM running on the same PC as configuration shows? 

 **Check to see if they have multiple file sets. If they do, check to see if DIS vendor is set up in the other file set(s) with a different PC name. 

 Is DIS set up as a vendor on that IM? Parameters on this vendor shows which PC the IM is set up on and that needs to be active to process price books. All 3 lines as shown in the screen shot below need to have the same PC name assigned. 

   

 View the Error Log under the Electronic Commerce Configuration menu.