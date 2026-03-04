---
title: "Quantum — General Ledger"
source: "DIS_Video_Training_Knowledge_Base.md"
tags: ["DIS System Training", "Quantum"]
version: "1.0"
last_updated: "2026-03-04"
short_description: "The **Quantum — General Ledger (GL)** module is the central component of the DIS (Dealer Information System) platform’s accounting functionality. It provides a structured framework for recording, organizing, and reporting financial transactions ac..."
long_description: "This document provides a comprehensive overview of the Quantum — General Ledger module within the DIS platform, derived from internal training sessions."
---

# Quantum — General Ledger

**Source Sessions**: 04, 05, 06, 07, 13

### Overview

The **Quantum — General Ledger (GL)** module is the central component of the DIS (Dealer Information System) platform’s accounting functionality. It provides a structured framework for recording, organizing, and reporting financial transactions across multiple divisions and departments within an enterprise. The module ensures accurate financial statement generation, supports detailed departmental profit analysis, and integrates with other system modules such as Accounts Receivable, Parts Inventory, and Point of Sale (POS).

This module is critical because it enforces standardized accounting practices, maintains the integrity of financial data through strict mapping and validation rules, and offers advanced reporting capabilities including scheduled account tracking and custom queries via Data Mine. It also supports complex organizational structures by allowing multi-division and departmental financial management, intercompany transfers, and year-end adjustments.

### Core Concepts

**GL Account Structure**  
General Ledger accounts are carefully structured to reflect the organization’s divisions, account types, and departments. The GL account number is a composite key with the following components:

- **First Character (Division Code):** Represents the physical location or branch (e.g., a specific store). This is mandatory and must be unique per division.
- **Second Character (Account Type):** Indicates the type of account, such as Asset, Liability, Sale, Cost of Sale, or Expense.
- **Middle Digits (Sequencing):** Used to order accounts on financial statements and group related accounts.
- **Last Digit(s) (Department Code):** Represents profit centers within a division (e.g., Sales, Parts, Service), enabling departmentalized financial reporting.

**Standard Accounting Numbering**  
The system follows conventional accounting numbering conventions for account types:

- Assets start with `1`
- Liabilities start with `2`
- Equity accounts (including owner’s equity and retained earnings) are grouped with liabilities
- Sales accounts start with `3`
- Cost of Sale accounts start with `4` or `5`
- Expenses and other income/expense accounts use higher digits (`6`, `7`, `8`, `9`)

**Departmentalization**  
Departments are treated as profit centers, allowing the same base GL account to be replicated across departments by changing the last digit. This facilitates detailed departmental profit and loss reporting and analysis.

**Sales and Cost of Sales Mapping**  
Each sales account must have a unique, corresponding cost of sales account. This one-to-one mapping is essential to maintain balanced financial statements. Cost of sales accounts cannot be shared among multiple sales accounts, as this causes imbalance in financial reporting.

**Subledger vs. Scheduled Accounts**  
- **Subledgered Accounts:** Balances are controlled by other system modules (e.g., Accounts Receivable, Parts Inventory) and summarized in the GL.
- **Scheduled Accounts:** Tracked within the GL using special **edit codes** that allow detailed transaction-level tracking by identifiers such as customer name, document number, or unit number.

**Edit Codes**  
Edit codes are single-letter flags assigned to GL accounts to control their behavior:

- `N`: Schedule by name/address number
- `D`: Schedule by document number
- `U`: Schedule by unit number (does not affect unit cost)
- `B`: Bank accounts used in check reconciliation
- `T`: Other specialized tracking

**Financial Statement Format (FIN File)**  
The `FIN` file controls the layout, grouping, and subtotals of the financial statement. It is a global file shared across all divisions in a file set, ensuring consistent reporting. The placement of GL accounts within the numerical ranges defined in the `FIN` file determines where they appear on the financial statement.

**Data Mine**  
A powerful reporting tool that allows users to create complex, custom queries against GL data. It supports advanced filtering logic, including combined `AND`/`OR` conditions, and queries can be shared among users.

**Check Reconciliation**  
A process to reconcile bank accounts by entering bank statement balances, service charges, and interest earned, then clearing outstanding checks and deposits. Only GL accounts with the `B` edit code are available for reconciliation.

### System Architecture & Data Model

The Quantum GL module organizes data hierarchically:

