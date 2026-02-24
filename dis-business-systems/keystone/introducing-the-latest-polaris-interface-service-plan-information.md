---
title: "Introducing the Latest Polaris Interface: Service Plan Information"
source: "combined_Keyston.md"
tags: ["Keystone"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Introducing the Latest Polaris Interface: Service Plan Information."
long_description: "This document provides information about Introducing the Latest Polaris Interface: Service Plan Information from the DIS Keystone system."
---

## Introduction

This new interface allows you to quickly view service plan information by providing a Polaris vehicle identification number (VIN or serial number). Service plan information can include extended service contracts, warranty information, or information provided by the issuing dealer.

## Previously Released Interfaces
(Click titles to view documentation)
- Parts Locator
- Parts Inventory
- Price Files
- Unit Promotions
- Vehicle Service History
- Vehicle Specifications

## SERVICE PLAN INFORMATION

### To View Service Plan Information:

1.  Follow one of these paths from the Keystone main menu to access the Get Vehicle Specs screen.
    *   `(Units | Inquire/Update (Complete Access) | Highlight Unit and click the Inquire Unit or Update Unit button)`.
    *   `(Service | Inquire/Update Service Units | Provide Serial Number and click Enter)`.

2.  One of the following screens opens depending on the path taken:
    *   **Inquire/Update Units - Unit Information:** This screen displays detailed information about a specific unit in your inventory.
    *   **Inquire/Update Service Units - View/Update:** This screen provides an overview of the current equipment being serviced.

3.  Click the **Polaris Inquiry** button.

4.  The **Get Vehicle Specs** screen opens.

5.  Enter the Unit or Serial number in the provided fields. Alternatively, you can click **Unit** or **Serial#** and select them from the list that appears.

6.  Click the **Service Plan Info** button.

7.  The **Unit Service Plan** screen opens, displaying a message at the bottom of the screen stating that the request is being processed. The fields on the Unit Services Plan screen then populate with service plan information for the specified unit.

    **Example Populated Data:**
    *   **Unit:** P40000
    *   **Make:** TOURING
    *   **Serial #:** 5VPDW36N7D3018540
    *   **Model:** V13DW36NX
    *   **Extended Service Contract:**
        *   **Company:** AIZ
        *   **Type:** POLARIS VICTORY US PHASE II PROMO
        *   **Start Date:** 05/11/2013
        *   **Expiration Date:** 05/11/2013
        *   **Deductable:** 50
    *   **Dealer Info:**
        *   **Name:** AUSTIN TRAILERS & MOTORSPOR
        *   **Contact:** CHRISTINE BERLIN
        *   **Phone:** T: 816-350-7777
        *   **State:** MO US
    *   **Warranty:**
        *   **Type:** Basic
        *   **Start Date:** 05/11/2013
        *   **End Date:** 05/11/2014

8.  Enter another Unit or Serial number in the provided fields and click **Enter** to retrieve the service plan information. Alternatively, you can click **Unit** or **Serial#** and select them from the list that appears.

## PRICE FILES

### To Configure Part Price Updates:

The Price File Interface checks for updates twice a day. Default times are 7:00 AM and 2:00 PM, but can be changed in Backup Options (Parts | Price Update/ Parts Lists | Scheduled Price Updates | click the **Backup Options** button). Price book updates will only occur once a day. The system checks to ensure an update has not already been downloaded on that day before downloading an update. During the process, the existing price book is updated and the number of parts that have had a price change is sent to the user profile specified in the User Profile to Notify field in Electronic Commerce Configuration. The notified user will need to select Automatic Price Update from Price Book to update the inventory.

The configuration can be viewed in the **Polaris COMMUNICATIONS - Configure** screen, which displays:
*   Dealer Information
*   User ID
*   Passwords
*   Authorization ID
*   Price update subscription details, including the user profile to notify and the last update date.

## UNIT PROMOTIONS

### To View Promotion Options:

The promotions available to a specific model can be accessed by clicking the **Model Promotions** button on the Get Vehicle Specs screen.

1.  Follow one of these paths from the Keystone main menu to access the Get Vehicle Specs screen.
    *   `(Units | Inquire/Update (Complete Access) | Highlight Unit and click the Inquire Update Unit button)`.
    *   `(Service | Inquire/Update Service Units | Provide Serial Number and click Enter)`.

2.  One of the following screens opens depending on the path taken.

3.  Click the **Polaris Inquiry** button.

4.  The **Get Vehicle Specs** screen opens.

5.  Click the **Model Promotions** button. The **Model Promos** screen opens.

6.  Enter the Model number for the unit in the **Model** number field if you have not already supplied it. Click **Enter**. The following promotion information will display in the table:
    *   Start and end date for the promotion
    *   The promotion option type
    *   The class and category of the promotion

    **Example Promotion Data:**
    *   **Northeast ATV FAC (6264):**
        *   **Promo Code:** ATV-18-084-A
        *   **Dates:** 07/25/2018 - 12/30/2018
        *   **Type:** Standard - Base
        *   **Class:** Only 1 Rebate per VIN
        *   **Cat:** Finished Goods
    *   **FAL ATV Spirt U.S. (6288):**
        *   **Promo Code:** ATV-18-092-A
        *   **Dates:** 07/25/2018 - 12/30/2018
        *   **Type:** Standard - Base
        *   **Class:** Allow Multiple Rebates per VIN
        *   **Cat:** Finished Goods

7.  Select a promotion from the table and click the **Options** button. The **Model Promos – Options** screen opens displaying each option with its details, including whether it can be bundled together with another option (indicated by `AND/OR`).

8.  Click the **Fold/Unfold** button. The Option fields expand showing additional information depending on the type of option, such as amounts of rebates or the minimum finance charge.

    **Example Expanded Option Details:**
    *   **REBATE:** Northeast ATV FAC (6264) Rebate 1000.00
        *   **Rebate Amount:** 1000.00
    *   **FINANCE:** SHEFFIELD - 2.99% / 5.99% / 11.99% - 36 mos.
        *   **Min Finance Charge:** 0.00
        *   **Promo Apr:** 2.99, **Std Apr:** 0.00, **Default Apr:** 0.00

## VEHICLE SERVICE HISTORY

### To Access Vehicle Service History

The vehicle service history information can be accessed by clicking the **Polaris Inquiry** button on either the **Inquire/Update Units** or **Inquire/Update Service Units** screens.

1.  Click the **Polaris Inquiry** button.
2.  The **Polaris Communication – Get Vehicle Specs** screen opens.
3.  Enter the unit VIN in the **Serial#** field and click the **Service History** button.
4.  The **Service History – Bulletins** screen opens, allowing you to work with bulletins or warranty claims.

### Bulletins

You can print a report of the bulletins listed in the table, view the PDF of a selected bulletin, and view bulletins associated with a selected bulletin.

*   Click **Print** to generate a report of the bulletins listed in the table.
*   Click **Related Bulletins** to open the **Related Bulletins** screen, listing bulletins and the bulletins they are associated with.
*   Select a bulletin in the table and click the **Link to PDF Details** button to view a PDF of the bulletin (e.g., a Technical Service Bulletin).

### Warranty Claim History

Claim History allows you to view the cause, complaint, and corrective action taken for each warranty claim as well as the parts and diagnostics associated with the claim.

1.  From the **Service History - Bulletins** screen, click the **Claims** button. The **Service History - Claims** screen opens. Click **Print** to generate a report listing the claims.
2.  Select a claim and click the **Cause/Complaint** button to view the recorded cause, complaint, and correction. Click **Print** to print this information in a report.
    *   **Cause:** The reason for the issue (e.g., "bad inspections").
    *   **Complaint:** The customer's or dealer's reported issue (e.g., "numerous imperfection in paint finish on tank/saddlebag").
    *   **Correction:** The action taken to resolve the issue (e.g., "new saddlebag lid r/h/ new fuel tank").
3.  Select a claim from the table and click the **Parts** button to view information about parts associated with the claim, including the part number, description, and quantity.
4.  Select a claim from the table and click the **Diagnostic Codes** button to view diagnostic types and codes associated with the claim (e.g., `FailureDate: 2013-01-18`).

## PARTS LOCATOR

### View Polaris Part Location Information

Using the Polaris interface, you can search for and view Polaris parts available at all of the other dealerships who subscribe to the Polaris Interface through DIS Corporation.

1.  Select **Parts Inquiry** from the Keystone main menu (`Parts | Parts Inquiry`). The **Parts Inquiry - Information** screen opens.
2.  Type the vendor code that you use for Polaris and the part number that you are searching for, then click the **Comms** button.
3.  The **Dealer Locator** screen opens, allowing you to select the Search Type to locate parts. The **Dealer** option is the default Search Type. Leave it selected and click **Enter**.

    > **Note:** You can view part inventory for dealerships within a specific mile radius of your dealership by typing the maximum mileage in the **Distance** field and selecting the **Dealer Radius** Search Type. You can also view information directly from Polaris by selecting the **Supplier** Search Type.

4.  The **Dealer Locator** screen populates with the names, locations, and phone numbers for dealerships that have the part, as well as the quantity of the part currently in their inventory.
5.  If you click the **Fold/Unfold** button on the **Dealer Locator** screen, three additional lines of information will display:
    *   **Contact:** Name of the contact at the dealership.
    *   **Email:** The contact's Email address.
    *   **Web:** The address for the dealership's website.
6.  If you click the **Email** button (often represented by an envelope icon), an email will open on your system with the contact's email address already inserted. You will only need to provide the Subject and context before sending.

## PARTS INVENTORY

### Submit Polaris Part Inventory

Your available Polaris Part Inventory is updated for the Dealer Locator option during your nightly backup. You can submit your inventory file immediately using the Send Part Inventory option. You can submit all of your Polaris part inventory or just parts from specific classes.

#### Send Inventory Immediately

1.  Select **Send Part Inventory** from the Keystone main menu (`Manufacturers | Polaris | Send Part Inventory`). The **Submit Part Inventory** screen opens.
2.  Click the button **Click Here to Send Inventory Immediately** to submit your inventory.

### View Status of Part Inventory Submission

You can check the status of each submission and resend it if it failed.

1.  Select **Resend/Review Log** from the Keystone main menu (`Manufacturers | Polaris | Resend/Review Log`). The **Send List** screen opens.
2.  Review the statuses of the submitted inventory files in the table. If a submission did not go through for any reason, it will have a **Failed** status.
3.  Highlight the failed file and click the **Resend** button to submit the inventory file again.

## VEHICLE SPECIFICATIONS

### View Vehicle Specifications and Available Options

You can enter the serial number for a Polaris unit in your inventory and view its specifications as well as any available options. You can access this information from either the Units or Service menus.

1.  Follow one of these paths from the Keystone main menu:
    *   `(Units | Inquire/Update (Complete Access) | Highlight Unit and click Update Unit button)`.
    *   `(Service | Inquire/Update Service Units | Provide Serial Number and click Enter)`.
2.  One of the corresponding screens opens depending on the path taken.
3.  Click the **Polaris Inquiry** button.
4.  The **Get Vehicle Specs** screen opens.
5.  Click the **Retrieve Specs** button. The fields on the Get Vehicle Specs screen populate with the available specifications about the unit.
    *   **Example Data:** Year, New/Used, Product Line, Engine, Size, Production Date, Warranty Date, Sale Date, Description, Weight, Notes, Serial #, Model Group, Model Class, etc.
6.  If there are options available for the unit, the **Options** button will appear. Click the **Options** button.
7.  The **Get Vehicle Specs** screen displays options that are available for the unit. You can toggle between the Specifications and Options by clicking the **Specifications/Options** buttons.
    *   **Example Options:** Motor, Dash-Mounted Fan, Windshield Washer, Headlights, Bumpers, Body Color, Batteries, etc.
8.  You can click the **Specifications** button, supply a new serial number, and click **Enter** to view that unit's specifications and available options.

    > **Note:** You can view specifications/options for any Polaris unit from this screen, even those that are not in your inventory.


title: "POS_Profitability_Report_Article"
source: "POS_Profitability_Report_Article.pdf"
tags: ["POS", "Profitability Report", "Keystone", "Sales Analysis", "Cost Calculation", "Report Setup", "DIS", "Labor Costing", "Parts Costing", "Inventory"]
version: "1.0"
last_updated: "2024-05-22"
short_description: "A guide on setting up and running the POS Profitability Report in the Keystone system. This document outlines how to create report templates, select various parameters, and generate reports to track profit margins on a ticket-by-ticket basis for different departments, salespeople, and customers."
long_description: "This technical document provides a comprehensive walkthrough of the POS Profitability Report feature within the DIS Keystone software. The report is designed to allow users to track profit margins for all Point of Sale (POS) invoices on a detailed, per-ticket basis. The guide is divided into three main sections. The first section, 'Setting up the report,' offers a step-by-step process for creating new report templates. This includes naming the report, defining column headings, assigning document types (e.g., invoices, work orders), and linking specific sales codes to the report columns. The second section, 'Running the Report,' explains how to generate a report using a pre-configured template, specifying parameters such as date range, salesperson, and customer. The final and most detailed section, 'How Cost is Calculated,' provides a thorough explanation of the logic used to determine the cost of sales. It breaks down the calculation methods for different categories, including Parts, Miscellaneous Sales, Labor, and Unit Costing (Whole Goods), detailing how the system uses sales code formats, GL account settings, and default factors to derive cost figures. This guide is essential for users who need to perform in-depth sales and profit analysis."