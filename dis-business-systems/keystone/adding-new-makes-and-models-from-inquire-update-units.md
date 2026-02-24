---
title: "Adding New Makes and Models from Inquire/Update Units"
source: "combined_Keyston.md"
tags: ["Keystone"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Adding New Makes and Models from Inquire/Update Units."
long_description: "This document provides information about Adding New Makes and Models from Inquire/Update Units from the DIS Keystone system."
---

## INTRODUCTION

Beginning with Release 21v1, you will be able to add Makes up to 10 characters in length and Models up to 16 characters in length. While you can add new Makes and Models directly into the Make/Model Table, you can also add them while in the process of entering the unit information in Inquire/Update Units. When new Makes and Models are added, a Long and Short Make and Model will need to be entered.

> **Note:** Though the instructions are based on adding Makes/Models using the Inquire/Update option, the same procedure can be used to add new Makes/Models in the P.O.S. or Service menu options.

## To Add New Makes/Models from Inquire/Update Units

1.  Select Inquire/Update (Complete Access) from the Keystone main menu (**Units | Inquire/Update (Complete Access)**). Click the **Add Unit** button.

2.  The Inquire/Update Units – Unit Information screen opens. Type the Unit number, Long Make name, and Long Model name that you are adding. Click **Enter**.

3.  One of the three following messages appears at the bottom of the screen:

| # | Message | Meaning |
|---|---|---|
| 1 | `DIS-2006 G/L Acct# does not exist or is restricted for this division.` | Both Make and Model already exist. |
| 2 | `DIS-0025 Unit Model is not valid.` | Unit Make exists, Model does not. |
| 3 | `DIS-0024 Unit Make is not valid.` | Unit Make and Model do not exist. |

4.  If message 2 or 3 displays, the Make and/or Model needs to be added to the system. Click **Long Make:**.

5.  The Select Make/Model screen opens with the Long Make and/or Model you are about to add listed in the fields at the top of the screen. Click the **Add** button.

6.  The Add Make screen opens listing the Long Make and the Short Make. The Short Make will be the first 9 characters of the Long Make - change if desired.

7.  Select the **Allow blank Model** check box to allow a unit of this Make to be added into inventory without also adding a Model.

8.  Click the **Continue** button.

9.  The Add Model screen opens listing the Long Model and the Short Model. The Short Model will be the first 9 characters of the Long Model - change if desired. Leave the **Active** check box selected.

10. Provide a description for the Model if desired and click the **Continue** button.

11. The Select Make/Model screen opens displaying the Make and Model at the top of the table. Highlight the Make/Model and click the **Select** button.

12. The Unit information screen re-opens with the new Make and Model added to the system. Supply the rest of the unit information.


title: "AGCO API Part Inventory Transmissions"
source: "AGCO_API_Part_Inventory_Transmissions.pdf"
tags: ["AGCO", "API", "Inventory Transmission", "DIS", "Keystone", "Interface Manager", "Technical Guide", "Dealer Instructions", "Parts Locator"]
version: "1.0"
last_updated: "2024-05-23"
short_description: "This guide provides instructions for dealers on using the AGCO API to transmit daily parts inventory files. It details how to identify the designated PC for transmissions and ensure the DIS Interface Manager is running correctly for successful nightly backups."
long_description: "This technical document is intended for dealers using the Dealer Information Systems (DIS) Keystone business system to manage their AGCO parts inventory. It outlines the process for transmitting daily AGCO parts inventory files to AGCO, which is necessary for displaying Parts Locator information on the AGCO Website and for generating Suggested Stock Orders. The guide explains that these transmissions occur automatically during the nightly DIS Backup, provided certain conditions are met. The core instructions focus on two key areas: first, how to determine which specific PC in the dealership is configured to transmit the API data by navigating through the Electronic Commerce Configuration in the Keystone system. Second, it details how to verify that the DIS Interface Manager program is running on that designated PC, which is a prerequisite for the transmission. The document includes step-by-step instructions with screenshots, warning callouts, and important notes to guide the user through identifying the correct workstation, user job, and checking the status of the Electronic Commerce Client. It also provides troubleshooting information for situations like power outages and contact details for the DIS Response Line."