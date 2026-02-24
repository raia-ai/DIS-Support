---
title: "G/L Power Add and Copy"
source: "combined_Keyston.md"
tags: ["Keystone"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about G/L Power Add and Copy."
long_description: "This document provides information about G/L Power Add and Copy from the DIS Keystone system."
---

## Introduction

This option allows you to group multiple divisions and add or update a general ledger account in all of those divisions from any one of the grouped divisions. This prevents you from having to enter or update the general ledger information in each division separately. Furthermore, the system now prompts for the correct type of additional accounts during setup, guiding you through the process while showing the assigned accounts and their associated information on one screen.

You can also generate a report that lists the differences in each account across grouped divisions, allowing you to quickly identify differences and sync the accounts if desired.

## To Group Divisions

1.  Select **Account Maintenance** (`Accounting | General Ledger | Account Maintenance`). The Account Maintenance screen opens.

    *   *Image: The GENERAL LEDGER ACCOUNT MAINTENANCE screen is displayed, showing a "Link Divisions" button and a field for "Account Number".*

2.  Click the **Link Divisions** button. The Link Divisions screen opens.

    *   *Image: The GENERAL LEDGER ACCOUNT MAINTENANCE - Link Divisions screen is displayed. It shows a list of divisions with a "Group" field next to each one.*

    | Group | Div | Name               |
    | :---- | :-- | :----------------- |
    | 1     | C   | WHISKEY RIVER TRAC |
    | 1     | D   | WHISKEY RIVER TRAC |

3.  Enter the same number into the group fields for each division that you would like to link together and click **Enter** to save. The grouping character MUST be a number between 1 and 9.

4.  When you have finished grouping divisions, click **Enter** to save the assignments.

    > **Note:** Any accounts that are now added or updated in a division linked in a group, are replicated in all of the divisions in the group. Remove the numbers and click **Enter** to work in a single division.

## To Generate Exception Report

The Exception Report allows you to compare the same general ledger account across the divisions that you specify.

1.  Click the **Exception Report** button on the Link Divisions screen as shown below.

    *   *Image: The GENERAL LEDGER ACCOUNT MAINTENANCE - Link Divisions screen with the "Exception Report" button highlighted. Divisions C and D are both assigned to Group 1.*

2.  The Select Divisions screen opens, allowing you to group the divisions together that you would like to consider when generating the report. Group the divisions together by assigning them the same number between 1 and 9.

    *   *Image: The GENERAL LEDGER ACCOUNT MAINTENANCE - Select Divisions screen is displayed, showing a "Submit Report" button and the list of divisions available for grouping.*

3.  Click the **Submit Report** button.

### The GL Account Exceptions report is generated.

The report shows differences between accounts in the grouped divisions.

*   *Image: A sample "GL ACCOUNT EXCEPTIONS" report. It lists accounts and shows discrepancies between Division C and Division D. For Account 30801, Division D is marked as "Missing". For Account 31103, an asterisk (*) marks a difference in the Account1 assignment.*

-   An asterisk displays if the Edit Code, Account1/Account2 assignment, Factor, or Type is different than the accounts in the other divisions grouped for the Exception report.
-   If an additional account is not assigned in a linked division, the word **Missing** displays.
-   If there is an account among those listed that you would like to replicate in the other grouped divisions, access the correct account in that division and click **Enter**. The Account information will be replicated in all linked divisions.

The last page(s) of the report list Cost of Sale accounts that are currently not paired with a sales account as shown below.

*   *Image: A sample report page titled "COS ACCOUNTS NOT ASSIGNED TO SALES ACCOUNTS", listing several accounts that are not properly paired.*

## To Add/Update Account in all Linked Divisions

If divisions are linked, a message appears next to the Account Number field stating **Linked Divisions will be updated** when you access the Account Maintenance screen. When this message displays, any new accounts will be added in all of the linked divisions. Likewise, any updates will be applied across all linked divisions.

> **Note:** you can add an account to a single division or update an account for a single division by clicking the **Link Divisions** button, removing the numbers from the Group fields, and clicking **Enter**.

1.  Select **Account Maintenance** (`Accounting | General Ledger | Account Maintenance`). The Maintenance screen opens.

    *   *Image: The GENERAL LEDGER ACCOUNT MAINTENANCE screen shows the message "Linked Divisions will be updated" next to the Account Number field.*

2.  Provide the new account number and click **Enter**. The Account # screen opens.

    *   *Image: The GENERAL LEDGER ACCOUNT MAINTENANCE - Account # screen opens for a new account (e.g., C15100). Fields for Title, Edit Code, Type, etc., are available for input.*

3.  Enter the name of the G/L Account, the Edit Code, and the Account Type in the fields provided. You can click the Account #1 and/or Account #2 buttons to select the accounts from existing accounts or Click **Enter**.

4.  If you clicked **Enter** or the account number that was entered wasn't an acceptable account, the **Add Accounts** screen will display. Notice that it prompts for the specific account types based on the Edit code that was entered on the previous screen. Do one of the following:
    -   Provide the existing account number(s) in the Account # fields or click the Account # button and select the account(s) from the list that displays.
    -   Create a New Account by entering the account details in the fields provided.

    *   *Image: The Add Accounts screen prompts the user to define related accounts. In this example, based on the primary account's Edit Code, it asks for a "1 Sales-New Units" account and a "2 Cost of Sales-New Units" account.*

5.  Click the **Validate** button or **Enter** to verify the provided account information. If there are errors, a message will display at the bottom of the screen with specific details. Otherwise a validation message appears as shown below.

    *   *Image: The Add Accounts screen after validation, showing the message "Entries have been validated. Press Accept or Enter to add new accounts."*

6.  Click **Accept** or **Enter** to assign the new account(s).

### Account Creation and Replication

The Account # screen re-opens with the account fields populated.

*   *Image: The GENERAL LEDGER ACCOUNT MAINTENANCE screen for account C15100 is now populated with the newly assigned linked accounts (Account #1: C32800, Account #2: C52700).*

A duplicate account has also been created for any other grouped divisions, with each division's code preceding the duplicated account numbers as shown below.

*   *Image: A side-by-side view showing the newly created account in another linked division. The account number is now D15100, and its linked accounts are D23800 and D52700, demonstrating the automatic replication and prefixing with the division code 'D'.*