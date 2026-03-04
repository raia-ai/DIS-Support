---
title: "Quantum — Point of Sale"
source: "DIS_Video_Training_Knowledge_Base.md"
tags: ["DIS System Training", "Quantum"]
version: "1.0"
last_updated: "2026-03-04"
short_description: "The **Quantum — Point of Sale (POS)** module within the DIS platform is a comprehensive system designed to manage sales transactions, work orders, parts transfers, labor tracking, and invoicing for dealerships. It integrates customer management, i..."
long_description: "This document provides a comprehensive overview of the Quantum — Point of Sale module within the DIS platform, derived from internal training sessions."
---

# Quantum — Point of Sale

**Source Sessions**: 08, 18, 19, 20, 25, 26, 42

### Overview

The **Quantum — Point of Sale (POS)** module within the DIS platform is a comprehensive system designed to manage sales transactions, work orders, parts transfers, labor tracking, and invoicing for dealerships. It integrates customer management, inventory control, technician time tracking, and accounting processes to streamline dealership operations. The module supports various transaction types, including cash sales, charge sales, internal work, warranty work, and parts transfers, providing flexibility and control over complex billing scenarios.

This module is critical for dealerships because it ensures accurate billing, inventory management, and labor tracking while maintaining compliance with accounting standards. Features such as Point of Sale Lockout, shop supplies charges, and POS security enhance financial control and customer management. Additionally, the ability to create and use Standard Jobs and work order segmentation improves efficiency in service operations.

### Core Concepts

- **Shop Supplies:** A configurable miscellaneous charge automatically added to specific document types (e.g., work orders). It can be a fixed amount or a percentage. While convenient, automatic application risks customer disputes if not disclosed upfront.

- **Point of Sale Lockout:** A security feature that blocks a customer from making further purchases. Lockout can be applied manually by assigning a special credit code ('Z') or automatically based on business rules such as exceeding credit limits or having past-due balances.

- **Credit Codes:** Codes assigned to customers to manage their purchasing status. The 'Z' credit code specifically activates the POS Lockout.

- **POS Printer Jobs:** The first user to access POS with a specific printer initiates a background job that owns the printer. All print jobs on that printer route to the initiating user's report center, regardless of who printed them.

- **Customer Edit Codes:** Single-letter codes summarizing customer status:
  - **M:** Marketing database customer
  - **C:** Cash-only customer
  - **R:** Receivables (charge) customer
  - **W:** Equipment purchaser
  - **L:** Equipment renter

- **Document Statuses:** Indicate the state of POS documents:
  - **O:** Open
  - **C:** Closed
  - **V:** Voided

- **Cash vs. Charge Transactions:** Transactions can be toggled between cash and charge. Switching back to charge after cash does not repopulate default credit card info.

- **Sold By Field:** Identifies the employee creating the invoice; must be set up as a "sold by address" in Marketing.

- **POS Security:** Optional feature requiring user ID and password for document access, configurable for locking or reporting on actions.

- **Time Clock Integration:** Technician labor is recorded via time clock punches linked to work orders. Voiding work orders with time clock entries is restricted to maintain data integrity.

- **Prepayments & Deposits:** Customers can prepay for ordered parts or deposits, which may include tax. Freight prepayments require manual tracking.

- **Standard Lines:** Pre-configured invoice lines (e.g., freight charges) that can be quickly added using codes.

- **Rolling Invoices:** When parts are partially fulfilled, closing an invoice automatically creates a new invoice for backordered parts with associated prepayments.

- **Parts Transfers:** Facilitate inter-divisional part requests and fulfillment with status tracking (requested, accepted, shipped).

- **Copying Documents & Alternate Sessions:** Users can copy quotes or templates to new invoices and open a second POS session to look up documents without losing their place.

- **Work Orders:** Central to service operations, linking customers, serialized units, labor, and parts. Supports segmentation, flat-rate billing, internal vs. customer transactions, and multiple payers.

- **Standard Jobs:** Templates for frequently performed services stored under generic or model-specific customer records, allowing quick copying to work orders.

### System Architecture & Data Model

