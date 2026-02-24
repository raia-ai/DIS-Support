---
title: "Sales Logistics - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Sales Logistics - Ag Internal."
long_description: "This document provides internal system administration information about Sales Logistics - Ag Internal."
---

_Sales Logistics - AG Internal_

Sales Logistics: Dealership unit inventory on iOS and Android devices!  

 Put detailed, current unit inventory information in the hands of your sales team, wherever they happen to be. Unit Information is automatically passed from your Keystone or Quantum business system to our Sales Logistics server. Authorized sales reps automatically receive inventory updates from Sales Logistics on their smartphone or tablet. Add unlimited images, search and filter the entire inventory, take physical inventory, track inventory aging, check out units for a demo, and much more.  

   

   Sales Logistics FAQs  

    

 What kind of devices can I use?    
   

 Smartphones  
 Tablets  

     

 What operating systems can I use?   

 Apple IOS (14.3 or higher)  
 Android (11.0 or higher)  

      

   

 What are the requirements for the devices?   

 GPS for location services  
 Rear facing camera (lens facing away from the user) for taking unit pictures and QR code scanning.  
 Internet connectivity via WIFI or cellular 4G/LTE for data syncing  

 Note: Devices that lack the requirements stated above will be unable to access the app on the Play Store or App Store.   

    

 How often is the inventory list updated?   
 The data is refreshed every 15 minutes.  

  

 What units are included?   

 Available (both new and used), ordered, and rental units. (A, O, R)  

 Note : Be sure your internal units are set up correctly as fixed assets, so they are not included as available units.   

    

 What information will be available to your sales staff?   

 Make, model, description.  
 Product code, in date, traded on unit.  
 Retail price, discount percent, suggested list, dealer list, cost.   
 Year, unit status, color, horsepower, and hours. 
 Location log updated by GPS location each time an image is assigned or a QR tag is assigned.  
 Internal and external specs.   
 Rental revenue, rental cost, rental start date and rental status.   

  

 Can I restrict certain information from being viewed?   

 Yes. costing information, including unit cost, flooring amount, rental revenue and rental cost, can be masked if requested.  

  

 How can I use the dropdown to quickly locate a unit in my inventory?   

 The dropdown categories can be used to filter or sort the list of units:  

 All Makes :  In alphabetical order by make, includes new and used.  

 Groups :  New, Used, Rental, Other, uses new or used field (blank will be included in New) and unit status code.  

 Favorites :  User specific indicated by the star icon. 

 What's Hot :  Across all users, units indicated by the flame icon.  

 Untagged :  Units not assigned a QR cod. 

 Nearby :  Units within 3.5 miles or 5 KM. 

 Description:  Units sorted in alphabetical order by description.  

  

 Can I search for a particular stock number?   

 Yes. Tap the search icon    at the top to search by make, model, stock number, description or serial number. To search for a particular stock number, enter the stock number, or partial number, and all units that contain those numbers (or letters) will be displayed.  

  

 How many times can a password be used if I have multiple devices?   

 Only once . If you would like to install the application on multiple devices, you will need multiple email addresses setup in the Prism Admin page.   

 Passwords are system generated. You do not need to remember them.  

 Once you are signed into the app you are always logged in unless you delete the app.  

   

  What are the icons on the unit info page?   

  unit is a favorite for this user   

  unit is on the 'hot' list and is priced to sell   

  unit is tagged with a QR code   

     

 How are units tagged and what does this do?     

 Units can be assigned or tagged with a QR code. QR codes (aka Quick Response codes) are machine-readable labels that can be attached to a unit. Once tagged, scanning the QR label with your phone or tablet immediately brings up the unit information screen. Assigning the code or scanning the label also updates the GPS location.   

 Note: Be sure to attach the QR label in an easily accessible location on each unit - a vertical surface works best.   

     

 How is the Location History log updated?   

 An on-going history log shows you the date and time, the user, and the GPS location each time one of the following events occurs:   

 When a QR code is assigned.  
 Each time the QR label is scanned.  
 When a unit picture is added.  

     

 Can sales staff make changes to the unit information?   

 No, they cannot make changes to the unit detail information.   

 However, sales staff can add unit images or tag units, but these are not sent back to the business system.  

     

 How do I add a new salesperson?   

 To add a new salesperson, or to add a new device for a salesperson, click the Prism icon from any Keystone or Quantum session.  Need Access? Call or email into support.  

  

    

   

 On the Staff tab, click Add to add a new salesperson.    

 Enter the employee email, name, and password information. 

 Click Save. The email address and password can now be used to log into Sales Logistics. 

 The user will be prompted for the following on the login screen. 

 Enterprise ID = Dealer Number 
 Username and Password setup in Prism 

  

   

   

 Troubleshooting Tips 

 1)To Check status of a unit in Middle Tier use this internal only tool to check. 

 This is good for any dealer that has any type of unit feed. 

 Just change the dealer number (upper case) and unit number . 

 https://172.16.66.13:8181/wholegoods/getEquipment?enterpriseNumber=SW2258&stockNumber=E42420 

   
 

  

 Valid response should look like this. 

 Click on the URL highlighted to display information about the unit. 

   

  To format the data in your browser you need JSON View extension enabled. 

 https://chrome.google.com/webstore/detail/json-viewer/aimiinbnnkboelefkjlenlgimcabobli?hl=en-US 

   

 All the information comes from the unit's menu in the Business system. 

 2) How to update a unit in Keystone/Quantum to trigger an update to Middle Tier (Sales Logistics and  any unit feeds) 

 Log into Keystone/Quantum menu Units Inquire/Update (Complete Access) 

   

 Enter in unit number and click Update Unit. 

 *note* you will need to be in the same division that the GL account resides in to update the unit. 

   

 Change something like the color field and or add a color. Then change it back to what it was before.  

 Because a change is being made this should update to MT right away. 

 If in the SL app you can get out and back in. This will trigger a sync on the app itself. 

  

 TROUBLESHOOTING: 

 1) How to check if PRISM jobs are running in AS400 

 At a command line and enter WRKACTJOB and then page down. 

   

 Don’t see them running? 

 Type PRJOBS START 

 Still don’t see them running. 

 Check to see if there is an EPC lock WRKDTAARA EPCLOCK$ and delete it. Then type PRJOBS START 

 3) Check PRISM job log to Middle Tier 

 At a command line type and enter CHKJLOG. 

 Take a 5 to upload.log 

   

 Take a B and hit enter to go to the bottom. That is the latest data. 

   

 Look to the right. Status codes in 200’s are correct. 

   

 How to see what URLS are being used. 

 At a command line type DSPPFM ARWEBCFG1 

   

 For those that use WinSCP to log into Quantum server 

 You can find the picture sync script log file here: 

 /opt/scripts/syncunitpics/syncunitpics.log 

  

 If a dealer calls in about seeing this message when logging into the Prism admin page. 

   

 Most likely, have them hit enter and it will go through, this is a bug web development is aware of.