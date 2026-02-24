---
title: "Prevent Duplicate Address Entry"
source: "combined_Quantum_docs.md"
tags: ["Quantum"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Prevent Duplicate Address Entry."
long_description: "This document provides information about Prevent Duplicate Address Entry from the DIS Quantum system."
---

## Introduction

Prevent Duplicate Address Entry allows you to check if a customer already has an address number in your system before you create a new one for them. The information that the customer provides is compared against information in the system and any matching results such as a phone number or street address are listed in search results. You can then view all of the information tied to the matching results and verify if it is the customer.

When this feature is enabled, you can specify which fields on the Add New Cash Customer screen require entry for a customer to be added into the system as well as the fields that require entry for conducting a search. Additionally, you can select words to exclude from being searched and specify the fields (Name, City, Phone number, etc.) that display as search results.

## Enable Point of Sale – Find Option

The Point of Sale - Find option must be turned on before the feature can be used.

1.  Open **Point of Sale Menu Twenty-Seven** in Quantum (Security | OPT DIS Master Menu | Point of Sale | Click Next Arrow to Menu Twenty-Seven or Click Alt + A and enter Menu **X636R** in the Command line).

2.  Type the number `6` in the **Enter Option Number** field at the bottom of the page to select `6. FIND (search) activated` and click **Enter**.

## Build Index

The build index option allows you to create an index of all of the customer information that currently exists in your system. Once the index has been built, it will be used to search for information that matches the customer information you provide.

1.  Select **Build Index** from the Quantum main menu (Security | Initial Data Entry | Configure Address FIND Search | Build Index).

2.  The Index is built and a message displays at the bottom of the screen stating the build has been submitted for batch processing.

> **Note:** Once the index has been built, any customer information added after the first build will be automatically added.

## Reserved Words

Words such as Street, Suite, and city names frequently appear in customer address information and if entered in a search, can return meaningless search results. To prevent this from happening, common words can be added to the Reserved Words index which will prevent them from being listed in search results.

> **Note:** An index of Reserved Words is automatically supplied with this feature, but you can delete them or add new ones if desired.

### To Add Reserved Words

1.  Select **Reserved Words** from the Quantum main menu (Security | Initial Data Entry | Configure Address FIND Search | Reserved Words).

2.  The **Maintain Reserved Words** screen opens displaying any existing Reserved Words.

3.  Click the **Add** button.

4.  The **Add Word** screen opens.

5.  Click in the **Type** field and enter whether the Reserved Word you are adding is associated with a customer's name, address, or city.

6.  Type the Reserved Word that you would like to add in the **Word** field and click **Continue**. A message displays at the bottom on the screen stating that the word has been added.

7.  Add another word if desired.

8.  Click **Cancel** to return to the **Maintain Reserved Words** screen.

### Delete a Reserved Word

1.  Select a Reserved Word from the table on the **Maintain Reserved Words** screen and click the **Delete** button.
    > **Note:** You can enter the Type and Word into the fields above the table and click **Enter** to position to the option in the table.

2.  The **Delete Word** screen opens displaying the Reserved Word you selected for deletion.

3.  Click **Continue** to delete the Reserved Word. The Maintain Reserved Words screen re-opens with the word removed from the table and a message at the bottom of the screen stating the word has been removed.

## Configure Find Fields

Once you have built the Index and added/deleted any Reserved Words, you can configure the FIND fields. This option allows you to configure all divisions (Master) or just the division you are working in.

1.  Select **Configure Point of Sale FIND** from the Quantum main menu (Security | Initial Data Entry | Configure Address FIND Search | Configure Point of Sale).

2.  The screen opens in **Master Configuration** by default. Click the **Create Divisional Confg** button if you only want to configure the division that you are working in.
    > **Note:** If the option is currently set for divisional configuration and you want to apply the Master Configuration, click the **Delete Divisional Confg** button. (Divisional or Master Configuration displays above the table indicating which option is currently configured.)

    | Description | Type | Length | Display Length | Search Priority | Required for Entry | Required for Find |
    | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
    | Name | NAME | 28 | 18 | 3 | Y | Y |
    | Extended Name | NAME | 15 | - | - | N | N |
    | Address | ADDRESS | 20 | - | - | N | N |
    | Extended Address | ADDRESS | 20 | - | - | N | N |
    | City, State | CITY | 20 | 11 | 4 | Y | Y |
    | Zip/Postal | ZIPPOSTAL | 9 | - | - | N | N |
    | Phone 1 | AREAPHONE | 10 | 12 | 1 | Y | Y |
    | Phone 2 | AREAPHONE | 10 | 12 | 2 | N | N |

3.  In the **Display Length** column provide the number of search result characters to display for each FIND field.
    > **Note:** A figure must be provided for a Find field to display in the search results. In the example above, search results will only display for Name, City/State, Phone 1, and Phone 2.
    > **Note:** The total number for all Display Length entries cannot exceed 62.

4.  In the **Search Priority** column, assign a priority number to the Find Fields that you assigned a Display Length.

5.  In the **Required for Entry** column, specify whether or not each field must be filled out on the Add New Cash Customer screen to enter a new customer into the system. Enter **Y** for yes and **N** for no.

6.  In the **Required for Find** column, specify each field that must be filled out on the Add New Cash Customer screen to conduct a search on it. Enter **Y** for yes and **N** for no.

7.  Click **Enter** to save your specifications.

## Set Search Options

Once you have configured the Find fields, the search options need to be set to determine what is required for search results to be selected/displayed.

1.  Click the **Master Configuration** button on the Configure FIND Fields screen. The Master Configuration screen opens.

2.  Click the **Priority** drop-down arrow and select whether **ALL** or **ANY** of the search priority assignments must be found in order for customer information to display in the search results. Selecting the **Any** option will conduct a more in-depth search.

3.  Click the **Criteria** drop-down arrow and select whether **ALL** or **ANY** of the fields you provide information for on the Add New Cash Customer screen must be found in order for customer information to display in the search results. Choosing the **Any** option will conduct a more in-depth search.

4.  Click the **Find Method** drop-down arrow and select whether the search results must **contain**, **start with**, or **equal** the information provided on the Add New Cash Customer screen. Choosing the **Equal** option will produce a more precise list of search results.

5.  Select the **Include digits** check box if you would like to search for any digits entered for the customer when they were added into the system through the Add New Cash Customer screen.

6.  Click **Accept** to save the search options you selected.

## Conduct Search/Add a New Customer

When adding a new cash customer in P.O.S. after the Prevent Duplicate Address option has been turned on and all options have been configured, the fields on the Add New Cash customer screen that you designated Required for Entry and Find (Search) will have Plus signs and Asterisks next to them.

*   If you would like to search and see if the customer is already entered into the system, you can enter information in the fields with an asterisk next to them and click **OK**.
*   If you are sure that the customer does not have an existing address number and do not want to conduct a search, select the **Bypass Search** check box to add the customer immediately.

1.  Select **Invoicing** from the Quantum main menu (P.O.S. | Invoicing) and click **Enter** after you have provided your printer information.

2.  On the Invoicing Entrance screen, provide the code for the Document Type that you are creating and click **Enter**.

3.  The **Add New Cash Customer** screen opens. Provide information in the fields designated as "Required for search" and any other fields that you want to conduct a search for existing information on, then click **OK**.

4.  The **Point of Sale – Find Address List** screen opens displaying any incidences where existing customer information matches what you provided on the Add New Cash Customer screen.
    > **Note:** If matching information for fields not selected to display on the Configure FIND fields screen is found, a message will display at the bottom of the screen stating "*Matching criteria was found on data not displayed" and an asterisk will display next to the address line in the table.

5.  If you find information in the search results that you think matches the customer, highlight the entry and click the **Display** button to view the information on the **Show Address Data** screen.

6.  When you are done viewing the address information, click **Exit** to return to the **Find Address List** screen.

7.  Repeat Steps 5-6 until you have found the customer's information or are sure that they do not exist in the system, then do one of the following:
    *   If you find the customer's address information, highlight the address line on the Find Address List screen and click the **Select** button. The Invoicing Entrance screen will re-open with the customer address number displayed in the Address field. Click **Enter** to proceed with creating the document.
    *   If you do not find the customer's address information, click the **Bypass** button on the Find Address List screen. The Add New Cash Customer screen re-opens. Select the **Bypass Search** check box, add the customer information, and click **OK** to add them to the system and proceed with creating the document.


title: "Quantum_Admin"
source: "Quantum_Admin.pdf"
tags: ["Quantum Admin", "User Management", "Theme Customization", "Security Maintenance", "DIS", "Roles", "Permissions", "UI Configuration", "System Administration"]
version: "1.0"
last_updated: "2024-05-24"
short_description: "A guide to the Quantum Admin module, detailing how to customize the user interface theme (colors and logos) and manage user access, including adding users, assigning administrative roles, and updating permissions."
long_description: "This document serves as a comprehensive manual for the Quantum Admin functionality within the DIS Quantum system. It provides step-by-step instructions for system administrators to access the administration panel through Security Maintenance. The guide is divided into two main parts. The first part covers theme customization, explaining how to set colors and logos for the Quantum interface across the entire enterprise, specific filesets, or individual divisions. It details the process of selecting colors, uploading logo files (png, jpg, gif), managing saved logos, and applying changes. The second part focuses on user and role management. It outlines the procedures for adding new users, defining their credentials, and assigning specific administrative roles such as Administrator, User Creation, Theme Changes, and Quantum Remote Access. The document also explains how to update existing user information, change passwords, and remove users from the system."