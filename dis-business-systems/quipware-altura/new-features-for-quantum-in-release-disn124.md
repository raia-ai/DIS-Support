---
title: "New Features for Quantum in Release DIS_N124"
source: "salesforce_articles.md"
tags: ["Quipware", "Altura"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about New Features for Quantum in Release DIS_N124."
long_description: "This document provides information about New Features for Quantum in Release DIS_N124 from the DIS Salesforce Knowledge Base."
---

_This article introduces new features available in Quantum that are currently in limited release._

INTRODUCTION    

 This document provides an overview of the main new features in Quantum Release DIS_N124. These features are currently in limited release but will be available to all dealerships in the future. Contact DIS at 1-800-426-8870 or Sales@discorp.com for additional information or to purchase products. 

 ALTURA 

 New Altura and Notify Menu Options on Left Side of Quantum Home Page 

 A new Altura option has been added to the left menu bar on the Quantum Home page. If a dealership has Notify installed, then the Altura option becomes a fly-out menu offering both options when selected. 

 

 While the Notify option has been moved from the top menu options to the left menu bar, the Notify options in Point of Sale and Customer 360 remain in the same location. 

 Users have to sign into Altura the first time they select the Altura option. After signing in one time, users remain signed in and are taken directly to their Altura dashboard when they select the Altura option. 

 POS 

 Automatic “Untitled Segment” Titles for Service Logistics Dealers 

 Invoice Segments that are created without providing a title using a Note sales code will now result in an “Untitled Segment” being automatically assigned to the segment when the invoice is placed on Hold. The title can be updated by selecting the note line and clicking the Edit Line button. 

 To ensure proper system function, invoice segments require a title that is created using a Note Sales Code as shown below. 

 

 If a segment is created and detail lines are added without a Note sales code created title, the Untitled Segment title is automatically applied if the invoice is put on hold using the Hold or Print & Hold button.  

 

 Internal/Warranty Address Required when Applying I/W Work Order Defaults 

 A new feature has been put in place to ensure that if the I (Internal) or W (Warranty) option is assigned to the invoice through Work Order Defaults, an internal address or unit number (for I) or warranty address (for W) must already be assigned under the Unit Info tab on the Sold-To screen in Invoicing (see below). 

 

 If the letter I is entered on the Work Order Defaults screen and an Internal Address/unit number is not supplied or the letter W is entered and a warranty address hasn’t been provided, an error message similar to the following 2 screenshots displays and the user must remove the letter before they can exit the Work Order Defaults screen. 

 

 

 If the Warranty Address, Internal Address, or Unit Number is removed from the Unit Info tab on the Sold-To screen after the work order defaults have been set, the assigned Internal/Warranty (I or W) default is removed and no longer displays on the Work Order Defaults screen. 

 Remember, default Internal and Warranty addresses can be assigned through Security Maintenance. 

 

 New Standard Line Screen Layout and Selection Method 

 The Standard Line screen layout has been updated to allow users to perform multiple actions and view the Standard Line entries that have already been added to the system. You can also now easily select and apply the Standard Line to a P.O.S. Invoice. 

 Add and View Standard Lines 

 Select Standard Line (P.O.S. | Table Maintenance | Standard Line) . The Standard Line Maintenance screen displays. 

 

 Click the Add button to add a new standard line. 
 Select a Standard Line and click Inquire to view additional details about the standard line. 
 Use the Position To fields and Sort by options to locate existing standard lines. 

 Add Standard Line in P.O.S. 

 A new Standard Line button has been added to the P.O.S. Detail screen allowing you to quickly lookup and add the desired standard line. 

 

 Select the Std Line button on the Detail screen in Invoicing. The Select Standard Line screen displays. 
 Select the Standard Line you want to add to the invoice. 
 Click the Select button. The Detail screen re-opens with the standard line information added as a detail line at the top of the screen. 

 

 Click Enter to add it to the invoice. 

 ARCHIVE  

 Posting Edit List (Log)  

 When an accounting batch is posted through either Create Source Documents or the Post P.O.S. Documents menu option, a new Posting Edit List is generated and saved in Work with Archived Documents under the POS Batch Reports Document Type. The List (log) shows who posted the batch and whether it was posted from Create Source Documents (CSD) or Point of Sale (POS).  

  

 Access Work with Archived Documents (Archive | Work with Archived Documents) and select the POS Batch Reports Option.  
 Click OK . The Work with Archived Documents screen displays.  

 

 Select the DIV X CSD/POS Check For Errors Edit List document. Note that the document includes whether it was generated from a posting batch in CSD or POS.  
 Select the Open As PDF button to display the Edit List. The Posting Edit List document displays, listing the posted from location as well as the user who posted the batch.