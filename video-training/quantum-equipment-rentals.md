---
title: "Quantum — Equipment Rentals"
source: "DIS_Video_Training_Knowledge_Base.md"
tags: ["DIS System Training", "Quantum"]
version: "1.0"
last_updated: "2026-03-04"
short_description: "The **Quantum — Equipment Rentals** module within the DIS (Dealer Information System) platform is a specialized, for-purchase extension designed to manage the rental lifecycle of equipment efficiently. It enables dealers to designate equipment as ..."
long_description: "This document provides a comprehensive overview of the Quantum — Equipment Rentals module within the DIS platform, derived from internal training sessions."
---

# Quantum — Equipment Rentals

**Source Sessions**: 30, 31, 32

### Overview

The **Quantum — Equipment Rentals** module within the DIS (Dealer Information System) platform is a specialized, for-purchase extension designed to manage the rental lifecycle of equipment efficiently. It enables dealers to designate equipment as rental units, assign rental rates, create rental contracts, and handle billing through integration with the Point of Sale (POS) system. This module supports flexible billing methods, including pre-bill (payment upfront) and post-bill (payment after rental), and accommodates complex scenarios such as prorated charges and re-renting equipment.

This module is critical for dealers who maintain a rental fleet, as it streamlines rental operations, enforces business rules, and integrates rental revenue tracking with accounting. By managing rental units, rates, contracts, and invoicing within a unified system, dealers can improve accuracy, reduce administrative overhead, and provide better customer service.

### Core Concepts

- **Rental Units and R-Status:** Equipment must be added to the system as a unit and explicitly designated as a rental unit by assigning it an "R-status." This status marks the unit as available for rent.

- **Unit Class:** Every rental unit must be assigned a **class**, which is the primary categorization linking the unit to its rental rates. Without a class, rental rates cannot be applied, preventing the unit from being rented.

- **Rental Rates and Rate Tables:** Rental rates are managed centrally in master rate tables organized by division. Rates are assigned to unit classes rather than individual units. The system supports tiered rates, typically daily, weekly, and monthly, with flexibility in defining the length of these periods.

- **Billing Methods:** The module supports two main billing methods:
  - **Pre-bill:** Customers pay upfront before the rental period begins.
  - **Post-bill:** Customers are invoiced after the rental period or at scheduled intervals during an open rental contract.

- **Prorating:** The system allows prorating rental charges when rental periods do not align exactly with standard billing increments (e.g., charging for one and a half weeks).

- **Rental Contracts vs. Reservations:** Rental processing begins with a **reservation**, a preliminary, non-binding record. Once finalized and all system validations pass, the reservation is converted into a formal, billable **rental contract**.

- **Damage Waiver:** An optional fee charged to customers who do not provide their own insurance, protecting the dealer against potential equipment damage.

- **Re-rent:** The practice of renting equipment from another company to sub-rent to a customer, which has distinct accounting and operational implications.

- **Attachments:** Certain rental items (e.g., buckets) can be designated as rental attachments. These are treated as separate rentable units with their own inventory counts but are typically rented alongside a primary unit.

- **Notes:** Two types of notes exist on rental contracts:
  - **Dealer Notes:** Internal notes visible only to dealership staff.
  - **Contract Notes:** Customer-facing notes printed on the rental agreement.

### System Architecture & Data Model

- **Unit Hierarchy:** Each unit is defined by a hierarchy of `group`, `type`, and `class`. The **class** is the key attribute linking the unit to rental rates and billing logic.

- **Rental Tab on Unit Record:** Rental-specific fields reside on a dedicated "Rental" tab within the unit master record. Key fields include:
  - Rental status (e.g., "Available" or "R-status")
  - Rental class assignment
  - Replacement value
  - Damage waiver eligibility
  - Attachment designation checkbox

- **Rate Tables:** Rates are stored in master tables keyed by division and rate code. Each rate code includes daily, weekly, and monthly pricing tiers.

- **Rental Contracts:** A rental contract record links the customer, the specific rental unit (or quantity for non-serialized units), and the applicable rate via the unit’s class. Contracts also include billing and delivery dates, notes, and optional overrides.

- **Sales Codes:** Sales codes track rental revenue and contract numbers for General Ledger (GL) integration. The system requires specific sales code types:
  - Rental sales code: must be a "miscellaneous unit" type.
  - Contract number sales code: must be a "miscellaneous description" type.

- **Job Site Table:** A universal job site maintenance table exists for specifying delivery locations, though users often enter addresses directly on contracts.

- **Employee Integration:** Employees must be configured in the Payroll module to be selectable as salespersons or contacts on rental contracts.

- **Laser Forms:** Rental contracts and agreements are printed using laser forms, which require careful formatting.

### Key Procedures

#### Setting Up the Equipment Rentals Module

1. Navigate to `Equipment Rental > Maintenance > Options`.
2. Configure basic rental settings, including contract form usage, printing preferences, billing defaults, and service status for returned units.
3. Go to `Equipment Rental > Maintenance > Point of Sale Defaults`.
4. Define the default document type for rentals and assign appropriate sales codes for rental revenue and contract numbers.
5. Create or verify sales codes ensuring they meet type requirements.
6. Access `Equipment Rental > Maintenance > Work with Rates` to define rental rate tables.
7. Create rental groups, types, and classes as needed.
8. Add or designate units as rental units, assigning them to a class and setting their rental status to "Available."

#### Creating a Rental Unit

