---
title: "Parts Physical Inventory Procedures without Group/Van"
source: "combined_Keyston.md"
tags: ["Keystone"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Parts Physical Inventory Procedures without Group/Van."
long_description: "This document provides information about Parts Physical Inventory Procedures without Group/Van from the DIS Keystone system."
---

## INTRODUCTION

The following instructions cover the process of conducting physical inventory without the Group/Van option. These instructions are split into three sections to be completed before, during, and after taking inventory and should be completed in the order that they are listed. Once you have completed the instructions in a section, you do not need repeat the instructions until the next time that you conduct physical inventory.

## INSTRUCTIONS

### Complete These Steps Before Taking Inventory:

1.  **Select the On-Hand Quantity Report** from the Keystone menu (`Parts | Parts Reports | On-Hand Quantity Report`) or (`Menu X36, option 5`).
    On the screen that opens:
    - Leave the **All** check boxes selected in the Vendor Code and Class sections.
    - Leave the Group section blank.
    - Click **Enter**.
    - Type `-999999999` in the Low on Hand field and `-1` in the High on Hand field.
    - Click **Enter**.
    - Correct any negative on-hand quantities that you find in the On-Hand Quantity Report.

2.  **Verify parts have bin locations.** Select the Bin Location Range Report from the Keystone menu (`Parts | Parts Reports | Bin Location Range Report`) or (`Menu X36, option 14`).
    On the screen that opens:
    - Leave the **All** check boxes selected for the Vendor and Class sections.
    - Leave the From and To Bin Locations blank.
    - Select the **Report all blank locations with Available Quantity** check box.
    - Click **Enter**.
    - If you find unassigned bin locations, make note as they will be fixed in Step 5.

3.  **Verify all parts have prices.** Select the Net or List Price Missing Report from the Keystone menu (`Parts | Parts Reports | Net or List Price Missing Report`) or (`Menu X36, option 3`).
    On the screen that opens:
    - Leave the **All** check boxes selected for the Vendor and Class sections.
    - Select the **Include Superseded Parts** check box.
    - If the Case/New Holland Marketing Codes OPT is turned on, the **Include MFR marketing codes** check box will display. Select the check box if you would like the report to show CNH marketing codes.

4.  **Both Parts and P.O.S. End of Month procedures must be run for the most efficient results.** You only need to run the End of Month procedures once, even if you are performing inventory for multiple divisions, as the re-organization process will automatically include all divisions.

    a) Select **Parts End of Month Procedures** from the Keystone menu (`Parts | End of Month Procedures`) or (`Menu X3, option 10`). This requires a dedicated system.
    On the screen that opens:
    - Leave the **Date of oldest order history to keep** field blank.
    - Click **Enter**.

    b) After you have run Parts End of Month, Select **POS End of Month** from the Keystone menu (`POS | POS End of Month`) or (`Menu X5, option 4`). This requires a dedicated system.
    On the screen that opens:
    - Click the **Division (_) only** button.

5.  **Consider fixing bin locations that were entered incorrectly.** For instructions on getting a DataMine of all bin numbers, click here. Confirm that all bin locations are valid and fix those that are not by completing the following steps:
    - Examine the report and find any bins that were entered incorrectly, such as A2 instead of A-2.
    - If you find bin assignments that need to be corrected, press **Alt** and **A** on the keyboard while Keystone is open.
    - In the AS/400 Command Line, type `PFBIN` and click **OK**.
    - The Change Bin Location screen opens. Type in the existing (incorrect) bin location such as A2 in the example above and type the New (correct) bin location A-2. Click **Enter**.
    - Repeat as necessary.

6.  **Find open counter tickets and work orders** by selecting the Work-In-Process Report from the Keystone menu (`POS | POS Reports | Work-In-Process Report`) or (`Menu X56, option 5`).
    On the screen that opens:
    - Leave the **All** check box selected in the Documents section.
    - Leave the **Repair Orders** and **Counter Tickets** check boxes selected.
    - Select the **Document Detail** check box.
    - Select the Sort by option of your choice.
    - Click **Enter**.
    - Close as many tickets as possible.

