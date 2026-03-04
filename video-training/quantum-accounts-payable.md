---
title: "Quantum — Accounts Payable"
source: "DIS_Video_Training_Knowledge_Base.md"
tags: ["DIS System Training", "Quantum"]
version: "1.0"
last_updated: "2026-03-04"
short_description: "The **Quantum — Accounts Payable** module within the DIS (Dealer Information System) platform is designed to manage the entire lifecycle of vendor payables efficiently and accurately. It centralizes vendor information, streamlines invoice processi..."
long_description: "This document provides a comprehensive overview of the Quantum — Accounts Payable module within the DIS platform, derived from internal training sessions."
---

# Quantum — Accounts Payable

**Source Sessions**: 14, 15, 16, 23

### Overview

The **Quantum — Accounts Payable** module within the DIS (Dealer Information System) platform is designed to manage the entire lifecycle of vendor payables efficiently and accurately. It centralizes vendor information, streamlines invoice processing, and facilitates payment execution, ensuring timely and correct payments to suppliers. This module is critical for maintaining strong vendor relationships, managing cash flow, and ensuring compliance with accounting standards.

By integrating tightly with the General Ledger and other modules such as Point of Sale and Units, Quantum Payables supports comprehensive financial management. It handles vendor maintenance, invoice entry, payment processing (including check runs and electronic funds transfers), and reporting such as aging analysis. The system also supports specialized workflows like invoice corrections, EFT pre-validation, and handling of miscellaneous vendors for one-time payments.

### Core Concepts

- **Vendor Master File**: This is the central repository for all vendor-related data, shared across all divisions within the organization. Each vendor is assigned a unique six-character alphanumeric ID, which must be unique across divisions. The vendor master stores detailed information such as business name, address, tax ID (for 1099 vendors), payment terms, and default General Ledger (GL) accounts. Accurate vendor data is essential for proper invoice processing and payment.

- **Invoice Entry and Batching**: Invoices are entered in batches tied to the user’s workstation session. Each invoice record is linked to a vendor and includes details such as invoice number, date, amount, and GL account distributions. The system supports splitting invoices across multiple GL accounts and departments. Batches help organize invoice processing but have limited reporting visibility. Empty batches should be deleted to maintain system cleanliness.

- **Payment Processing**: The module supports generating payment runs based on invoice due dates. Users can review invoices due for payment via reports and then print checks or process electronic payments. The system enforces check number sequencing and supports customization of check printing formats, including Canadian-specific formats.

- **Aging of Payables**: The system categorizes payables by due dates to provide aging reports, which help manage cash flow and avoid missed payments. Regular review of aging reports is recommended.

- **Invoice Corrections and Cancellation**: Invoices can only be canceled after they have been fully created and saved. For complex corrections, offsetting transactions can be entered and merged to clear vendor balances. Canceling invoices in closed accounting periods is possible but discouraged due to reconciliation complexities.

- **Electronic Funds Transfer (EFT) Pre-validation**: For vendors set up for EFT, the system sends a zero-dollar "pre-note" transaction to validate banking information. Once validated, the vendor’s EFT status is marked as "Active." Users with appropriate permissions may manually activate EFT status, but this carries risk if banking details are incorrect.

- **Miscellaneous Vendors**: The system supports a special vendor ID format for one-time payments via manual checks. This miscellaneous vendor ID must begin with the division’s three-letter code followed by a numeric identifier (commonly `999`). Proper setup is required to enable entering payee names on manual checks.

- **Unit Cost Association**: Costs related to equipment units can be added through payable invoices by using special codes in the invoice description. This integrates payables with inventory and unit management.

### System Architecture & Data Model

- **Vendor Master File**: A shared, centralized file across all divisions, keyed by a unique six-character alphanumeric vendor ID. Each vendor record includes contact details, tax ID, payment terms, default AP GL account, and EFT configuration (including an 'Active' flag).

- **Invoice Records**: Each invoice is a discrete record linked to a vendor. Invoices are entered in batches, which are session-specific and tied to the user’s workstation. Invoice lines can be distributed across multiple GL accounts and departments.

- **Payment Records**: Payments (checks or EFTs) are linked to the invoices they settle. The system enforces sequential check numbering and supports manual check entry.

- **Unit and Make/Model Files**: Units are shared across divisions and linked to makes and models. Makes and models are keyed by short codes, with long descriptions used for display. Unit status codes track lifecycle stages (e.g., On Order, Available).

