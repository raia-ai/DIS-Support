---
title: "Updating MAI last Fiscal EOY date in Security Maintenance - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Updating MAI last Fiscal EOY date in Security Maintenance - Ag Internal."
long_description: "This document provides internal system administration information about Updating MAI last Fiscal EOY date in Security Maintenance - Ag Internal."
---

_Updating MAI last Fiscal EOY date in Security Maintenance - AG Internal_

Updating MAI last Fiscal EOY date in Security Maintenance 

  

 Introduction 

 As of 23V2 we have added a last Fiscal EOY date to Security Maintenance. The issue is this date isn’t added until after the first EOY. The purpose of this project is to proactively add the date (update MAI) as we upgrade our dealers. 

 This date does two things: 

 It prevents closing the first fiscal month before running EOY for previous year. 
 It prevents running EOY if it’s already been run. 

   

 Steps to update the EOY date 

 Check to see how many File Sets and how many Divisions they have – Display MASP (in multiple File Sets if needed) 

 From a command line type DSPPFM MASP 

 

 Check their fiscal start and oldest open.  Type W150 in the Control field to get to column 150. 

 150 = fiscal start 

 151 = oldest open month 

 

 In this example the date is 0000 which means the system doesn’t know if EOY has been run. 

 

 Here’s how the same screen looks in Quantum. The system doesn’t know if EOY has been run. 

 

 Go to Retained Earnings to determine if and when EOY was run. Displaying transactions in Quantum will show date/time stamp. 

 In this example EOY for 2021 was run on 03/11/2022. March is closed, so the EOY transaction shows in History Transactions. 

 Based on this information, the EOY date in Security Maintenance should be 0122 (The first month of the new fiscal year). 

 

 At a command line type UPDDTA MAI  

 Page down.  Check division to make sure it’s the one you want to change. 

 If the division is correct press enter and update the ‘MAI EOY Last Ran’ field.  

 

 In this example enter 0122. 

 

 Verify dates by displaying MAI 

 

 You’ll now see the EOY date in Security Maintenance.