7.  **Select Parts Inventory Freeze** from the Keystone menu (`Parts | Parts Inventory Adjustment | Parts Inventory Freeze`) or (`Menu X33, option 4`). This requires a dedicated system in ALL Divisions.
    - Run this procedure in each division to be counted. This will be used after the count is done for the Parts Inventory Variation Report which will list discrepancies and adjustment amounts by part.
    > **Note:** If you are going to shut down all parts activity while counting inventory, the Inventory Freeze file should be run after the parts activity has stopped, and not run again until inventory is completely finished.

8.  **Select Parts Inventory Pad** from the Keystone menu (`Parts | Part Report | Parts Inventory Pad`) or (`Menu X36, option 1`).
    On the screen that opens:
    - Leave the **All Vendors** and **All Classes** check boxes selected.
    - Click **Enter**. The second Parts Inventory Pad screen opens.
    - Unselect the **Print Detail** check box.
    - Click **Enter**. The Time Delay – Parts Inventory Pad screen opens.
    - Click the **No Delay** button.
    - You can compare it with an "after inventory" report to calculate the change in inventory value after adjustments.

### Complete These Steps When Taking Inventory:

1.  **Select the Parts Inventory Adjustment Report** from the Keystone menu (`Parts | Parts Inventory Adjustment | Parts Inventory Adjustment Report`) or (`Menu X33, option 2`).
    On the screen that opens:
    - Select **Bin** for Sequence of report.
    - Select whether to Print available quantity or Print on-hand quantity.
    - Select whether you would like to print the report double spaced or not and the number of copies that you would like printed.
    - Click **Enter**.
    - Type `A` in the **From** field in the Bin Location section.
    - Type `99999999` in the **To** field in the Bin Location section.
    - Select whether or not to start a new page after each bin.
    - Select Compress or Expand for a Bin sort sequence:

| If You Select Compressed: | If You Select Expanded: |
| :--- | :--- |
| The report will sort and list bin locations from left to right by each character in the bin location. If you had the bin locations: AA1, AA2, AA11, AA22, AB1 – They would be listed in this order:<br>AA1<br>AA11<br>AA2<br>AA22<br>AB1 | The report will sort and list bin locations letters first, then numbers. Bin locations must begin with letters, end in numbers, and not mix. If you had the bin locations AA1, AA2, AA11, AA22, A1B – They would be listed in this order:<br>AA1<br>AA2<br>AA11<br>AA22<br>AB1 |
| This is the most commonly used method as it sorts and lists the bin locations as they were entered into the system and does not separate bin locations by letters and numbers like the expanded method does. | You **CANNOT** use this method if bin locations have mixed letters and numbers. A bin location of A-1A would be reconfigured and then sorted and listed as AA-1. Characters other than letters and numbers are ignored in sorting and listing. |

    - Select whether or not to start a new page after each bin.
    - Click **Enter** to print the report.

2.  **Count part quantities in inventory.**

### Complete These Steps After Inventory Has Been Taken:

1.  **Adjust part quantities** by selecting Parts Inventory Adjustment from the Keystone menu (`Parts | Parts Inventory Adjustment | Parts Inventory Adjustment`) or (`Menu X33, option 1`).
    On the screen that opens:
    - Type in the bin location that you would like to begin inventory adjustment with or type in the letter `A` to start from the first bin.
    - Select whether to display the Available quantity or On-hand quantity.
      > **Note:** Make the same selection as you did previously.
    - Click the **Next Arrow** on the Keystone tool bar.
    - The second Parts Inventory Adjustment screen opens displaying the Vendor, Part Number, and Description for the first part assigned to this bin.
    - Verify the quantity in the On hand/Available field.
        - If the quantity is correct, click **Enter**.
        - If the quantity is incorrect, click in the field and type in the correct quantity, then click **Enter**.
    - The part information for the part assigned to the next listed bin displays.
    - Continue verifying/adjusting quantities until you have gone through all of the bins/parts. You MUST click Enter for every part number on the report.

2.  **Select the Parts Inventory Exception Report** from the Keystone menu (`Parts | Parts Inventory Adjustment | Parts Inventory Exception Report`) or (`Menu X33, option 3`).
    On the screen that opens:
    - The Date Selection field defaults to the most recent date for the "Last Count Date".
    - Select whether to print No Quantity, Quantity Available, or Quantity On-Hand.
      > **Note:** Make the same selection as you have previously or select No Quantity if you want to be notified of variances but want to take a blind count on the re-count.