1. Open the unit master record via `Unit Information`.
2. Use the "Add Next Unit" function to expedite entry if applicable.
3. Enter unit details such as unit number and description.
4. Navigate to the "Rental" tab.
5. Set the rental status to "Available" (assigning R-status).
6. Assign the unit to a rental class.
7. Enter the replacement value.
8. Enable the damage waiver option if applicable.
9. If the unit is an attachment, check the "This is an attachment" box on the rental tab.
10. Save the unit record.

#### Setting Up Rental Rates

1. Navigate to `Equipment Rental > Maintenance > Work with Rates`.
2. Select "Maintain Standard Rates" to create or edit rate codes.
3. Define daily, weekly, and monthly rates for each rate code.
4. Return to the "Work with Rates" screen.
5. Highlight the desired rental class.
6. Click "Select Rates" and assign appropriate rate codes to the class.

#### Creating a Rental Contract

1. Navigate to `Equipment Rental > Rent Equipment`.
2. Search for and select the customer renting the equipment.
3. Select the rental unit from the list of available units.
4. Confirm or adjust the "On Rent" date (defaults to current date).
5. Specify delivery date and method.
6. Add internal notes in "Dealer Notes" or customer-facing notes in "Contract Notes."
7. Enter a customer Purchase Order (P.O.) number if provided.
8. If necessary, override standard rates with negotiated pricing and choose whether to prorate related tiers.
9. Review the screen for any error or warning messages; resolve all before proceeding.
10. Convert the reservation into a formal rental contract.

#### Handling Rental Invoices Reaching the 'Z' Suffix

1. When a rental invoice document number suffix reaches 'Z', create a new rental invoice in the POS module.
2. Copy line items from the 'Z' invoice to the new invoice.
3. Close out the original 'Z' invoice manually.

### Menu Navigation

- `Equipment Rental > Maintenance > Options`
- `Equipment Rental > Maintenance > Point of Sale Defaults`
- `Equipment Rental > Maintenance > Work with Rates`
- `Equipment Rental > Maintenance > Units`
- `Equipment Rental > Rent Equipment`
- `Unit Information > Add Next Unit`
- `Accounting > Receivables > Maintenance > EARN01` (for updating customer credit card info)
- AS/400 command line: `DATE (F4)` (to change system date for session)

### Business Rules & Constraints

- Rental units **must** have an assigned rental class before they can be rented.
- Rental rates are division-specific and must be entered using decimals.
- The default rental sales code must be a "miscellaneous unit" type.
- The sales code for contract numbers must be a "miscellaneous description" type.
- Each sales account must have a corresponding cost of sale account.
- Reservations cannot be converted to contracts if any error or warning messages remain unresolved.
- Delivery dates cannot be set in the future if the billing start date is today.
- Non-serialized rental items require a quantity to be entered.
- The dispatching feature of the module is deprecated and no longer used.
- Rental invoices must be manually managed when document suffixes reach 'Z'.

### Configuration Options

- **Contract Form Usage:** Option to use a laser form for printing rental contracts and agreements.
- **Printing Preferences:** Enable printing of job site directions, additional lines, totals, engine overtime rates, and rental rates on contracts.
- **Returned Unit Status:** Configure whether returned units automatically become available or require manual service status updates.
- **Billing Defaults:** Set default billing method to pre-bill or post-bill.
- **Prorating:** Enable or disable prorating of rental charges for partial periods.
- **Credit Limit Checks:** Option to enforce credit limit checks before rental contracts are finalized.
- **Damage Waiver:** Enable charging a damage waiver fee for customers without insurance.
- **Post Bill Option:** Allow rental contracts to defer invoicing until contract closure or billing period end.
- **Rent to Sell:** Option to convert rental agreements into sales transactions.
- **Employee Setup:** Employees must be configured in the Payroll module to be selectable on rental contracts.

### Common Pitfalls & Warnings

- Failing to assign a rental class to a unit prevents rental rates from applying and blocks rental processing.
- Attempting to create a reservation for a unit without an assigned rate will fail.
- Using whole numbers instead of decimals for rental rates causes errors.
- The rental "attachment" feature in the rental tab is distinct from the attachment relationship in the core unit record; confusing these can cause inventory and rental issues.
- Ignoring error or warning messages on rental contract screens blocks contract finalization.
- Exiting the rental module via the "Exit" button closes the module entirely; use "Cancel" to return to previous screens without losing context.
- The dispatching component is obsolete and should not be used.
- Laser forms for rental agreements require careful formatting and can be difficult to customize.
- Running periodic invoicing on-demand requires manual closing of invoices, whereas scheduled jobs automate this process.
- Changing the system date within a session may not affect all system processes as expected.

### Key Terminology

- **R-Status:** A designation indicating a unit is available for rental.
- **Class:** The primary categorization of a rental unit that links it to rental rates.
- **Pre-bill:** Billing method where the customer pays before the rental period begins.
- **Post-bill:** Billing method where the customer is invoiced after the rental period or at scheduled intervals.
- **Prorate:** Charging a proportional rental fee for partial rental periods.
- **Re-rent:** Renting equipment from another company to sub-rent to a customer.
- **Damage Waiver:** An optional fee charged to cover potential equipment damage when the customer lacks insurance.
- **Rental Fleet:** A designated group of equipment maintained for rental purposes.
- **Rental Contract:** A dynamic, billable document containing specific rental details.
- **Rental Agreement:** A static document outlining the standard terms and conditions of rental.
- **Reservation:** A preliminary, non-binding rental record before contract finalization.
- **Dealer Notes:** Internal notes on a rental contract, not visible to customers.
- **Contract Notes:** Customer-facing notes printed on rental contracts.
- **Attachment (in Rentals):** A rentable item associated with a primary unit but tracked separately with its own inventory.
- **Periodic Invoicing:** Automated or on-demand process generating invoices for open rental contracts.

---