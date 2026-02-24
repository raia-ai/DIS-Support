---
title: "Submit CLAAS Purchase Order (Stock Order) – Quantum/Altura"
source: "salesforce_articles.md"
tags: ["Quipware", "Altura"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Submit CLAAS Purchase Order (Stock Order) – Quantum/Altura."
long_description: "This document provides information about Submit CLAAS Purchase Order (Stock Order) – Quantum/Altura from the DIS Salesforce Knowledge Base."
---

_Instructions on submitting orders to CLAAS_

Introduction 

 The CLAAS interface allows you to submit Purchase Orders (Stock Orders) directly to their system. As part of this process, dealerships receive notification of when the parts are scheduled to be shipped, when the parts are actually shipped, and can access the order to see it's current status as detailed in this article. 

   

 To Submit Order to CLAAS 

 Create the purchase order in Quantum and Finalize it . 

 The Order Details screen in Altura opens and includes any  Ship-To Address information provided in Quantum. 

 Note : If you need to finish the following process at a later time, you can access the order by selecting Purchase Order (Manufacturer | CLAAS | Purchase Order) in Altura. 

 

 You must select the following fields and provide the associated information: 

 Details Section 

 Order Type : Select the drop-down and choose the correct order type from the list that appears. 
 Ship Date : Click the field and select the date you want to submit the order – normally the current date. 
 PO# : This is the name assigned to the order in Quantum and does not need to be changed. 
 If you are drop shipping the Order, select the Drop Ship check box at the top of the section. If you select the Drop Ship check box, you must also provide a Comment and a contact phone number. 
 Comments : Click the field and type any desired comments. If you selected the Drop Ship check box, you must provide a comment. 
 Contact Number : If the Drop Ship check box is selected, you must provide a phone number. 

 Ship To Address Section 

 This section lists the Ship To information provided in Quantum. You can change it if necessary. If you selected the Drop Ship check box, you must update these fields with the correct information. Note the following: 

 Shipments can only be sent to the U.S. and Canada 
 Zip codes are the 5 number version and NOT the 9 number version 
 Postal Codes must be configured as Letter Number Letter Number Letter Number (spaces are automatically added) 

 When you have finished entering information in the Details and Ship To Address sections, click the Save Progress button in the lower-right hand corner. 

  

 Review Order 

 The next step in the process is to review the order and confirm the Details, Ship To Address, and included parts are correct. 

 Click the Review option under Actions on the left-side of the screen. The Review screen displays. 

 

 Do one of the following: 

 If there is an issue with any of the Details or Ship To Address information associated with the order, select the Edit option under the Actions section on the left-side of the screen and make the necessary updates, save the updates, click the Save Progress button, then Review the order again. 
 If/when the order is correct, click the Submit Purchase Order button. A message displays at the bottom of the screen stating Purchase Order Submitted, the Status at the top of the screen changes to Submitted, and the selectable options on the left-side of the screen are updated as shown below. 

 

 After submitting the order, the Acknowledgement option on the left-side of the screen is grayed out. After a moment, click the Refresh button at the top of your browser as shown below. The Acknowledgement option becomes selectable. 

 

 Select the Acknowledgement option. The Status switches to Acknowledged and the screen updates with the following information as indicated by the green arrows above: 

 CLAAS No. (CLAAS order number) 
 Customer No. 
 The dollar amounts for the order (pretax, tax, total with tax) 
 The Ordered Part Number as identified by CLAAS 
 The Originating Warehouse (the warehouse from where the part will be shipped) 

 View Purchase Orders/Shipment Information 

 When orders are shipped from CLAAS, CLAAS sends notification emails to the dealership. At any time, dealerships can access the purchase orders in the system through Altura and then select them to view specific details about the order. 

 Select Purchase Orders (Manufacturers | CLAAS | Purchase Orders). The Purchase Orders – CLAAS screen displays, listing orders in the system and their current status. 

 

 Click anywhere on an order line to view specific order details. The Purchase Orders Details screen opens by default. 

 

 The following information is provided: 

 The order details and Ship To Address information mentioned in the previous section. 
 Part lines that include the part number as identified by CLAAS, the quantity of the part ordered, and the dealership bin location if it is assigned in Quantum. 
 The Part Lines can be sorted and searched to list and locate any parts. 

 Select the Acknowledgement option to open the Acknowledgement screen. 

 

 The information that displays on this screen is the same as what is listed above. 

 Click the Shipment option. The Shipment Purchase Order screen displays. 

 

 The Shipment number associated with each of the part lines is listed on the right side of the screen and is hyperlinked. 

 Select a Shipment hyperlink to view Shipment details. The Shipment Details screen displays. 

 

 The Shipment Details screen lists: 

 All Purchase Order numbers with parts that are included on the shipment (there can be multiple purchase orders included in a shipment). These Purchase Order numbers are hyperlinked allowing you to select them and access the Shipment Purchase Order screen detailed above. 
 The date the shipment was shipped and when it is expected to arrive. 
 The number of packages on the shipment, who is transporting the shipment, and the package/box number(s). 
 All of the part lines on the order, the number of those parts ordered, and the number of those parts shipped. 

 When shipments arrive, access Quantum and receive them as you normally would. 

   

 Miscellaneous Information 

 The warehouses where parts are shipped from and the company that ships the parts are determined by CLAAS. 
 If there is an error or incomplete information provided when the order is entered and finalized in Quantum, an Error message displays when Altura opens as shown below 

 

 Click the Edit Purchase Order button to access the Purchase Orders Detail screen in Altura and resolve the issue(s).