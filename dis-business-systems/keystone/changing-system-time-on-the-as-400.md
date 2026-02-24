---
title: "Changing System Time on the AS/400"
source: "combined_Keyston.md"
tags: ["Keystone"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Changing System Time on the AS/400."
long_description: "This document provides information about Changing System Time on the AS/400 from the DIS Keystone system."
---

## INTRODUCTION

Daylight Saving Time begins the second Sunday of March and ends the first Sunday in November. While newer systems automatically change the time, the time change should be verified first thing on the following Monday. These instructions cover how to verify the time change occurred and how to correct the time if it did not.

> **Note**: Some operating systems are set to change time at the previous Daylight Saving Time intervals (First Sunday of April/Last Sunday of October). As a safety precaution, verify your system time first thing on Monday morning following these dates.

## INSTRUCTIONS

1.  Press the **Alt** and **A** keys on your keyboard at the same time or select **AS/400 Command Line** (System | AS/400 Command Line) from the Keystone main menu. The AS/400 Command line opens. Type `WRKSYSVAL QHOUR` in the provided field and click **OK**.

    *   **AS/400 Command**
    *   `WRKSYSVAL QHOUR`

2.  The **Work with System Values** screen opens. Highlight the **QHOUR** line and click the **Display** button.

3.  The **Display System Value** screen opens displaying the current **Hour** setting on the system. If the hour setting is correct, click **OK** twice to return to the Keystone main menu. If the hour setting is not correct, proceed with the instructions on the next page.

4.  Click **OK**. The **Work with System Values** screen re-opens. Highlight the **QHOUR** line and click the **Change** button.

5.  The **Change System Value** screen opens. Click inside the **Hour** field and type the correct hour of the day. Remember to use military time if it is after noon.

6.  Click **OK** twice to return to the Keystone main menu.

## If you use Time Clock

*   Verify and if need be change your system time before anyone signs into Time Clock. Otherwise, wait until after everyone has clocked out for the day before changing. Changing the system time while technicians are clocked in can result in an hour being added to the staff's time.

*   If your main store is in a state that does not observe Daylight Saving Time AND you have stores in other states that do observe Daylight Saving Time, contact DIS for assistance with your Time Clock configuration: 800-426-8870.