- **File Set:** Represents the entire enterprise or company.
- **Division:** A physical location or branch within the file set. Each GL account must begin with the division code.
- **GL Account Number:** A composite key structured as `[Division][Account Type][Sequencer][Department]`.
- **Account Types:** Defined by the second character and edit codes, including Asset (A), Liability (L), Sale (S), Cost of Sale (C), Expense (E), and Income (I).
- **Account Mapping:** Sales accounts must be uniquely mapped to cost of sales accounts to maintain balanced financial statements.
- **Scheduled Account Data:** Transactions linked to scheduled accounts include identifiers such as customer address number, document number, or unit number, depending on the edit code.
- **FIN File:** Governs the financial statement format, grouping, and subtotals, shared across all divisions.
- **Data Mine Queries:** Stored centrally on the server, enabling multi-user access and collaboration.

### Key Procedures

#### Creating a New Department

1. Navigate to **Department Configuration**.
2. Enter the desired department name (e.g., "Trucking").
3. Click **Add** to save the new department.

#### Running a Scheduled Account Report

1. Navigate to `Accounting > General Ledger > Schedules > Scheduled Account Report`.
2. Enter the GL account number.
3. Select the report type: Detail or Aged.
4. Leave the transaction date range open to view all outstanding transactions.
5. Optionally, select "Purge zero balances" to exclude cleared items.
6. Run the report.

#### Performing a Scheduled Account Inquiry

1. Navigate to `Accounting > General Ledger > Schedules > Scheduled Account Inquiry`.
2. Enter the GL account number.
3. Enter the specific identifier (e.g., customer address number).
4. View all transactions for that GL account and identifier.

#### Using Data Mine for Custom Reporting

1. Open Data Mine.
2. Create a new query.
3. Add filters to specify desired data (e.g., account type, date range).
4. When using `OR` conditions, duplicate any `AND` conditions on both sides of the `OR`.
5. Add a description and set visibility to all users if desired.
6. Save the query.

#### Performing Check Reconciliation

1. Navigate to `Accounting > General Ledger > Check Reconciliation`.
2. Select the bank account (only accounts with `B` edit code are listed).
3. Enter the bank statement’s opening and ending balances.
4. Enter service charges and interest earned, specifying corresponding GL accounts.
5. Mark cleared checks and deposits.
6. Ensure the difference between system and bank balances is zero.

#### Importing a Spreadsheet into a Journal Entry

1. Navigate to `Accounting > General Ledger > Create Source Documents`.
2. Click on `Recurrent Transactions`.
3. Click `Import`.
4. Select the spreadsheet file from the `Keystone` directory on the AS/400.
5. The imported transaction appears in the recurrent transactions list.
6. Select the transaction and click `Post`.

#### Fixing Financial Statement Format (FIN File)

1. Identify the account appearing incorrectly on the financial statement.
2. Navigate to `Security > Initial Data Entry > Financial Statement Format`.
3. Enter the account number.
4. Delete the existing entry.
5. Create a new entry with the correct account number and settings.

#### Creating a Journal Entry

1. Navigate to `Accounting > General Ledger > Create Source Documents`.
2. Enter a document number, description, and date.
3. Input GL account numbers, debit or credit amounts, and descriptions for each line.
4. Verify total debits equal total credits.
5. Post the journal entry.

### Menu Navigation

- `Accounting > General Ledger`
- `Accounting > General Ledger > Account Inquiry`
- `Accounting > General Ledger > Account Maintenance`
- `Accounting > General Ledger > Chart of Accounts`
- `Accounting > General Ledger > Schedules > Scheduled Account Inquiry`
- `Accounting > General Ledger > Schedules > Scheduled Account Report`
- `Accounting > General Ledger > Check Reconciliation`
- `Accounting > General Ledger > Create Source Documents`
- `Accounting > Financial Reports > Financial Statement`
- `Accounting > Financial Reports > Trial Balance`
- `Security > Initial Data Entry > Financial Statement Format`
- `Security > Security Maintenance`
- `Point of Sale > Table Maintenance`
- `Point of Sale > Table Maintenance > Document Class`
- `Point of Sale > Table Maintenance > Sales Code`
- `Point of Sale > Table Maintenance > Price Table`
- `Point of Sale > Table Maintenance > Discount`
- `System > Change Division`

### Business Rules & Constraints