- **Batching Model**: Invoice batches are temporary containers for grouping invoices during entry. Batches are identified by batch numbers, which appear in detailed transaction views and can be used for filtering in data mining.

### Key Procedures

#### How to Create a New Vendor

1. Navigate to `Accounting > Payables > Vendor Maintenance`.
2. Enter a unique six-character alphanumeric vendor ID.
3. Fill in the vendor’s business name, address, and contact information.
4. Enter the vendor’s tax ID if applicable (for 1099 vendors).
5. Assign the appropriate AP GL account and set default expense accounts if desired.
6. Set payment terms for the vendor.
7. Save the vendor record.

#### How to Enter a Payable Invoice

1. Navigate to `Accounting > Payables > Invoice Entry`.
2. Create or select an existing batch.
3. Select the vendor.
4. Enter the invoice number, date, and amount.
5. The system will pre-fill GL account distributions based on vendor defaults; modify if necessary.
6. Add invoice line items, supporting splits across GL accounts and departments.
7. Add the invoice to the batch.
8. Repeat for all invoices in the batch.
9. Post the batch to finalize entries.

#### How to Process a Check Run

1. Navigate to `Accounting > Payables > Payables Due Report` to review invoices due for payment.
2. Navigate to `Accounting > Payables > Print Payable Checks`.
3. Enter the cutoff date for invoices to include.
4. Enter the check date and starting check number.
5. Select vendors to pay.
6. Print checks according to the configured format.

#### How to Cancel an Invoice

1. Ensure the invoice has been fully created and posted.
2. Navigate to `Accounting > Payables > Cancel Invoices`.
3. Select the invoice to cancel.
4. Confirm cancellation. Note: invoices modified via the 'change' function cannot be canceled directly and require offsetting entries.

#### How to Create a Net-Zero Invoice for EFT Pre-note

1. Navigate to `Accounting > Payables > Invoice Entry`.
2. Create a new invoice for the EFT vendor.
3. On the first distribution line, enter a small positive amount (e.g., $0.01).
4. On the second distribution line, enter the corresponding negative amount (e.g., -$0.01) to the same GL account.
5. Post the invoice to trigger the EFT pre-note validation.

#### How to Test Miscellaneous Vendor Setup

1. Navigate to `Payables > Intermanual Checks`.
2. Enter the miscellaneous vendor ID.
3. Attempt to enter a payee name.
4. If the payee name field is editable, the vendor ID is correctly configured with the division prefix.

#### How to Add a New Unit with New Make/Model

1. Navigate to the unit entry screen.
2. Enter a new unit number.
3. In the make and model fields, type the new make and model names.
4. Press Enter.
5. Click the 'Make Model Table' button.
6. Confirm creation of the new make and set options (e.g., allow blank model).
7. Confirm creation of the new model.
8. Select the newly created make and model.
9. Complete unit details and save.
10. Enter 'On Order' purchase order details in the pop-up.

#### How to Add Cost to a Unit via Invoice

1. Navigate to `Accounting > Payables > Invoice Entry`.
2. Create an invoice for the vendor supplying the unit.
3. Enter the unit number in the invoice line item.
4. In the description, type `@C` or `INV COST` to flag the cost addition.
5. Enter the cost amount and post the invoice.

#### How to Sell a Unit

1. Navigate to `Point of Sale > Invoicing`.
2. Start a new equipment sale invoice (document type 'E').
3. Add the unit number to the invoice.
4. Enter the selling price and any applicable charges or discounts.
5. If financing, enter the financed amount as a negative sales code.
6. Print and close the invoice.

#### How to Pay for a Unit via Manual Check

1. Navigate to `Accounting > Payables > Enter Manual Checks`.
2. Enter the check date, vendor, and check number (no alphabetic characters allowed).
3. Select vendor invoices to pay.
4. Verify total amount and post the check.

### Menu Navigation

- `Accounting > Payables > Vendor Maintenance`
- `Accounting > Payables > Group Code Maintenance`
- `Accounting > Payables > Invoice Entry`
- `Accounting > Payables > Correct Due Dates/Discounts`
- `Accounting > Payables > Cancel Invoices`
- `Accounting > Payables > Payables Due Report`
- `Accounting > Payables > Print Payable Checks`
- `Accounting > Payables > Vendor Inquiry`
- `Accounting > Payables > Intermanual Checks`
- `Accounting > Payables > Enter Manual Checks`
- `Point of Sale > Invoicing`
- Unit entry and make/model maintenance screens (accessed via unit management module)

