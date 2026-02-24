---
title: "Export Electronic Version of Vendor Totals 1099 Form"
source: "combined_Keyston.md"
tags: ["Keystone"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Export Electronic Version of Vendor Totals 1099 Form."
long_description: "This document provides information about Export Electronic Version of Vendor Totals 1099 Form from the DIS Keystone system."
---

## INTRODUCTION

You can create an electronic version of your Vendor Totals 1099 Reports and export it to a directory in your IFS. The file is a comma delimited file in ASCII format that can be used with Mag-Filer software (additional third party product) to create the 1099 Forms. For more information on Mag-Filer software, including demonstrations and how to purchase, please consult the software provider.

## To Create and Export 1099 Forms:

1.  Select **Vendor Totals for 1099 Preparation** (Accounting | Payables | Vendor Totals for 1099 Preparation) from the Keystone main menu. The **Vendor Totals – 1099 Preparation Selection** screen opens.

2.  On the **VENDOR TOTALS - 1099 Preparation Selection** screen, configure the following options:
    -   **Sort by**: Select either `Vendor Name` or `Vendor Address Number`.
    -   **Select by**: Choose one of the following criteria: `General Ledger Account`, `Group Code`, or `Address Number`.
    -   **Calendar year for report**: Enter the relevant calendar year (e.g., 16 for 2016).

    > **Note:** Consider creating a group code for all vendors that require a 1099 form and assigning it to each vendor.

3.  Click **Enter**.

4.  One of the following screens will open depending on your selection in the previous step:
    -   **VENDOR TOTALS - 1099 Preparation Selection by G/L Account**:
        -   Select the desired accounts: `All Payable Accounts`, `Only Trade Payable Accounts`, `Only Flooring Payable Accounts`, or specify `Specific General Ledger Accounts`.
    -   **VENDOR TOTALS - 1099 Preparation Selection by Group Codes**:
        -   Enter the relevant `Group Codes`.
    -   **VENDOR TOTALS - 1099 Preparation Selection by Address Numbers**:
        -   Enter the specific `Address Numbers`.

5.  Provide the Group Code, General Ledger Account, or Vendor Address Number information as required on the screen.

6.  Click the **Export electronic 1099 file** button. A message appears at the bottom of the screen stating the 1099 file has been exported to the following directory in your IFS:
    `(\\Keystone\Keystone\Export\Payables\Fileu)`

7.  The exported file will be named `X12_1099_yyyy-mm-dd.csv`, where the date in the file name is the date it was created.

    > **Note:** If a file with the same name already exists when the export occurs, the old file will be replaced with the new file.

8.  The electronic 1099 file is now ready for use with Mag-Filer.


title: "Export Electronic Version of W2 Forms"
source: "Export_Electronic_Version_of_W2_Forms.pdf"
version: "1.0"
last_updated: "2026-01-18"
short_description: "A step-by-step guide on how to create and export an electronic, comma-delimited ASCII version of W-2 forms using the Keystone DIS software for submission to the IRS via third-party software like Mag-Filer."