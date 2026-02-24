---
title: "Convert Part Prices from U.S. to Canadian"
source: "combined_Keyston.md"
tags: ["Keystone"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Convert Part Prices from U.S. to Canadian."
long_description: "This document provides information about Convert Part Prices from U.S. to Canadian from the DIS Keystone system."
---

## Introduction
When part pricing data from a US vendor is listed in US prices, the price book can be converted to reflect current Canadian prices. This procedure will need to be repeated each time a new price book is downloaded or any time the exchange rate changes.

## To Change Pricing:
1.  Select **Configure Vendor/Class** (Parts | Parts Configuration | Configure Vendor/Class). Set the pricing factors at the bottom of the screen AS IF the price book is using current Canadian pricing.
2.  Download the US price book file from your WebLocker and create the price book as you normally would.
3.  Select **Display/Print/Change Price Book** (Parts | Price Update/Part Lists | Display/Print/Change Price Book). The Price Book Selection screen opens.

    > **UI Screenshot: DISPLAY/PRINT/CHANGE PRICE BOOK - Price Book Selection**
    > This screen displays a list of available price books with columns for Price Book, Description, Update Status, and Creation Date. The options to "Display," "Print," "Change Single Part," and "Change All Parts" are available.

4.  Select the price book that you would like to change and click the **Change All Parts** button.
5.  The Change Price Book screen opens.

    > **UI Screenshot: DISPLAY/PRINT/CHANGE PRICE BOOK - Change: IMPERIAL**
    > This screen allows for applying percentage-based changes to different price categories.
    > - **Price Categories:** Dlr.List, Sug.List, Internal, Dir.Net
    > - **Note:** "The percentage fields have two implied decimal positions. To increase prices by 5.25% enter 10525. To decrease prices by 5.25% enter 9475."
    > - **Warning:** "Changes made here affect all file sets"

6.  Type the current exchange rate (1.4200% in this example, entered as `14200`) in the **Sug List** and **Dlr Net** fields and click the **Submit Change** button.

## Reprice Parts Already in Inventory:
While the instructions on the first page will change the prices for all parts ordered thereafter, you will need to follow these instructions to change the parts already in inventory.

1.  Print a **Parts Inventory Pad Summary** (Parts | Parts Reports | Parts Inventory Pad (Print Summary check box selected)) for the vendor whose parts you would like to reprice.
2.  Select **Automatic Update from Price Book** (Parts | Price Update/Part Lists | Automatic Update from Price Book). The Automatic Price Update screen opens.

    > **UI Screenshot: Automatic Price Update - From Price Book**
    > - A field is provided to enter the `Vendor code`.
    > - **Warning:** "If you continue, this job will require the exclusive use of this session until the update has completed."

3.  Type the vendor code for the vendor of the parts you would like to reprice and click **Enter** (The green check mark). The Automatic Price Update - Supersession screen opens.

    > **UI Screenshot: Automatic Price Update - Supersession**
    > This screen provides options for handling supersession data from the price book.
    > - **Question 1:** "If the price book contains manufacturer supersession information, should this be used to replace any dealership-supplied supersession for the vendor?"
    >   - **Option:** "Yes. Checking this box will allow supersession information from the price book to overlay supersession information that you may have manually entered at Parts Posting and Maintenance."
    > - **Question 2:** "If a part currently has no dealership-supplied supersession, but supersession information is found in the price book, should this information be added to that part?"
    >   - **Option:** "Yes. Checking this box will allow supersession information from the price book to be added to a part that previously had no supersession information."
    > - **Note:** "If the price book does not contain supersession information, the answers to these questions do not matter."

4.  Make your selections for the supersession options and click **Enter** to update the prices of parts in inventory.
5.  Print another Parts Inventory Pad Summary to record the inventory valuation change for accounting purposes.


title: "Inquire/Update Reservations with Direct Fill"
source: "Direct_Fill_Part_Reservations.pdf"
tags: ["Keystone", "DIS", "Parts", "Reservations", "Direct Fill", "Stock Order", "Inventory Management", "POS", "Invoicing"]
version: "1.0"
last_updated: "2024-05-23"
short_description: "A guide on using the Direct Fill option in the Keystone system to manually fill reserved parts from on-hand inventory, bypassing the standard order-receipt process."
long_description: "This document provides a step-by-step guide for the 'Inquire/Update Reservations with Direct Fill' feature within the Keystone software. The Direct Fill option allows users to force-fill reserved parts from on-hand inventory, which is useful when priority orders need to be fulfilled before their designated stock order arrives. The guide details how to navigate to the 'Inquire/Update Reservation Priorities' screen, identify parts that are ordered but can be filled from available stock, and execute the fill process. It covers selecting the part, specifying the quantity to fill, and confirming the action. The process concludes by illustrating how the part's status is updated on the Point of Sale (POS) invoice, where the priority code changes to reflect its new 'available' status."