- **Division Code Prefix:** All GL accounts must begin with the company’s division code.
- **Unique Cost of Sale Account:** Each sales account must be linked to a unique cost of sale account; sharing cost accounts among sales accounts is prohibited.
- **Mandatory Sales Account Mapping:** Every cost of sale account must be mapped to a corresponding sales account to appear correctly on financial statements.
- **GL Account Uniqueness:** GL account numbers must be unique across all divisions within the same file set to avoid conflicts.
- **Document Number Validation:** The system does not validate document numbers; users must enforce their own controls.
- **Edit Code Application:** Special edit codes (`N`, `D`, `U`, `B`, `T`) can be applied to any GL account type.
- **Check Reconciliation Accounts:** Only GL accounts with the `B` edit code are available for bank reconciliation.
- **User Sessions:** A user can have up to five concurrent sessions but may only be active in one division at a time.
- **Security Maintenance:** Only one user can access security maintenance at a time within a file set.
- **Discount Codes:** A blank discount code must always exist in the discount table.
- **Intercompany Transfers:** Posting transactions across divisions requires an intercompany transfer account configured in security maintenance.
- **Trial Balance vs. Financial Statement:** The trial balance is the authoritative report for system balance; the financial statement may be out of balance due to mapping issues.

### Configuration Options

- **Department Configuration:** Define and manage profit centers to structure GL accounts for departmental reporting and Management 360.
- **Intercompany Transfer Account:** Set in `Security > Security Maintenance > Additional Information` to handle cross-division postings.
- **Financial Statement Format (FIN File):** Customize the layout, grouping, and subtotals of financial statements.
- **Bypass Authority:** Assign user permissions to bypass security gates for specific modules and divisions.
- **Data Mine Sharing:** Configure queries to be visible to all users for collaboration.
- **Data Mine Excel Export:** Enable automatic export of query results to Excel.
- **Automated End-of-Day Jobs:** Schedule end-of-day processes for accounting, parts, and POS modules.
- **POS Table Maintenance:** Configure document classes, sales codes, price tables, and discounts to control how POS transactions post to the GL.
- **13th Month Accounting:** Enable a 13th fiscal period for year-end CPA adjustments.

### Common Pitfalls & Warnings

- **GL Accounts Starting with Zero:** Avoid creating GL accounts beginning with zero to prevent system issues.
- **Non-Standard Account Numbering:** Deviating from standard numbering conventions can cause reporting problems.
- **Orphan Cost of Sale Accounts:** Cost of sale accounts without corresponding sales accounts cause financial statements to be out of balance.
- **Sharing Cost of Sale Accounts:** Mapping multiple sales accounts to the same cost of sale account leads to imbalance.
- **Renaming GL Accounts:** Changing GL account numbers after archival causes audit discrepancies.
- **Accidental End-of-Day Execution:** Running end-of-day processes manually can cause errors; rely on scheduled jobs.
- **Data Mine Filter Logic:** When using `OR` conditions, forgetting to apply `AND` conditions on both sides results in incorrect query results.
- **Check Reconciliation GL Accounts:** Users must know the correct GL accounts for bank fees and interest; the system does not provide lookups during reconciliation.
- **Working in Multiple Divisions:** Users should avoid working in different divisions simultaneously to prevent data conflicts.
- **Security of Imported Files:** Files imported for journal entries reside in a shared directory without security; sensitive files should be deleted after processing.
- **13th Month Adjustments:** Using the 13th month can cause reporting anomalies in subsequent years if not managed carefully.

### Key Terminology

- **Account Type:** Classification of GL accounts such as Asset (A), Liability (L), Sale (S), Cost of Sale (C), Expense (E), and Income (I).
- **Bypass Authority:** User permission to bypass security gates without entering a password.
- **Cost of Sale Account:** A GL account representing the cost associated with sales; must be uniquely mapped to a sales account.
- **Data Mine:** A reporting tool for creating custom queries and reports from GL data.
- **Department:** A profit center within a division used for financial reporting.
- **Division:** A physical location or branch within the enterprise.
- **Edit Code:** A single-letter code assigned to GL accounts to control tracking and behavior.
- **FIN File:** The file controlling the financial statement format, grouping, and subtotals.
- **Intercompany Transfer Account:** An account used to balance transactions between divisions.
- **Orphan Account:** A cost of sale account without a corresponding sales account, causing imbalance.
- **Recurrent Transactions:** Saved journal entry templates that can be imported and posted repeatedly.
- **Scheduled Account:** A GL account tracked with edit codes for detailed transaction-level reporting.
- **Security Gate:** A password-protected access point to system modules or functions.
- **Subledgered Account:** A GL account whose balance is controlled by another system module.
- **Trial Balance:** The definitive report to verify if the GL is balanced.
- **Unit Number Scheduling:** Tracking transactions by unit number without affecting unit cost.
- **User Session:** An active connection to the system; users may have up to five concurrent sessions but only one active division.

---