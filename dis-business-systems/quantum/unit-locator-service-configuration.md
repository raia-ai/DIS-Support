---
title: "Unit Locator Service Configuration"
source: "combined_Quantum_docs.md"
tags: ["Quantum"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Unit Locator Service Configuration."
long_description: "This document provides information about Unit Locator Service Configuration from the DIS Quantum system."
---

## Introduction

The Unit Locator Service feature allows you to post information on units in your inventory to 6 different unit locator services. Some services allow you to assign unit make/model combinations in your inventory to their unit description and code categories. Assignments can be made to entire make/model combinations through Quantum Admin or to individual units through Inquire/Update Units.

This document covers how to enable unit locator services, configure which unit information is available, and assign make/model combinations to unit locator service descriptions and codes when available.

For best results, ensure all of the units in your inventory have the correct Make/Model assignments. Click here to view a document on how to correct or change any incorrect Make/Model assignments.

## Enable Unit Locator Services in Quantum Admin

1.  Select the **Unit Locator** tab in Quantum Admin. The Unit Locator Configurations for File Set screen opens.

    *   **Unit Locator Configuration Screen:**
        | Unit Locator Service | Unit Locator Enabled | New/Used | Send Units To Unit Locator By Default | Actions |
        | :--- | :---: | :---: | :---: | :--- |
        | TRACTORHOUSE | ☑ | Used | ☐ | Edit Unit Locator Make/Model Assi... Reload Categories |
        | TOMROWE | ☑ | Used | ☐ | Edit Unit Locator Make/Model Assi... Reload Categories |
        | FASTLINE | ☑ | Both | ☐ | Edit Unit Locator Make/Model Assi... Reload Categories |
        | DEALERSPIKE | ☐ | Both | ☐ | Edit Unit Locator Make/Model Assi... Reload Categories |
        | TEAMSI | ☐ | Both | ☐ | Edit Unit Locator Make/Model Assi... Reload Categories |
        | IRONSOLUTIONS | ☐ | Both | ☐ | Edit Unit Locator Make/Model Assi... Reload Categories |

2.  Do the following for the unit locator services(s) you would like to enable:
    *   Select the **Unit Locator Enabled** check box to provide unit information to the specific provider.
    *   Click the **New/Used** drop-down arrow and select whether you would like to include information on units designated as new, used, or both new and used when submitting unit information to the unit locator service.
    *   Select the **Send Units to Unit Locator by Default** check box to send all units with an Available status to the specified unit locator service.

> **Note:** Unit locator service descriptions and codes are automatically updated every night. If you would like to immediately refresh the categories for a service, click the **Reload Categories** button on the service line.

## Assign Specific Unit Make/Model to Unit Locator Service Descriptions/Codes

You can assign specific make/model combinations from your system to the Category Descriptions/Codes provided by the TractorHouse, Tom Rowe, and Fastline unit locator services.

> **Note:** This option does not exist for the Dealer Spike, Team SI, and Iron Solutions services. You can submit information to these unit location services for all available units by selecting the **Send Units to Unit Locator by Default** check box or for individual units through the Inquire/Update Units option.

In order for make/model combinations to be available for assignment, there must be a unit of that make/model in your inventory with an Available status.

1.  Click **Edit Unit Locator Make/Model Assignments** for the unit locator service that you would like to configure. The `Edit UEL make/model Assignments for:` screen opens for that service.

    *   **TRACTORHOUSE Assignment Screen:**
        | Make | Model | Category Description | Unit Locator Category | Action |
        | :--- | :--- | :--- | :--- | :--- |
        | CASE | CX36B | Tractors 100 HP to 174 HP | 1109 | Clear Assignment |
        | ... | ... | ... | ... | ... |

    > **Note:** The left side of the table lists every make/model combination that currently has a unit in your inventory assigned to it with an Available status.

2.  Locate the make/model combination to configure and click the **Category Description** OR **Unit Locator (Code) Category** drop-down arrow on the same line. Scroll and select the description or number you would like to assign.

    For the Dealer Spike, Team SI, and Iron Solutions unit locator services, click in the Description or Unit Locator field and enter your dealership-defined assignment.

    *   **DEALERSPIKE Assignment Screen:**
        | Make | Model | Category Description | Unit Locator Category |
        | :--- | :--- | :--- | :--- |
        | BISHOP | 580SK | Backhoe | 54321 |
        | BUSHHOG | 2610L-12 | | |

3.  Click the **Save All Changes** button to save the assignment.
    
    > **Note:** To remove an assignment, click the **Clear Assignment** button, then click the **Save All Changes** button.

## View All Unit Assignments

The Unit Locator option in Quantum admin allows you to view all of the current unit locator service assignments for units in your inventory.

1.  Click the **View All Unit Assignments** button at the top of the Unit Locator Configuration screen.

    The Unit Locator Unit Assignments screen opens displaying a variety of information about the units.

    You can setup the table to best meet your needs.
    *   Click on the drop-down arrow for any column header and re-organize the contents in the table by that column's contents in ascending or descending order.
    *   Click on the drop-down arrow for any column, hover your cursor over the `Columns` option, and select or unselect the check boxes on the list of available columns that displays. Select a check box to display the column or unselect it to remove the column.
    *   Click on the drop-down arrow for any column, and provide a filter to only list matching contents in the table. You can apply filters to multiple columns. When a filter is applied, the column header becomes italicized and bolded as shown below.
        *   *Example: Filtering by Make "KUBOTA" and Model "B2320".*
    *   Re-order the columns by clicking on a column header and dragging it to the desired location. A check mark in a green circle and arrows indicate where the column will display.
    *   Export the contents displayed in the table to an Excel spreadsheet by clicking the **>Excel** button.

## Configure Unit Locator Services Assignments by Individual Unit

In addition to configuring unit locator service assignments by make/model combination, you can make assignments to individual units through the Inquire/Update Units option. Assignments can be changed as desired.

1.  Select **Inquire/Update – Complete Access** (`Units | Inquire/Update – Complete Access`). The Unit Selection screen opens.
2.  Select the unit that you would like to make Unit Locator service assignments for and click the **Update Unit** button. The Unit Information screen opens displaying basic information.
3.  Click the **Unit Locator** button on the lower left of the screen. The Unit Locator Configuration screen opens showing any current Unit Locator service assignments for the unit.

    > **Note:** The unit locator services must be activated in Quantum Admin to be configured in this option.

    *   **Initial Unit Locator Configuration Screen (per unit):**
        | Provider | Category Desc | Category Code | Send To Unit Locator |
        | :--- | :--- | :--- | :---: |
        | TRACTORHOUSE | Use Default | | ☐ |
        | TOMROWE | Use Default | | ☐ |
        | FASTLINE | Use Default | | ☐ |
        | DEALERSPIKE | Categories Not Required For This Provider | | ☐ |
        | TEAMSI | Categories Not Required For This Provider | | ☐ |
        | IRONSOLUTIONS | Categories Not Required For This Provider | | ☐ |

    If the Unit is currently set to the default for the unit locator service, do one of the following:

    **For TractorHouse, Tom Rowe, and Fastline services**
    *   Click the Default/Override drop-down arrow for the unit locator services that you would like to configure and select **Unit Override**. The Category Description field becomes available.
    
    **For Dealer Spike, Team SI, and Iron Solutions services**
    *   Select the **Send to Unit Locator** check box to submit this unit's information to the Unit Locator service and proceed to Step 5.

4.  Click the **Category Description** or **Category Code** drop-down arrow and do one of the following:
    *   Type the description or code that you would like to apply. The list of options is filtered to reflect your entry. Select the desired option. Both fields populate.
    *   Scroll through the list of options until you find the description or code that you would like to assign to the unit and select it. Both fields populate.

5.  Select the **Send to Unit Locator** check box to submit this unit's information to the Unit Locator service.

6.  A red triangle in a field corner indicates that information has not been saved. Click the **Save Changes** button. A message displays stating the save was successful.

7.  Repeat Steps 2 through 6 to configure unit locator service assignments for any additional units.

    > **Note:** To remove assignments, click Unit Override drop-down arrow, select **Use Default**, then click the **Save Changes** button.