- **Document Types:** Distinct classifications (e.g., Counter Ticket, Work Order, Quote, Transfer) control behavior and sales code restrictions.

- **Shop Supplies Charges:** Linked to specific document types; charges apply only if configured.

- **Credit Codes:** Stored in customer receivables maintenance; presence of 'Z' triggers POS Lockout.

- **POS Printer Jobs:** Background jobs owned by the first user to access a printer, routing all print output to that user's report center.

- **Customer Records:** Contain edit codes indicating status and history.

- **Sold By Addresses:** Employee records maintained in Marketing module, linked to invoices.

- **Time Clock Data:** Technician punches linked to work orders; labor lines associated with segments.

- **Work Orders:** Comprise header and detail lines for parts and labor; support multiple billing parties via "bill to" codes.

- **Document Suffixes:** Used for rolling invoices (e.g., suffix 'B' for backordered parts invoice).

- **Sales Codes:** Define transaction types and map to General Ledger accounts; can be restricted by document type.

- **Parts Transfer Status Codes:**
  - **T:** Transfer requested
  - **t:** Transfer accepted
  - **u:** Part shipped/in transit

- **Standard Jobs:** Stored as work orders under a generic customer (e.g., "star jobs"), with unique 8-character document numbers and descriptions on the Unit Info tab.

- **Internal Umbrella Customer:** A generic internal customer flagged as internal to handle internal work orders not tied to specific stock numbers.

- **Cash Customer Records:** Special customer records with address number format `space, cash, [Division Letter]` used as clearing accounts for cash and credit card sales.

### Key Procedures

#### 1. Setting Up Shop Supplies

1. Navigate to the shop supplies configuration area.
2. Define the charge amount or percentage.
3. Associate the charge with the appropriate document type (e.g., 'W' for work order).

#### 2. Installing and Configuring Point of Sale Lockout

1. Navigate to `POI Security > opt DIS master menu > Point of Sale > fourth menu > Point of Sale Lockout feature`.
2. Select option 6 to install the feature for manual use.
3. Go to `Credit Code Maintenance`.
4. Create or verify the 'Z' credit code with a clear description (e.g., "Accounting Hold").

#### 3. Manually Locking a Customer Account

1. Access the customer's account in receivables maintenance.
2. Assign the 'Z' credit code to the account.

#### 4. Creating a New Invoice

1. Navigate to `POS > Invoicing`.
2. Enter the document type (e.g., 'C' for Counter Ticket).
3. Search for the customer by name or phone number (partial phone number allowed).
4. Review any open documents warning.
5. Open a new document.
6. Review any red credit messages.
7. Enter the "Sold By" employee code.
8. Add items to the invoice.

#### 5. Posting a POS Batch

1. Navigate to `POS > post POS documents > Review and Post POS Documents`.
2. Review the batch for errors.
3. If errors exist, correct them directly in the batch posting screen or source documents.
4. Re-run error checks.
5. Generate an edit list and recap the batch.
6. Post the batch.

#### 6. Correcting a Document in a Failed Posting Batch

1. Identify the problematic document and error.
2. Delete the document's GL entry lines from the batch.
3. Optionally process or cancel the batch.
4. Use `Reclaim POS Documents` to release the document.
5. Reopen and correct the document.
6. Print and close the document again.
7. Include the corrected document in the next batch.

#### 7. Setting Up the Cash Customer for a Division

1. Create a new customer record.
2. Set the address number as `space, cash, [Division Letter]` (e.g., `space, cash, H`).
3. Enter a descriptive name (e.g., "Cash Sale H").
4. Assign the division's cash GL account.
5. Set a standard tax code.
6. Save the record.

#### 8. Handling Prepayments for Ordered Parts

1. Add ordered parts to the invoice.
2. Note the total in the "Ordered Parts" field (includes tax).
3. Add a "Prepayment" line with the prepayment amount.
4. For prepaid freight, add a descriptive note manually.

#### 9. Initiating a Parts Transfer

1. Add the needed part to the invoice.
2. If out of stock, enter 'T' to open the transfer inquiry.
3. Select the division with stock.
4. Specify quantity and forward the request.
5. The invoice line updates with a 'T' priority code.

