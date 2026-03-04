---
title: "Quantum — Purchase Orders"
source: "DIS_Video_Training_Knowledge_Base.md"
tags: ["DIS System Training", "Quantum"]
version: "1.0"
last_updated: "2026-03-04"
short_description: "The **Quantum — Purchase Orders** module within the DIS platform’s Payables system streamlines the management of purchase orders (POs) for dealerships. It facilitates the creation, receipt, and invoicing of purchase orders, linking procurement act..."
long_description: "This document provides a comprehensive overview of the Quantum — Purchase Orders module within the DIS platform, derived from internal training sessions."
---

# Quantum — Purchase Orders

**Source Sessions**: 37

### Overview

The **Quantum — Purchase Orders** module within the DIS platform’s Payables system streamlines the management of purchase orders (POs) for dealerships. It facilitates the creation, receipt, and invoicing of purchase orders, linking procurement activities directly to inventory, expenses, and vendor payables. This module supports both simple and complex workflows, accommodating centralized accounting controls and partial shipments, which are common in dealership operations.

This module is critical because it ensures accurate financial tracking of purchases, integrates with inventory and work orders, and supports resale of purchased items. By managing purchase codes, linking POs to parts stock orders, and handling partial receipts, Quantum Purchase Orders help dealerships maintain precise control over their procurement and accounting processes, reducing errors and improving operational efficiency.

### Core Concepts

**Single vs. Double Posting Process**  
Quantum offers two distinct posting methods for handling purchase order invoices:

- **Single Posting**: When a PO batch is posted, the system immediately creates the vendor invoice and posts it to the vendor’s account. This method is simpler and preferred for new installations. However, it does not allow users to drill down into PO details from the vendor invoice, and any discrepancies between the PO amount and the final vendor invoice require manual accounting adjustments.

- **Double Posting**: This is a two-step process. First, posting the PO increases inventory or expenses and credits a liability account called **Accrued Purchase Orders**. Then, an accounting user manually enters the vendor’s invoice in a separate **Invoice Entry** screen and applies it against the accrued PO. This method provides greater control and verification, suitable for centralized accounting departments.

**Purchase Codes**  
Purchase Codes are three-character identifiers used to classify items on a PO. Each code links to a specific General Ledger (GL) debit account, such as inventory or expense accounts. Purchase Codes can also be linked to corresponding sales codes, enabling purchased items to be resold on work orders or counter tickets with correct costing and pricing logic. The type of Purchase Code (e.g., inventory part, miscellaneous quantity, or description) determines required fields and validation rules.

**Linking POs to Parts Stock Orders**  
When a parts stock order is finalized, the system can automatically generate a single-line PO representing the total order value. Users may add additional parts or expenses (such as freight) to this PO. A system option controls whether parts originally on the stock order are received again if manually added to the PO, preventing duplicate receiving.

**Partial Receipts (Splitting a PO)**  
Quantum supports partial receipt of purchase orders. Users can select specific PO lines to close, generating an invoice for the received items while leaving the remaining lines open. The PO status changes to **Partial (P)**, and each partial receipt uses a unique invoice number.

**Reselling from a PO**  
Certain PO line items, such as outside labor, trucking, or special-order parts, can be directly resold to customers on specific work orders or counter tickets. When creating the PO, users select the customer and target work order, allowing the system to push the cost from the PO line to the work order using the linked purchase and sales codes.

**PO Line Types**  
POs can include various line types, such as inventory parts, miscellaneous parts (non-stocked), equipment, freight, outside labor, and other expenses. Each line type is controlled by a specific purchase code.

### System Architecture & Data Model

The Quantum Purchase Orders module is structured around several key data entities:

- **Purchase Codes**: Central to the module, these codes link a 3-character identifier to a description, a GL debit account, and optionally a sales code for resale. The purchase code type dictates required fields and validation logic. For example, if linked sales codes do not use quantity, the purchase code cannot require quantity input.

- **Purchase Orders**: Each PO consists of a header and multiple detail lines. The header includes vendor information, PO number, dates, and status. Detail lines contain purchase codes, descriptions, quantities, costs, and resale information.

- **PO Status**: The system tracks PO status as:
  - **O (Open)**: PO is active and open for receiving.
  - **P (Partial)**: Some lines have been closed due to partial receipt.
  - **C (Closed)**: All lines have been received and invoiced.

- **Accrued Purchase Orders Account**: In double posting, this GL liability account temporarily holds the credit side of the transaction until the vendor invoice is processed.

### Key Procedures

#### Creating and Partially Receiving a Stock Order PO

