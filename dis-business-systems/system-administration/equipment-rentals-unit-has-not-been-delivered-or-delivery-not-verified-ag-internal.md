---
title: "Equipment Rentals: Unit ?????? has not been delivered, or delivery not verified. - AG Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Equipment Rentals: Unit ?????? has not been delivered, or delivery not verified. - AG Internal."
long_description: "This document provides internal system administration information about Equipment Rentals: Unit ?????? has not been delivered, or delivery not verified. - AG Internal."
---

_Equipment Rentals: Unit ?????? has not been delivered, or delivery not verified. - AG Internal_

Introduction 

 Equipment Rentals used to have a feature called Dispatch.  The idea was to keep track of where the units were in the process of getting them to the customer and then back from the customer.  This feature was disabled due to problems with the feature.  

 Occasionally a customer will X out of a screen when setting up a contract and the dispatch setting will get messed up. This can cause the following error when trying to close the contract. 

 Unit ?????? has not been delivered, or delivery not verified.  

  

 Solution 

 Typically when this happens we can manually update the status in the old Dispatch option with a hidden command key.  

 Please do not share this with our customers.  

 Take the menu option to Rent Equipment (X9-1) 

 On the Rental Customer screen hit F22. 

 Find the unit number you are working with.  This screen is in date time order so page down to the On Rent Date and time from the contract. 

 Use the Change option to change the status in dispatch from “Will Call”  to “Deliver”. 

 Then use the select option on the same line. Fill in the Delivery date and time.  (You can use the on rent date and time for this.) 

 Then Confirm. 

 Now you should be able to close the contract with out the error coming up. 

  

  If this does not work and the status is "Deliver". 

 Take the option to Change and change to "Will Call". 

 Then select and fill in the delivery date and time.  (Again, you can use the on rent date and time) 

 Then Confirm. 

 Now you should be able to close the contract with out the error coming up. 

  

 Note: 

 The process can change a little based on the Status in Dispatch. If you get stuck please contact Ruth.  
 The select and change options take you to different places depending on the Status. 
 If you get to a screen that talks about Consignment just back out.  Setting up something in consignment won’t help with this situation. 

  

 **This document is a work in process.  If you find information that should be added for change please let Ruth know. **