---
title: "General System Review"
source: "DIS_Video_Training_Knowledge_Base.md"
tags: ["DIS System Training", "General System Review"]
version: "1.0"
last_updated: "2026-03-04"
short_description: "The **General System Review** module within the DIS (Dealer Information System) platform provides a comprehensive framework for managing core accounting, inventory, and customer receivables processes. It integrates financial reporting, transaction..."
long_description: "This document provides a comprehensive overview of the General System Review module within the DIS platform, derived from internal training sessions."
---

# General System Review

**Source Sessions**: 17, 38, 40

### Overview

The **General System Review** module within the DIS (Dealer Information System) platform provides a comprehensive framework for managing core accounting, inventory, and customer receivables processes. It integrates financial reporting, transaction management, and inventory control across multiple divisions, enabling dealerships to maintain accurate financial records, streamline operations, and support centralized accounting functions. This module is critical for ensuring data integrity, facilitating audit trails, and supporting decision-making through detailed reporting and analysis tools.

This module covers key areas such as customer account management, accounts receivable processing, general ledger accounting, inventory tracking for both units and parts, and system security features. It also supports multi-division operations by allowing combined financial reporting and centralized control over user access and transaction processing. The system’s architecture enforces strict business rules and constraints to maintain accounting accuracy and operational consistency.

### Core Concepts

- **Customer Types and Edit Codes:** Customers are classified by single-letter **edit codes** that define their transaction capabilities and history. These include Receivables Customers (R), Marketing Customers (M), Unit Sales Customers (W), Rental Customers (L), and Cash Customers (C). These codes determine how customers interact with the system, such as whether they can purchase on credit or only pay cash.

- **Statement Types:** The system supports two primary statement types for receivables:
  - **Balance Forward:** Summarizes previous unpaid invoices into a single balance forward amount. Payments apply to the overall balance rather than specific invoices.
  - **Open Item:** Lists each unpaid invoice individually until paid. Payments must be manually applied to specific invoices.

- **Corporate Receivables:** Enables a parent (corporate) customer account to assume financial responsibility for subsidiary (child) accounts, facilitating centralized billing and accounting.

- **Credit Management:** Customer credit card information is stored securely in encrypted files with audit trails for access. Private label cards are recommended for storage, while public bank cards are discouraged.

- **Interest Calculation:** Interest can be calculated on past-due balances with configurable options to control whether interest accrues on previously charged interest and whether interest amounts are aged or kept current.

- **DataMine Tool:** A powerful query and reporting tool used for analyzing posting batches and verifying accounting entries. It requires manual adjustment of debit/credit signs when exporting data for reconciliation.

- **Point of Sale (POS) Security:** A system-wide setting that enforces user authentication for POS transactions and controls user permissions for document handling and sales code access.

- **Inventory Management:** The system tracks whole goods (units) and parts inventory separately, supporting statuses such as Available, Rented, Sold, and On Order for units. Parts inventory supports both full physical counts and cycle counts by group.

- **Financial Reporting:** Supports combined financial statements across multiple divisions using predefined report groups, ensuring consistent chart of accounts structure for accurate aggregation.

- **End-of-Period Procedures:** Strict controls govern month-end and year-end closing processes, requiring all batches to be posted or canceled and users to be logged out of accounting modules.

### System Architecture & Data Model

- **Customer Records:** Each customer record includes an edit code indicating their transaction type and status. Corporate receivables are modeled by linking child customer accounts to a parent corporate account via designated fields.

- **General Ledger (GL) Accounts:** GL accounts are assigned edit codes that define their function and enforce system logic. Examples include:
  - **A:** Accounts Receivable
  - **P:** Payables
  - **B:** Bank Reconciliation
  - **S:** Sales
  - **W:** Whole Goods Inventory and Cost of Sales
  - **F:** Flooring/Equipment Payables

- **Division and File Set Structure:** The system is organized by divisions within a file set. GL accounts are prefixed with division codes, which are removed during combined reporting to aggregate data across divisions.

- **Transaction Batches and Sessions:** Each user session is linked to a temporary batch via a session ID. Sessions can be monitored and taken over by other users once inactive.

- **Inventory Freeze Snapshot:** During physical inventory counts, the system takes a snapshot of on-hand quantities at a point in time (inventory freeze) to compare against physical counts.

- **Easy File Attachments:** Users can attach digital documents or notes to specific GL transactions, viewable only when the transaction is selected.

### Key Procedures

1. **Converting a Cash Customer to a Receivables Customer**
   1. Navigate to `Receivables > Receivables Maintenance`.
   2. Locate and select the cash customer record.
   3. Assign a receivables general ledger account number.
   4. Specify the statement type as either Open Item or Balance Forward.
   5. Save the changes.

2. **Setting Up a Corporate Receivable Account**
   1. Create a customer record for the corporate (parent) entity.
   2. Edit the corporate customer record to enter its own customer number in the "corporate address" field.
   3. Set the statement printing option for the corporate account (e.g., consolidated statement).
   4. For each subsidiary (child) customer, enter the parent's customer number in the "parent" field.
   5. Save all records.

