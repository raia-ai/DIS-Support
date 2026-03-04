---
title: "Quantum — Units & Whole Goods"
source: "DIS_Video_Training_Knowledge_Base.md"
tags: ["DIS System Training", "Quantum"]
version: "1.0"
last_updated: "2026-03-04"
short_description: "The **Quantum — Units & Whole Goods** module within the DIS platform is designed to comprehensively manage dealership inventory, from units on order through to sold and transferred goods. It provides dealerships with tools to track unit status, co..."
long_description: "This document provides a comprehensive overview of the Quantum — Units & Whole Goods module within the DIS platform, derived from internal training sessions."
---

# Quantum — Units & Whole Goods

**Source Sessions**: 21, 22

### Overview

The **Quantum — Units & Whole Goods** module within the DIS platform is designed to comprehensively manage dealership inventory, from units on order through to sold and transferred goods. It provides dealerships with tools to track unit status, costs, trade-ins, and financing (flooring), ensuring accurate inventory control and financial integration. This module is critical for maintaining visibility into unit lifecycle stages, supporting sales processes, and aligning inventory data with accounting and rental operations.

By integrating with related modules such as Point of Sale, Rentals, and Accounting, Quantum Units enables dealerships to streamline workflows around unit ordering, receiving, costing, and depreciation. It also supports multi-division structures with security controls to ensure users access inventory data relevant to their operational context. The module’s flexibility in configuration allows dealerships to tailor processes such as trade-in handling, over-allowance management, and rental unit sales to their specific business rules.

### Core Concepts

**Unit Views:** The system offers three levels of access to unit information, each controlling visibility and edit permissions:

- **Limited View:** Users can see most unit details except cost information.
- **Complete View:** Users can view all unit details, including cost, but cannot make changes.
- **Complete Access:** Users have full rights to view and modify all unit data.

**Divisional Security:** Quantum Units supports multiple divisions within a dealership. A security gate feature prompts users to select the correct division when accessing unit data, ensuring inventory is managed within the proper organizational context and preventing unauthorized cross-division access.

**Unit Status:** Each unit is tracked with a status reflecting its current lifecycle stage. Common statuses include:

- Available
- Sold
- Transferred
- Rental
- Ordered (units on order but not yet received)

**Flooring:** Flooring refers to the financing arrangement for dealer inventory. The system can be configured to automatically set the flooring due date to the unit’s sale date, facilitating compliance with manufacturer requirements.

**Trade-ins and Over-allowance:** The module supports trade-in processing with the ability to handle over-allowance—providing customers more than the trade-in’s cash value as a sales incentive. Over-allowance amounts can be configured to either increase the cost basis of the new unit or be posted to a separate over-allowance general ledger account.

**Costing:** Units maintain two primary cost fields:

- `Original Cost`: The initial cost of the unit.
- `Cost`: The current cost, including any added costs such as reconditioning.

The difference between these is the `Added Cost`, which reflects additional expenses incurred post-purchase.

**Unit Order and Budgeting:** This feature tracks units that are ordered but not yet received. Units with an "O" (ordered) status are excluded from main inventory until formally received, at which point they are assigned unique unit and serial numbers.

**Depreciation:** The module supports posting depreciation for units, but only for the oldest open accounting month. This requires dealerships to maintain up-to-date financial periods.

### System Architecture & Data Model

The Quantum Units module is tightly integrated with the **Point of Sale**, **Rentals**, and **Accounting** modules, enabling seamless data flow across sales, rental, and financial processes.

- **Unit Records:** Each unit record includes key fields such as:
  - `Unit Number` (unique identifier)
  - `Serial Number`
  - `Make` and `Model` (linked to a shared Make/Model table used by Point of Sale and Units)
  - `Color` (a 5-character field, which can be repurposed as a manufacturing number)
  - `Hour Meter` (updated automatically from Rentals upon rental return)
  - `Original Cost` and `Cost`
  - `GL Account` (links the unit to the dealership’s General Ledger)

- **Divisions:** Data is segmented by division codes (e.g., "J", "S"), creating organizational silos for security and reporting.

- **Text Fields:** External and internal specifications for units support multiple lines of text, using the pipe character (`|`) to denote line breaks.

- **Quantum Unit Location Table:** Integrates with the Sales Logistics handheld application, linking unit location data with mobile inventory management tools.

