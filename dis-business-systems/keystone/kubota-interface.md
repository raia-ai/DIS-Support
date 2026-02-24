---
title: "Kubota Interface"
source: "combined_Keyston.md"
tags: ["Keystone"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Kubota Interface."
long_description: "This document provides information about Kubota Interface from the DIS Keystone system."
---

## Introduction

The Kubota Interface allows you to view part availability, place part orders, work with Kubota payables invoices, create orders using DBS codes based on material groups, and view quotes. A brief description of each option is provided below. Click on any option (blue text) to go to the section in this document that details its capabilities and functions:

-   **Kubota Part Availability** - Allows you to view part information as well as part availability at specific warehouse locations.
-   **Kubota Parts Locator** - Allows you to submit your available part quantities for posting on the Kubota website and view available part quantities at other dealerships.
-   **Kubota Part Orders** - Lets you configure the shipment, place the order, and track its delivery.
-   **Kubota Material Groups/Part Categories** - Part Categories are created from Kubota Material Groups. You can use these Part Categories to create suggested stock orders for Kubota parts.
-   **Kubota Invoicing** - Only available in Quantum.
-   **Integrated Kubota Quote** – Only available in Quantum.

## Kubota Part Availability

### To View Part Availability

There are two ways to check part availability:

1.  Select **Parts Inquiry (Parts | Parts Inquiry)**.
    -   Type the vendor code for Kubota into the Vendor field and enter the part number for the part whose availability you would like to check.
    -   Click the **Comms** button.

2.  Select **Invoicing (P.O.S. | Invoicing)**, select your printer, click Enter, and click the **Part Availability** button on the Point of Sale – Invoicing Entrance screen.
    -   The Part Availability - Inquiry screen opens.
    -   Click inside the Part column, type the part number for the part to check availability on, and click the **Mfg Inq** button.

The Kubota Communication screen opens displaying part information and availability.

## Kubota Parts Locator

Parts Locator allows you to locate Kubota parts at other dealerships, the quantity they have available, and their phone number. Dealers who are closest to your location will be listed first.

This option also allows you to submit your Kubota part inventory to be posted on the Kubota website and the DIS business system. After configuration, your system will submit a new file containing your Kubota part inventory every night your DIS backup is run.

> **Note:** If the file submission fails during backup, the system will attempt to submit it again at 9:00 a.m. the following morning.

### To Locate Dealers with Available Parts

1.  Click the **Locator** button on the Kubota Communication – Part Availability screen (accessed through instructions in previous section).

The Kubota Communication – Dealer Locator screen opens listing dealers with the part, the quantity available, their contact information and the last time they submitted their part information.

## Kubota Part Orders

### To View Pre-Edit Options

The pre-edit option provides you with information including ship-to locations, depot availability, and various messages such as discounts. This information allows you to make an educated decision on the best shipping method. Access this option through the Parts or P.O.S. menu as shown below.

1.  Select **Order Inquiry (Parts | Stock Order | Order Inquiry)**. The Order Inquiry - Current Order Headers screen opens.
    -   Click on the order in the table and then click the **Pre-Edit** button.

2.  Select **Priority Orders (P.O.S. | Priority Orders)** and double-click on the Kubota order in the table.
    -   The Priority Orders – Update Lines screen opens. Click the **PreEdit** button.

The Pre-Edit Parameters screen opens.

3.  Enter the Order Type into the field provided or click **Order Type** and double-click the order type from the Select Order Type Codes screen (see below).

4.  Select the **Show Availability** check box on the Pre-Edit Parameters screen and click **Enter**. The Order Pre-Edit screen opens displaying shipping information and other messages.

### To Finalize Order

Once the order has been created, you will need to finalize it.

1.  Select **Print/Finalize Order (Parts | Stock Order | Create Stock Order | Print/Finalize Order)**.
    -   The Print/Finalize Order screen opens.
    -   Type the order number into the field provided, select the **Finalize** check box and click **Enter**.
    -   The Print/Finalize Order – Order Information screen opens with the default fields filled in based on your dealer number.

2.  Verify that the Ship To Address is correct. If you are drop-shipping or need to change the address for another reason, click inside the field and type over the existing text.

3.  Click the **Validate** button on the Print/Finalize Order - Order Information screen.
    The Order Validation screen opens displaying information such as order minimum, correct order type with parts, whether or not a single shipment warehouse is available or warnings.

4.  After you have validated the order, click the **Back Arrow** to return to the Print/Finalize Order - Order Information screen.
    -   If you altered the Ship To Address, a corrected address appears on the right side of the screen. Select the **Use Corrected Ship To Address** check box to use the corrected address information.

The **View Messages** button appears allowing you to view the messages that appeared in the order validation screen.

### To Select Shipment Method and Change Order Quantities

You can change the way a whole order is shipped, the way a single part is shipped, or select to ship from a single warehouse if all parts on the order are available from that warehouse. Additionally, you can change the quantity of a part ordered or remove a part from the order.

**Change Shipping Method for Whole Order**

1.  Click **Ship Via** on the Print/Finalize Order - Order Information screen.
    -   The Select Ship Via Code screen opens. Choose an option from the table and click **Select** to have the whole order shipped via this method.

**Change Shipping Method for Individual Part**

1.  Click the **Change Part Shipping** button on the Print/Finalize Order – Order Information screen (**Parts | Stock Order | Create Stock Order | Print/Finalize Order**).
    The Print/Finalize Order – Override Shipping screen opens displaying the current shipping method for the parts on order.

2.  Click in the shipment field for the part that you would like to change the shipment method for, then click the **Ship Via** column header.
    The Select Ship Via Code screen opens. Choose an option from the table and click **Select** to have the individual part shipped via this method. Click **Enter** to save changes.

**Change Order Quantity or Remove Part from Order**

1.  While on the Override Shipping screen, you can change the quantity of a part that you order by clicking on the number listed below the quantity header and changing it to the quantity that you would like to order.
    **OR**
2.  You can remove a part from the order by changing the order quantity to zero.
    -   When you click **Enter**, the quantity ordered will be updated or the order line will be removed from the order depending on what the Qty was changed to.
    -   Click the **Back Arrow** to return to the Order Information screen. Click the **Validate** button and re-validate the order.

**Ship from Single Warehouse**

If all of the parts and quantities are available from any single warehouse, The Single Shipping Warehouse field and text will display on the Print/Finalize Order screen allowing you to ship from a single warehouse and potentially reduce shipping expenses.

1.  Click **Single Shipping Warehouse** while on the Order Information screen.
    The Select Warehouse Code - Single Shipment Available screen opens displaying the codes for available warehouses.

2.  Click on the warehouse code for the warehouse that you would like to use, then click the **Select** button.

### To Transmit Order

Once you have all of the options set the way you would like and have validated the order, the final step in the order process is transmitting the order to Kubota.

1.  Click the **Transmit Order** button on the Print/Finalize Order – Order Information screen.

The Print/Finalize Order - View Order Messages screen opens with a message from Kubota confirming the order has been accepted. The total price for the order is listed as is the Order Confirmation number.

### To Check Order Status

After the order has been placed and accepted, you can check on the status and track the order.

1.  Select **Kubota – Parts Order Status (Manufacturers | Kubota | Parts Order Status)**. The Kubota Communication – Order Inquiry screen opens.

2.  Type the Order Number in the field provided or click **Order Number** and select the order from the list that appears or supply information for any of the available parameters and click **Enter**.
    The Kubota Communication - Parts Order Status screen opens displaying information about the order, including all of the parts on the order, the quantity of the parts being shipped, the ship date, warehouse it is being shipped from, and the tracking number.

3.  Click the **Show Tracking** button on the Kubota Communication – Parts Order Status screen to connect directly to the shippers website and view the current tracking detail.

You may also check the status of an order by clicking the **Order Status** button on a Kubota Communication screen.

## Kubota Material Groups and Part Categories

Part Category assignments are created based upon Kubota material groups. Part Category assignments are made and updated every time the Kubota price update is run. Part Category codes can be viewed through Parts Inquiry – Information and used to generate Kubota suggested stock orders.

### To View Part Category Assignments

1.  Select **Parts inquiry (Parts | Parts Inquiry)**. The Parts Inquiry - Information screen opens.
2.  Provide the Kubota part number, select the Order Information tab, and click **Enter**. The Part category code displays.

### To Create a Kubota Suggested Stock Order

1.  Select **Create Suggested Stock Order (Parts | Stock Order | Create Stock Order | Create Suggested Stock Order)**. The Create Suggested Stock Order screen opens.

2.  Enter your dealership defined Kubota code in the vendor field and click **Enter**.
    The second Create Suggested Stock Order screen opens.

3.  Enter the material group DBS code in the Select by part category field, select the **Include** option and Click **OK** to generate the suggested stock order.

See the following page for a table of Kubota Material Groups and their corresponding DBS codes.

### Current Material Groups

| Current Material Groups | DBS Code |
| ----------------------- | -------- |
| TOOLS                   | 1        |
| PAINT                   | 2        |
| BKT TEETH               | 3        |
| HOSE DS                 | 4        |
| CUT EDGE                | 5        |
| HYD CYL                 | 7        |
| LINKAGE                 | 8        |
| PLUGS                   | 9        |
| CHEMICALS               | !        |
| BATTERIES               | #        |
| PUMP/GEN                | %        |
| TIREDS                  | &        |
| TOOLBOXES               | *        |
| ACCESSORY               | A        |
| BLADE                   | B        |
| BELT                    | C        |
| FASTENERS               | D        |
| FILTER                  | F        |
| GASKETS                 | G        |
| HOSES                   | H        |
| APPARELDS               | I        |
| TIRE                    | J        |
| HAYTOOL                 | K        |
| ROLLERS                 | L        |
| MERCH DS                | M        |
| BATTERYDS               | N        |
| PARTS                   | P        |
| PARTS CE                | Q        |
| RUBTRK DS               | R        |
| TWINEDS                 | S        |
| TOYS                    | T        |
| RUB TRACK               | U        |
| BEARING                 | V        |
| WHEEL                   | W        |
| ELECTRIC                | X        |
| HARDWARE                | Y        |

### New Material Groups

| New Material Groups | DBS Code |
| ------------------- | -------- |
| OIL                 | O        |
| REPL-ENG            | E        |
| BULK OIL            | @        |
| FIXTURES            | Z        |
| CHAINS DS           | 6        |


title: "Cleanup Make/Model Table Entries"
source: "Make_Model_Table_Cleanup_-_Keystone.pdf"
tags: ["Keystone", "Make/Model Table", "Data Cleanup", "Merge Units", "Inventory Management", "System Administration", "DIS"]
version: "1.0"
last_updated: "2024-05-23"
short_description: "A guide on how to clean up and merge duplicate or incorrectly entered Unit Makes and Models within the Keystone system. It covers the process for merging both Makes and Models to ensure data consistency."
long_description: "This document provides step-by-step instructions for system administrators and users of the Keystone software, developed by Dealer Information Systems (DIS). The primary focus is on data maintenance within the Make/Model Table. Unit Makes and Models are often entered with slight variations or misspellings (e.g., \"KUBOTA\", \"KUBOATA\", \"KUBTA\"), which can lead to inaccuracies in inventory and customer unit records. This guide details two main procedures: merging unit Makes and merging unit Models. The \"Merge Unit Makes\" section explains how to select a standard Make and merge all its variations into the correct one. The \"Merge Unit Models\" section outlines a similar process, but it involves deleting a redundant model and reassigning its associated units to the correct model under the correct make. The document includes screenshots and notes to clarify the process, ensuring that users can effectively clean up their data, leading to more accurate reporting and streamlined operations."