---
title: "Perform and Submit Activate (ASIP) Inspection - Quantum / Altura"
source: "salesforce_articles.md"
tags: ["Quipware", "Altura"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Perform and Submit Activate (ASIP) Inspection - Quantum / Altura."
long_description: "This document provides information about Perform and Submit Activate (ASIP) Inspection - Quantum / Altura from the DIS Salesforce Knowledge Base."
---

_ASIP Inspection Process_

Introduction 

 Activate is a program that provides technicians with prebuilt inspection checklists for units/equipment. The intention is the inspections are performed on customer equipment before any work is completed so dealerships can provide the customer with a quote based on issues found during the inspection. The customer then selects which maintenance to perform, and the service manager enters the agreed upon maintenance into Activate which relays this information back to Quantum adding any parts, estimated labor, and notes to the work order. 

 This article details the following aspects of the Activate inspection process: 

 Create Work Order in Quantum & Generate Inspection(s) 
 Download, Complete, and Submit Inspection Checklists 
 Create Quote/List of Offers 
 Log Customer Maintenance Decisions 
 View Work Order with Activate Maintenance & Associated Information in Quantum/Altura 

  

 Create Work Order in Quantum 

 Create a work order in Quantum as you normally would. This ensures the correct unit is selected and logs the time spent performing the inspection of the equipment. 

 The unit information and technician must be entered / assigned to the work order. 

 

 Click the Navigation button and select Service 360 from the fly-out menu. 

 The Work Order displays in Altura. 

 

 Select the ASIP check box at the top of the screen. 

 Important! If the unit information was not provided in Quantum and/or a technician has not been assigned to the work order, the ASIP check box is NOT enabled and NOT selectable. 

 Within a minute of selecting the ASIP check box, the work order information is communicated to Activate, and an inspection for the equipment is generated/available for technicians to select on their tablet or phone. 

  

 Download and Perform Inspection (Technician) 

 The technician receives notice that they have a new work order to complete (see below). 

 

 Select Download to access the inspection. The Inspection checklist(s) download along with the customer and unit information. 

 

 Select the General tab. The General tab allows the technician to provide/update general information about the unit and take/attach any relevant pictures of the unit. 

 

 Tap on any Machine Information entry line and update the information as necessary. 

 Tap on the Camera icon associated with any of the Machine Media options and take/add images. 

 Notice that the current machine section being photographed is both at the top and bottom of the screen. 

 

 Tap Next Section to go to the next machine section to be photographed and record any desired images. 

 Proceed through each Image section or tap Done when finished to return to the main Inspection screen. 

 Select the Detail tab. Available check lists display. 

 Note : Dealerships can require that technicians perform specific inspection steps. Required steps are indicated by an exclamation check mark icon on the right side of the screen (encircled below). Technicians must complete these steps in order to submit the inspection and move on. 

 

 If the unit passes the inspection checklist/step, either select the check box as shown above or swipe right. The inspection step is marked as Passed. 

 If the unit DOES NOT pass an inspection step, swipe left. This opens the Inspection Detail screen. 

 

 Tap on the Notes section and provide any desired notes. 

 Select the camera or recorder icon and take/record any relevant media for the issue. 

 Tap Done when you have finished providing details about the inspection step issue. 

 

 Select the Action option and select Complete to indicated the inspection has been completed. 

 

 A notification displays at the top of the screen stating the Inspection has been sent. The service manager can now review the inspection results in Activate. 

  

 Create Quote/List of Offers in Activate (Service Manager) 

 The completed inspection displays in the To-Do List in Activate. 

 

 Select the Follow-up button for the inspection. The Opportunity Details screen displays listing any issues/opportunities noted by the technician during the inspection process. 

 

 View each portion of the completed inspection / potential offers and add parts and labor. Select the Parts option to view/select parts from a vendor diagram similar to the following. 

 

 Once parts and labor are added, send the quote to the customer for review via the provided link. An Action report containing the issues/offer(s) allows customers to approve or deny the service offers. 

  

 Log Customer Maintenance Decisions (Service Manager) 

 Once you’ve received the customer response, enter the information in Activate. 

 

 Select one of the available tabs to designate if the customer: 

 Has approved cost of parts AND labor ( PARTS AND LABOR ) 
 Just wants the parts ( PARTS ONLY ) 
 Does not want the work performed ( NO ) 
 Wants the work performed at a later date ( LATER ) 
 The offer isn’t applicable to the customer for whatever reason ( N/A ) 

 After selecting the appropriate tab, select the Approved or Not Approved option. 

 Once you’ve entered all customer selections, select the Save button on the right-side of the Offer Line. 

 If an Offer is approved, it will say so at the top of the Offer table and a Link to DIS button displays in the Offer line as shown below. 

 

 Click the Link to DIS button for all approved offers. A message displays stating the Lead linked successfully and the offer is now added to the work order in Quantum. 

 

 Click the OK button and exit from Activate. 

  

 View Work Order with Added Activate Maintenance 

 Access the work order in Altura or Quantum. Note that each approved issue/offer is listed as its own segment on the work order as shown below. 

 

 Select a Work Order segment. 

 

 The parts that were selected/added in Activate are now assigned to the work order segment. 

 This is how the work order appears in Quantum (Note the New technician notes exist message). 

 

 Important! If a part was added in Activate that IS NOT currently in inventory, the part is added to the work order as a Note line (uses sales code with Notes format). If the part that was added in Activate IS currently in your inventory, it is added as a Part Line (uses sales code with Parts format). The intention is that the parts department will order/adjust the part, add it to the work order, and delete the note lines from the work order. 

 Remove the Note lines from the work order when the parts to be used are added to the work order. 

 

 In the fields at the top of the screen, enter the Segment and Note sales code assigned to the Note lines to be removed. 

 Select the Navigation button, then select Notes . 

 

 Select the note lines and click the Delete Line button. 

 Repeat this process for every segment to remove note lines used to show parts that were not in inventory. 

  

 View Inspection Report / Re-Process ASIP (Re-Link to Quantum) 

 You can access the work order in Altura and view the completed Inspection Report or request that ASIP Re-Process the information if there were any issues with receiving inspection information when Link to Quantum was selected in Activate. 

 

 View Report 

 Select the Action ellipsis ( …), then select the Inspection Report option. A report similar to the following displays. 

 

  

 Re-Process ASIP 

 If all of the information from Activate does not migrate to Quantum correctly, you can request that Activate resubmit the information. 

 Select the Action ellipsis ( …), then select the Re-Process ASIP option. Any information that did not migrate to Quantum from Activate correctly is uploaded. 

  

 View all ASIP Work Orders in Altura 

 

 Select Work Orders in Altura (Service | Work Orders) . 

 Select Filter on the Work Orders screen, then select the ASIP check box at the bottom of the Filter Results screen. 

 Select Apply . Only ASIP work orders display on the Work Orders screen. 

  

 View all Parts on Work Order 

 A Work Order Parts Summary can be generated that provides a single listing with total quantity of all of the parts on a work order.  Since the same part can be listed in multiple segments, this report prevents you from having to look through each segment of a work order to tally the total quantity of a part needed. 

 

 Select the Action icon next to the ASIP check box. 

 Select WO Parts Summary . The Parts Summary is generated.