---
title: "CSPS User Documentation"
source: "combined_Quantum_docs.md"
tags: ["Quantum"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about CSPS User Documentation."
long_description: "This document provides information about CSPS User Documentation from the DIS Quantum system."
---

## Introduction

The new CSPS interface allows you to immediately access information on parts through communication with the manufacturer. You can view availability and pricing, promotions, supersession information, notes about the part, and other general information. You can also finalize and submit orders, view open and submitted orders, cancel orders, process returns (buybacks), and view the backorder inquiry. This document provides an overview of all that is possible with the new CSPS interface.

## Part Inquiry

### Part Availability and Pricing

CSPS allows you to view a variety of information about CNH parts including part pricing and availability.

1.  Access the Parts Inquiry screen (Parts | Parts Inquiry), enter a CNH part number and click the Comms button. The Pricing Info screen opens allowing you to view pricing and availability of parts at CNH warehouses.

    > **UI Example: Pricing Info Screen**
    > - **Vendor:** CAS
    > - **Part #:** A10326
    > - **Description:** BALL JOINT
    > - **Pricing Details:** Shows List Price, Basic Disc, Net Price, Performance Disc, etc.
    > - **Availability:** Lists quantities at various warehouses (e.g., ATLANTA: 0, LEBANON: 149, DALLAS: 0).

    **Note:** The Customer View Opt (Security | OPT DIS Master Menu | Parts | Menu 8) allows you to control what price levels, if any, display on the screen.

If none of the CNH warehouses have the part available, the **Check Vintage Avail** button appears. Click this button to search for the part from another source.

### Promotions

When a sales promotion for a part is available, a button with the promotion code will display in the **Promo Offer** row.

1.  Click on the button to view the details about the promotion. The **Promotional Discount** screen opens.

    > **UI Example: Promotional Discount at Net Price Screen**
    > - **Promo:** 17NA000019
    > - **Description:** Seasonal Monthly Depot
    > - **Details:** Seasonal Monthly Depot Stock Order - one order per location per month. Minimum $15,000. 52-Def 1, Ext 3 month terms.

The information that displays depends on the type of promotion that was selected. There are 10 different types of promotions.

### Parts Supersession

You can view all supersession information about a part by clicking the **Sub Parts** button.

1.  Click the **Sub Parts** button on the Pricing Info or General Info screen. The Supersession screen opens displaying the available supersession parts. Click the **Fold/Unfold** button to view availability and notes for each sub part.

    > **UI Example: Supersession Screen**
    > - **Part #:** A10326
    > - **Description:** BALL JOINT
    > - **Table Columns:** Sub From, Description, Qty, Type, Back Note
    > - **Example Row:** K0275868, A10326, BALL JOINT, 1, S, N

The letter F or T displays on the availability line for each listed part, indicating whether the supersession parts are sub to or sub from.

### General Info

CSPS allows you to view general information about the specified part such as dimensions and weights.

1.  Click the **General Info** button while on the Pricing Info screen. The General Info screen opens allowing you to view the dimensions of the part and packaging information. Depending on the part, you can also click buttons to view product/model, kit, and remanufacturer details.

    > **UI Example: General Info Screen**
    > - **Part #:** A10326
    > - **Description:** BALL JOINT
    > - **Details:** Status, Haz Code, Return Code, PCC Description.
    > - **Weight, Dimensions, & Packaging:** Height (in), Length (in), Width (in), Weight (lbs), Pkg Qty.

    **Note:** The Kit and Reman buttons do not show unless there is something to display.

### Part Notes/Messages

If there is additional information about a part, it can be viewed by clicking the **Notes/Messages** button.

1.  Click the **Notes/Messages** button on the General Info screen. The Notes screen opens listing the part and any information provided by CNH about the part.

## Order Inquiry

Order Inquiry allows you to find information about open/submitted orders and returns (Buybacks).

1.  Select **Order Inquiry** from the Quantum main menu (Parts | Stock Order | Order Inquiry). The Current Order Headers screen opens.
    *   Click the **Mfr Inquiry** button to find information about submitted orders and buybacks.
    *   Click the **CSPS Open Orders** button to view information about open orders and buybacks.

If an order/return has a status of pending assigned in the Supplemental Order# column, the order or return has been assigned a CSPS order/buyback number, but has not been submitted.
**Note:** Supplemental orders that display on the right side of the Supplemental Order# column (right justified) are from CCN Web.

### Open Orders

1.  Select an open order/buyback from the Current Order Headers screen or provide the order information and click **Enter** on the Open Order Inquiry screen, the Open Orders screen displays.
2.  Highlight an order and click the **Select** button.
3.  A screen opens providing buttons to view **Part Lines**, **Service Levels**, and **Order Pricing Details**.

### Submitted Orders

1.  Select an order/buyback that has been assigned a CSPS# (Supplemental Order#) from the Current Orders Header screen or select **Order Status Inquiry** from the CSPS menu. The first Order Inquiry screen opens.
2.  Click **Enter** to continue.
3.  Select the order and click one of the available buttons to view part details, shipping information, or header details.

*   **Part Details:** If you click the **Part Details** button, the Order Details screen opens showing the parts on order. Press the **Fold/Unfold** button to display additional information (e.g., warehouse, ship date, status).
*   **Headers Detail:** If you click the **Headers Detail** button, a screen opens displaying the order summary. From here you can view the Service Levels or order pricing.
*   **Shipping Info:** If you click the **Shipping Info** button, the Parts Order Shipping screen opens displaying the parts being shipped from each warehouse with the expected ship date. Press the **Fold/Unfold** button to view additional information such as the dispatch note number and weight.
*   **Tracking:** If you click the **Tracking** button on the Parts Order Shipping screen, the most recent information provided by the carrier displays.
    **Note:** This may be a future option and not readily available.

## Finalize/Submit Order

1.  Select **Print/Finalize Order** from the Quantum main menu (Parts | Stock Order | Create Stock Order | Print/Finalize Order). The Order Information screen opens allowing you to provide information necessary to finalize/submit the order.
2.  Click inside the Order Type field and supply the order type or click **Order Type**. The Select Order Type Code screen opens.

    > **Order Types:**
    > - 50: BDA (Breakdown Assistance)
    > - 51: ULTRA
    > - 52: Unit Down
    > - 54: DSO
    > - 56: Stock order - Terms
    > - 57: Stock Order - Extended terms
    > - 58: Stock Order - Cash

    The first available order type (50) is BDA (Breakdown Assistance). If you select this option, the Breakdown Order (BDA) Details screen opens. Information is required in all fields except the ASIST Report# and Prev Part Ord# fields.

3.  Click inside the Delivery Addr field and type 1 (Dealership) or 990 (Ship-To Address). You can also click the **Delivery Addr** button and select one of the options from the Select Delivery Code screen.
4.  If an order is created from a dropship invoice, the POS Ship-To address will be used. If using a ship-to address, U.S. dealers may receive address corrections which can be used to insure proper delivery. Verify the address information on the One Time Ship-To screen and change if necessary. Click **Enter** if it is correct.
    **Note:** Select the **Use Address Correction** check box if you would like to use the address correction that was provided.
5.  If your dealership is close to a CNH warehouse and you would like to pick up the parts to save time and shipping costs, you can select the **Depot Pickup** check box.
    **Note:** This box must be checked for each order you would like to pick up.
6.  Enter any notes regarding the order in the **Order Notes** field.
7.  Enter any information that you would like printed on the shipment in the **Case Text** field.
8.  Enter any information that you would like printed on the invoice in the **Invoice Text** field.
9.  Once an order has been validated, you can check to see if parts may be able to be picked up directly from the supplier instead of the CNH warehouse. If this option is available, Y (Yes) will display in the DFS (Direct from Supplier) Pickup Avail field. Click the **View DFS Vendors** button. The DFS Pickup screen opens.
    *   Select the vendor and click the **Pickup** button to view the vendors where you can pick up parts.
    *   Click the **View Parts** button to view the parts available from each vendor. When ready, highlight each vendor and click the **Pickup** button to confirm you will be picking up the listed parts.

### Select Service Level

You can change the method of shipment from each warehouse. Only specific combinations of order type/delivery address will allow changing the service level.
**Note:** Service levels are dealer specific and don't need to be modified until the order has been validated.

1.  Click the **Service Levels** button on the Order Information screen. The Service Level Selection screen opens.
2.  Select a warehouse from the table and click the **Change Ship Code** button. The Change Service Level screen opens allowing you to select/remove a shipping option for parts from the selected warehouse.

### Large Orders

When a large order (currently an order of 100 lines or more) is validated, a message appears stating that the order is large.

Large orders take extra time to process. You can exit and come back later or stay on the screen and press the **Retrieve Details** button to see if CNH has finished processing the order. This process can take several minutes and involve pressing the **Retrieve Details** button more than once. If you come back later, you will still need to click the **Retrieve Details** button.

If you click the **Retrieve Details** button, two different messages appear:
*   **Order data being retrieved** – this message appears after clicking the Retrieve Details button.
*   **Order processing in progress** – This message appears if CNH hasn't finished processing the order.

When the order is ready to be reviewed and checked for errors or promotions, additional buttons such as the **View Avail Promos** button may display.

### Part Message Information

If a message regarding the order is generated when the order is validated, you may see a message at the bottom of the screen stating *Part Warnings or Errors Exist*.
**Note:** If a CSPS number has been assigned and you need to change the order type or delivery address, use the **Cancel CSPS Order** button.

Click the **Part Lines** button. The Order Details screen opens allowing you to view the messages for the parts ordered.

If there is a message to be reviewed, the letter E or W will display in the MSG column. Select the part and click the **Messages** button. If you just want to view error messages that prevent the order from being submitted, click the **Errors** button.

1.  An **E** designates an **Error** message that will stop the order from being submitted. Instances that might generate an Error message would be if the part was invalid or was a Conditional substitution.
2.  A **W** designates a **Warning** message. While these types of messages do not stop the order from being submitted, they should be examined.

### Substitutions

If substitution parts are available, they can be viewed on the Order Details screen.

1.  Click the **Part Lines** button on the Order Information screen. The Order Details screen opens.
2.  If a substitution part is available for a part on the order, the substitution part number will be listed in the **Sub Parts** column. To view additional details about the substitution parts, click the **Manage Subs** button. The screen that opens depends on whether it is a Simple Sub or a Conditional Sub.

*   **Simple Substitution:** If the substitution part is a Simple substitution, it will not require additional input. CNH will automatically substitute the part (whether single or multiple) when the order is filled.
*   **Conditional Substitution:** If the part substitution is conditional, you will have to accept one of the listed sub parts. This must be done for every conditional substitution on the order. Click the **Fold/Unfold** button and view the additional information provided, then make the part selection. Select one of the parts and click the **Accept** button. If none of the sub parts are accepted, the order cannot be submitted.

### BOAT (Back Order Available Tool) Information

This option shows additional information on a backorder that helps determine when the part may be available in the warehouse.

1.  Select any back ordered part, then click the **BOAT Info** button. The Back Order Availability screen opens. The part number, status, quantity, and Estimated Ship Date (if there is one) display. Click **Cancel** to return to the previous screen or **Backorder Cancel** to cancel the back order.

### Pricing

There are two different types of pricing that can be seen on an order:

1.  **Order Pricing** – Accessed by clicking the **Pricing** button on the Order Details screen. This screen shows any discounts as well as other expenses such as freight.
2.  **Part Line Pricing** - Accessed by clicking the **Fold/Unfold** button while on the Part Lines-Pricing screen. This screen shows additional discounts and percentages for each part line.

### Promotions

Promotions may be available on certain order types. Promotions can be seen through one of these two methods:

1.  While on the main Finalize Order screen, click the **View Avail Promos** button. The Header Promos screen opens. Select a promotion from the table and click the **Promo Details** button. A screen opens listing all of the parts available for the promotion.
2.  You can also view the promotion at the part level on the **Part Lines** screen. When a Y is listed in the Pro column, it means that there is a promotion available for the part. Select the part and click the **Promos** button. The Promo Lines screen opens. Select a promotion and click the **Promo Details** button. The Promo Lines screen populates with information regarding the promotion.

**Note:** certain promotions require that a dollar amount be met before the order can be submitted.

### Corporate Orders

There are restrictions that affect orders and corporate orders.

*   If a stock order has been validated at least once it can't be added to a corporate order unless the CSPS order is cancelled.
*   If an order is part of a corporate order it can't be finalized and validated as a separate order.

## Canceling Orders

1.  Once an order has been placed, you can cancel it unless it is attached to a corporate order (Parts | Stock Order | Cancel Order). If it is on a corporate order, this message will display:
    > Order is on Corporate Order and cannot be cancelled
    Remove the order from the corporate order and it can be cancelled.
2.  If an order has been validated but not submitted, a screen displays when you try to cancel the order, asking to "Continue and cancel CSPS Open Order?".

## Buybacks (Returns)

Processing Buybacks is similar to finalizing orders as you select the Buyback type and validate it.

1.  Select **Print/Finalize Return** from the Quantum main menu (Parts | Stock Return/Phase-out | Print Finalize Return).
2.  On the Print/Finalize Return screen, enter the CNH vendor code, return number, and select the Finalize check box. The Buyback Information screen opens.
3.  Enter the Buyback type in the field provided or click the **Buyback Type** button and select it from the list that appears.
4.  If the Buyback shows a status of *Not Valid*, click the **Part Lines** button and review the part lines for messages. Blocking messages prevent Buybacks from being submitted while Warning messages do not. Review messages and take corrective actions as necessary.

## Backorder Inquiry

Backorder Inquiry allows the you to view outstanding backorders and cancel them if desired.

1.  Select **Backorder Inquiry** from the Quantum main menu (Manufacturers | CSPS Comm Menu | Backorder Inquiry). The Backorder Inquiry Selection screen opens.
2.  Supply your CNH vendor code and any other parameters for orders such as a timeframe for outstanding backorders, then click **Enter**.
3.  The Backorder Cancel screen opens displaying all of the backorders that fall within the parameters that you specified. You can select one or more items on the order and cancel them by clicking the **Submit** button. The Backorder Cancel screen opens displaying the parts you are cancelling.
4.  Click the **Confirm Submit** button.
5.  The parts that you selected to cancel now have a status of **Cancelled**.
6.  When you click the **Back** button, the Backorder Cancel screen re-opens showing all of the parts on the order. Those that were cancelled, now show the status of Cancelled.

## Reset CSPS Password

CSPS allows you to change your CSPS credentials or BDA order defaults.

1.  Select **Electronic Commerce Configuration** from the Quantum main menu (Security | Electronic Commerce | Electronic Commerce Configuration).
2.  Click the **Change Credentials** button. The **Reset Password** button displays.

The password is automatically changed every 55 days (checked during parts EOD) because CNH requires it to be changed every 60 days, but you can change it at any time. Click the **Reset Password** button.

Click the **Reset Password Now** button. The system will lock other users from doing any transactions until the reset has completed.
**Note:** when you change the password using this option, it also changes the password for the CSPS portal.


title: "Customer_360_1"
source: "Customer_360_1.pdf"
tags: ["Customer 360", "Quantum", "Customer Information", "CRM", "Sales", "Reporting", "DIS", "Point of Sale", "Customer Management"]
version: "1.0"
last_updated: "2024-05-23"
short_description: "A guide to using the Customer 360 feature in the Quantum software. It details how to search for customers, view comprehensive customer data, and perform actions like creating calls, documents, and payments from one centralized location."
long_description: "This document provides a detailed walkthrough of the 'Customer 360' feature within the DIS Quantum software. Customer 360 is a powerful, centralized hub for accessing all customer-related information and functionalities. The guide covers how to initiate a customer search using various criteria like name, phone number, or associated data through the Quantum Search. It explains the different sections of the Customer 360 dashboard, including customer balance, call history, overall sales ranking, and contact information. The document also describes the interactive graphs that visualize customer interactions, such as equipment owned, parts on order, open documents, and rental history. For each section, it outlines the specific actions users can perform, such as creating sales calls, receiving payments, viewing part availability, creating quotes, and editing contact details. Additionally, it provides instructions on how to customize data tables (sorting, filtering, reordering columns) and export data to a spreadsheet. The purpose is to equip users with the knowledge to efficiently manage and interact with customer data from one unified interface, improving workflow and customer service."