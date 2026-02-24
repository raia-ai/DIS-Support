---
title: "Perform a Complete System Save"
source: "combined_Keyston.md"
tags: ["Keystone"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Perform a Complete System Save."
long_description: "This document provides information about Perform a Complete System Save from the DIS Keystone system."
---

## Introduction

A Complete System Save provides a backup of the normal business data, queries, user profiles, hardware configurations, business system programs, and the operating system.

Do a Complete System Save (System Backup) before AND after any major hardware or software change, such as adding a remote store or upgrading to the latest release of the DIS program. Even if nothing is changing, a complete system backup should be done **AT LEAST** every six months. A good system backup can be the difference between a two-day recovery and a five-day recovery should a disaster strike.

## Instructions

### Prepare for a Complete System Save

1.  **Delete old backups on tape.**
    *   Open a command line by pressing `Alt` and `A` on your keyboard at the same time.
    *   Type `WRKF DISSAVLIB/*ALL`, and click **OK**. The Work with Files screen opens.
    *   Any files in the format `DISnnnn00a` (where `n` is any number, `a` is any letter) are old backups on disk. You can delete them to save space on the backup tape. If you do not delete them, they will be included in the system save you are performing.

2.  **Calculate how many tapes to initialize.**
    *   Open a command line (`Alt + A`).
    *   Type `WRKSYSSTS` and click **OK**. The Work with System Status screen opens.
    *   Make sure you are in Intermediate mode. Check by clicking **Functions** and choosing the **Select assistance level** option or pressing `Shift + F9` on your keyboard.
    *   Determine the number of tapes you will need for the system save as follows:
        Multiply **SYSTEM ASP** by **% ASP USED**. Divide that number by the size of tapes you will use for the backup, then round up to the next whole number – ie. 2.54 = 3 tapes.
    *   **Example Calculation from System Status:**
        *   System ASP: `211.6 G`
        *   % system ASP used: `30.6178 %`
        *   Total used space: `211.6 G * 0.306178 = 64.79 G`

> **Note:** All tapes must be of the same size or the system save will not work.

### For Systems That Use a Tape Drive

1.  **Initialize the tapes.**
    *   Put the tape in the drive.
    *   Open a command line by pressing `Alt` and `A` on your keyboard at the same time.
    *   Type `INZTAP` and click **OK/Enter**. The Initialize Tape screen opens. Enter the information as shown below.
    > **Note:** If `*CTGTYPE` is not an option you will need to put in the size of tape you are using.

    **Initialize Tape (INZTAP) Settings:**
    ```
    Device . . . . . . . . . . . . . : TAP01
    New volume identifier  . . . . . . : SAVEDS
    New owner identifier . . . . . . . : *BLANK
    Volume identifier  . . . . . . . . : *MOUNTED
    Check for active files . . . . . . : *NO
    Tape density . . . . . . . . . . . : *CTGTYPE
    Code . . . . . . . . . . . . . . . : *EBCDIC
    End of tape option . . . . . . . . : *REWIND
    Clear  . . . . . . . . . . . . . . : *NO
    ```
    *   When the procedure finishes, initialize additional tapes if necessary.
    *   Open a command line (`Alt + A`).
    *   Type `CLROUTQ QEZJOBLOG` and click **OK/Enter**. This will delete old job logs and ensure the system is operating at peak efficiency.

### For Systems That Use an Optical Drive

1.  **Initialize the optical drive.**
    *   Open a command line by pressing `Alt` and `A` on your keyboard at the same time.
    *   Type `INZOPT` and click **OK/Enter**. The Initialize Optical screen opens. Enter the information shown in the screen shot below.

    **Initialize Optical (INZOPT) Settings:**
    ```
    Volume identifier  . . . . . . . . : *MOUNTED
    New Volume identifier  . . . . . . : Saveds
    Device . . . . . . . . . . . . . . : rms01
    Volume full threshold  . . . . . . : *CALC
    Check for an active volume . . . . : *no
    End of media option  . . . . . . . : *LEAVE
    Clear  . . . . . . . . . . . . . . : *NO
    Text 'description' . . . . . . . . : BLANK

    Additional Parameters
    Volume type  . . . . . . . . . . . : *PRIMARY
    Coded character set ID . . . . . . : *CALC
    Media format . . . . . . . . . . . : *MEDTYPE
    ```

### Perform the System Save

*   Make sure you are at the system console (the sign-on screen will show QCTL as the subsystem). Sign on as **QSECOFR**.
*   If you do not have a configured system console, call the Response Line at 800.426.8870 for assistance in setting one up.
*   At the AS/400 main menu, type `DSPMSG QSYSOPR` and click **OK/Enter**.
*   Answer and clear all messages, then click **OK** to return to the main menu.
*   At the AS/400 main menu, type `GO SAVE` and click **OK/Enter**.
*   At the Save menu, scroll down and click **Entire System** in the `Save System and User Data` section.

## Configure Command Defaults

On the Specify Commands Defaults screen that opens, enter the information as shown in the screen shots for your specific configuration.