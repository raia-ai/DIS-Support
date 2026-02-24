---
title: "Adding New Makes and Models from Inquire/Update Units"
source: "combined_Quantum_docs.md"
tags: ["Quantum"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Adding New Makes and Models from Inquire/Update Units."
long_description: "This document provides information about Adding New Makes and Models from Inquire/Update Units from the DIS Quantum system."
---

## INTRODUCTION

Beginning with Release 21v1, you will be able to add Makes up to 10 characters in length and Models up to 16 characters in length. While you can add new Makes and Models directly into the Make/Model Table, you can also add them while in the process of entering the unit information in Inquire/Update Units. When new Makes and Models are added, a Long and Short Make and Model will need to be entered.

> **Note**: Though the instructions are based on adding Makes/Models using the Inquire/Update option, the same procedure can be used to add new Makes/Models in the P.O.S. or Service menu options.

## To Add New Makes/Models from Inquire/Update Units

1.  Select Inquire/Update (Complete Access) from the main menu (`Units | Inquire/Update (Complete Access)`). Click the **Add Unit** button.

2.  The Inquire/Update Units – Unit Information screen opens. Type the Unit number, Long Make name, and Long Model name that you are adding. Click **Enter**.

3.  One of the three following messages appears at the bottom of the screen:

| Message Number | Message Text                                                          | Meaning                           |
| :------------- | :-------------------------------------------------------------------- | :-------------------------------- |
| 1              | `DIS-2006 G/L Acct# does not exist or is restricted for this division.` | Both Make and Model already exist.    |
| 2              | `DIS-0025 Unit Model is not valid.`                                     | Unit Make exists, Model does not. |
| 3              | `DIS-0024 Unit Make is not valid.`                                     | Unit Make and Model do not exist. |

4.  If message 2 or 3 displays, the Make and/or Model needs to be added to the system. Click **Long Make:**.

5.  The Select Make/Model screen opens with the Long Make and/or Model you are about to add listed in the fields at the top of the screen. Click the **Add** button.

6.  The Add Make screen opens listing the Long Make and the Short Make. The Short Make will be the first 9 characters of the Long Make – change if desired.

7.  Select the **Allow blank Model** check box to allow a unit of this Make to be added into inventory without also adding a Model.

8.  Click the **Continue** button.

9.  The Add Model screen opens listing the Long Model and the Short Model. The Short Model will be the first 9 characters of the Long Model – change if desired. Leave the **Active** check box selected.

10. Provide a description for the Model if desired and click the **Continue** button.

11. The Select Make/Model screen opens displaying the Make and Model at the top of the table. Highlight the Make/Model and click the **Select** button.

12. The Unit Information screen re-opens with the new Make and Model added to the system. Supply the rest of the unit information.


title: "CLASS_PIM_-_Quantum"
source: "CLASS_PIM_-_Quantum.pdf"
tags: ["CLAAS", "PIM", "Quantum", "Inventory Management", "DIS", "Dealer System", "Parts Inventory", "Vendor Maintenance", "File Transfer", "Reporting"]
version: "1.0"
last_updated: "2024-05-23"
short_description: "This document provides a comprehensive guide for configuring and using the CLAAS Parts Inventory Management (PIM) module within the DIS Quantum dealership system. It covers communication setup, vendor maintenance, managing suggested orders and transfers, and generating various reports."
long_description: "This user guide details the functionality of the CLAAS Parts Inventory Management (PIM) feature in the DIS Quantum system. The PIM module is designed to help dealerships maintain a consistent inventory level for CLAAS parts by facilitating automated part file transfers between the dealership's system and CLAAS. The document outlines the initial configuration steps required to enable PIM communications, including setting up Warehouse Group Codes, Warehouse Codes, and vendor/class combinations. It provides step-by-step instructions on how to configure Electronic Commerce Communications and Vendor Maintenance for both inventory and PIM-specific settings. The guide also explains how to monitor the status of submitted and received files, and how to resend failed submissions. Further sections are dedicated to working with suggested stock orders and transfers originating from CLAAS, including how to view, modify, complete, or delete them. Finally, the document covers the generation and interpretation of key reports, such as the Suggested Orders Report and the Relevant Items Report, which help in managing inventory and identifying parts to add. An overview of the different types of files exchanged between the dealership and CLAAS is also included, clarifying the purpose of Purchase Order, Transactional Demand, Dealer Item, Relevant Item, and Order Export files."