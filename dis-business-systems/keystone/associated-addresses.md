---
title: "Associated Addresses"
source: "combined_Keyston.md"
tags: ["Keystone"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Associated Addresses."
long_description: "This document provides information about Associated Addresses from the DIS Keystone system."
---

## Introduction

The new Associated Addresses feature allows you to group multiple customers together by their customer address number, allowing you to view how the group performs as a whole. Customer Addresses can be grouped through the following menu options:

-   Address Maintenance
-   Receivables Maintenance
-   Sales Ranking – this option also allows you to exclude customers from associated groups.
-   Sales Ranking Report – this option also allows you to exclude customers from associated groups.

After the associated groups have been created, you can currently process and/or view their collective data through the following menu options:

-   Sold Units Inquiry
-   Part Sales History (including Transaction and Summary reports)
-   Inquire/Update Service Units
-   Sales Ranking and Sales Ranking Report

> The Associated Addresses feature uses the Sales Ranking files. Sales Ranking Report files are updated once every day (7:00 pm by default). Therefore, most changes to Associated Address details will not display until the following day.

## To Associate a Group of Customer Addresses

Customer Addresses can be associated through the Address Maintenance/Receivables Maintenance menu options with the Use Instead feature or through the Combine Address feature in the Sales Ranking/Sales Ranking Report options. Before associating addresses, decide which customer address will be the primary address and which addresses will be secondary addresses. You can add secondary addresses at any time. Once an associated address grouping has been established, you can either permanently delete the grouping or exclude secondary address from being included with the associated address information.

### Through Address Maintenance and Receivables Maintenance

1.  Do one of the following:
    -   Select **Address Maintenance (Marketing | Address Maintenance)**.
        - The first Address Maintenance screen opens. Provide one of the secondary addresses and click **Enter**. The second Address Maintenance screen opens.
        - Unselect the `Allow new POS documents without extra security` check box at the bottom of the screen, provide the primary customer address in the `Instead use address number` field that appears, and click **Enter** to save.

    -   Select **Receivables Maintenance (Accounting | Receivables | Receivables Maintenance)**.
        - The first Receivables Maintenance screen opens. Provide one of the secondary addresses and click **Enter**.
        - Click **Forward** until you have reached the final Receivables Maintenance screen.
        - Unselect the `Allow new POS documents without extra security` check box at the bottom of the screen, provide the primary customer address in the `Instead use address number` field that appears, and click **Enter** to save.

2.  Repeat the steps through the menu option of choice for the remainder of secondary addresses that you want to associate with the primary address.

### Through Sales Ranking and Sales Ranking Report

1.  Do one of the following:
    -   Select **Sales Ranking (Marketing | Sales Ranking)**. The Sales Ranking screen opens.
    -   Select **Sales Ranking Report (Marketing | Sales Ranking Report)**. The Parameters screen opens.

2.  Once you have accessed one of the screens in the previous step, click the **Combine** button. The `Combine Addr#s` screen opens listing secondary addresses and the primary address with which they are combined (associated).

    | Addr# | Name | Combine with Addr# | Name |
    | :--- | :--- | :--- | :--- |
    | CORB01 | RAYMOND CORBIN | COD001 | PETER CODDINGHAM |
    | GLAD01 | JOEY GLADSTONE | TANN01 | TANNER FAMILY |
    | HALE01 | STEVE HALE | TANN01 | TANNER FAMILY |
    | KATS01 | JESSE KATSOPOLIS | TANN01 | TANNER FAMILY |
    | KATS02 | BECKY KATSOPOLIS | TANN01 | TANNER FAMILY |
    | KATS03 | NICKY KATSOPOLIS | TANN01 | TANNER FAMILY |

3.  Click the **Add** button. The `Create New Addr# Combination` screen opens.
    -   Type a secondary customer address number in the `Addr#` field and the primary address in the `Combine with Addr#` field. Click **Enter** to save.
    > **Note:** The address association will not display in the table until the Sales Ranking Report files have been updated.

## Delete Associated Address Grouping

Once a customer address grouping has been established, it can quickly be deleted.

1.  Do one of the following:
    -   Through the Address or Receivables Maintenance options, navigate to the screen with the `Use Instead` field. Clear out the field and click **Enter**. The grouping is deleted.
    -   While on the `Combine Addr#s` screen, select the associated grouping from the table that you would like to remove and click the **Remove from list** button. The `Confirm Deletion` screen opens.
        - Click the **OK** button. The grouping is deleted and removed from the table. Repeat the process for any other combinations that you would like to delete.

## Exclude Address from Associated Group

You can exclude a customer address that has been assigned to the associated group through the Sales Ranking/Sales Ranking Report options.

1.  While on the Sales Ranking or Sales Ranking Report screen, click the **Exclude** button.
2.  The `Exclude Addr#s` screen opens listing the customer addresses currently excluded from group association.
3.  Click the **Add** button.
4.  The `Exclude Addr#` screen opens. Type the customer address number you would like to exclude from all associated groups and click **Enter**.
5.  Repeat the previous step to exclude additional customer addresses.
6.  Click **Return** when finished. The customer addresses are added to the exclusion table.

## Delete an Exclusion

Customer address numbers that have been excluded from group association can be permanently removed.

1.  Select the excluded customer address from the table on the `Exclude Addr#s` screen.
    > **Note:** Hold down the Ctrl key while clicking addresses to select multiple addresses.
2.  Click the **Remove from list** button. The `Delete Excluded Addr#s` screen opens listing the selected excluded addresses. Verify that you want to delete these address exclusions.
3.  Click the **OK** button. The excluded addresses are deleted.

## View Associated Address Group Information

After you have setup associated address groups, you can view the associated group information through multiple menu options. This section provides detail on how to view the information in each available menu option.

### Sold Units Inquiry

1.  Select **Sold Units Inquiry (Units | Sold Units Inquiry)**. The Sold Units Inquiry entry screen opens. Provide the address of a customer in the Address field and click **Enter**. The second Sold Units Inquiry screen opens.
2.  The units sold to the customer display in the table. If the customer is part of an associated group, the `Switch to Associated View` button will appear on the left side of the screen.
3.  Click the **Switch to Associated View** button. The screen opens in Associated View listing all of the units sold to members of the group. Units are listed in order by the date the unit was sold. The address of the customer that the unit was sold to is listed on the third line in the Serial # column.
4.  Click the **Associated Addresses** button to view all of the members that comprise the associated group. Even if a member of the associated group is excluded, they will still be listed in the table.
5.  Click the **Switch to Single View** button to only list the units sold to the customer you entered on the initial Sold Units Inquiry screen.

### Inquire/Update Service Units

1.  Select **Inquire/Update Service Units (Service | Inquire/Update Service Units)**. The Search Only screen opens. Provide a customer address and click **Enter**. The Current Equipment screen opens listing one of the customer's units. Units are listed and accessed in order of the unit serial number.
2.  Click the **Next Unit** button to view the next unit for the customer address you provided on the Search Only screen.
3.  Click the **Next Unit – Assoc** or **Previous Unit – Assoc** button to view the next/previous unit in the system that belongs to a member of the associated address group.
4.  Click the **Assoc Addresses** button to view all of the members that comprise the associated group. Even if a member of the associated group is excluded, they will still be listed in the table.

### Part Sales History

#### Transaction Review

1.  Select **Part Sales History (P.O.S. | Part Sales History)**. The Data Selection screen opens. Provide a customer address and click **Enter**. The Transaction Review screen opens listing the parts sold to the customer. Part sales are listed by the transaction date.
2.  Click the **Switch to Assoc. View** button. The Associated View screen opens displaying part sales for all members of the associated group.
3.  Click the **Fold/Unfold** button to reveal additional detail about each part transaction. The address of the associated group member is listed on the second line of each transaction under the description column.
4.  Click the **Associated Addresses** button to view all of the members that comprise the associated group. Even if a member of the associated group is excluded, they will still be listed in the table.
5.  Click the **Print** button and select the number of copies to generate the Transactions Report. If the report is generated while in associated view, it will be indicated in the right-side of the header information and customer addresses will be provided for each part sales transaction.
6.  Click the **Switch to Single View** button to just list part sale history information for the customer address that was initially provided.

#### Summary Totals Display

1.  Click the **Summary** button on the first Part Sales History screen.
2.  The Summary Totals Display screen opens providing a yearly history of part sales broken down into monthly segments.
3.  Click the **Switch to Assoc. View** button. Though the address at the top of the screen remains the same, the figures in the table adjust to reflect all of the included customers in the associated address group.
4.  Click the **Associated Addresses** button to view all of the members that comprise the associated group. Even if a member of the associated group is excluded, they will still be listed in the table.
5.  Click the **Switch to Single View** button to view the individual summary for the customer you originally entered.
6.  Click the **Print** button and select the number of copies to generate the History Summary report. If the report is generated while in associated view, it will be indicated in the right-side of the header information.

### Sales Ranking and Sales Ranking Report

When processing the sales ranking data and/or generating the sales ranking report, you can view the information for associated groups if desired. While in the Sales Ranking or Sales Ranking Report options, type the letter “Y” in the `Use Combine Addr# List` field to generate the data for associated groups.

-   The Sales Rankings will be generated according to associated group figures.
-   The Sales Ranking Report will list the figures for an associated group by the primary address instead of by individual customers.


title: "Average_Costing_Article"
source: "Average_Costing_Article.pdf"
tags: ["average costing", "inventory valuation", "dealer net", "DIS Business System", "Keystone", "parts management", "accounting", "cost method", "inventory reporting"]
version: "1.0"
last_updated: "2024-05-23"
short_description: "This document explains the Average Costing feature in the DIS Business System. It details how to enable the feature, how it differs from the default Dealer Net (replacement cost) method, and its impact on inventory valuation, gross margins, and reporting."
long_description: "A comprehensive guide to the Average Costing functionality within the Dealer Information Systems (DIS) Business System. The document begins by introducing the concept of Average Costing as an alternative to the standard Dealer Net (replacement cost) method for inventory valuation. It provides step-by-step instructions on how to enable this feature via the OPT PARTS MENU. The core of the document explains the calculation used to determine the average cost of a part each time a new receipt is recorded. It presents the formula: [(Current average cost x On hand quantity) + (New receipt cost x New receipt quantity)] / (Total on hand quantity) = New average cost. The guide uses clear tables to illustrate the impact of increasing costs on inventory valuation and gross margins under both the Replacement Cost Method and the Average Cost Method. It highlights that while average cost typically results in higher gross margins, it also has tax and accounting implications for a dealership. The document then outlines all the specific areas and reports within the DIS system where Average Cost is used, including Parts Inquiry, Parts Posting & Maintenance, order receiving, inventory reports, and Point of Sale (P.O.S.) transactions. It includes screenshots and detailed explanations for each functional area, ensuring users understand how to manage and interpret data when Average Costing is active."