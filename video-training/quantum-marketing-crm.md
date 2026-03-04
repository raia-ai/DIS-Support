---
title: "Quantum — Marketing & CRM"
source: "DIS_Video_Training_Knowledge_Base.md"
tags: ["DIS System Training", "Quantum"]
version: "1.0"
last_updated: "2026-03-04"
short_description: "The **Quantum — Marketing & CRM** module within the DIS platform is designed to centralize and streamline customer relationship management, marketing segmentation, and sales tracking for dealerships. It integrates customer data with sales, service..."
long_description: "This document provides a comprehensive overview of the Quantum — Marketing & CRM module within the DIS platform, derived from internal training sessions."
---

# Quantum — Marketing & CRM

**Source Sessions**: 27, 28, 29

### Overview

The **Quantum — Marketing & CRM** module within the DIS platform is designed to centralize and streamline customer relationship management, marketing segmentation, and sales tracking for dealerships. It integrates customer data with sales, service, rentals, and point-of-sale (POS) operations to provide a comprehensive view of customer interactions and history. This module enables dealerships to manage customer accessibility across various system components, track sales activities, and analyze customer value through ranking and demographic segmentation.

By consolidating customer information and marketing activities, the module supports targeted marketing campaigns, accurate commission tracking, and improved customer service. Its integration with POS and equipment rental modules ensures that customer flags and data flow seamlessly, enabling efficient transaction processing and service history tracking.

### Core Concepts

- **Customer Accessibility Flags:** Customer records in Address Maintenance use boolean flags to control their availability in different system modules. For example, the **Cash Customer** flag allows non-accounts receivable customers to appear in POS, while the **Rental Customer** flag enables access in the Equipment Rentals module. The **Track as Contact** flag includes the customer in the Contacts section for CRM activities.

- **Default Salesperson Assignment:** Assigning a salesperson to a customer record automatically populates the "Sold By" field on invoices and work orders, facilitating commission tracking and sales accountability.

- **Sales Call Logging:** The module supports logging sales calls with customers, capturing details such as representative, call type, topic, notes, and status (Open or Closed). This feature aids in managing follow-ups and maintaining a history of customer interactions.

- **Service History and Serial Numbers:** Equipment units must have a **Serial Number** entered to enable service history tracking and to be selectable on work orders. Units without serial numbers do not appear in serial number lookups and cannot have service history tracked.

- **Purchase Order (PO) Number Enforcement:** If the **PO Required** flag is set to 'Yes' on a customer's business info, the system enforces mandatory entry of a PO number on transactions involving that customer.

- **Management 360 Departmentalization:** This feature assigns General Ledger (GL) sales and cost of sales accounts to specific departments (primarily Sales and Cost of Sales) for dashboard reporting. Assigning a sales account automatically assigns the corresponding cost of sale account to the same department.

- **Sales Ranking:** A tool that analyzes customer sales data across categories (Parts, Service, Units, Rentals) and assigns ranks (e.g., A, B, C) based on sales volume percentages. These ranks are stored in demographic fields on customer records and displayed in the **Customer 360** screen for quick assessment of customer value.

- **Customer Grouping via Demographics:** The module supports customer segmentation using **Demographics**, a structured and multi-field classification system that replaces the older, less descriptive **Sort Codes** method.

- **Sales Representative Management:** Customers can be assigned to specific sales representatives, a requirement for some businesses. The system supports reassigning customers and their sales call histories when sales reps change.

### System Architecture & Data Model

- **Address Maintenance as Master Record:** The customer’s Address Maintenance record is the central data hub, containing key flags and fields that determine customer visibility and behavior across POS, Rentals, and Marketing modules.

- **Boolean Flags for Module Integration:** Flags such as `Cash Customer`, `Rental Customer`, and `Track as Contact` on the address record control module access and functionality.

- **Data Flow to POS and Rentals:** Customer data, including default salesperson IDs and PO requirements, flow from Address Maintenance into POS transactions and Equipment Rentals, ensuring consistent data usage.

- **Service History Dependency on Serial Numbers:** The `Serial Number` field on equipment records is critical for linking service history and enabling selection in work orders.

- **GL Account Departmentalization:** Sales and Cost of Sales GL accounts are linked; assigning one to a department in Management 360 automatically assigns the other to the same department.

- **Customer Demographics Storage:** Demographic fields on customer records store sales ranks and other classification data. These fields are customizable and support historical tracking by creating new fields for each period.

- **Sales Ranking Data Flow:** The Sales Ranking process reads sales transactions, calculates ranks based on defined criteria, and writes results to demographic fields, which are then used for filtering and reporting in the Contacts module.

### Key Procedures

#### 1. Adding a Shipping Address from an Invoice

1. Start a new invoice in Point of Sale for the desired customer.
2. On the main "Sold To" screen, select the `Ship Address` option from the left-hand menu.
3. Create a new shipping address for the customer directly within this screen.

#### 2. Logging a Sales Call

1. Navigate to `Marketing > Contacts`.
2. Select the customer for whom you want to log a call.
3. Go to the `Sales Calls` section.
4. Create a new sales call entry, filling in the representative, call type, topic, and notes.
5. By default, the call status is set to "Open" for follow-up; change to "Closed" when completed.

#### 3. Adding Equipment to a Customer

