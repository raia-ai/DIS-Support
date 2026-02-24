---
title: "Quantum Admin"
source: "combined_Quantum_docs.md"
tags: ["Quantum"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Quantum Admin."
long_description: "This document provides information about Quantum Admin from the DIS Quantum system."
---

## Introduction

Quantum Admin allows you to set the theme (colors and logos) that displays on the Quantum interface for all divisions within every fileset, all the divisions within a specific fileset, or a single division. As you create or update a theme, a live preview displays in the lower portion of the screen allowing you to view it before implementation.

Quantum Admin also allows you to specify the Users who have access and designate the roles that are assigned to them.

## To Access Quantum Admin

1.  Select **Security Maintenance** (`Security` | `Security Maintenance`) from the Quantum main menu. The Security Maintenance screen opens.

2.  Enter your master security code in the **Division Code** field and click **Enter**. The Security Maintenance master screen opens.

3.  Click **Users Authority & Quantum**, then click the **Quantum Admin** tab that displays.

    > **Note:** Turn off the pop-up blockers if the Quantum Admin tab does not display.

4.  The Quantum Admin screen displays. Select the **Theme** tab if it is not already selected.

## To Setup and Apply Themes

The following instructions cover the entire process of setting up and applying themes. You can choose to complete any or all of these options at any time. The lower section of the screen allows you to preview the changes as you make them.

### Specify fileset(s) or division(s) to apply theme

-   Highlight the fileset(s) or division(s) that you would like to assign the theme. If you would like to assign the theme to all filesets and divisions, select the **Enterprise** folder.

### Specify interface color

-   Select the color to assign to the theme from the **Color** section (e.g., Blue, Green, Orange, Red, Yellow).

### Upload logo

1.  Click the **Select Logo** button.
    > **Note:** The logo must be saved as a .png, .jpg, or .gif file.
2.  On the screen that appears, navigate to and select the logo file that you saved on your computer, then click **Open**.
3.  Click the **Upload** button. The uploaded file will display in the **Available Logos** field.

### View, apply, or delete saved logo files

-   All saved logos display in the **Available Logos** field.
    -   Click on any logo file name to apply it to the selected fileset(s) or division(s).
    -   Click the **Delete** button to the right of any logo file name to remove it from the system.
    > **Note:** If you do not want to display a logo, upload a blank 1" x 1" file and apply it.

### Save Changes or Reset Defaults

-   Click the **Save All** button to save the new theme settings. If you exit Quantum Admin before saving, the new settings will be lost.
-   Click the **Reset To Defaults** button to return to the original theme settings.

> **Note:** You must restart your computer to display the new theme settings.

## To Add New Quantum Admin Users, Assign Roles, and Update

### Add User

1.  Select the **Users** tab on the left side of the screen. The Users screen opens displaying all users already added to Quantum Admin and the roles that have been assigned to them.

2.  Click the **Add User** button.

3.  The **Add User** screen opens.
    -   Enter the new user's E-mail address in the **Username** field.
    -   Enter the new user's position with the dealership in the **Description** field.
    -   Enter a password for the new user. Passwords must be 8 characters in length and contain a number, uppercase letter, and lowercase letter.
    -   Re-enter the password in the **Confirm Password** field. If the same password is not entered, the field will display a red line at the bottom, indicating an error has been made.
    -   Select the **Enabled** check box.
    
    > **Note:** If user access to Quantum Admin ever needs to be temporarily removed, unselect the **Enabled** check box.

### Assign Admin Roles

The following roles are available to be assigned to a user:
-   **Administrator** – This role allows a user to use everything in Quantum Admin. It does not provide them with Quantum Remote Access (QRA).
-   **User Creation** – This role allows a user to add, modify, delete, disable, and enable other users.
-   **Theme Changes** – This role allows a user to make changes to Quantum Admin themes.
-   **Quantum Remote Access** – This role provides a user Quantum Remote Access when connecting to Quantum.

**To assign or remove roles:**

1.  From the **Add User** or **Edit User** screen, locate the **Available Roles** and **Selected Roles** boxes.
2.  Select an available role and click the `→` arrow to assign the role to the user.
3.  Alternatively, select an assigned role and click the `←` arrow to remove the role from the user.
4.  Once a user has been added and assigned roles, click the **Save** button. If you click **Close** before saving, the user will not be added to Quantum Admin.

### Update user roles/password or delete them from Quantum Admin

-   **To remove a user** from Quantum Admin, click the **Delete** button on the same line as the user.
-   **To update an Admin user's password or roles**, click the **Edit** button on the same line as the user. The **Edit User** screen opens.
    -   On the **Edit User** screen, you can modify the user's description, enabled status, and roles.
    -   Click the **Change Password** button to change the user's password. The password fields will display.
    -   Click the **Save** button to save the modifications. If you click **Close** before clicking the **Save** button, updates will not be saved.


title: "Quantum_New_Features_Guide_20v2"
source: "Quantum_New_Features_Guide_20v2.pdf"
tags: ["Quantum", "Release Notes", "20v2", "Management 360", "Customer 360", "Point of Sale", "Parts Management", "Security", "Fleet Management", "DIS"]
version: "1.0"
last_updated: "2024-05-24"
short_description: "This document provides a summary of the primary new features included in Quantum Release 20v2. It details enhancements such as the Management 360 feature for KPI tracking, improved Customer 360 search functionality, updates to parts and inventory management, and new security and reporting options in Point of Sale and Fleet Management."
long_description: "The \"Summary of New Features for Quantum in Release 20v2\" is a guide from Dealer Information Systems (DIS) that outlines the enhancements in the R20v2 update for its Quantum software. The document is structured to walk users through the new functionalities across different modules, often including screenshots for visual reference. Key additions include the 'Management 360' feature, designed to provide Key Performance Indicators (KPIs) to measure business success. The 'Customer 360' module receives an enhanced search feature with additional fields. The 'Parts' module is updated with capabilities to select part lists for returns/phase-outs, the ability to use decimals in bulk quantities, and a new 'Print/Finalize' button for stock orders. For 'Point of Sale' (P.O.S.), the guide details a new \"Remit to\" address for Productivity Plus, security warnings for sales code changes, and new automated report archiving. The document also covers new order download options for Stihl and Kinze, a parts locator for Kobelco, added security gates for P.O.S. invoicing, a second bin location for parts, and an option to print service notes with the Scheduled Maintenance Due Report in Fleet Management."