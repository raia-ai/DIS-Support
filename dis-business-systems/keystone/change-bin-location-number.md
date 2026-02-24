---
title: "Change Bin Location Number"
source: "combined_Keyston.md"
tags: ["Keystone"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Change Bin Location Number."
long_description: "This document provides information about Change Bin Location Number from the DIS Keystone system."
---

## INTRODUCTION
If you are renaming your Bin Location Numbers or moving all of the parts from one bin location to another, you can quickly change the Bin Location using the Steps below. All parts assigned to the original Bin Location Number will automatically be re-assigned the new Bin Location Numbers.

## To Change Bin Location:
1. Press the **Alt** and **A** keys on your keyboard at the same time. The AS/400 Command screen opens.
   
   *AS/400 Command Screen Example:*
   ```
   AS/400 Command
   PFBIN
   ```

2. Type **PFBIN** in the available field and click **OK**. The Change Bin Location (PFBIN) screen opens.
   
   *Change Bin Location Screen Example:*
   ```
   Change Bin Location (PFBIN)

   Current bin location   ZZ56
   New bin location       ZZ4857
   ```

3. Type the existing Bin Location Number in the **Current bin location** field and the Bin Location Number that you are changing to in the **New bin location** field.

4. Click **Enter**. The Bin Location Number is changed and the Keystone main menu re-opens.

> **Note:** If you have bin locations that begin with a blank space or are changing to a Bin Location Number that begins with a blank space, a single quote will need to be entered at the beginning and end of the location as shown below.
> 
> *Example with Single Quotes:*
> ```
> Change Bin Location (PFBIN)
> 
> Current bin location   ZZ56
> New bin location       'ZZ485'
> ```


title: "Changing System Time on the AS/400"
source: "Changing_System_Time.pdf"
tags: ["AS/400", "system time", "daylight saving", "QHOUR", "Keystone", "DIS", "time change", "WRKSYSVAL", "time clock"]
version: "1.0"
last_updated: "2024-05-24"
short_description: "A guide on how to verify and manually change the system time on an AS/400 system, specifically for adjusting to Daylight Saving Time. It covers using the WRKSYSVAL QHOUR command to check and update the hour setting."
long_description: "This document provides step-by-step instructions for users of the Keystone system, which runs on an AS/400 platform, to manage system time changes related to Daylight Saving Time. The guide explains that while some newer systems adjust automatically, it's crucial to verify the time on the Monday following a time change. It details the process of accessing the AS/400 command line, using the WRKSYSVAL QHOUR command to inspect the current hour (QHOUR) system value, and how to change it if incorrect. The instructions cover both displaying the current value and modifying it using the 'Work with System Values' screen. Special considerations are included for businesses that use the Time Clock feature, advising them to change the time before employees clock in or after they clock out to avoid discrepancies in logged hours. It also provides contact information for assistance with complex configurations involving multiple locations in different time zones."