---
title: "Quantum — Parts Management"
source: "DIS_Video_Training_Knowledge_Base.md"
tags: ["DIS System Training", "Quantum"]
version: "1.0"
last_updated: "2026-03-04"
short_description: "The **Quantum — Parts Management** module within the DIS (Dealer Information System) platform is a comprehensive solution designed to streamline the management of parts inventory, ordering, pricing, and inter-divisional transfers across dealership..."
long_description: "This document provides a comprehensive overview of the Quantum — Parts Management module within the DIS platform, derived from internal training sessions."
---

# Quantum — Parts Management

**Source Sessions**: 09, 10, 11, 12, 39, 41, 43

### Overview

The **Quantum — Parts Management** module within the DIS (Dealer Information System) platform is a comprehensive solution designed to streamline the management of parts inventory, ordering, pricing, and inter-divisional transfers across dealership operations. It supports detailed configuration of vendors, parts, and classes, enabling dealerships to optimize stock levels, automate ordering processes, and maintain accurate inventory records. The module also facilitates complex business processes such as parts returns, kits assembly, and inter-division parts transfers, ensuring operational efficiency and financial accuracy.

This module is critical for dealerships to maintain optimal parts availability, reduce carrying costs, and improve customer service by ensuring the right parts are available when needed. It integrates inventory management with pricing strategies, vendor relationships, and sales processes, providing a unified platform for parts operations across multiple divisions and locations.

### Core Concepts

**Vendor Class Configuration**  
Vendor classes are a foundational concept in Quantum Parts Management. Each vendor is assigned a unique three-character vendor code, distinct from accounts payable vendor codes. Vendor classes define default behaviors for parts supplied by that vendor, including part number structure, automatic ordering methods, pricing strategies, and default part classes. This classification enables consistent management of parts from the same source and supports enterprise-wide vendor standardization.

**Part Number Structure**  
Part numbers in the system are 18 characters long and can be segmented into up to four parts for sorting and reporting, although most modern implementations use a single segment. Part numbers uniquely identify parts in combination with their vendor code. The system supports supersession chains, allowing automatic replacement of obsolete parts with current equivalents.

**Part Classes**  
Parts are grouped into classes within each vendor to control ordering logic, pricing, and stocking strategies. Classes can represent categories such as direct-ship parts, non-air-freightable items (e.g., paint, oil), special order parts, or captive parts restricted to specific dealers. This grouping facilitates targeted stock ordering and pricing policies.

**Automatic Ordering Methods**  
Quantum supports three primary methods for suggested stock ordering:  
- **DIS Method**: A seasonal approach based on sales from the same period 12 months prior.  
- **Case Method**: Another seasonal method using sales data from 150 days ago.  
- **Annual Method**: A non-seasonal method averaging sales over the last 365 days.  

These methods help dealerships maintain optimal stock levels by analyzing historical sales trends.

**Pricing and Costing**  
The system calculates pricing based on dealer net or suggested list prices and supports various discount structures and replacement cost calculations. Quick codes and class codes assist in pricing and lookup efficiency.

**Inter-divisional Parts Transfers**  
Quantum facilitates parts transfers between divisions within the same enterprise. Transfers can be processed either as direct parts transfers, requiring manual journal entries for financial reconciliation, or through an invoice process that automates financial transactions. Proper configuration ensures accurate inventory and accounting records.

**Part Lists and Kits**  
Part lists group parts for various operational needs, such as importing inventory counts, creating stock orders, or assembling kits. Kits are specialized part lists where a single non-stocking "kit part number" represents a bundle of component parts. Selling a kit relieves inventory for all components while invoicing only the kit master part.

**Inventory Management Concepts**  
The system distinguishes between **Available** quantity (physical stock on hand) and **On-Hand** quantity (available plus reserved for repair orders or counter tickets). It supports bulk parts management, minimum/maximum stock levels, and inventory groups for managing stock across multiple locations or service trucks.