### Business Rules & Constraints

- Vendor IDs must be unique six-character alphanumeric codes across all divisions.
- Miscellaneous vendor IDs must begin with the division’s three-letter code followed by a numeric identifier (e.g., `HHH999`).
- An invoice cannot be entered or paid unless the vendor exists in the system.
- Duplicate invoice numbers for the same vendor are not allowed.
- Invoices must be fully created and saved before cancellation is possible.
- Zero-dollar invoices are not permitted; use net-zero invoices with offsetting lines for EFT pre-note purposes.
- Check numbers must be sequential and cannot be reused or be lower than the last used number.
- Check numbers entered manually cannot contain alphabetic characters.
- The tax code field in vendor maintenance is intended for Canadian GST/PST and should not be used for US vendors.
- Canceling transactions in closed accounting periods is allowed but discouraged due to reconciliation difficulties.
- Units sold must have unique stock numbers; reusing stock numbers for trade-ins causes system errors.
- The 'Receive Unit' option is only available when the unit status is 'On Order' (O).
- EFT pre-note validation must be completed before live EFT payments unless manual activation is performed with risk.

### Configuration Options

- **Default Payment Terms**: Set system-wide default payment terms that apply automatically to new vendors.
- **Default GL Accounts**: Assign default expense GL accounts per vendor to streamline invoice entry.
- **Check Printing Format**: Customize check layouts to match user check stock, including Canadian check format options.
- **1099 Vendor Grouping**: Configure vendors as 1099 vendors and generate 1099 reports/files.
- **Vendor Hold**: Place vendors on hold to exclude them from payment runs.
- **EFT Vendor Configuration**: Enter banking details and manage EFT activation status within vendor maintenance.
- **Make/Model Creation Options**: When creating new makes, configure whether models without codes are allowed.

### Common Pitfalls & Warnings

- **Incorrect Vendor Selection**: Selecting the wrong vendor during invoice entry can be difficult to correct later; verify carefully.
- **Ignoring Aging Reports**: Failure to regularly review payables aging reports may result in missed payment deadlines.
- **Misuse of Tax Code Field**: Using the tax code field for US vendors can cause incorrect tax calculations.
- **Improper Miscellaneous Vendor Setup**: Omitting the division prefix in miscellaneous vendor IDs prevents entering payee names on manual checks.
- **Reusing Stock Numbers for Trade-ins**: This causes the system to 'unsell' the original unit, leading to accounting errors.
- **Canceling Invoices in Closed Periods**: While allowed, it complicates reconciliation and should be avoided if possible.
- **Manually Activating EFT Without Pre-note**: Skipping EFT pre-note validation risks payment failures due to incorrect banking information.
- **Leaving Empty Invoice Batches**: Abandoned batches remain in the system; use the 'Delete Batch' function to clean them up.
- **Entering Incorrect Due Dates**: Can cause invoices to be paid prematurely or late; verify due dates carefully.

### Key Terminology

- **Accounts Payable (AP)**: Short-term liabilities owed to vendors for goods or services received.
- **Vendor**: An individual or company supplying goods or services, identified by a unique vendor ID.
- **Vendor Master File**: Centralized database containing all vendor information.
- **Invoice**: A document recording a payable transaction from a vendor.
- **Batch**: A temporary grouping of invoices entered during a user session.
- **Check Run**: The process of selecting and paying due invoices via checks or electronic payments.
- **EFT (Electronic Funds Transfer)**: Electronic payment method requiring bank account validation via pre-note.
- **Pre-note**: A zero-dollar EFT transaction sent to verify vendor banking details before live payments.
- **Miscellaneous Vendor**: A vendor ID used for one-time or manual payments, requiring a division code prefix.
- **GL Account**: General Ledger account used to categorize expenses and liabilities.
- **Make/Model**: Manufacturer and product line identifiers for units (equipment or vehicles).
- **Unit**: An individual piece of equipment or vehicle tracked in inventory and linked to payables.
- **On Order (O) Status**: Unit status indicating the item has been ordered but not yet received.
- **Available (A) Status**: Unit status indicating the item is in stock and ready for sale.
- **Trade Payables**: Standard accounts payable related to regular business operations.
- **Flooring**: Equipment payables handled separately from trade payables.
- **Group Code**: A code used to group vendors for reporting or payment purposes, such as 1099 classification.

---