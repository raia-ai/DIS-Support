---
title: "AGCO API Part Inventory Transmissions"
source: "combined_Keyston.md"
tags: ["Keystone"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about AGCO API Part Inventory Transmissions."
long_description: "This document provides information about AGCO API Part Inventory Transmissions from the DIS Keystone system."
---

## Introduction

These instructions are for dealers who use AGCO API to transmit their daily AGCO parts inventory files to AGCO to display Parts Locator info on the AGCO Website and/or generate Suggested Stock Orders.

Every night that your DIS Backup is scheduled to run, the business system will create a fresh file containing your current AGCO parts inventory information and transmit that file to AGCO.

In order for AGCO to receive your daily parts inventory files:
- The Interface Manager program must be running when the Business System sends the file during your nightly DIS Backup.
- The PC that is designated to transmit the data file to AGCO must be turned on. Once you determine which PC is transmitting your AGCO API files, DIS strongly suggests that you put a label on the PC that reminds users NOT to turn it off!

> **WARNING**
> **Do NOT turn off this PC !**
> **This PC transmits AGCO API files during the nightly system backup.**

**Important**: Different PCs may be used in your dealership to communicate with AGCO for API, Credit Cards, and Parts Orders. It is important to identify which PC is configured to transmit your parts inventory files to AGCO.

## To Determine Which PC is Configured to Transmit the API Data:

1.  Select **Electronic Commerce Configuration** from the Keystone menu (`Security | Electronic Commerce Menu | Electronic Commerce Configuration`). The Electronic Commerce Configuration screen opens.
    
    *Image: The Electronic Commerce Configuration screen showing a table with vendor information.*
    
    | Ven | Name | Com Ver | Description |
    | :--- | :--- | :--- | :--- |
    | AGC | AGCO TEST | AGC | 500 AGCO Communications |

2.  Find and select your AGCO vendor, then click the **Parameters** button.

3.  The Configure Communication Devices screen opens. **DO NOT MAKE CHANGES TO THIS SCREEN.**

    *Image: The Configure Communication Devices screen, highlighting the Workstation Name for the AGCOFTP transaction.*
    
    | Transaction | Description | Workstation Name |
    | :--- | :--- | :--- |
    | AGCOFTP | Parts Load via FTP | HOLT |

4.  Find **AGCOFTP** in the Transaction column and make note of the Workstation Name assigned to the transaction. In this example, the Workstation name is **Holt**.

5.  Return to the Keystone main menu by clicking the **Back Arrow** on the Keystone tool bar.

6.  Press **Alt + A** on your keyboard to open an AS400 Command Line.

7.  Type `d u` (d space bar u) in the field and click **OK**.

8.  The Work with User Jobs screen opens.

    *Image: The Work with User Jobs screen showing active jobs.*

    | Job | User | Type | Status | Function |
    | :--- | :--- | :--- | :--- | :--- |
    | HOLTA | JASONH | INTER | ACTIVE | MNU-MASTER |
    
9.  Find the name that was listed in the Workstation Name column (**Holt** in this example) on the Configure Communication Devices screen in the **Job** column on the Work with User Jobs screen.
    **Important**: The name that is listed in the Workstation Name column will be listed with a letter after it. This indicates that the PC has multiple sessions active.

10. The second column of the Work with User Jobs screen lists the User login for the employee (**JasonH** in this example). So in this example, if you can find User JasonH, and see his sessions running on the PC named HOLT, this is the PC that is configured to transmit the AGCO API files.

In Summary, in order for your AGCO API files to transmit at night with your DIS Backup, the PC of the user for the job/workstation assigned to the transaction AGCOFTP must be turned on with the Interface Manager Program running.

## To Determine if your Interface Manager Program is Running:

1.  If your system tray is configured to display all icons, you will be able to see the Interface Manager icon (a blue D as shown below) in the lower right hand corner if the Interface Manager is running. System Trays display differently on different PCs; a couple of examples are displayed below.
    
    *Image: Two examples of the Windows system tray showing the blue 'D' icon for the DIS Interface Manager.*

2.  Click on the Interface Manager icon to open the DIS Interface Manager screen.
    
    *Image: The DIS Interface Manager window with the 'Electronic Commerce Client' highlighted under the 'Interfaces' section.*

3.  Locate **Electronic Commerce Client (ECC)** in the Interfaces section and make sure there is a blue triangle before it like in the example above. The blue triangle indicates the Electronic Commerce Client is active and ready to transmit your AGCO API files when they are created during the DIS Backup.

    *Image: The Status log in the DIS Interface Manager showing various components starting successfully.*
    
    ```
    Status
    14:34:49 ECC: Manufacturer CLA initialized successfully.
    14:34:49 ECC: Component AGC started successfully.
    14:34:49 ECC: Component CAS started successfully.
    14:34:49 ECC: Component CEN started successfully.
    14:34:49 ECC: Component DIS started successfully.
    14:34:49 ECC: Component FPA started successfully.
    14:34:49 ECC: Component NHD started successfully.
    14:34:49 ECC: Monitoring for manufacturer files....
    14:34:51 ECC: ONLINE: Ready for AGCO Communications.
    14:34:51 ECC ONLINE: Ready for CCN Communications.
    14:34:52 ECC: ONLINE: Ready for Connect2 Communications.
    ```

4.  If there is a stop sign in front of Electronic Commerce Client in the Interfaces section, the Electronic Commerce Client is not currently running. Click on the blue triangle on the toolbar to start it.
    
    *Image: The DIS Interface Manager showing a stop sign icon next to 'Electronic Commerce Client', indicating it is not running.*

5.  A message in the Status box states **ECC: ONLINE Ready for AGCO Communications**.

    *Image: The Status box in the DIS Interface Manager with the message '14:34:51 ECC: ONLINE: Ready for AGCO Communications.' highlighted.*

## Additional Information

In the event that there is a power outage or an interruption in your internet service during the night, the Business System will attempt to resend the API files at 9 am (your time) the following morning, but to ensure that your inventory information is reported correctly on the AGCO Dealer Website and your suggested stock orders are accurate, it is very important that AGCO receive your data during the night when possible.

If you have questions please contact the DIS Response Line by phone at 1-800-426-8870 or via email at [SUPPORT@discorp.com](mailto:SUPPORT@discorp.com).


title: "Associated Addresses - Keystone"
source: "Associated_Addresses_-_Keystone.pdf"
tags: ["associated addresses", "customer grouping", "sales ranking", "Keystone software", "DIS", "address maintenance", "receivables maintenance", "reporting", "data management"]
version: "1.0"
last_updated: "2026-01-18"
short_description: "A guide on using the Associated Addresses feature in Keystone software to group multiple customer accounts for consolidated viewing and reporting of sales data, history, and service units."
long_description: "This document provides a comprehensive walkthrough of the 'Associated Addresses' feature in the DIS Keystone system. This feature allows users to group multiple customer addresses under a single primary address, enabling a holistic view of the group's performance. The guide covers the entire lifecycle of managing these groups, including how to create associations through various menu options like Address Maintenance, Receivables Maintenance, and Sales Ranking. It details the process of defining primary and secondary addresses and using the 'Use Instead' or 'Combine Address' features. The document also explains how to view collective data for these groups in modules such as Sold Units Inquiry, Part Sales History (including Transaction and Summary reports), and Inquire/Update Service Units. Furthermore, it outlines procedures for deleting associated address groupings, excluding specific customers from a group, and removing those exclusions. The guide uses screenshots and step-by-step instructions to clarify the process of associating, viewing, and managing customer address groups for enhanced sales analysis and reporting."