3.  **Repeat Step 1 for every part listed on the report.**

> **Summary of Parts Inventory Exception Report:** This report prints a list of all parts that have a Last Count Date prior to the date entered on the Parts Inventory Exception Report. The parts listed on this report are parts that are on the current count sheet whose quantities have not been confirmed in the Parts Inventory Adjustment option. If every part number has been processed, there should be no parts on this report.

### Complete These Steps When Inventory is Completely Finished:

1.  **Compare before and after part inventories.** Select the Parts Inventory Variation Report from the Keystone menu (`Parts | Parts Inventory Adjustment | Parts Inventory Variation Report`) or (`Menu X33, option 5`).
    On the screen that opens:
    - Select **Bin** for the sequence section.
    - Leave the **All** check box selected for the Class section.
    - Select the **Available** or **On Hand** option for the Quantity section.
      > **Note:** Make the same selection as you have previously.
    - Select the number of copies of the report that you would like.
    - Leave the **All** check box selected in the Enter group number section.
    - Select whether to use Dealer Net or Average Cost (This option only appears if you have the Average Cost option turned on).
    - Select the **Parts with changes from inventory adjustments** option for the Report Type.
    - Click **Enter**.
    - Type in a From and To range in the Bin Location section or leave blank for all bins.
    - Select Compress or Expand for Bin Sort Sequence (see previous table for details).
    - Click **Enter**.

> **Summary of Parts Inventory Variation Report:** This report compares the part quantities when you did the inventory freeze to the part quantities recorded after inventory was taken. The Grand Totals at the bottom of the report document the total change to inventory valuation from the count corrections.

2.  **Select Parts Inventory Pad from the Keystone menu again** (`Parts | Part Report | Parts Inventory Pad`) or (`Menu X36, option 1`).
    On the screen that opens:
    - Leave the **All Vendors** and **All Classes** check boxes selected.
    - Click **Enter**. The second Parts Inventory Pad screen opens.
    - Unselect the **Print Detail** check box.
    - Click **Enter**. The Time Delay – Parts Inventory Pad screen opens.
    - Click the **No Delay** button.
    - Compare this Parts Pad Summary with the one created prior to taking inventory. This will show the differences from the first Parts Pad Summary created, but will not offer specific reasoning as to why any differences exist.

> **Summary of Parts Inventory Pad:** By comparing the Parts Pad Summaries from before and after inventory was taken, the difference in value can be determined by Vendor/Class. Note, however, that the difference will include every change that occurs between the times the summaries are run and does not itemize the reasons. Therefore, if changes have been made outside of the parts inventory adjustment process (sales, inventory receipt, etc.), these summaries cannot be used to solely determine the changes that occurred as a result of count corrections.


title: "Parts_Vendor_Class_Configuration_Article"
source: "Parts_Vendor_Class_Configuration_Article.pdf"
tags: ["Keystone", "Parts Configuration", "Vendor Configuration", "Class Configuration", "Pricing Matrix", "Inventory Management", "DIS", "Software Guide", "Automatic Ordering"]
version: "1.0"
last_updated: "2026-01-18"
short_description: "A comprehensive guide on configuring parts vendors and classes within the Keystone software system. It details the procedures for adding new vendors, assigning class codes, and setting up pricing matrices."
long_description: "This document provides step-by-step instructions for configuring parts within the Keystone system, specifically focusing on the Parts Vendor/Class Configuration module. It is intended to be a printable guide for system administrators and parts managers. The guide covers three main procedures: adding a new vendor to the system, creating and assigning specific class codes to that vendor, and setting up a detailed pricing matrix for a specific class of parts. Key configuration options detailed include setting up part number segments, choosing an automatic ordering method (DIS, Case, or Annual), defining class codes for pricing and ordering logic, and establishing multi-tiered pricing based on cost. The document includes screenshots of the user interface to aid in navigation and data entry, ensuring users can accurately set up vendor and part information for inventory management, ordering, and sales processes."