3. **Applying Payments**
   - For **Balance Forward** customers, payments are automatically applied to the oldest outstanding balances.
   - For **Open Item** customers, manually apply payments to specific invoices via `Receivables > Enter Payments` or `Receivables > Apply Credits`.

4. **Creating Form Letters**
   1. Go to `Receivables > Letters > Letters Maintenance`.
   2. Create a new letter and assign a name.
   3. Use system variables (e.g., `@01` for customer name, `@08` for account balance) to compose the letter.
   4. Save the letter.
   5. Generate letters for selected customers via `Receivables > Letters > Print Letters`.

5. **Taking Over Another User’s Session**
   1. Navigate to `System > Workstation ID`.
   2. Identify inactive sessions (displayed in black).
   3. Ensure the original user has signed off.
   4. Select the inactive session to take it over; your session ID will change accordingly.

6. **Analyzing a Posting Batch in DataMine**
   1. Identify a transaction’s date-time stamp from GL Inquiry.
   2. Go to `System > DataMine`.
   3. Create a new query filtering on the noted date-time stamp.
   4. Run the query to view all transactions in that posting batch.

7. **Running a Combined Financial Statement**
   1. Navigate to `Accounting > Financial Reports > Financial Statement`.
   2. Select a predefined multiple report group containing desired divisions.
   3. Choose the GL period.
   4. Execute the report to generate combined and individual division statements.

8. **Performing a Cycle Count (Inventory Adjustment by Group)**
   1. Navigate to `Parts > Part Inventory Adjustment > Inventory Adjustment By Group`.
   2. Define the count scope (e.g., bin range).
   3. Print count sheets after the system performs an inventory freeze.
   4. Physically count parts and record quantities.
   5. Enter counts into the system.
   6. Run the Inventory Variation Report to identify discrepancies.
   7. Use the report to adjust GL accounts accordingly.

9. **Making an End-of-Year Adjustment**
   1. Navigate to `Accounting > End of Year > Accounting End of Year Adjustments`.
   2. Enter the first day of the oldest open month.
   3. Specify the Retained Earnings GL account.
   4. Enter adjusting journal entries.
   5. Post the batch to update balance sheet accounts and retained earnings.

### Menu Navigation

- `Point of Sale > Table Maintenance > Credit Card`
- `Receivables > Receivables Maintenance`
- `Receivables > Enter Payments`
- `Receivables > Apply Credits`
- `Receivables > Reports > (various reports)`
- `Receivables > Letters > Letters Maintenance`
- `Receivables > Letters > Print Letters`
- `Receivables > Calculate Interest`
- `Receivables > Print Statements`
- `System > Version`
- `System > Custom Code`
- `System > Change Division/File Set`
- `System > Workstation ID`
- `System > DataMine`
- `System > Security > Initial Data Entry > Required Fields`
- `System > Security > Point of Sale Security > User Maintenance`
- `System > Security > Point of Sale Security > Sales Codes by User`
- `Accounting > Receivables > Inquiry`
- `Accounting > Receivables > Maintenance`
- `Accounting > Payables > Vendor Maintenance`
- `Accounting > Payables > Invoice Entry`
- `Accounting > Payables > Manual Checks`
- `Accounting > Payables > Due Dates and Discounts`
- `Accounting > General Ledger > Maintenance`
- `Accounting > General Ledger > Inquiry`
- `Accounting > General Ledger > Create Source Documents`
- `Accounting > Financial Reports > Financial Statement`
- `Accounting > Financial Reports > Trial Balance`
- `Accounting > Financial Reports > Daily Operating Control`
- `Accounting > End of Month > Combined End of Month`
- `Accounting > End of Year > Accounting End of Year Adjustments`
- `Security Maintenance > Quantum > Quantum Configuration`
- `Units > Inquire/Update Units`
- `Units > Unit Reports > Sales Analysis`
- `Parts > Parts Inquiry`
- `Parts > Part Inventory Adjustment > Inventory Adjustment`
- `Parts > Part Inventory Adjustment > Inventory Adjustment By Group`
- `Parts > Stock Order > Create a Suggested Stock Order`
- `Purchase Orders > Maintenance`

### Business Rules & Constraints