1. Navigate to `Marketing > Contacts` and select the customer.
2. Go to the `Equipment` section.
3. Add a new piece of equipment.
4. Enter a valid `Serial Number` to ensure the unit appears in POS lookups and service history tracking functions properly.

#### 4. Running the Sales Ranking Process with Historical Tracking

1. Create new, uniquely named demographic fields for the current period (e.g., "2024 Parts Rank") under customer demographics.
2. Navigate to `Marketing > Sales Ranking`.
3. Set the date range for the sales data analysis.
4. Map the ranking output to the newly created demographic fields.
5. Execute the ranking process to populate the fields without overwriting previous period data.
6. Use `Marketing > Contacts` to filter and compare customer ranks across periods.

#### 5. Reassigning Customers to a New Sales Representative

1. Use the system's "search and replace" functionality.
2. Search for the employee record of the outgoing sales representative.
3. Replace it with the new sales representative's employee record.
4. This transfers all assigned customers and their sales call histories to the new representative.

### Menu Navigation

- `Marketing > Address Maintenance`
- `Marketing > Address Inquiry`
- `Marketing > List of Addresses`
- `Marketing > Contacts`
- `Marketing > Sales Calls > Configuration`
- `Marketing > Sales Ranking`
- `POS Invoicing > (customer selected) > Ship Address`

### Business Rules & Constraints

- Customers not flagged as **Cash Customer** will not appear in POS if they are not on accounts receivable.
- A **Cash Customer** must have a tax code assigned to be valid in POS.
- The system enforces mandatory PO number entry on transactions for customers with the **PO Required** flag set to 'Yes'.
- Equipment units without a `Serial Number` cannot have service history tracked and will not appear in serial number lookups on work orders.
- Adding discount codes directly to customer master records is strongly discouraged due to potential widespread issues.
- Management 360 departmentalization currently affects only Sales and Cost of Sales GL accounts; other account types have no dashboard impact.
- Sales Ranking allows different ranks per sales category; a customer may be ranked differently in Parts, Service, Units, and Rentals.
- The `Customer Sales Summary` report prints all customers, which can result in very large reports for dealerships with extensive customer bases.
- Some businesses require every customer to be assigned a sales representative.

### Configuration Options

- **Track as Contact Default:** The system can be configured to default the "Track as Contact" flag to 'Yes' when creating new customers.
- **Sales Call Types and Topics:** Configurable dropdown menus for call types and topics are managed under `Marketing > Sales Calls > Configuration`.
- **Sales Ranking Parameters:** Users can configure date ranges, divisions, and ranking criteria (such as percentage of total sales dollars) for the Sales Ranking process.
- **User-Defined Demographic Fields:** Users can create and name custom demographic fields to store sales ranks and other customer attributes, enabling historical tracking and advanced filtering.

### Common Pitfalls & Warnings

- **Forgetting the "Cash Customer" Flag:** New customers often fail to appear in POS because the "Cash Customer" box is not checked.
- **Discount Codes on Customer Records:** Using the `Discount Code` field in Address Maintenance can cause major system issues and is not recommended.
- **Missing Serial Numbers on Equipment:** Equipment added without serial numbers will not be selectable in work orders and will lack service history tracking.
- **Limited Notes Capacity in Sales Calls:** The notes field in sales call logs has a small character limit despite its large appearance; use the `Notebook` feature for extensive notes.
- **Tedious Management 360 Setup:** Assigning GL accounts to departments is time-consuming and often neglected, leading to inaccurate dashboard data.
- **Confusing Sales Ranking Workflow:** The process of creating demographic fields and running sales rankings for historical comparison is complex and prone to errors.
- **Unclear Sort Codes:** The legacy sort code system lacks validation and descriptive meaning, causing confusion when interpreting customer groupings.
- **Ranking Process Reliability:** The sales ranking process may not always execute successfully due to system complexity or dependencies.

### Key Terminology

- **Cash Customer:** A flag in Address Maintenance enabling non-accounts receivable customers to be used in POS transactions.
- **Rental Customer:** A flag indicating a customer is eligible for equipment rentals.
- **Track as Contact:** A flag that includes the customer in the Contacts module for CRM activities.
- **Serial Number:** A unique identifier for equipment units required for service history tracking and selection in work orders.
- **PO Required:** A flag that enforces mandatory Purchase Order number entry on transactions.
- **Management 360:** A dashboard feature requiring departmentalization of sales and cost of sales GL accounts for reporting.
- **Sales Ranking:** A marketing tool that categorizes customers based on sales volume across different categories, storing ranks in demographic fields.
- **Customer 360:** A screen providing a comprehensive overview of a customer, including sales ranks.
- **Demographics:** Structured customer classification fields used for grouping and filtering, replacing the older sort codes.
- **Sort Codes:** Legacy single-character customer grouping codes without validation or descriptive meaning.
- **Sales Calls:** Logged interactions with customers, including details and status for follow-up management.
- **Open Call:** A sales call logged but not yet completed, indicating pending follow-up.
- **System Edit Codes:** Single-letter codes automatically assigned to addresses (e.g., 'W' for sold equipment, 'V' for vendor) used for filtering and reporting.
- **Sales Representative (Sales Rep):** An employee assigned to manage customer accounts and sales activities.

---