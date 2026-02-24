---
title: "Service Scheduling"
source: "combined_Quantum_docs.md"
tags: ["Quantum"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Service Scheduling."
long_description: "This document provides information about Service Scheduling from the DIS Quantum system."
---

## Introduction

The Service Scheduling option allows you to schedule work events for technicians from an existing work order or from scratch. Once an event has been scheduled, you can continue to add information to it as a Planned Work event and if desired, convert it to a Work Order.

In order to use this option, you must have Time Clock with Technician View installed/turned on. Contact the DIS response line for assistance at 1-800-426-8870 or Support@discorp.com.

A one-time setup fee is required for Service Scheduling. For more information or to order Service Scheduling, contact DIS sales at 1-800-426-8870 or Sales@discorp.com.

## Service Scheduling Layout and Setup

The Service Scheduling option consists of several individual features and sections that make up the option as a whole and allow you to perform a variety of actions. This section introduces each individual feature/characteristic to allow a more thorough grasp of how they all work together.

1.  Select **Technician View** (P.O.S. | Time Clock | Technician View). The Technician View screen opens displaying the current Now Working On punches.
2.  Click the **Service Schedule** button. The Service Schedule screen opens displaying the service schedule on the left side and the service table on the right.

> To expand either side, hover your cursor over the green dividing line until the handlebars appear, then click your mouse and pull to expand the side you would like to view.

## Viewing Options

An option exists that allows you to control how the available information displays. You can select the default view which displays both the Service Schedule and Service Table. You can also select to only view the Service Schedule OR the Service Table.

1.  Click the **Settings icon** in the upper-right corner of the screen. The Settings screen displays. Select the **Options Tab** if it is not already selected.
2.  In the **View** section, do one of the following:
    *   **Schedule and Grid:** Select this option to view both the schedule and the table (default setting).
    *   **Schedule Only:** Select this option to just view the Service Schedule.
    *   **Grid Only:** Select this option to just view the grid (Service Table).

## Service Schedule

This section of the document provides an overview of the Service Schedule section. When the Service Schedule option is opened, the entire current day displays by default.

The current schedule period being displayed is indicated in the title fields just below the task bar. The current time is indicated by a red circle with a line extending from it.

All employees currently punched into time clock in the division that you are working in display in the **Staff** column to the left of the schedule.

### Staff Column

When you initially enter the Service Schedule option, all staff that punch into time clock are listed in the Staff column. To limit the employees listed in the column to just technicians:

1.  Click the **Exit Arrow** in the upper-left corner to return to the Technician View screen.
2.  Click the **Define List** button. On the Define List screen that opens, select each job code (department) not assigned to technicians and click the **Include/Exclude** button. Only employees assigned to job codes with a **Y** in the Include column will display in the Staff column.

> **Note:** Job codes are assigned to each employee through (Accounting | Payroll | Payroll (Full Access)).

You can also control the employees listed in the Staff column and the order in which they are displayed through the drop-down menu on the right side of the Staff column header. Click the drop-down arrow:

*   Select **ascending/descending** to change the order in which the technicians are listed.
*   Select the checkboxes for the employees you would like to display on the schedule. Unselect the check boxes to remove them.

> **Note:** Leaving the Filters check box unselected will list all employees for the division that are currently punched in with a job code that has not been excluded through the Define List option.

The **0-UNASSIGNED** entry in the first position of the Staff column displays by default. This row can be used as a staging area to allow a visual representation of the work that needs to be completed for the day but is yet to be assigned to a technician. Remove this entry by unselecting the 0-UNASSIGNED check box.

## Task Bar

There are multiple options on the Task Bar that allow you to control the information that displays in both the service schedule and service table.

*   **Exit Arrow**: Click to return to the Quantum Technician View screen.
*   **Date field and Scroll button**: Allow you to position the schedule to the day of your choice. Enter the date you would like to view on the schedule in the Date field and click the **Scroll** button to position to that date. Alternatively, you can click the calendar icon in the Date field and select the date from the calendar that appears.
*   **Zoom buttons**: Click to increase or decrease the length of the time periods shown on the schedule. The Service Schedule can be viewed in several different lengths of time, ranging from 2-minute increments to years.
*   **Refresh button**: Click to update the entries on the schedule. Since multiple employees can schedule jobs at the same time, an entry may occur while you are working with the schedule. Clicking the Refresh button will display an up-to-date Service Schedule.
*   **Search field**: Enter search terms to locate information on the schedule OR in the service table. Entries that do not match the search terms will be removed from both sections.
*   **Reload Schedule button**: Click to reload the schedule to the default view. The default view is the current day broken down into hourly increments.
*   **Settings button**: Click to work with View and Refresh options as well as Category Tags, Status Tags, or Reason Codes.

### View and Refresh Options

If you select the Options Tab on the Settings screen, you can configure which view you would like to display (as discussed previously in this document), the Auto Refresh interval, and/or the Auto Scroll option.

*   **Auto Refresh**: The Auto Refresh option allows you to control how often the service schedule information is updated. Select the **Enable** check box and enter the amount of time to wait before updating the information. Time can be entered in 15 second intervals. In the screen shot example, the information in the Service Schedule/Table is updated every minute and 45 seconds.
    > **Note:** The interval time begins when there isn't activity (mouse movement/keystrokes) on the associated PC. The refresh timer restarts with any activity with the displaying PC.
*   **Auto Scroll**: The Auto Scroll option automatically returns the Service Schedule view to either the current time or noon on the current day every time the information is refreshed. In order to configure this option, you must also have the Auto Refresh option configured.

### Category Tags, Status Tags, and Reason Codes

Once the Settings screen is open, click on the tab for the Setting you would like to configure. Configuration options for each of these settings is described below:

*   **Category Tags**: These are dealership defined, but is intended to represent the que for the item. You can add as many category tags as desired and edit or delete them any time. Category tags can be assigned any available priority level, but it is not required.
*   **Status Tags**: These are dealership defined, but is intended to represent the order within the que. You can add as many status tags as desired and edit or delete them anytime. Status tags can be assigned any available priority level, but it is not required.
*   **Reason Codes**: Reason codes are added, edited, and/or deleted in Table Maintenance (P.O.S. | Table Maintenance). Priority levels can be assigned to Reason codes if desired.

When you have finished configuring the settings, click **Exit** to return to the Service Scheduling screen.

## Service Schedule Event Indicators

When viewing a populated schedule, there are several indicators applied to the scheduling events that provide specific details. These indicators are defined below.

> **Note:** The process of scheduling an event is covered in the Schedule an Event section.

*   **Time Clock Punches**: Closed Technician time clock punches will display as an all-gray scheduling event. Open Time clock punches will display as a gray scheduling event with a colored bar across the bottom that matches the division color.
*   **Scheduled Events (from Service Table)**: Scheduled events that are associated with an event in the Service Table, but not a time clock entry, will display in the color assigned to the division.
*   **Standalone Scheduled Events**: Scheduled events that are not associated with an event in the Service Table such as vacation and appointments will display with a light blue background color.
*   **Top Line**: The top line of a scheduled event displays the customer name and make/model for the unit OR the description if customer name and make/model are not available.
    > **Note:** The customer must be tracked as a contact in order for their name to display. If not, a blank space may display.
*   **Bottom Line**: The bottom line of the scheduled event displays the reason code, work order number, segment #, and/or segment title/planned work event title.
*   **Priority Bar**: If a schedule event has a priority assigned to it, a bar displays across the top of the event indicating the priority level that is assigned.
    > **Note:** If an event has more than one priority level assigned to it, the highest priority level displays.
*   **Customer Type Circle**: A circle with a specific color and the initial I (blue), W (red), or C (green) indicates whether the planned work has been assigned a customer type of Internal, Warranty, or Customer.
*   **Reason Code**: If planned work has been assigned a reason code, the reason code will be included in the event and placed within parentheses.
*   **Customer Address Number**: If a work order is opened to a customer address number, that number will always display, even if the items are designated as customer, internal, or warranty.
*   **Internal Unit**: If the work order has been opened to an internal unit, the unit will display in the event along with the associated division.
*   **Multiple Job Codes**: If multiple job codes are included on a time clock entry, they will all be combined into a single entry on the Service Schedule.

Any changes made to a work order will instantly be updated and reflected in the event on the schedule.

## Service Table

All of the current work orders that are designated a W type document within the division are automatically imported into the service table when the Service Scheduling option is enabled. Planned Work events will be added to the service table as you create them.

### Service Table Column Information

Most of the columns of information within this table are self-explanatory and can be determined by hovering your cursor over the column header. Definitions for more complex column information are provided below.

*   **Expansion Icon (+)**: Click to view an easy-to-read layout of the basic details about the work.
*   **P (Priority) column**: If the work order has been assigned a tag or reason code that has an assigned priority level, the highest priority level will display in this column. Priority level colors are assigned by DIS.
*   **S (Scheduled) column**: If the work order has been placed on the schedule at any time, this column will have a selected check box.
*   **Latest column**: Provides the most recent date that the event was placed on the schedule.
*   **Labor Group column**: Lists the class to which the work order is assigned. There are 5 classes:
    1.  **Labor Ready**: Open work orders with parts or other dollar items on them. These work orders do not have labor on them.
    2.  **In Process**: Open work orders that have labor lines posted within a dealership-defined threshold.
        > **Note:** The threshold is setup during the installation process – DIS recommends 14 days.
    3.  **Check Close**: Open work orders with all labor lines posted after a dealership-defined threshold.
    4.  **New**: Work orders with a zero-dollar amount.
    5.  **Closed**: Work orders with a closed status.
*   **Wip "..." columns**: List information that was added to the service note section on the work order.
*   **RC Code and RC Description columns**: Reflect the Reason Code employed on the transaction line.
*   **Address Columns**: Columns listing All Customer and Ship-To (Street) addresses can be added to the table, but are hidden by default. This information also displays in expanded view or when hovering over a scheduled event.
*   **Segmented Work Order**: If a work order is segmented, the work order will display as a whole on the top line with each segment of the work order listed below it.

## Arrange Service Table Information

The service table allows you to arrange the information in the table to best suit your needs. Hovering your cursor over a column header and clicking the drop-down arrow will provide you with some or all of the following options for that column:

*   **Sort Ascending/Descending**: Use this option to select whether the information in the table is displayed in ascending or descending order according to the information in that column.
*   **Columns**: Hover over columns and select which columns you want to display in the table. Check boxes will appear. Select the check boxes for the columns that you want to display in the table. Unselect check boxes to remove the columns from the table.
*   **Group by this field/Show in Groups**: Select this option to list the information in the table by clusters of matching entries in the specified column.
*   **Filters**: Hover over this option to produce a filter field. Enter filters to determine the information that is displayed in the table. A filter can be set on multiple columns at the same time.
    > **Note:** Headers for columns that have a filter applied will be italicized.
*   **Reorder Columns**: Change the order in which columns are displayed by clicking on a column header and dragging it to the desired location. A double-arrowed green line indicates where the column will be placed.
*   **Reset Page**: Click the **Reset Page** button in the bottom-right corner to reset the table to the original default setting.

## Create Planned Work/Convert to Work Order from Service Table

You can create, edit, and delete Planned Work events using the buttons in the lower-left corner of the service table (`New`, `Edit`, `Delete`).

> **Note:** You can also create and work with events directly through the service schedule as part of the scheduling process. (See the Schedule an Event section below.)

### Create Planned Work Event

1.  Click the **New** button in the bottom-left corner of the service table. The Planned Work screen opens.
2.  Enter all of the available information for the event. You must click the Document Type drop-down arrow and select one of the available W document types.
    *   You can conduct searches for customers and/or units by clicking the **Search** button in the respective section. Searches can be conducted on more than one search term by placing a space in between each term.
    > **Note:** In order for a customer to be located through the search process, they must be tracked as a contact in the system.

### Edit or Delete Planned Work Event

Until a Planned Work event has been converted to a work order, you can add additional information to it and edit most of the existing information. You can also remove it from the system.

1.  Select the event from the service table and do one of the following:
    *   **To Edit**: Click the **Edit** button. The Planned Work screen opens allowing you to add or edit information. Click **OK** to save your changes.
    *   **To Delete**: Click the **Delete** button. The Delete Service Scheduling screen opens. Click **Yes** to remove the Planned Work event from the system.

### Convert Planned Event to Work Order

Once a customer address number or unit number has been added to the Planned Work Event, it can be converted to a work order by clicking the **Convert to WO** button at the bottom of the Planned Work screen.

> **Note:** Once a Planned Work event has been converted to a work order, it can only be deleted through P.O.S. Invoicing.

## Schedule an Event

There are two ways that an event can be scheduled:

*   Select an existing event in the service table and drag it to the desired position on the schedule.
*   Click and drag your mouse over a specific time frame to create a new event directly on the schedule.

### Schedule Event from Service Table

1.  Click the event in the table that you would like to add to the schedule.
2.  While holding down the button on your mouse, drag and drop it on the technician's line on the schedule where you would like to begin the event. As you drag your mouse over the schedule, the time updates to indicate where the event will begin if you dropped it.

### Create an Event on the Schedule

1.  Click on the technician's line in the schedule at the time that you would like to begin the event and drag for the length of time that you would like the event to last. The event screen opens allowing you to provide basic information for the event and confirm the length.
2.  When you have finished adding information, either click **Save** to enter the event with its current information or **Create Work Item** to add additional information on the Planned Work screen.

## Work with Event on Schedule

Once an event has been placed on the schedule, the following actions can be taken:

*   **Edit/Add event details**: Double-click on an event to open the event detail screen.
    *   Enter information in the available fields or change existing information and click **Save**.
    *   Click **Delete** to remove the event from the schedule.
    *   Click **Cancel** to return to the schedule without making any changes.
    *   Click **Edit Work Item** to convert the event to Planned Work.

*   **Expand or decrease the length of the event**: By default, work orders that are dragged from the table and dropped onto the schedule are an hour in length. Hovering your cursor over the event displays basic details about the event and produces a set of handle bars on each side. Click the handle bars on the side of the event that you want to expand or decrease and drag in that direction. As you pull, two clocks appear showing the duration of the event if you were to release your mouse.

*   **Move the event**: To move the event, click on it and drag it to the desired location.

*   **Remove the event from the schedule**: Right-click on the event and then click **Delete event**. This does not remove the planned work from the table, just the schedule.

> **Note:** Time clock punch events cannot be deleted through Service Scheduling.


title: "Unit_Locator_Service_Configuration"
source: "Unit_Locator_Service_Configuration.pdf"
tags: ["Quantum Admin", "Unit Locator", "Inventory Management", "Configuration", "TractorHouse", "Dealer Spike", "DIS", "Software Guide", "Fastline", "Iron Solutions"]
version: "1.0"
last_updated: "2024-05-23"
short_description: "A technical guide on how to configure the Unit Locator Service feature in Quantum Admin. This document details enabling services, assigning inventory to categories, and managing individual unit postings."
long_description: "This document provides a comprehensive walkthrough of the Unit Locator Service Configuration within the Quantum system. The Unit Locator feature enables users to post information about inventory units to six different external unit locator services, such as TractorHouse, Tom Rowe, and Fastline. The guide covers the initial setup process in Quantum Admin, including how to enable specific locator services, define which units (new, used, or both) are included, and set a default to send all available units automatically. It further explains how to assign specific make/model combinations from inventory to the corresponding description and code categories provided by each service. The document differentiates between services that allow category mapping (TractorHouse, Tom Rowe, Fastline) and those that do not (Dealer Spike, Team SI, Iron Solutions). Additionally, it details the process for making assignments for individual units through the Inquire/Update Units screen, allowing for overrides of the default make/model configurations. Finally, it explains how to use the 'View All Unit Assignments' screen to review, sort, filter, and export a comprehensive list of all current unit locator service assignments."