- Customers with posted transactions cannot be deleted; instead, they can be restricted to cash/credit card purchases or flagged as "Do Not Sell."
- When converting a cash customer to a receivables customer, the statement type (Open Item or Balance Forward) must be specified.
- Payments cannot be applied to specific invoices at the point of sale for Balance Forward customers.
- Custom code modifications require paid updates with each new system release; customer-funded developments are integrated as optional features.
- Sessions can only be taken over if the original user has signed off and the session is inactive.
- A customer can only be associated with one Accounts Receivable (A edit code) GL account.
- A vendor can only be associated with one Payables (P edit code) or Flooring (F edit code) GL account.
- Transactions can be merged in both Receivables and Payables modules; however, only Payables supports splitting transactions.
- Posting dates and GL months must align within the same accounting period.
- Manual checks require the check amount to balance with the total invoices paid.
- Purchase order changes made after automatic PO generation are not reflected on the PO.
- Depreciation batches cannot be posted for future months until the current month is closed.
- Units imported from files are always created with an "Available" status and cannot be imported as "On Order" or "Rental."
- End-of-year adjustments must be performed through the dedicated End of Year Adjustments menu, not the standard journal entry interface.
- Journals enabled require table-validated User IDs for all transactions.
- Physical inventory counts use a frozen snapshot; parts sold after the freeze but before counting may cause discrepancies.
- New GL accounts must be manually mapped to reports like the Daily Operating Control (DOC) to ensure accurate reporting.
- The system prevents running end-of-month procedures if any user has open batches in accounting modules.

### Configuration Options

- **Receivables OPT Menu Settings:**
  - Control application order of balance forward credits (e.g., oldest bucket first or interest charges first).
  - Enable automatic printing of detailed aged receivables reports at month-end.
  - Configure printing of zero-balance statements.
  - Set Canadian GST calculation methods.
  - Control aging behavior of interest transactions and credit memos.
  - Prevent calculation of interest on interest.
  - Include or exclude paid open item invoices and payments on statements.
  - Calculate and print interest on statements without posting to accounts.

- **Point of Sale Security:**
  - Enable or disable POS security system-wide.
  - Configure user permissions for closing/reopening documents and sales code access.

- **Vendor Default Allocations:**
  - Set default GL account allocations per vendor to speed invoice entry in Payables.

- **GL Account Edit Codes:**
  - Assign edit codes (A, B, W, S, F, P, etc.) to GL accounts to enforce system logic and accounting rules.

- **Multiple Report Groups:**
  - Define groups of divisions for combined financial reporting.

- **Daily Operating Control (DOC) Mapping:**
  - Manually map GL accounts to DOC report lines to ensure accurate operational reporting.

- **User Security for Divisions:**
  - Control division access and permissions via `Security Maintenance > Quantum > Quantum Configuration`.

- **Automated Purchase Order Generation:**
  - Enable automatic creation of purchase orders when parts stock orders are finalized.

- **Parts Order Codes/Methods:**
  - Configure rules per part or vendor to control suggested stock order calculations.

### Common Pitfalls & Warnings

- Applying a discount code at the customer level applies it universally, including to equipment and labor, which is often undesirable; use price table maintenance for part-specific discounts instead.
- Including paid invoices on statements can confuse customers and lead to duplicate payments.
- The built-in form letter generator produces basic output; for professional letters, export data and use external mail merge tools.
- Improperly exiting sessions (e.g., closing windows without proper sign-off) can lock sessions, requiring manual intervention to release.
- When using DataMine for batch reconciliation, manual adjustment of debit/credit signs is necessary for liability, sales, and income accounts.
- Changing invoice totals after allocation screens in Payables does not update allocations automatically; manual adjustment or re-entry is required.
- Adding tax codes to purchase orders can override customer resale status, potentially affecting tax calculations.
- Forgetting to map new GL accounts to the DOC report results in inaccurate operational reporting.
- Running combined end-of-month procedures with open batches will fail; ensure all batches are posted or canceled.
- Physical inventory cycle counts during business hours may show discrepancies due to sales occurring after the inventory freeze.
- Always exit system screens using provided menu options rather than window controls to avoid session locks.

### Key Terminology

- **Edit Codes:** Single-letter codes assigned to customer or GL account records that define their status and system behavior (e.g., R for Receivables customer, A for AR GL account).
- **Balance Forward:** A receivables statement type summarizing unpaid invoices into a single balance.
- **Open Item:** A receivables statement type listing each unpaid invoice individually.
- **Corporate Receivable:** A parent customer account responsible for subsidiary accounts’ billing.
- **Archiving:** Storing digital copies of transaction documents for later viewing.
- **File Set:** A collection of divisions sharing a common chart of accounts and data files.
- **DataMine:** The system’s primary data query and analysis tool for transaction and posting batch review.
- **Flooring:** Equipment payables tracked against specific stock numbers.
- **Double Posting:** An accounting method where purchase order credits go to an accrued payables account.
- **Easy File:** A feature allowing attachment of documents or notes to specific GL transactions.
- **Inventory Freeze:** A snapshot of inventory quantities taken at a point in time during physical counts.
- **Variation Report:** A report showing differences between frozen inventory and physical counts with financial impact.
- **Suggested Stock Order:** System-generated parts purchase orders based on sales history and ordering rules.
- **Bulk Quantity:** Parts purchased in large units but sold in smaller increments.
- **Multiple Report Group:** A user-defined set of divisions for combined financial reporting.
- **Session ID:** A unique identifier for a user session linked to temporary batches and system activities.

---