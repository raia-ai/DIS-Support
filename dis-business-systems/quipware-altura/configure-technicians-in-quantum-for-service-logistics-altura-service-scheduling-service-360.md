---
title: "Configure Technicians in Quantum for Service Logistics/Altura Service Scheduling/Service 360"
source: "salesforce_articles.md"
tags: ["Quipware", "Altura"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Configure Technicians in Quantum for Service Logistics/Altura Service Scheduling/Service 360."
long_description: "This document provides information about Configure Technicians in Quantum for Service Logistics/Altura Service Scheduling/Service 360 from the DIS Salesforce Knowledge Base."
---

_Configure Technicians in Quantum for Service Logistics/Altura Service Scheduling/Service 360 – Service Logistics_

Introduction 

 This document provides instruction on how to add Technicians in Service Logistics for Quantum users, as well as how to ensure their correct email and Work Type labor rates are used. 

 Click here for instructions on managing technicians that have been added to the system. 
 Click  here for instructions on how to remove a technician once they have been added. 

  

 To Add Technicians 

 Select Address Maintenance (Marketing | Address Maintenance) . The first Address Maintenance screen opens. 

 

 Enter the Address Number for the Technician in the provided field and click Enter . The next Address Maintenance screen displays. 

 Important! Ensure you are in the correct division for the technician that is being added. If a technician is already in the system, but assigned to the wrong division, contact DIS Support to correct the issue UNLESS  you are on 24V3 or higher OR DIS_81 or higher. Dealerships on 24V3 or higher OR DIS_81 or higher can change a technician's division using the instructions in the Change a Technician's Division Assignment section below. 

 

 Enter the Technicians last and first name in the fields provided. 

 Enter a unique E-mail for the technician. 

 Important! The E-mail address must be a valid E-mail address and unique to the Technician. The same E-mail address CANNOT be used for more than one technician. If the technician has already been entered into the system, but has been assigned a fake or Non-unique E-mail address, replace it with a valid and unique address. The E-mail will be updated in Altura the next time the information is synced. 

 Select the Technician check box. 

 Click Enter to save. 

 Note: Once a technician has been added in Time Clock/Had their labor rates verified, they can be assigned to a new division. See the section after the following for instructions on assigning the technician to a new division. 

  

 Verify Labor Rates assigned to Technicians 

 The system determines labor billing rates according the Work Type rates assigned to the technician performing the work. 

 Select Table Maintenance (P.O.S. | Time Clock | Table Maintenance). The TC Table Maintenance screen opens. 

 

 Click the Technician Table button. The Technician Table screen displays. 

 Type the Technician ID in the provided field and click OK . The next Technician Table screen displays. 

 

 Verify the technician’s labor rates for each of the work types. If necessary, update and click OK to save. 

  

  

  

 To Change a Technician's Division Assignment 

 Important! your dealership must either be on 24V3 or higher OR DIS_NR81 or higher to access/complete this process. 

 When a technician is added to the system, they are assigned to the division from which they were added. To change the division that a technician is assigned, access the technician in Address Maintenance.  

 

 Click the Change Tech Division button, select the new division, and then click Select and Return . 

  

 Run a Test Punch for the New Technician 

 Punching the technician in and then immediately out of Time Clock establishes them so they can be accessed for setup in Altura and/or Service Logistics. 

 Once technicians are setup in Quantum, access Technician Management in Altura (Admin Settings | Staff Users | User Management | Technician Management tab). 

 

 Assign each technician the Role of technician and a password to complete setting up the technician(s). Click here for more information on user roles and permissions in Altura.