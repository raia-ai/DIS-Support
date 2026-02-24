---
title: "Configure Cycle Counts - Quantum"
source: "salesforce_articles.md"
tags: ["Quipware", "Altura"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Configure Cycle Counts - Quantum."
long_description: "This document provides information about Configure Cycle Counts - Quantum from the DIS Salesforce Knowledge Base."
---

_Configure Cycle Counts - Quantum_

Introduction 

 Use cycle counting to break down inventory counts into smaller batches. This allows parts to be counted on a frequent basis, creating a more effective strategy for minimizing inaccuracies. 

 An automatic list of parts is generated each day based on the relative demand or value to your dealership. This selection process is based on a set of user defined parameters, allowing you to control this calculation. Use Cycle Count Configuration to set up your cycle count parameters to reflect the way you want your parts list to be calculated each day. 

 Important! This feature is only available for dealerships who use DIS barcode scanners or are performing the cycle count in Altura. Barcode scanners ARE NOT required for performing a cycle count in Altura. 

 Important! When a physical inventory is taken, the system updates the last count date for the counted parts. As a result, daily cycle counts may stop generating as cycle counts are generated based on the last count date and the number of times the part has been counted. This is especially true after an annual physical inventory has been taken. 

 Consider creating a manual count as it may take time before parts start showing up in generated cycle counts. 

 To Configure Cycle Count Parameters 

 Select  Cycle Count Configuration (Parts | Parts Inventory Adjustment | Parts Inventory Cycle Count | Cycle Count Configuration) . The Cycle Count Configuration - Cycle Count Defaults screen opens. 

 

 Select the Export Part Count List.... check box if you would like to remove the current inventory quantity from the exported count list and prevent those who are counting parts from being influenced by current inventory numbers. 

 Select the Default to print "Report.... check box to have a report print if any variances are found between the beginning quantity and the quantity entered after counting. 

 Type the number of days in a year that you would like to perform cycle counting in the Number of days per year that cycle count will be performed field. (After holidays and weekends, there are usually around 250 work days a year.) 

 The number of times that the part is counted per year depends on the demand level that it falls under. Click in the column and type over the existing number if you wish to change the frequency that parts within the listed demand level are counted. 

  

 To Calculate a Parts Demand Level Ranking 

 You can use the Data Mine option to calculate a parts Demand Level Ranking. By using Data Mine, the demand level will be re-calculated every time that part is updated - such as through a sale. 

 Click the  Data Mine Defaults  button on the Cycle Count Configuration - Cycle Count Defaults screen. The Cycle Count Configuration - Data Mining Defaults screen opens. 

   

 In the Number of months to include in "Demand Range" field, type the number of months to consider when calculating the demand level. 

 In the Demand Level = N... field, type the minimum number of months a part must be in inventory before it can be assigned a demand level. 

 Select the Define Level "5" if inactive.... option if you would like to put inactive parts into a demand level that will not be included in cycle counting. Inactive parts are those without on-hand quantity and a last receive/sale date preceding the last count date. 

 Select whether to use Calls or Pieces to define demand levels. In the third column of the table, type the demand minimum for each level. Demand is defined by Calls or Pieces. 

 Click  Enter  to save. Click  Back  to return to the Cycle Count Configuration - Cycle Count Defaults screen. 

  

 To Define a Parts On-Hand Quantity by Priority Order Code 

 You can use the Priority Order Codes assigned to parts to define the on-hand quantity for a part. This allows you to obtain a more accurate reading of the actual parts on-hand. 

 Click the  Reservations Config  button on the Cycle Count Configuration - Cycle Count Defaults screen. The Cycle Count Configuration - Reservations Configuration screen opens. 

    

 In the Subtract from Onhand? column, click on any box to add or remove the subtract from on-hand quantity designation. Parts assigned to designated Priority Order Codes will be removed from on-hand quantity totals. This only affects the on-hand amount if the document is still open. 

 Click  Enter  to save. Click  Back  to return to the Cycle Count Configuration - Cycle Count Defaults screen. 

  

 Screen Field Definitions 

 Additional details about the information found on screens in this procedure are listed below. 

 
 Cycle Count Configuration - Cycle Count Defaults 

 
 
 Field 

 
 Notes 

 
 
 Export Part Count List with On Hand Quantity set to zero ("Blind Count") 

 
 Select if you would like the count to be a "blind count" (on-hand quantity will display as zero). 

 
 
 Default to print "Report of Changes to Quantity" when count validated 

 
 Select if you would like a report to print of changed part quantities when the count is validated. 

 
 
 Number of days per year that cycle count will be performed 

 
 Supply the number of days per year that the count will be performed (default is 250). 

 
 
 Demand Level 

 
 Displays the demand level rank. This is calculated using Data Mine default parameters that are set up as a function of the Demand Analysis Report (Parts | Parts Reports | Demand Analysis Report) . 

 
 
 Description 

 
 Displays the demand level description. 

 
 
 Number of Parts 

 
 Displays the number of parts for that level. 

 
 
 Count Per Year 

 
 You can change the default number of times a part should be counted for each demand. 

 
 
 Total Counts 

 
 Displays the total counts for the level. 

 
 
 Percent of Total 

 
 Displays the percent of level from total parts. 

 
 
 Daily Counts 

 
 Displays the number of counts per day. 

 
 

   

 
 Cycle Count Configuration - Data Mining Defaults 

 
 
 Field 

 
 Notes 

 
 
 Number of months to include in "Demand Range" 

 
 Select the number of months to use when calculating the demand level, up to 108. 

 
 
 Demand Level = N. Inactive parts are categorized as new if they have been added in the last 

 
 Select the minimum number of months in inventory before new parts (N) can be assigned a demand level, up to 99 months. 

 
 
 Define Level "5" if Inactive, has zero quantity, and its last sale date & last receipt date are before the last date counted. 

 
 Click "Yes" if you have a large number of inactive parts. This will put these parts into level 5. 

 Note:  This will place parts with no on-hand quantity and where  both  Last Receive Date and Last Sale Date precede the Last Count Date into a separate demand level. This level will not be included in your cycle counting. 

 
 
 Define "Demand" using "Calls" (sale events) or "Pieces" (quantity sold). 

 
 Select either Calls or Pieces to use to define demand levels. 

 
 
 Demand Level 

 
 Displays the demand level rank. 

 
 
 Description 

 
 Displays the demand level description. 

 
 
 Demand Minimum 

 
 Number of demand minimum defaults can be changed, if desired.   

 
 

   

 
 Cycle Count Configuration - Reservations Configuration 

 
 
 Field 

 
 Notes 

 
 
 Priority Order Code 

 
 Displays the priority order code. 

 
 
 Subtract from Onhand? 

 
 Select the priority order codes you wish to subtract from the on-hand amount when calculating the on-shelf quantity for exporting the count list.   

 Note:  This only affects the on-hand amount if the document is still open. 

 
 
 Description 

 
 Displays the priority order code description.