### System Architecture & Data Model

**Vendor Class**  
A vendor class is identified by a three-character code and serves as the top-level grouping for parts. It defines default parameters for all parts associated with that vendor, including pricing, ordering methods, and part classes.

**Part Record**  
The core entity representing an individual part. Each part record includes:  
- Vendor code and 18-character part number (unique identifier).  
- Part class assignment.  
- Descriptions (short and long).  
- Bin locations (primary and overflow).  
- Pricing information, including cost and selling price.  
- Quick code for simplified lookup.  
- Bulk quantity for parts sold in bulk.  
- Supersession links to track replaced parts.

**Part Class**  
Sub-groupings within a vendor that categorize parts for ordering and pricing logic.

**Divisions and Groups**  
Quantum supports multi-divisional operations. Each division maintains its own inventory and general ledger accounts. Inventory can be grouped logically (e.g., service trucks or vans) to manage stock across multiple physical locations.

**Sales Codes**  
Sales codes (e.g., PC, PS, PT) define accounting treatments for parts transactions such as customer sales, stock sales, and parts transfers. These codes are mapped to vendors and used in pricing and reporting.

**Supersession Chain**  
The system maintains a chain of superseded parts, enabling automatic replacement of obsolete parts during receiving or sales.

**Part Lists and Kits Data**  
Part lists are collections of parts identified by a list name and type. Kits are special part lists with a master kit part number flagged to represent the bundle.

### Key Procedures

#### Configuring a New Vendor Class

1. Navigate to `Parts > Parts Configuration > Configure Vendor Class`.  
2. Enter a unique three-character vendor code.  
3. Define the part number structure (typically a single 18-character segment).  
4. Select an automatic ordering method (DIS, Case, or Annual).  
5. Set the default part class for new parts from this vendor.  
6. Configure additional options such as backward supersession and core charge inclusion.

#### Importing a Part List

1. Navigate to `Parts > Price Update Part Lists > Parts Catalog List Configuration`.  
2. Add the vendor to the catalog list and map an appropriate sales code.  
3. Navigate to `Parts > Price Update Part Lists > Part Lists`.  
4. Select the option to import a part list.  
5. Specify the import file and associated vendor.

#### Creating and Receiving a Manual Stock Order

1. Navigate to `Parts > Stock Order > Create Manual Stock Order`.  
2. Enter the vendor and assign a name to the order, then click "Create".  
3. Add parts manually or import from a part list.  
4. Print and finalize the order once complete.  
5. Upon receipt of parts, navigate to `Parts > Receive Order` and receive the stock into inventory.

#### Adding a New Part Record

1. Navigate to `Parts > Parts Posting and Maintenance`.  
2. Select "Add Record" transaction.  
3. Enter the vendor code and new part number (ending with `<` symbol).  
4. Complete the part details screen, including description, class, pricing, and bin locations.  
5. Save the new part record.

#### Performing a Physical Inventory Adjustment

1. Ensure no active users are in Parts or Point of Sale modules (`DD` command can verify).  
2. Run the "Parts Inventory Freeze" process to snapshot current inventory.  
3. Print the "Parts Inventory Adjustment Report" sorted by bin or part number, optionally as a blind count.  
4. Conduct the physical count using the report as a guide.

#### Creating a Suggested Stock Return

1. Navigate to `Parts > Stock Return > Create Suggested Stock Return`.  
2. Select the vendor for the return.  
3. Define filtering criteria: part classes, return codes, minimum months in inventory, months since last receipt, months with no sales, and minimum dollar value per line.  
4. Set return limits such as maximum dollar value or line count.  
5. Configure options like including superseded parts and printing order.  
6. Execute the process to generate Report A (parts to return) and Report B (excess parts).

#### Creating and Using a Part Kit