1. Finalize a stock order in the Parts module; this automatically generates a PO with a single line representing the total order value.
2. Receive a partial shipment of goods.
3. Navigate to `Parts > Stock Order > Receive Order > Correct Order Before Receiving`.
4. Select the stock order and adjust quantities and costs for the received items, then post the receipt.
5. Open the corresponding PO in the Purchase Order entry screen.
6. Edit the stock order line on the PO to match the value of the received shipment.
7. Add new PO lines for associated costs (e.g., freight) using appropriate purchase codes.
8. Click **Print and Close**.
9. When prompted, enter the vendor’s invoice number for this partial shipment.
10. Check the **Close Select Lines** box.
11. Select the PO lines corresponding to the received items and freight.
12. Click **Close Lines**; the PO status updates to **P (Partial)**.
13. Manually remove the invoice number from the PO header to prevent confusion on future receipts.

#### Receiving the Final Shipment and Closing the PO

1. Receive the remaining items via `Parts > Stock Order > Receive Order`.
2. Note the value of the final shipment.
3. Open the partially closed PO.
4. Edit the original stock order line to reflect the final shipment’s cost.
5. Add any additional freight charges as new PO lines.
6. Click **Print and Close**.
7. Confirm the total invoice amount matches the vendor’s invoice.
8. Enter the new vendor invoice number and due date.
9. Click **Close Order**; the PO status changes to **C (Closed)**.

#### Creating a PO to Resell Trucking to a Work Order

1. Start a new PO from the Purchase Order menu.
2. Select the vendor (e.g., trucking company).
3. In the customer name field, search for and select the target customer work order.
4. The system populates the customer and work order details in the PO header.
5. Add a detail line with the appropriate purchase code for trucking (e.g., 'PZT') and ensure the **Resale** flag is set.
6. Enter a description and the total cost.
7. Press Enter; confirm the target work order in the popup window.
8. Confirm the selection; the cost is pushed to the specified work order.
9. Close the PO to create the payable to the vendor.

### Menu Navigation

- `Parts > Stock Order > Receive Order > Correct Order Before Receiving`
- Purchase Orders are accessed via the **Payables** module (exact menu path varies by installation)
- PO creation and entry screens are typically found under the **Payables > Purchase Orders** menu

### Business Rules & Constraints

- Switching from **Double Posting** to **Single Posting** requires the **Accrued Purchase Orders** GL account to be fully cleared.
- PO details cannot be drilled down from vendor inquiry screens if the PO was posted using the Single Posting method.
- The type of a Purchase Code must be compatible with the linked Sales Code, especially regarding quantity usage.
- POs can be created for vendors in one division but assigned to another division, supporting centralized purchasing.
- When reselling from a PO, the target work order must be in an **Open** or **Reopened** status.
- Partial receipts require manual removal of invoice numbers from the PO header after closing selected lines to avoid confusion.

### Configuration Options

- **Single vs. Double Posting Process**: Choose the PO-to-invoice workflow method.
- **PO Number Linked to Inventory Orders**: Enable or disable automatic PO creation from parts stock orders.
- **Parts on PO Not Received if Also Stock Ordered**: Prevents duplicate receiving of parts that appear on both stock orders and manually added PO lines.
- **Allow Exchange Rate**: Option to store a static exchange rate with the invoice; most dealerships prefer manual management.
- **PO Print Options**: Configure printed PO details, such as including purchase code descriptions or GL debit account descriptions.
- **Split PO Includes Receive Date**: Option to print the receive date on the in-house copy when a PO is split.

### Common Pitfalls & Warnings

- **Leaving Invoice Number on Partial PO**: After partially closing a PO, the system retains the invoice number in the header. Users must manually clear this to prevent confusion with subsequent invoices.
- **PO/Invoice Amount Mismatch in Single Posting**: If the vendor invoice differs from the PO amount, manual accounting adjustments are necessary.
- **System Behavior When Editing Partial POs**: Editing partially closed POs can cause the system to behave unpredictably, such as automatically jumping between lines, requiring users to exit and re-enter the screen to regain control.

### Key Terminology

- **Single Posting**: Posting method where the PO batch immediately creates the vendor invoice and posts it to accounts payable.
- **Double Posting**: Two-step posting method where the PO posts to an accrued liability account first, followed by manual invoice entry to finalize payables.
- **Accrued Purchase Orders**: A GL liability account used as a temporary holding account during double posting.
- **Purchase Code**: A three-character code defining the GL debit account and other properties for purchased items.
- **Splitting a PO**: Closing selected lines on a PO to process partial receipts while leaving other lines open for future receipt. The PO status changes to Partial (P).

---