- **Data Import:** Bulk import of unit data is supported, excluding cost information. Mandatory fields for import include unit number, make, and GL account.

### Key Procedures

#### 1. Looking Up a Unit

1. Navigate to `Units > Inquire/Update Units`.
2. Select the appropriate **Unit View** (Limited, Complete, or Complete Access) based on your security level and task.
3. Use the `Define Search` function to filter units by criteria such as status, division, make, or model.
4. Review the unit details as needed.

#### 2. Adding a Unit on Order

1. Navigate to `Units > Unit Order and Budgeting`.
2. Select the option to add a new unit.
3. Enter required information including order number, make, and model.
4. Save the record; the unit will have an "O" status indicating it is on order.

#### 3. Receiving an Ordered Unit

1. Access the receive function within `Units > Unit Order and Budgeting`.
2. Select the ordered unit to receive.
3. The system assigns a unique unit number and serial number, officially adding the unit to inventory.
4. The unit status changes from "Ordered" to "Available."

#### 4. Handling a Trade-in with Over-allowance

1. When accepting a trade-in, enter the trade-in value.
2. The system calculates any over-allowance amount.
3. Based on configuration, the over-allowance is either:
   - Added to the cost of the new unit, or
   - Posted to a designated over-allowance GL account.
4. Complete the sale transaction accordingly.

#### 5. Changing the GL Account for a Unit

1. Navigate to `Units > Change Unit Account Number`.
2. Enter the unit number to modify.
3. Input the new GL account number.
4. The system temporarily moves the unit’s cost to a holding account, updates the GL account, then transfers the cost back.

### Menu Navigation

- `Units > Inquire/Update Units`
- `Units > Unit Order and Budgeting`
- `Units > Sold Units Inquiry`
- `Units > Units Depreciation`
- `Units > Change Unit Account Number`
- `Units > Quantum Unit Location Table`
- `Units > Import Units`
- `Security > OPT DIS Master Menu > Units`

### Business Rules & Constraints

- The `color` field is limited to 5 characters and may be repurposed as a manufacturing number.
- Units with status "Ordered" are excluded from main inventory until received.
- Depreciation postings are restricted to the oldest open accounting month; financial periods must be kept current.
- Users can only change the GL account for units within their own division and that are available.
- Over-allowance on trade-ins can be capped by a percentage or a maximum dollar amount.
- The system can enforce warnings or block sales of units currently rented out.
- Cost data cannot be imported via the bulk import process.
- When importing units, unit number, make, and GL account are mandatory fields.

### Configuration Options

- **Reporting:** Option to rename the `color` field column heading to `manufacturing number` on inventory flooring reports.
- **Security:** Control visibility of unit transaction history for users in Limited View.
- **Flooring:** Enable automatic setting of flooring due date to the unit’s sale date.
- **Rentals:** Configure invoice form length and whether rental start dates are cleared when a unit is sold.
- **User Interface:** Show or hide serial number selection in the `Inquire/Update Units` screen; control default behavior of the `Define Search` function.
- **Data Management:** Allow users to add new makes and models dynamically within Units and Point of Sale modules.
- **Sales Process:** Configure soft warnings or hard stops when attempting to sell units currently rented.
- **Trade-ins:** Define how trade-in allowances and over-allowances are applied and posted.
- **Sold Units Inquiry:** Enable or disable viewing of sold units history.

### Common Pitfalls & Warnings

- The `hour meter` reading reliably updates only from the Rentals module upon rental return; updates from work orders are unreliable.
- Manual depreciation via recurring transactions can cause negative depreciation values if not carefully managed.
- Failure to close accounting periods timely will prevent depreciation posting for current months.
- Over-allowance configurations must be carefully set to avoid unintended financial postings.
- Users must ensure correct division selection to avoid data access errors due to divisional security gates.

### Key Terminology

- **Flooring:** Financing arrangement for dealer inventory, often tied to manufacturer requirements.
- **Over-allowance:** The amount by which a trade-in allowance exceeds the trade-in’s actual cash value, used as a sales incentive.
- **OPT Settings:** System-wide configuration options controlling module behavior.
- **Unit Order and Budgeting:** Feature for tracking units ordered but not yet received into inventory.
- **Sales Logistics:** A handheld mobile application integrated with the Quantum Unit Location Table for field inventory management.

---