1. Navigate to `Parts > Part Lists > Add/Change/Delete` and create a new list.  
2. Name the list and set the type to **Kit**.  
3. Add component parts with quantities required for one kit.  
4. Create a master kit part number in `Parts Posting and Maintenance` as a non-stocking part.  
5. Add the master kit part to the list with quantity 1 and flag it as the **Kit Part Number**.  
6. Ensure `Parts > Part Lists > Catalog List Configuration` is set up for relevant sales codes.  
7. Sell the kit via Point of Sale by selecting the part list; the invoice will show only the master kit part number.

#### Correcting Incorrect Vendor Codes

1. Identify the incorrect vendor code and the correct standardized vendor code.  
2. Create or verify the correct vendor exists with all necessary classes configured.  
3. Use the "Reconfigure Parts" utility to reassign parts from the incorrect to the correct vendor.

#### Using Bearing Interchange Feature

1. In any part number entry field, type `#` followed by the stamped part number.  
2. Select the interchange type (e.g., bearing, filter).  
3. Choose the manufacturer to view their corresponding part number.

### Menu Navigation

- `Parts > Parts Configuration > Configure Vendor Class`  
- `Parts > Price Update Part Lists > Parts Catalog List Configuration`  
- `Parts > Price Update Part Lists > Part Lists`  
- `Parts > Stock Order > Create Manual Stock Order`  
- `Parts > Receive Order`  
- `Parts > Order Inquiry`  
- `Parts > Parts Posting and Maintenance`  
- `Parts > Parts Inquiry`  
- `Parts > Stock Return > Create Suggested Stock Return`  
- `Parts > Part Lists > Add/Change/Delete`  
- `Manufacturers > Bearing Interchange Manufacturer Name Vendor Code Table`  
- `Equipment Rental > Work with Rates > Periods`  
- `Equipment Rental > Maintenance > Options`  
- `Equipment Rental > Maintenance > POS Defaults`  
- `Equipment Rental > Maintenance > Rental Sales Codes`  
- `Equipment Rental > Automatic Periodic Invoicing`  
- `Equipment Rental > Reports > Additional Reports > Create Report Files`  
- `Service > Service Utilities > Service Divisional Profile`

### Business Rules & Constraints

- The **"Force ROB Default"** setting on a vendor class allows inventory to go negative by bypassing out-of-stock prompts at point of sale, which can cause inaccurate inventory counts. Use with caution.  
- Sales code tables (PC, PS, PT) must be updated to include new vendors to prevent errors during point-of-sale batch posting.  
- Stock orders cannot be received until they have been finalized.  
- Parts cannot be deleted if they are reserved on open invoices, orders, or returns.  
- The vendor code on a part record is immutable after creation.  
- Part classes must be valid and pre-defined; the system does not prompt for class codes during entry.  
- The system does not prevent selling parts that are on a pending stock return, which may lead to negative inventory.  
- Stock Phase-Out permanently deletes the part record and cannot be reversed.  
- For kits to function correctly, all relevant sales codes must be configured in the Catalog List Configuration.  
- The pound sign (`#`) is reserved for bearing interchange functionality and must not be used in regular part numbers.  
- Rental units belonging to other divisions cannot have their status changed via the standard inquiry screen; changes must be made through the Rental Status Maintenance screen.  
- Inter-divisional rentals require all divisions to be in the same General Ledger period.  
- The Parts Inventory Freeze process cannot run if active users are logged into Parts or Point of Sale modules.

### Configuration Options

