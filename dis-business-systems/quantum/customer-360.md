---
title: "Customer 360"
source: "combined_Quantum_docs.md"
tags: ["Quantum"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Customer 360."
long_description: "This document provides information about Customer 360 from the DIS Quantum system."
---

## Introduction

Customer 360 is a customer-focused feature that allows you to instantly access customer information located under multiple menu options from one centralized location. Customer 360 provides the following information and capabilities:

-   Search and locate customers by their name, telephone, or address number.
-   Use Quantum Search to locate a customer through associated information in the system. Search for information such as name, telephone number, street address, parts, document numbers, or unit number/serial number. Search results will display each customer with matching information.
-   View information for a customer, including:
    -   **Balance** - Total balance, past due balance, total number of unpaid invoices.
    -   **Last Call** - View details regarding the last sales call made and edit if desired.
    -   **Overall Ranking** – The total amount a customer has spent with a breakdown by parts, service, units, and rentals and how it compares to all customers in your division. This is updated daily.
    -   **Contact Information** - View phone numbers, street address, email, and website addresses.
    -   **Account Rep** – The primary sales rep assigned to the customer, their email address, and their phone number. Primary sales reps are assigned to customers through (Marketing | Contacts).
-   Perform additional actions, including:
    -   **Create Call** - Schedule a sales call with a customer and record the pertinent details from the call.
    -   **Receive Payment** – Specify the amount, document type, sales code, and transaction description.
    -   **Create Document** – Open up P.O.S. Invoicing and create a document for the customer.
    -   **View Part Availability** – View the available quantity, quantity reserved, location, and dealer list price for parts. Create a quote, work order, or sales order for those parts.
    -   **Create Rental Document** – View or create a rental quote/reservation and turn it into a contract.
    -   **Edit customer contact information**.

## Instructions

1.  Open Quantum on the browser of your choice and click the **Cust 360** icon on the left side of the screen. The Customer 360 Search screen opens.

2.  Do one of the following:
    -   Conduct a search for a customer by entering their name, telephone number, and/or address number in the fields at the top of the screen and clicking the **Search** button. Unless you enter a valid customer address number, the Select Address screen will open allowing you to select the customer.
    -   Conduct a search for a customer based on their information in the system by entering it in the lower field and clicking the **Quantum Search** button. Searches can be conducted on a variety of information such as names, phone numbers, and part numbers or parts purchased by customer.
        -   All customers with data that match the search terms display in the lower portion of the screen. The source of the matching data is listed.
        -   The search information that you provided is highlighted in yellow.
        -   A blue icon next to the customer name indicates whether they are a receivable, cash customer, or a contact set up through (Marketing | Contacts).
        -   A blue icon without a question mark will always take you to Customer 360.
        -   A blue icon with a question mark indicates a prospective customer set up through (Marketing | Contacts). Selecting it will take you to Customer 360 if Sales 360 is not installed or the contacts landing page if Sales 360 is installed. Click `here` to view documentation on Sales 360 and contact `sales@discorp.com` for additional information.
        -   Click on a customer to select them.

3.  Click the **Point of Sale** button to open the Point of Sale - Invoicing Entrance - Active Documents screen and create a document.

## Understanding the Customer 360 Screen

If you conducted a search and accessed Customer 360, the main customer information screen displays. Each feature available in Customer 360 is broken down in the sections that follow.

### Customer Contact Information

This section displays the customer contact information including their street address, phone number, fax number, email address, and website address. You can click **Edit Contact Information** and provide information or change existing information.

### Balance

The current customer balance displays on the Stats bar if the customer is a receivable. If the customer has a past due balance, an alarm clock icon will display. If a customer has been restricted to cash or credit card purchases through (Receivables | Receivables Maintenance), the credit card lock icon will display. Click on the section to display the following information:
-   The customers total balance.
-   Their past due balance.
-   The number of unpaid invoices.

Click on any of the four options in the drop-down menu to display the Receivables Inquiry screen. Then click the **Transactions** button to view invoices that are paid/unpaid by the customer. Click **Exit** to return to Customer 360.

### Sales Call Information

If you have placed a sales call with a customer, the date is listed on the Stats bar. If a sales call has never been made, **Create Call** will display instead of a date. Click on the section to create a call or view/edit information regarding the last sales call. Click **Exit** to return to Customer 360.

### Overall Ranking

This feature displays the total sales amount for the customer in all divisions for the current fiscal period and provides a star ranking by which to compare the customer's current fiscal activity against other customers. Click on this section to display the following information:
-   Days since the last parts, service, units, or rental transaction.
-   Total sale amounts for the last three fiscal periods broken down by parts, service, units, and rentals.
-   Click on any period to see each invoice amount broken down by parts, service, units, and rentals. Click on the document hyperlink to work with the document in Point of Sale. When finished, click **Hold** and then **Exit** to return to Customer 360.
-   A star ranking of how the activity compares with other customers in your division.

> **Note**: In order for data to populate in the Overall Ranking section, the Sales Ranking Report (Marketing | Sales Ranking Report) or the Customer Sales Summary Report (P.O.S. | P.O.S. Reports | Customer Sales Summary) must be configured. Click `here` to view documentation on configuring these reports.

### Graphs

There are four graphs that detail a customer's interactions with your dealership. You can hover your cursor over a segment on any graph and view the details that make up that segment.

#### Equipment Graph

This graph displays the equipment owned by the customer. This can include equipment that has been sold, serviced, added in contacts, out on demo, or reserved.
-   Click on the center of the Equipment graph to open the Equipment screen.
-   Locate specific equipment in the table by typing full or partial search terms in the Search field. Matching information is automatically highlighted in yellow. Click the direction arrows to the right of the Search field to parse through matching information.
-   Use the scroll bars to view the available information about the equipment listed in the table.
-   Click an entry in the **Unit#** column to go to Inquire/Update Units. From there, click **Exit** to return to Customer 360.
-   Click an entry in the **Serial#** column to go to Inquire/Update Service Units. From there, click **Exit** to return to Customer 360.
-   Click an entry in the **Open WO** or **Reserve Inv** column to work with the document in Point of Sale. From there, click **Hold** and then **Exit** to return to Customer 360.

> **Note**: You can arrange the information in the table to best suit your needs. Click `here` for details.

#### Parts Graph

This graph displays information on parts that are reserved on open P.O.S. documents. Click on the center of the graph to open the Parts Reserved screen which breaks down information by the following categories:
-   **Will Call** - Parts that were received and are now available for pick up.
-   **On Order** - Parts placed on a document with a priority order code of N, P, Q, S, T, 1, 2, 3, or 4.
-   **Other** - Parts on an open document that fall outside of the Will Call and On Order categories.

-   Locate specific parts in the table by typing full or partial search terms in the Search field. Matching information is automatically highlighted in yellow. Click the direction arrows to the right of the Search field to parse through matching information.
-   Use the scroll bars to view all of the available information about the parts listed in the table.
-   Click an entry in the **Part** Column to go to Parts Inquiry. Click **Exit** to return to Customer 360.
-   Click an entry in the **Document** column to work with the document in Point of Sale. From there, click **Hold** and then **Exit** to return to Customer 360.

> **Note**: You can arrange the information in the table to best suit your needs. Click `here` for details.

#### Documents Graph

This graph displays the Total open documents for the customer broken down by work orders, sales orders, and quotes.
-   Click on the center of the Documents graph to access the Open Documents screen.
-   Locate specific parts in the table by typing full or partial search terms in the Search field. Matching information is automatically highlighted in yellow. Click the direction arrows to the right of the Search field to parse through matching information.
-   Click on an entry in the **Document#** column to work with the document in Point of Sale. From there, click **Hold** and then **Exit** to return to Customer 360.

> **Note**: You can arrange the information in the table to best suit your needs. Click `here` for details.

#### Rentals Graph

This graph displays the rental units a customer reserved, currently has on rent, and rented in the last 24 months.
-   Click on the center of the Rentals graph to open the Rentals by Customer screen and view information about units currently on rent.
    > **Note**: Click on a segment of the graph to view the information related to that segment.
-   Highlight a rental transaction and click **Select** to view/work with that rental quote, reservation, or contract.
-   Clear the filter fields (except the address field) and click **Enter** to view all contracts, reservations, and quotes created for the customer.
-   Create a quote or reservation for the customer. You can also convert quotes/reservations to contracts.

> **Note**: You can arrange the information in the table to best suit your needs. Click `here` for details.

## Action Buttons

### Receive Payment

If a customer is a receivable, the Receive Payment option will be available. Use this option to create a P.O.S. document. The first time you use this option, you must supply the payment amount, document type, sold by information, and sales code for the entry. Most of the information that you supply will become the default information, but can be changed for any future payments received. From Point of Sale, you can click **Hold**, **Prt & Close**, or **Prt & Hold** and then **Exit** to return to Customer 360.

### Point of Sale

Use this option to create a document for the selected customer. You will be prompted to select the document type. Once selected, the P.O.S. Active Documents screen opens allowing you to create the document as you normally would.

### Quick Parts Quote

Use this option to check availability for a part. The Part Availability – Inquiry screen opens. You can enter a part number, quantity, and vendor code, then click **Enter** to view availability, price, and location. You can add the parts to an invoice, using the fields at the top of the screen and clicking **Add**. A message will appear at the bottom of the screen stating the number of part lines/priority order lines added. Click **POS Det** to open the Document Detail screen and process the invoice as normal. Click **POS Ent**, then **Exit** to return to Customer 360.

> **Note**: If the quantity of parts requested are not available, supply a Priority Code to use and the transaction line will be added to the invoice and a priority order created.

## Arrange Tables in Customer 360

Each table accessed through Customer 360 allows you to access tables of related data through linked document pages. Hovering your cursor over a column header and clicking the drop-down arrow will provide you with some or all of the following options for that column:

**Sort Ascending/Descending** – Use this option to select whether the information in the table is displayed in ascending or descending order according to the information in that column.

**Columns** - Hover over columns and select which columns you want to display in the table. Check boxes will appear. Select the check boxes for the columns that you want to display in the table. Unselect check boxes to remove the columns from the table.

**Filters** - Hover over this option to produce a filter field. Enter filters to determine the information that is displayed in the table. A filter can be set on multiple columns at the same time.
> **Note**: Headers for columns that have a filter applied will be italicized.

-   Change the order in which columns are displayed by clicking on a column header and dragging it to the desired location. A double-arrowed green line indicates where the column will be placed.

## Export Information to Spreadsheet

The data listed in the tables accessed through Customer 360 can be exported to a spreadsheet by clicking the **Excel** button.

-   Though the button specifies Excel, you can export the data into most spreadsheet software such as Google Docs.
-   The exported data maintains the same format (column order, sort order, etc.) as the table from which it is being exported. If the data in a column is hidden, it will not display in the spreadsheet.

Click `here` to view a Customer 360 tutorial.


title: "Customer_360"
source: "Customer_360.pdf"
tags: ["Customer 360", "Quantum", "CRM", "Customer Search", "Sales Reporting", "Parts Management", "Rental Management", "Point of Sale", "DIS Corp"]
version: "1.0"
last_updated: "2024-05-24"
short_description: "A user guide for the Customer 360 feature within the DIS Quantum software. This feature provides a centralized view of all customer information, including contact details, financial balances, sales history, and equipment records."
long_description: "This document serves as a comprehensive guide to the Customer 360 feature in the DIS Quantum system. Customer 360 is designed to provide a single, unified interface for accessing comprehensive customer data that is otherwise spread across multiple menu options. The guide details how users can search for customers using various criteria like name, phone number, parts, or document numbers. It explains the components of the customer information screen, which includes financial balance, last call details, overall sales ranking, contact information, and assigned account representative. The document outlines how to perform key actions directly from this screen, such as creating sales calls, receiving payments, creating POS documents, viewing part availability, and managing rental documents. It also describes the interactive graphs that visualize customer data related to equipment, parts, open documents, and rentals, allowing users to drill down for more specific information. Instructions are provided for customizing data tables through sorting, filtering, and column arrangement, as well as for exporting table data to spreadsheet applications like Excel or Google Docs."