---
title: "Prevent Sales Below Margin"
source: "combined_Keyston.md"
tags: ["Keystone"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Prevent Sales Below Margin."
long_description: "This document provides information about Prevent Sales Below Margin from the DIS Keystone system."
---

## Introduction
Keystone allows you to set options that require salespeople to provide a password in order to sell a part or unit below margin. This document covers how to set the available options, setup the margin percentages and passwords, process a sale below margin in Invoicing, and automatically or manually print the Sale Below Margin report.

## Set Options to Prevent Sales Below Margin/Print Report
There are two options pertaining to the Prevent Sales Below Margin option.

1.  Access **Point of Sale OPT Menu Eighteen** in Keystone (`Security | OPT DIS Master Menu | Point of Sale | Click the Next Arrow until you reach Menu 18`).

    **OPT POINT OF SALE MENU EIGHTEEN**

    *   **Prevent Sale Below Margin**
        1.  Prevent Sale Below Margin is not installed.
        2.  Prevent Sale Below Margin is installed.

    *   **Sale Below Margin Report**
        3.  Do not print Below Margin Report at EOD
        4.  Print All Below Margin attempts at EOD
        5.  Print Below Margin Overrides only at EOD

    *   **Timeclock Work Order Default Values**
        6.  Do not display the work order default value screen
        7.  Display work order default value screen if work order
        8.  Display work order default value screen if work order or sales order but not quote

2.  Type the number `2` in the **Enter Option Number** field at the bottom of the screen and click **Enter** to turn the OPT on.

3.  Enter option `3`, `4`, or `5` and click **Enter**. You can select to not print the report or print it at the end of day. You can print all attempts to sell below margin or just those that were successful.
    > **Note:** You can manually print this report at any time. Instructions are in the last section of this document.

## Set Margin Percentages and Password
You must provide the margin percentage to use when calculating the price at which the security gate feature displays and the password to use to get past it. Set the Parts and Units Margins separately.

1.  Select **Sales Margin Maintenance** from the Keystone main menu (`P.O.S. | Table Maintenance | Sales Margin Maintenance`). The top fields of the Sales Margin Maintenance screen display.

2.  Select the **All Vendors** check box or provide a specific vendor code to set margins for their parts.

3.  Select the **All Classes** check box or provide a specific class code to set margins for the parts of that class.

4.  Click **Enter**. The Sales Margin percent fields and text display at the bottom of the screen. The fields include:
    *   **Current Record**
    *   **Sales Margin percent:** (0-99.99 percent)
    *   **Upper Limit percent:** (100.00-999.99 percent, 999.99=no limit)

5.  Supply the minimum sales margin percentage a part can be sold at before the salesperson will need to pass through the security gate. Supply an upper limit percentage if desired.

6.  Click **Enter**. Repeat Steps 1-6 for any additional vendors/classes if you are setting sales margin percentages for specific vendors/classes.

7.  Set the Unit Sales Margin Percentage for all Makes and Models or specific Makes/Models using the same process that you used for Parts. Click **Enter** when you have finished.

8.  Click the **Maintain Password** button.

9.  The **Password Maintenance** screen opens.

    *   **Parts override password:** [text field]
    *   **Allow part cost to display** [checkbox]
    *   **Units override password:** [text field]
    *   **Allow unit cost to display** [checkbox]

10. Supply an override password for both part and unit sales that fall below the set sales margin percentage.

11. Unselect the **Allow part/unit cost to display** checkboxes if you do not want to reveal the cost of the part/unit to the salesperson.

12. Click **Enter** to save.

## To Process Sale Below Margin
When a salesperson attempts to sell a part below margin in Invoicing, the **Sale Below Minimum Margin** screen/gate will display.

This screen shows the following details:
*   **Customer:**
*   **Document:**
*   **Part Ven:**
*   **Class:**
*   **Part#:**
*   **Minimum Sale:** (calculated amount)
*   **Sale amount:** (amount entered by user)
*   **Enter password:** [password field]
*   **Authorized by:** [text field]

Follow these steps:
1.  Enter the password in the field provided.
2.  Enter the name of the person who provided the password in the **Authorized by** field. The name provided in the Authorized by field will display on the Sales Below Margin Report.
3.  Click **OK**.

## To Manually Run Sale Below Margin Report
While you can set an option to automatically run a Sales Below Margin Report during the End of Day procedures, you can also manually run the report at any time.

1.  Select **Sales Below Margin/Cost Report** from the Keystone main menu (`P.O.S. | Table Maintenance | Sales Below Margin/Cost Report`). The Sales Below Margin/Cost screen opens.

2.  Select the information that you would like to include on the report and how you would like it to be sorted.
    *   **Include:**
        *   Parts
        *   Units
        *   Both
    *   **Include Below Margin:**
        *   Overrides
        *   All Attempts
    *   **Sort by:**
        *   Address/Document/Part or Unit
        *   Vendor & Part/Make & Model

3.  Provide a **Starting** and **Ending** date using the MMDDYY format or click the calendar icons at the end of each field and select the date.

4.  Click **Enter** to run the report.

## Related Articles (Click to View):
*   Prevent Sales Below Cost
*   Prevent Sales Below Customer Price


title: "Reassign Button in POS Invoicing"
source: "Reassign_Button_in_POS_Invoicing.pdf"
tags: ["POS Invoicing", "Reassign Document", "Work Order", "Sales Order", "Keystone Software", "DIS", "Customer Management", "Point of Sale"]
version: "1.0"
last_updated: "2024-01-18"
short_description: "A guide on how to use the 'Reassign' button in the DIS Keystone POS Invoicing module to correct open sales or work orders assigned to the wrong customer or unit."
long_description: "This document provides a step-by-step tutorial for the 'New Reassign Button in POS Invoicing' feature within the DIS Keystone software. It is intended for users who need to correct errors on open sales or work orders, such as an incorrect customer or unit number, without recreating the entire document. The guide explains how to open an existing work order, use the 'Reassign' button, and navigate the 'Reassign Point of Sale Document' screen. It covers options for assigning a new customer address, keeping the same document number or assigning a new one, and refreshing part and labor prices based on the new customer's pricing tables. Additionally, it details how to retain or remove existing discount codes during the reassignment process. The document includes descriptive references to screenshots to visually guide the user through each step, from locating the button to confirming the changes."