- **Automatic Ordering Method:** Choose between DIS, Case, or Annual methods to control suggested stock ordering logic.  
- **Backward Supersession:** Enable to consider both forward and backward supersessions from the price book.  
- **Include Core Charges:** Enable to include core charges in pricing and ordering.  
- **Force ROB Default:** Allows inventory to go negative without prompting.  
- **Parts Transaction Log:** Enable logging of all changes to part records for audit purposes.  
- **Vendor Class Pricing:** Configure pricing methods such as percentage markup or discount from list price.  
- **Economic Ordering Quantity (EOQ):** Set EOQ parameters for ordering optimization.  
- **Special Process Codes:** Assign special codes for vendors requiring unique processing (e.g., Thermal King, CNH New Holland).  
- **Inventory Count Sheet Options:** Configure Parts Inventory Adjustment Report to sort by bin location or part number and to print as blind or with available quantities.  
- **Catalog List Configuration:** Map sales codes to part list types to enable kit processing and other special functions.  
- **Vacation/Sick Accrual Tables:** Define accrual rules and thresholds for employee paid time off.  
- **Rental Module Options:** Configure pre-bill vs. post-bill preferences, default sales codes, damage waiver percentages, rental periods, and rates.

### Common Pitfalls & Warnings

- Using multiple vendor codes for the same supplier across locations impairs enterprise-wide parts availability visibility. Standardize vendor codes.  
- Failure to replicate all classes when creating a new vendor causes reconfiguration processes to fail.  
- Deleting parts on closed but unposted invoices can cause costing errors in point-of-sale batch processing.  
- Negative on-hand quantities indicate inventory errors and require investigation.  
- The "Force ROB Default" setting can lead to inaccurate inventory and should be used judiciously.  
- Min/Max stock levels do not display in Parts Inquiry, which can cause confusion.  
- Technicians placing parts on work orders without physically pulling them leads to inaccurate inventory.  
- Temporary part lists imported from manufacturer catalogs are purged automatically unless made permanent.  
- Suggested stock return generation does not prioritize high-value parts, potentially leaving valuable items off the return list.  
- Attempting to sell kits without proper Catalog List Configuration results in errors.  
- The pound sign (`#`) must not be used in regular part numbers to avoid triggering bearing interchange unintentionally.  
- The Transfer Inquiry under the Parts Menu is misleading; it relates to Point of Sale, not parts transfers.  
- Rental reports require prior creation of report files and access to Keystone for GL account setup.

### Key Terminology

- **Available Quantity:** The physical quantity of a part on the shelf.  
- **On-Hand Quantity:** The total quantity in inventory, calculated as Available plus Reservations.  
- **Reservations:** Parts allocated to open repair orders or counter tickets.  
- **Vendor Class:** A three-character code representing a parts vendor, defining default settings for parts from that vendor.  
- **Part Class:** A classification grouping parts within a vendor for ordering and pricing purposes.  
- **Part List:** A user-defined collection of parts used for ordering, inventory counts, or kits.  
- **Kit:** A special part list where a single master part number represents multiple component parts sold together.  
- **Suggested Stock Order:** A system-generated order based on sales history and demand criteria.  
- **Manual Stock Order:** An order created manually by a user.  
- **Stock Return:** A process to return parts to a vendor, reducing inventory but retaining the part record.  
- **Stock Phase-Out:** A process that removes parts from inventory and deletes the part record permanently.  
- **Supersession:** The replacement of an obsolete part number with a current one, maintained as a chain in the system.  
- **Force ROB Default:** A setting allowing inventory to go negative without user prompt.  
- **Group Inventory:** Logical grouping of inventory locations, such as service trucks or vans.  
- **Bearing Interchange:** A feature for cross-referencing parts like bearings and filters across manufacturers using a `#` prefix.  
- **Pre-bill:** Rental invoicing at the start of the rental period.  
- **Post-bill:** Rental invoicing at the end of the rental period.  
- **Conditions:** Discounts or surcharges applied to rental contracts.  
- **Damage Waiver:** A fee charged on rental contracts to cover potential equipment damage.  
- **Enterprise Vendor:** A vendor standardized across all dealership locations for consistent parts management.  
- **Reconfigure Parts:** A utility to change attributes of parts, such as vendor assignment.  
- **Inventory Freeze:** A snapshot of inventory data at a specific time, used for physical inventory adjustments.  
- **Blind Count:** A physical inventory counting method where counters do not see system quantities.

---