---
title: "Equipment Management & Relationships | User Guide/How-to"
source: "salesforce_articles.md"
tags: ["Quipware", "Altura"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Equipment Management & Relationships | User Guide/How-to."
long_description: "This document provides information about Equipment Management & Relationships | User Guide/How-to from the DIS Salesforce Knowledge Base."
---

_QuipWare has many ways to identify a piece of equipment in the system.  This user guide provides general instructions and guidance specific to equipment groups, creation, maintenance, and set-up._

Module 1 - Equipment Relationships 

 Manufacturer Product Group . 2 

 Manufacturer Product Group Series Relationship . 3 

 Model . 4 

 Module 2 – Equipment Management .. 5 

 Section 1 – Model . 5 

 Creating a new Model 5 

 Enter Supplier Pricing . 6 

 Other Types of Pricing . 7 

 Special Pricing . 8 

 Section 2 - Attachment . 9 

 Creating the Attachment 9 

 Configuring the Model 10 

 Section 3 – Equipment Management Screen .. 11 

 Searching for Equipment 11 

 Search Results . 12 

 Equipment Screen . 13 

 Linecard . 15 

 Configure . 16 

 Configuration Screen . 17 

 Ownership Screen . 18 

 Warranty . 19 

 Section 4 – Financial, Document History, and Movement History .. 20 

 Financial Information: 20 

 Cumulative: 20 

 Analysis: 20 

 Graphics: 20 

 Movement History . 21 

 Document Financial History . 22 

 List of Figures . 23 

  

 Module 1 - Equipment Relationships 

 Manufacturer Product Group 

 QuipWare has many ways to identify a piece of equipment in the system.  Manufacturer, Product Group, Series and model identify it, these items all have relationships between each other.  For example, Manufacture to Model has a Many to one relationship, this means that you can only have one model for each manufacturer specified.

 Figure 1 – Manufacturer to Multiple Product Groups 

 

  

 Manufacturer and Product Group have a many to many relationship.  This means you can use a product group with many different manufacturer codes. 

  

 A Product Group is defined as similar types of equipment but not the same model or manufacturer.  For instance the group of dozers could include Volvo, Komatsu and Cat dozers of all types and sizes.  Groups can be classified detailed or in general. 

  

   

 Manufacturer Product Group Series Relationship 

 Figure 1_1 – Manufacturer, Product Group and Series 

 

  

 Series.  Is a further classification of Group, series can be used for searching and pricing.  In the above example the group is Dozers and the series under Dozers is Large, Medium and small. 

  

 Series is not required to set up equipment.  If the product catalogue does not contain a series designation it typically does not make sense to create one.

  

   

 Model 

 Figure 1_2 – Model Relationship 

 

  

  

 For Every Manufacturer, Group and Series you can have multiple models.  However, you can only have one series for every model. The relationship from model to series is one to many.  A model can have only one series. 

  

 Example: 

 Manufacturer: Crown

 Product Group: Class I

 Series: RR

 Model: RR5220-35

  

 

 The –35 in the model is the load capacity, in this example 3500 lbs. 

  

  

  

 Module 2 – Equipment Management 

 Section 1 – Model 

  

 The model file is similar to a parts price file.  The model file should contain all models of equipment that are sold or serviced by the dealer location.

  

 Creating a new Model 

  

 1. Double Click on the QuipWare application main menu folder on the desktop

 2. Double Click the QW Equipment icon

 3. Click the model Group on the Equipment Task Bar

 4. Click the Model icon

 

  

 Figure 2 – Model Detail Information Screen 

 

  

 5. Click  to create the new model 

 6. Select the Manufacturer

 7. Enter the Manufacturer supplier number or the number that is used to order the equipment from the supplier

 8. Enter the description, this description will print on customer documents.

 9. Enter product Group from the combo box

 10. Enter the Series

 11. Enter Weight and Volume

 12. Enter Open Information

 13. Enter the Required Statistic Code

 14. Enter any Status information

 15. Click OK to save all entered Information

  

 Enter Supplier Pricing 

 1. From the main model screen Click the Price L ist icon

 Figure 3 – Model Pricing Screen 

 

  

 2. Right Click and Select New > Supplier Price

 3. Enter the List Price (This is the price the customer is charged; typically the MSRP.

 4. Enter the Fleet Price (Often times there is not a fleet price however fleet price can be used to sell to other Dealers, National Account etc…)

 5. Enter Cost this is the price charged by the supplier.  (The supplier is not always the manufacturer)

 6. Click OK to save the changes

 7. Click Exit to return to the main screen

  

   

 Other Types of Pricing 

 Frozen Sale Price 

 A Frozen Sale price can be created for a type of customer for a particular period of time.

  

 1. Right Click New > Frozen Sale Price

 2. Enter the type of customer or List (MSRP)

 3. Enter Departments

 4. Currency and Date the price is good from.

 5. Enter the price that is being frozen for example List, Fleet or Net.

 7. The field to the right of the price is the date field.  Enter the date the price is good until.

 6. Click OK to Save the Price

  

 Figure 4 – Frozen Sale Price 

 

  

 Frozen List Price or Frozen Base Price 

  

 This is a base price that can be increased by a percentage amount.

  

 1. Right Click Select New > Frozen List Price

 2. Enter the price and the date the price is good for.

 3. Click OK 

 4. Click Exit to return to the main screen.

  

 Special Pricing 

  

 Special Pricing is used to give a customer a price for a given period of time. 

 1. Right Click Select New > Special Pricing

 Figure 5 – Special Pricing Entry 

 

  

 2. Enter the customer ID

 3. Enter a Contract number if this price is based on a contract to the customer

 4. Enter the Date the Contract is good from

 5. Enter the Date the contract price will end

 6. Enter the new price

 7. Enter the Branch the price is good for.

 8. Click OK 

 9. Click Exit in order to return to the main screen

  

  

 Section 2 - Attachment 

  

 Creating the Attachment 

  

 1. Click on the Attachment group on the Equipment Task Bar

 2. Click the Attachment icon

 3.  Enter the Manufacturer Code

 4. Enter the Attachment catalogue, part, id or the number, which is used to order this attachment for the parent equipment.

 5. Enter the Description

 6. If a line Card is associated with the attachment enter it here

 7. If the attachment is part of an option group enter the option group from the drop down box

             Example: 

                         An attachment might be associated with an option group if there is more then one choice for the option, such as color or type of tires.

 8. An alternate Plant reference id can be entered which can be used to order on a purchase order

 9. If the attachments can be categorized and the categories have been created select one at this point

 10. Enter the General Features

 Figure 6 – General Feature Options    

 
 Option

 
 Description 

 
 
 Equipment 

 
 If the attachment is going to be depreciated then it is equipment 

 
 
 Attachments 

 
 Items which are not inventoried 

 
 
 Parts 

 
 Items that are ordered separately as parts but are not typically depreciated 

 
 
 Option 

 
 If this is an option that can be purchase with the equipment 

 
 
 Accessory 

 
 An Accessory such as a mirror or even a CD player 

 
 

  

 11. Can be mounted by

 Figure 7 – Mounting Options 

 
 Option

 
 Description 

 
 
 Standard 

 
 Comes as a standard attachment 

 
 
 Factory 

 
 Is mounted by the factory 

 
 
 Dealer 

 
 Attached by the dealer 

 
 
 Importer 

 
 Attached by the importer 

 
 
 All Checked 

 
 All of the above applies 

 
 

  

  

 12. Enter pricing information for the attachment

 13. Click on the Configure button in order to define the Make, Group and Model the attachment is for.

  

 Configuring the Model 

 Figure 8 – Attachment Configure Screen 

 

  

 1. Select the Group, Manufacturer and Model the attachment is for

 2. Enter the quantity required

 3. Enter the quantity allowed

 4. Enter arrangement code an example might be for tires

 5. Click Add >> 

 6. Click Exit to return to the Main Attachment Screen

 7. Click OK on the main screen to save changes.

  

   

 Section 3 – Equipment Management Screen 

  

 Searching for Equipment 

 1. Click the Equipment group on the Equipment Task Bar

 2. Click on the Equipment icon

 3. At this point the Equipment Number field will be highlighted.

 4. To Search click the  on the button toolbar or enter an asterisk and hit tab or hit the Ctrl + f keys.

 5. The Homonyms Screen will appear

  

 Figure 9 – Equipment Homonyms Screen 

 

  

  

 At this point you can search by Group, Manufacturer, Series, Model, Description, Equipment or Dealer ID,

 Serial ID, Plat ID, Customer who owns equipment, model year, which inventory the equipment is assigned to Sales or Rent, how acquired reasons and Equipment Status.

  

 In addition you can search by the attachments that are on the parent equipments. Click on Advanced button to search by attachments.

  

 After the selections are made click F ind.  Clicking on the columns or moving the columns to different parts on the screen can organize the results. 

  

 

 Wild cards such as the asterisk can be used.

  

   

 Search Results 

 Figure 10 – Equipment Search Results Screen 

 

  

  

 Result Icons

  

        Equipment is available and has an attachment

                 Equipment is available to rent or sale

         Equipment is available but has notes attached to the equipment

      

      

 If the check is red it means the equipment is unavailable.

  

   

 Equipment Screen 

 Figure 11 – Equipment Management Screen 

 

  

  

 1. Dealer ID : Automatically assigned by QuipWare

 2. Equipment Description: Defaulted from the model file created earlier can be changed

 3. Serial ID: Factory Serial Number

 4. Plate ID: Crown intelligent part number

 5. New or Used Status Buttons: 

 6. Basis: Is this the basic unit

 7. Equipment Year 

 8. First Used Date: Automatically updated when the equipment is used either on a rental contract or a sales agreement.

 9. Product Group: Determined by the model number in the model file

 10. Manufacturer: Determined by the model number in the model file

 11. Series: Determined by the model number in the model file

 12. Model: Entered at the purchase order

 13. Power/Type: Enter the amount of power and type of power

 14. Odometer: Miles on Equipment

 15. Hour Meter: The number of hours on an hour meter

 16. How Acquired 

 17. Date Purchased: Comes from the purchase order or can be changed in the equipment file.

 18. Suggested Sale Price: This does not show up in the order screens it is used for used equipment and for reporting and inquiry purposes.

 19. Tracking Values: These values are from transactions in the system or from manual general ledger entries in QuipWare.

 20. Branch and Department where equipment is physically located

 21. Bin Location: All bin locations for equipment need to be secondary locations.

 22. Assigned To: Is this rental or sales equipment.

 23. Availability Status; is the equipment available to rent, on rent or down and in the shop.

 24. Tracked By Branch: Which branch is tracking the equipment the original branch that received the equipment.

 25. End User Defined Status: These choices can be added in the checking table

 26. Tracked By Department: Department tracking the status of the equipment

 27. Equipment Picture: Click on the Camera to add a picture of the equipment.

 28. Linecard: Click this button to see the Linecard screen

 29. Configure: Click this button to see the equipments configuration

 30. Ownership: Click on the ownership button to see additional information about the equipment.

 31. Warranty:   Warranty types and information.

  

  

   

 Linecard 

 Figure 12 – Linecard information 

  

  

   

 Configure 

 This screen will show any attachments on the basic unit.  Click on the Recycle or chasing errors icon to change the configuration.

 Figure 13 – Configuration Screen 

  

  

   

 Configuration Screen 

 The left windowpane will display the allowable attachments for the model of the equipment that was entered.

 Figure 14 – Configuration Screen 

  

  

 Ownership Screen 

 This screen will display the current owner and if owned by multiple owners.  If the owner of the equipment assigns an id to their trucks enter it on this screen. 

 Figure 15 – Ownership Details 

  

  

  

  

 Warranty 

  

 Figure 16 – Warranty Information Screen 

  

  

 Warranty: Type of Warranty

 H Meter: How many hours this type of warranty is good for

 From: The start date of the warranty

 Expiration: Warranty Expiration Date

 Description: The description of the warranty

 Type: Hours, Miles or Kilometers

 Max: Maximum amount the warranty will cover

 Days 

 Document References Field: When warranty is purchased or given this field can be used as a reference field.

  

   

 Section 4 – Financial, Document History, and Movement History 

  

 Financial Information: 

 Figure 17 – Cumulative Financial Information 

 

  

 Cumulative: 

  

 This screen will show MTD, YTD, and LTD management values for the equipment.  The Price with Configuration button can be checked or unchecked.  If checked it will show the parent units values and the values of the attachments. 

  

 In addition, if this is rental equipment the MTD, YTD and LTD rental days will be displayed.

  

 Analysis: 

  

 The analysis tab will allow an individual to display pre-defined worksheets.  These can be simple profit and loss calculations when the equipment is sold or a service analysis report.

  

 Graphics: 

  

 Displays the information from the analysis worksheets in graphical form.

   

 Movement History 

 Figure 18 – Movement History Screen 

 

  

 To view the equipment movement history Click the H istory icon

  

 The screen will display the movement history when received, rented, sold or moved from one branch location to another.

  

 Clicking on a movement record will display the following information:

  

 Department: Department where the transaction took place

 Document ID: The document number for this transaction

 Transaction Type or folder: 

 Customer ID: Customer who rented or purchased equipment

 Counter: Hour meter reading at time of transaction

 Odometer: Miles at time of transaction

  

   

 Document Financial History 

  

 Figure 19 – Document History Screen

 

  

  

  

 List of Figures 

 Figure 1 – Manufacturer to Multiple Product Groups . 1 

 Figure 1_1 – Manufacturer, Product Group and Series . 2 

 Figure 1_2 – Model Relationship . 3 

 Figure 2 – Model Detail Information Screen . 4 

 Figure 3 – Model Pricing Screen . 5 

 Figure 4 – Frozen Sale Price . 6 

 Figure 5 – Special Pricing Entry . 7 

 Figure 6 – General Feature Options . 8 

 Figure 7 – Mounting Options . 8 

 Figure 8 – Attachment Configure Screen . 9 

 Figure 9 – Equipment Homonyms Screen . 10 

 Figure 10 – Equipment Search Results Screen . 11 

 Figure 11 – Equipment Management Screen . 12 

 Figure 12 – Linecard information . 14 

 Figure 13 – Configuration Screen . 15 

 Figure 14 – Configuration Screen . 16 

 Figure 15 – Ownership Details . 17 

 Figure 16 – Warranty Information Screen . 18 

 Figure 17 – Cumulative Financial Information . 19 

 Figure 18 – Movement History Screen . 20