---
title: "New Features for Quantum in Releases 22v1 – 22v2"
source: "combined_Quantum_docs.md"
tags: ["Quantum"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about New Features for Quantum in Releases 22v1 – 22v2."
long_description: "This document provides information about New Features for Quantum in Releases 22v1 – 22v2 from the DIS Quantum system."
---

## Introduction
This document provides an overview of the primary new features in Quantum R22v1 – 22v2. If you are interested in purchasing Quantum or any other products, please contact DIS at 1-800-426-8870 or Sales@discorp.com.

## Accounting

### GL Power Add and Copy
The General Ledger Power Add option allows you to group multiple divisions and add or update a general ledger account in all of those divisions from any one of the grouped divisions. This prevents you from having to enter or update the general ledger information in each division separately. Furthermore, the system now prompts for the correct type of additional accounts during setup, guiding you through the process while showing the assigned accounts and their associated information on one screen.
You can also generate a report that lists the differences in each account across grouped divisions, allowing you to quickly identify differences and sync the accounts if desired.

**Click here** for in-depth instructions on using GL Power Add and Copy.

### Receivable Payment Batch Recovery
If your service is interrupted or your session is abruptly ended for any reason while creating a receivable's payment batch, the information is now saved and recoverable.

## Accounting/Archiving

### Check Reconciliation Reports
Check Reconciliation will now archive reports when completing the check reconciliation process. Reports will be located under the Accounting Reports option within the Work With Archived Documents menu item.

*Image: Screenshot of the 'Work with Archived Documents' screen showing archived check reconciliation reports.*

## Units

### Import (Additional) Unit Information
We have added the ability to import the following unit information through the .CSV file:
- New or Used – If this field isn't supplied the unit will be automatically designated as new.
- Retail Price
- Suggested List Price

**Click here** to view complete instructions for the import process, including the maximum entry length for the new fields and the spreadsheet column to which they must be assigned.

## P.O.S.

### Service Scheduling
The Service Scheduling option allows you to schedule work events for technicians from an existing work order or from scratch. Once an event has been scheduled, you can continue to add information to it as a Planned Work event and if desired, convert it to a Work Order.

*Image: Screenshot of the Service Scheduling interface, showing a calendar view with scheduled work events for technicians.*

**Click here** for instructions on using this powerful new tool. Contact DIS sales at 1-800-426-8870 or Sales@discorp.com for more information.

### Periodic Invoicing Printer Options
DIS now allows users to save their default printer settings in Periodic Invoicing. The same printer configuration screen that has been used in Invoice Entry now displays when Periodic Invoicing is accessed.

*Image: Screenshot of the 'Periodic Invoicing Printer Options' screen, allowing users to set default printers for various document types.*

### Segmented Work Orders with Enhanced Printing
A new paper-saving change allows you to print the segments of an enhanced work order one after the other rather than starting each segment on a new page.

## Manufacturers

### Kubota Interface Master
Canadian dealerships can now utilize many of the same features of the Kubota Interface previously only available to U.S. dealerships. The Kubota Interface allows you to view part availability at Kubota warehouses and other dealerships. You can view the location, price, and quantity of available parts. You can also use this option to place part orders.

- **Click here** to view the Canadian version of the Kubota Interface Master.
- **Click here** to view the most recent version of the Kubota Interface Master for U.S. dealerships.

### CLAAS PIM
CLAAS Parts Inventory Management (PIM) allows you to maintain a consistent inventory level for CLAAS parts through part file transfers between your dealership's system and CLAAS.

**Click here** to view a document on configuration, how to view the status of orders and resend if necessary, work with suggested transfers, and generate the Suggested Stock Orders Report.

### integrated Kubota Quote (iKQ) US Dealers Only
This feature allows you to quickly generate a quote for a customer from the Kubota website and send a PDF of the quote to the customers EasyFile in Sales 360.
> **Note:** This feature requires Easyfile and Sales 360. Contact Sales at 1-800-426-8870 or Sales@discorp.com for more information.
> This feature also requires DIS assistance with setup. If you are interested in this feature, please call or email the response line so we can add you to the install list and streamline the installation process.

#### To Configure iKQ (DIS will assist with the configuration process)
The first step of the process is entering the Kubota Dealer Numbers for the fileset which allows the assignment of quotes to specific divisions.

1.  Select **Kubota iKQ Configuration** (Manufacturers | Kubota | Kubota iKQ Configuration). The configuration screen opens displaying all of the Kubota Dealer numbers currently configured for your fileset.
    
    *Image: Screenshot of the Kubota iKQ Configuration screen listing dealer numbers.*
    
2.  Do one of the following:
    - Add a dealer number by clicking the **Add** button and entering the number on the following screen.
    - Change an existing number by selecting it from the table and clicking the **Change** button.
    - Delete an existing number by selecting it from the table and clicking the **Delete** button.
    
    Regardless of which option you perform, the screen that opens displays the Kubota Dealer Number field as shown below.
    
    *Image: Screenshot of the 'Edit Kubota Dealer Number' pop-up window.*
    
3.  Either enter the new number/change existing number and click **OK** to save or click **Delete** to remove the dealer number listed in the field.

#### To Generate Quote
> **Note:** These instructions are based on Kubota's Quote Website as of March 2019 and are subject to change.

1.  Access the integrated Kubota Quote website, provide your email address and password, then click the **Login** button.
    
    *Image: Screenshot of the Kubota website login page.*
    
2.  The Kubota iKQ dashboard displays.
    
    *Image: Screenshot of the Kubota iKQ dashboard showing new leads and quotes in progress.*
    
3.  Select the **Create New Quote** option. The Choose Quote Customer screen opens.
    
    *Image: Screenshot of the 'Choose Quote Customer' screen used to find or create a new customer.*
    
4.  Select the method by which you would like to locate the customer and provide the search terms. Click the search icon.
5.  Locate the customer in the Customer Search Results table and click the **Select** button.
6.  A new quote is created and the Add Products to Quote screen opens displaying the customer information and number for the newly created quote.
    
    *Image: Screenshot of the 'Add Products to Quote' screen after a new quote has been created.*
    
7.  Provide the identifying information for the equipment that you would like to quote in the Add Equipment field.
8.  Click the **Add** button. The Quote Options field displays listing the current information for the specified equipment. You may change the price of the equipment by clicking in the **Price Each** field and entering the amount that you would like to quote the equipment.
    
    *Image: Screenshot showing the added equipment details and pricing options on the quote.*
    
    A check box appears at the bottom of the screen allowing you to select whether or not to show the cash option on the quote.
    
    *Image: Screenshot showing the final quote details including cash option, taxes, and totals.*
    
9.  Click **Quote Actions** at the bottom of the screen, then click **Send to DBS**. A message appears stating the quote has been sent to the DBS.
    
    *Image: Confirmation message indicating 'Quote #3913 has been sent to DBS.'*

#### To Access Quote in Quantum
1.  Select **Sales 360** from the Quantum main menu. The Sales 360 dashboard opens. Click **Contacts**.
    
    *Image: Screenshot of the Sales 360 dashboard highlighting the 'Contacts' button.*
    
2.  Click the **Contacts** button at the bottom of the Sales 360 dashboard. The Quantum 360 Search screen opens.
    
    *Image: Screenshot of the Quantum 360 Search screen.*
    
3.  Enter your search terms into the Quantum Search line and click the **Quantum Search** button. The Quantum 360 Search screen opens displaying relevant matches. Select the contact from the search results. You MUST select the option with the contact icon.
    
    *Image: Screenshot of the Quantum 360 Search results, with the correct contact record highlighted.*
    
4.  The Contacts screen displays. Click the **EasyFile** option. The EasyFile screen displays.
5.  Select the quote you would like to view and click the **Open** button. A PDF of the quote displays.
    
    *Image: Screenshot of the EasyFile window showing a list of PDF quotes for the selected contact.*
    
    *Image: Example of the final PDF quote as generated and stored in Quantum.*

### Polaris Service Plan
This interface allows you to quickly view service plan information by providing a Polaris vehicle identification number (VIN or serial number). Service plan information can include extended service contracts, warranty information, or information provided by the issuing dealer.

#### To View Service Plan Information:
1.  Follow one of these paths from the Quantum main menu to access the Get Vehicle Specs screen.
    - (Units | Inquire/Update (Complete Access) | Highlight Unit and click the **Inquire Unit** or **Update Unit** button).
    - (Service | Inquire/Update Service Units | Provide Serial Number and click **Enter**).
2.  One of the following screens opens depending on the path taken.
    
    *Image: Side-by-side screenshots of the 'Inquire/Update Units' and 'Inquire/Update Service Units' screens, both showing a 'Polaris Inquiry' button.*
    
3.  Click the **Polaris Inquiry** button.
4.  The Get Vehicle Specs screen opens.
    
    *Image: Screenshot of the Polaris 'Get Vehicle Specs' screen.*
    
5.  Enter the Unit or Serial number in the provided fields. Alternatively, you can click **Unit** or **Serial#** and select them from the list that appears.
6.  Click the **Service Plan Info** button.
7.  The Unit Service Plan screen opens displaying a message at the bottom of the screen stating that the request is being processed. The fields on the Unit Services Plan screen then populate with service plan information for the specified unit.
    
    *Image: Screenshot of the Unit Service Plan screen populated with extended service contract and warranty information.*
    
8.  Enter another Unit or Serial number in the provided fields and click **Enter** to retrieve the service plan information. Alternatively, you can click **Unit** or **Serial#** and select them from the list that appears.

### JCB Communications
JCB Communications allows you to maintain a consistent inventory level for JCB parts through part file transfers between your dealership's system and JCB. You can specify the vendor/code combinations to consider when generating the part files, submit files to generate suggested orders immediately or during nightly backup, resend files that failed during submission, and specify customers whose sales transactions you don't want to consider when generating suggested stock orders.

#### Configure JCB Communications
In order for your system to communicate with JCB and transfer the files necessary to maintain desired part inventory, configuration will need to be completed. Setup will be completed with DIS assistance.

1.  Select **Electronic Commerce Configuration** (Security | Electronic Commerce | Electronic Commerce Communication). The Electronic Commerce Communication screen opens.
2.  Click the **Add** button. The Add Vendor/Comm Package screen opens.
3.  Provide information in the available fields and click **OK**. The JCB Communications - Configure screen opens.
    
    *Image: Screenshot of the JCB Communications configuration screen for entering dealer and FTP information.*
    
4.  Type the Dealer Number supplied by JCB in the Inventory Dealer Number field. This is for the current inventory download.
5.  Type your User ID, Locator Password, and Dealer Name in the provided fields.
6.  Select the **Reduce Available Qty by Van Inventory** check box if you do not want to consider your van inventory when providing your stock information to JCB.

#### Configure Vendor Maintenance - Inventory
This is standard Vendor Maintenance configuration where Vendor/Class combinations are entered to identify the part classes to be considered when generating and sending JCB part inventory files.

1.  Select **Vendor Maintenance-Inventory** (Manufacturers | JCB | Vendor Maintenance-Inventory). The Vendor Maintenance screen opens.
    
    *Image: Screenshot of the JCB Communications Vendor Maintenance screen.*
    
2.  Do one of the following:
    -   Click the **Add** button. The **Add/Vendor Class** screen opens. Any vendor can be added. Multiple classes can be added for a given vendor. Leaving the class field blank will add all classes. The program will not allow adding a vendor with a class if that vendor has already been added with the class field left blank. It also does not allow the same vendor/class combination to be added twice.
        
        *Image: The 'Add Vendor/Class' pop-up window.*
        
    -   Select a Vendor/Class from the table and click the **Delete** button. The Confirm Delete screen opens. Click **Yes** to remove the class from the table.
        
        *Image: The 'Confirm Delete' pop-up window.*

#### Send Part Locator Refresh
This option allows you to submit your current inventory including open orders and your sales history to JCB. The amount of information that is sent depends on the option that you select. This information will be used to calculate your suggested orders.

1.  Select **Send Part Locator Refresh** (Manufacturers | JCB | Send Part Locator Refresh). The Send Part Refresh screen opens.
    
    *Image: Screenshot of the 'Send Part Refresh' screen with options for immediate or scheduled data submission.*
    
2.  Do one of the following:
    -   Select the **Send a Part Refresh right now** option. This will immediately submit your current inventory including open orders and two years of sales history to JCB.
    -   Select the **Send a Part Refresh for this division during backup this evening** option to submit your current inventory including open orders and two years of sales history to JCB during your nightly backup.
    -   Select the **Send Daily Files for this division during backup this evening** option to submit your current inventory including open orders and seven days of sales history. This is the default option.
3.  Click **Enter** to submit the part refresh option.

#### Resend/Review Log

**View Status of Submitted Part Inventory Files**
Part Inventory files are automatically generated and sent after every scheduled backup. You can check the status of each submission and resend it if it failed.

1.  Select **Resend/Review Log** (Manufacturers | JCB | Resend/Review Log). The Send List screen opens displaying the files that have been sent.
    
    *Image: Screenshot of the JCB Communications Send List, showing the status of sent files.*
    
2.  To manually resubmit the file, highlight it and click the **Resend** button to submit the inventory file again.
3.  The **Resend File** screen opens verifying that you would like to resend the file. Click **OK** to resubmit the selected file.
    
    *Image: The 'Resend File' confirmation pop-up.*

**View Files Received from JCB**
You can view when part inventory files were sent to your dealership from JCB and whether or not the submission was successful. You can also select to resend any files that failed.

1.  Select **Resend/Review Log** (Manufacturers | JCB | Resend/Review Log). The Send List screen opens.
2.  Click the **Receive List** button. The Receive List screen opens showing when you received the files and whether or not the submission was successful. This screen is informational only.
    
    *Image: Screenshot of the JCB Communications Receive List, showing the status of received files.*

#### Customer Maintenance
The customer maintenance option allows you to designate customers whose sales invoices you would like to remove from consideration when generating the Transaction Demand file.

1.  Select **Customer Maintenance** (Manufacturers | JCB | Customer Maintenance). The Exclude Customers from Demand screen opens listing any customers that have already been added.
    
    *Image: Screenshot of the 'Exclude Customers from Demand' screen.*
    
2.  Do one of the following:
    -   Click the **Add** button. The **Add Address** screen opens. Enter the customer address in the field provided or click Address# and select it from the list that appears. Click **OK**. The customer is added to the table.
        > **Note:** If the customer is already added, a reminder message displays at the bottom of the screen.
        
        *Image: The 'Add Address' pop-up window.*
        
    -   Select a customer from the table and click **Delete**. The Delete Address screen opens verifying this is the customer that you would like to remove. Click **Ok** to remove the customer from the table.
        
        *Image: The 'Delete Address' pop-up window.*

### **New! (Release 22v2)** Purchase Orders linked to Stock Orders with CNH CSPS
If the OPT is set so that Purchase Orders are linked to Stock Orders, the program will now update the P.O. records to match changes made during the validation process. As a result, the CSPS stock order number will be cancelled during the validation process and replaced with the new P.O. number.

*Image: Screenshot of the 'PRINT / FINALIZE ORDER' screen showing the link between a Vendor Order and a CSPS#.*

## 360 Program Upgrades

### Sales 360
You can now post an almost unlimited number of messages on the Sales 360 dashboard rather than three as it was previously. Additionally, you can now view the quotes of multiple sales representatives.

**Click here** to view the latest version of the Sales 360 documentation.

Sales 360 allows sales representatives to schedule calendar events, view department messages on the Sales 360 dashboard, create and manage sales calls, generate quotes that can instantly be converted to a P.O.S. invoice, and provide/view contact information.
> **Note:** Sales 360 requires a one-time setup fee. Contact Sales at 1-800-426-8870 for more information.

*Image: Screenshot of the Sales 360 dashboard showing the calendar, department messages, and sales call/quote widgets.*

### Management 360
You can now view zero-dollar workorders in the Service WIP option. Contact DIS for assistance with enabling this OPT. In the same spirit of the Quantum Refacing project, we continue to implement improvements to how the information in Management 360 is presented to you.

**Click here** to view the latest version of the Management 360 documentation.

> **Note:** Setup of this feature requires DIS assistance. If you are interested in this feature, please call or email the response line so we can add you to the install list and streamline the installation process.

#### Service WIP
The Service WIP KPI allows you to view total dollar amounts for all open work orders in your system that have a balance (work orders without a balance do not display). You can view the figures for all divisions or a single division. The information in Service WIP is automatically updated every two hours. Open work orders are broken down into three classes.
You can drill down further into each class and view if the associated work orders will be charged internally, to a warranty, or to the customer. Service WIP allows you to view the dollar amounts of work orders under these classes depending on the status of the work order. Click the link at the bottom of the page for instructions.

*Image: Screenshot of the Management 360 Service WIP by Location KPI, showing a bar chart of work-in-progress values.*

### **New! (Release 22v2)** New Management 360 KPIs Available
As of Release 22v2, new Service Contribution and Parts Contribution KPIs provide an analysis of current service and part revenue dollar amounts and allows you to compare the figures to the current budget and the previous year's figures. A new Aged Receivables KPI provides you with a breakdown of receivables by their age category.

*Image: Screenshot of the new Management 360 KPIs: Service Contribution, Parts Contribution, and Aged Receivables.*

## General

### **New! (Release 22v2)** New Associated Addresses Feature
The new Associated Addresses feature allows you to group multiple customers together by their customer address number and view how the group performs as a whole.
Once configured, associated group information can currently be viewed through the Customer 360, Sold Units Inquiry, Part Sales History, and Inquire/Update Service Units menu options.

*Image: Screenshot of the Part Sales History screen showing the 'Associated View' button and grouped customer data.*

**Click here** for instructions on how to configure and view associated address information.

## P.O.S.

### Extra Security for New P.O.S. Documents
This feature allows you to trigger a security event when new P.O.S documents are created under a specified customer address and you would prefer the document be created under another address. As part of this feature, an alternative address is provided that users will be prompted to select when they have entered the initial customer address.

*Image: Screenshot of the 'New Document Extra Security' prompt, which requires the user to choose between creating a document under the entered address or an alternative recommended address.*

### **New! (Release 22v2)** New OPT for Extra Security Feature
As of Release 22v2, a new OPT allows you to select whether or not customer addresses with extra security applied are available for selection on the Select Address screen. By default, customer addresses with extra security applied will not display.

1.  Select **OPT DIS Master Menu** (Security | OPT DIS Master Menu).
2.  Select **Point of Sale** and navigate to Menu Twenty-Three.
3.  Type **7** in the Enter Option Number field and click **Enter** to omit customer addresses with extra security from displaying on the Select Address screen or type **8** and click **Enter** to include them.

*Image: Comparison screenshots showing the 'Select Address' screen with extra security addresses omitted (default) and included (OPT enabled).*

### Spellcheck Installed in Time Clock Work with Notes
Spellcheck has been added to all Work with Notes screens. When a spelling error has been made, the misspelled word will be underlined in red.

*Image: Screenshot of the Time Clock 'Work with Notes' screen showing a misspelled word underlined in red.*

## Security

### Quantum Admin
Quantum Admin allows you to set the theme (colors and logos) that displays on the Quantum interface for all divisions within every fileset, all the divisions within a specific fileset, or a single division. As you create or update a theme, a live preview displays in the lower portion of the screen allowing you to view it before implementation.
Quantum Admin also allows you to specify the Users who have access to Quantum Admin and designate the roles that are assigned to them.

*Image: Screenshot of the Quantum Admin screen for customizing themes, colors, and logos.*

**Click here** to view instructions on setting up and using Quantum Admin.

### **New! (Release 22v2)** New Unit Locator Feature
The Unit Locator Service feature allows you to post information on units in your inventory to 6 different unit locator services. Some services allow you to assign unit make/model combinations in your inventory to their unit description and code categories. Assignments can be made to entire make/model combinations through Quantum Admin or to individual units through Inquire/Update Units.
> **Note:** This feature requires a setup fee. Contact Sales at 1-800-426-8870 or Sales@discorp.com for more information.

**Click here** to view documentation on how to enable unit locator services, configure which unit information is available, and assign make/model combinations to unit locator service descriptions and codes when available.


title: "Polaris Interfaces Master Quantum"
source: "Polaris_Interfaces_Master_Quantum.pdf"
tags: ["Polaris", "Quantum", "DIS", "Price File", "Unit Promotions", "Vehicle Service History", "Parts Locator", "Dealer Management System", "DMS", "API Integration"]
version: "1.0"
last_updated: "2024-05-24"
short_description: "This document provides a comprehensive guide to using the Polaris interfaces within the DIS Quantum software, covering features like daily price file updates, unit promotion lookups, vehicle service history, parts location, inventory submission, and vehicle specifications."
long_description: "This user documentation from Dealer Information Systems (DIS) Corporation details the various Polaris Industries interfaces available within the Quantum Dealer Management System (DMS). The guide is intended for dealership staff using the Quantum software to manage Polaris-related operations. It introduces new interfaces for Price File updates and Unit Promotions, and also covers previously released interfaces for Vehicle Service History, Parts Locator, Parts Inventory, and Vehicle Specifications. The Price File interface automates daily price list updates for the USA and Canada, notifying a specified user of any changes. The Unit Promotions interface allows users to look up active promotions for Polaris models, including rebates, financing, and SPIFFs. The document provides detailed, step-by-step instructions with accompanying screenshots for configuring and using each interface. This includes navigating through the Quantum menus, entering data like VINs or model numbers, and interpreting the information returned from the Polaris system, such as promotion details, service bulletins, warranty claim history, and part availability at other dealerships."