#### 10. Accepting and Fulfilling a Parts Transfer

1. Access the parts transfer queue (`Parts > Transfer Inquiry` or via POS).
2. Review requested parts.
3. Choose to accept, reject, or skip the transfer.
4. Accepting converts note lines to part lines, affecting inventory.
5. Print and close the transfer invoice.

#### 11. Copying a Quote to a Sales Invoice Using Alternate Session

1. Open a new sales invoice in the primary POS session.
2. Open an alternate POS session.
3. Locate the quote in the alternate session.
4. Select and copy the quote.
5. Confirm copy options (reprice or keep pricing, void original).
6. Complete the copy; lines appear in the primary invoice.

#### 12. Creating a Work Order

1. Navigate to work order creation.
2. Select the customer.
3. Enter "Sold By" employee.
4. Select the serialized unit on the Unit Info tab.
5. Enter service description.

#### 13. Setting Minimum and Maximum Labor Charges on a Work Order

1. From the work order, go to the Sold To screen.
2. Click "Service Notes."
3. Access the "Service Info" tab.
4. Enter minimum and maximum labor charges.

#### 14. Correcting Technician Time Clock Punches

1. Navigate to `POS > Time Clock > Review by Technician`.
2. Select technician and date.
3. Add correct punch line before deleting incorrect one.
4. Note: Adding punches always clocks the technician out.

#### 15. Reopening a Closed Work Order

1. Locate the closed work order.
2. Select the customer portion.
3. Click "Reopen" (only if not posted).

#### 16. Handling Internal Work Orders

1. Create an "umbrella" internal customer flagged as internal.
2. Open work orders under this customer for internal jobs.
3. Select specific internal address on Unit Info tab.
4. Use 'I' in the IW box on sale lines to flag internal transactions.

#### 17. Flat-Rating a Work Order

1. Navigate to the work order.
2. Go to the Service Info screen.
3. Enter flat-rate amount in minimum and maximum fields.
4. Assign sales code.
5. Post labor to the work order.
6. Use "Auto Charge" to adjust labor charges to flat rate.

#### 18. Creating and Using Standard Jobs

1. Create a generic cash customer (e.g., "star jobs") to hold standard jobs.
2. In POS, switch to Standard Jobs view.
3. Create a new work order under the standard jobs customer.
4. Assign a unique 8-character document number.
5. Enter description on Unit Info tab.
6. Set flat rate in hours.
7. Add notes and parts (do not affect inventory).
8. Place the job on hold.
9. To use, create a customer work order, switch to Standard Jobs view, select and copy the job, choosing to reprice from current inventory.

### Menu Navigation

- `POI Security > opt DIS master menu > Point of Sale > fourth menu > Point of Sale Lockout feature`
- `Credit Code Maintenance`
- `POS > Invoicing`
- `POS > post POS documents > Create a point of sale posting batch`
- `POS > post POS documents > Review and Post POS Documents`
- `POS > post POS documents > Reclaim POS Documents`
- `Marketing > Address Maintenance`
- `Archive > Work with archive documents > POS documents e-form`
- `POS > Table Maintenance > Document Classification`
- `POS > Table Maintenance > Sales Code Maintenance`
- `Parts > Transfer Inquiry`
- `POS > Time Clock > Review by Technician`
- `POS > POS reports > Service recovery and efficiency`
- `System > AS400 command line`

### Business Rules & Constraints

- Shop supplies charges apply only if configured for the document type.
- POS Lockout requires a properly configured 'Z' credit code.
- Automatic lockout can be triggered by exceeding credit limits or past-due balances (default 30 days).
- Customers must have assigned credit limits to avoid unintended lockouts.
- POS documents cannot be changed after posting.
- Voiding work orders with time clock labor is restricted.
- Technician must clock out before clocking into a new job.
- Flat-rate labor adjustments require POS access lock permission.
- Labor line segments require corresponding note lines on the work order.
- Internal work orders must use an umbrella customer flagged as internal.
- Sales codes must be correctly mapped to GL accounts.
- Cash sales require a configured cash customer record per division.
- Parts transfers require vendor configuration in both sending and receiving divisions.
- Document numbers may be duplicated across divisions; division context is critical.
- Quotes remain indefinitely unless manually voided or set to auto-void on copy.
- Cannot reassign documents to different document types.
- Cannot copy lines between incompatible document types due to sales code restrictions.
- The "Reassign" function is disabled when multiple POS sessions are open.

### Configuration Options

- Shop supplies charge amount and document type association.
- POS Lockout modes:
  - Not installed (disabled)
  - Manual lockout via 'Z' credit code
  - Automatic lockout based on credit limit
  - Automatic lockout based on past-due status
  - Automatic lockout based on either credit limit or past-due
- POS Security requiring user ID/password and configurable reporting or locking.
- Time Clock Configuration with POS access lock for flat-rate adjustments.
- Sales code setup with GL account mappings.
- Document classification setup for quotes, transfers, counter tickets, and standard jobs.
- Parts transfer setup including sales code and laser form definitions.
- Cash customer records per division for cash and credit card sales.
- Option to print invoice counters for auditing.
- Option to generate time clock detail punch reports on work order print and close.
- Laser form configuration for office copies and transfer documents.

### Common Pitfalls & Warnings

- Automatic shop supplies charges can cause customer disputes if not disclosed.
- POS printer jobs are owned by the first user; printouts may go to the wrong user's report center.
- Missing sales code mappings cause posting batch errors.
- Enabling POS security requires thorough user setup and should be done during off-hours.
- Tax code changes on invoice lines persist until manually changed or invoice refreshed.
- Freight prepayments do not carry over automatically in rolled invoices; manual notes are needed.
- Exiting POS with multiple sessions requires closing each session individually.
- Forgetting to clock out or clock in causes time clock reporting errors.
- Auto-charge flat-rate labor fails if no labor is posted.
- Labor segments require note lines; missing these causes assignment failures.
- Incorrect use of parts transfer sales codes causes GL posting errors.
- Using identical document numbers across divisions can cause confusion.
- Failing to set up cash customer records causes cash sales posting failures.
- Reclaiming batches without verifying posted documents risks double posting.
- Not canceling or properly closing failed posting batches locks the batch to a workstation ID.
- Users may forget to switch POS views when working with Standard Jobs.
- Standard Job codes are limited to 8 characters; concise naming is necessary.

### Key Terminology

- **Shop Supplies:** Miscellaneous charge automatically added to certain document types.
- **Point of Sale Lockout:** Feature that prevents a customer from making purchases, activated via credit code 'Z'.
- **Credit Code:** Code representing customer credit status; 'Z' triggers lockout.
- **Background Process / Speed up job:** Printer job owned by the first POS user on a printer, routing all print output.
- **Edit Codes:** Single-letter customer status codes (M, C, R, W, L).
- **Sold By:** Employee record linked to invoices.
- **Standard Line:** Pre-configured invoice line for frequent charges or notes.
- **Rolling Invoice:** Automatically generated invoice for backordered parts after partial fulfillment.
- **Parts Transfer:** Inter-divisional part request and fulfillment process.
- **Alternate Session:** Secondary POS session for document lookup without losing primary session context.
- **Work Order:** Document detailing service work, parts, and labor for a customer.
- **Time Clock:** Technician labor tracking system integrated with work orders.
- **Auto Charge:** Function to adjust labor charges to a flat-rate amount.
- **POS Access Lock:** Security setting controlling flat-rate labor adjustments.
- **Segments:** Subdivisions of a work order to separate different job types or payers.
- **Umbrella Customer:** Generic internal customer account for internal work orders.
- **IW Box:** Field on sale lines to flag internal transactions.
- **Standard Job:** Template work order stored under a generic customer for reuse.
- **Star Jobs:** Generic customer record holding Standard Jobs.
- **Reclaim:** Process to release documents from a failed or canceled posting batch.
- **Post / Posting:** Sending closed POS transactions to the General Ledger.
- **Source Document Inquiry:** Tool to verify posted transactions.
- **Index (Re-indexing):** Maintenance task to rebuild database pointers.
- **Workstation ID:** Unique identifier for a user's session; relevant for batch locking.

---