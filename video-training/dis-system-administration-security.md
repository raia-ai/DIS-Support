---
title: "DIS System Administration & Security"
source: "DIS_Video_Training_Knowledge_Base.md"
tags: ["DIS System Training", "DIS System Administration & Security"]
version: "1.0"
last_updated: "2026-03-04"
short_description: "The **DIS System Administration & Security** module is a critical component of the Dealer Information System (DIS) platform, responsible for managing user access, system security, data organization, and operational integrity across dealership loca..."
long_description: "This document provides a comprehensive overview of the DIS System Administration & Security module within the DIS platform, derived from internal training sessions."
---

# DIS System Administration & Security

**Source Sessions**: 01, 02, 03

### Overview

The **DIS System Administration & Security** module is a critical component of the Dealer Information System (DIS) platform, responsible for managing user access, system security, data organization, and operational integrity across dealership locations. It provides administrators with tools to control user profiles, enforce security policies, configure system-wide settings, and oversee division-specific configurations such as backups and end-of-day processes. This module ensures that sensitive data remains protected, user actions are auditable, and system resources are properly allocated and maintained.

Given the multi-division nature of many dealerships, the module’s hierarchical data structure and security mechanisms are designed to prevent data corruption and unauthorized access. It also supports operational continuity through automated backup scheduling and end-of-day job management. The module integrates with internal employee portals and knowledge bases, facilitating efficient support and training for system users and administrators.

### Core Concepts

**System Access & Support Tools**  
Access to the DIS system for support staff is primarily through the DIS Corporate website, leading to the customer portal and internal tools such as **StaffLink**. StaffLink serves as the internal employee portal, providing access to customer-specific information, administrative tools, and a comprehensive **Knowledge Base (NKD)**. It also allows employees to switch between the internal (StaffLink) and customer-facing (Keystone) views of the system.

**Data Organization: File Sets and Divisions**  
Data within DIS is organized hierarchically. The highest level is the **File Set** (also called File Group), which contains one or more **Divisions**. Divisions typically represent individual dealership locations or business units but can also segregate different lines of business within the same location. Each user session operates within the context of a specific File Set and Division.

**User Profiles and Sessions**  
Every system user requires a unique **User Profile** (user ID). Users may have up to five concurrent sessions, but the use of generic or shared user IDs (e.g., "PARTS") is strongly discouraged due to session limits and auditability concerns. Each active session is assigned a unique temporary Workstation ID (e.g., `#Z`, `@1`), which ties in-progress work to that session.

**Special User IDs**  
- **QSECOFR**: The master security officer profile on the AS/400 system, with exclusive authority to create and manage user profiles.  
- **SUPPORT**: A special, non-billable user ID for DIS support staff with elevated privileges, including the ability to view security passwords.

**Security Maintenance and Security Gates**  
Security Maintenance is a restricted, single-user area for managing all security-related settings, including user access, passwords, and division information. The system employs **Security Gates** to password-protect specific menu options or entire application areas (e.g., Accounting, Payables). Access can be granted by entering the gate password or by assigning "Bypass Authority" to specific users.

**Backup and End-of-Day (EOD) Jobs**  
Each division has its own automated backup schedule and EOD job configuration. Backups can be performed on tape or disk (though disk backups are discouraged due to exponential growth). EOD jobs run in conjunction with backups and generate reports that are archived for later review. The system enforces that EOD jobs cannot be scheduled on days without a backup.

**Reporting and Printers**  
The system distinguishes between transactional printing (invoices, checks) and report printing. Reports are managed via DIS printers, and a **Dummy Printer** (e.g., 'NP' for No Print) is used to view reports on-screen or export them to Excel or PDF.

### System Architecture & Data Model

The DIS system’s data model is structured around a hierarchical relationship:

- **File Set (File Group)**: The top-level container for data, encompassing multiple divisions.  
- **Division (Branch/Store)**: A subdivision within a File Set, representing a physical location or business unit. Each division maintains its own configuration, backup schedule, and EOD job settings.

User sessions are always tied to a specific File Set and Division. When a user signs in for the first time, they must select their default File Set and Division. Each active session receives a unique Workstation ID, which links any in-progress work to that session. Improper disconnection can cause work to become "stuck" under a session ID, requiring manual intervention to resume.

The system maintains two distinct name fields for divisions:

- **Division Name**: Used for official reporting and appears on standard reports.  
- **Quantum Branch Preferred Name**: Used specifically by the Management 360 analytics and reporting tool.

This dual naming supports different reporting requirements within the platform.

### Key Procedures

**1. Creating a New User Profile**

1. Sign on to the AS/400 system as the **QSECOFR** user.  
2. At the command line, enter `WRKUSRPRF` and press Enter.  
3. Press `F6` to create a new user profile.  
4. Enter the new **User ID** (up to 10 characters).  
5. Set the initial **Password** (commonly the same as the User ID initially).  
6. Provide a **Description** (e.g., full name and department).  
7. Press Enter to create the profile.  
8. Sign off as QSECOFR.  
9. Have the new user sign on; they will be prompted to select their default File Set and Division.

**2. Finding a Forgotten Master Security Password**

1. Sign on using the **SUPPORT** user ID.  
2. At the AS/400 command line, enter `SHOW P` and press Enter.  
3. The system displays the Master Security password for the current division at the bottom of the screen.

**3. Viewing and Ending Active User Sessions**

1. Sign on as **QSECOFR**.  
2. Enter `WRKACTJOB` at the AS/400 command line and press Enter.  
3. Review the list of active jobs and users.  
4. To end a session, enter `4` next to the user’s job and press Enter.  
5. Confirm the action to disconnect the user.

**4. Setting Up an Automated Backup Schedule**

1. Navigate to `Security -> Backup`.  
2. Select the relevant File Set and click "Change".  
3. Configure the backup device, time (24-hour clock), and days of the week.  
4. Set user warnings and automatic logout parameters for users still logged in at backup time.

**5. Configuring End-of-Day (EOD) Jobs**

1. Within the File Set, access the "End of Day Jobs" section for the division.  
2. Select the EOD jobs to run (e.g., Accounting, Parts).  
3. Set report output to "NP" (No Print) to avoid printing large reports.

**6. Accessing Archived EOD Reports**

1. Go to the `Archive` menu.  
2. Select `Work with archive documents`.  
3. Choose the report type (e.g., Accounting end-of-day).  
4. Select the division to view archived reports.

**7. Switching Between StaffLink and Customer Views**

1. From the StaffLink main page, open the `Staff Tools` menu.  
2. Click the `Switch` option to toggle between the internal employee view (StaffLink) and the customer-facing Keystone view.

**8. Accessing Quantum Online Help**

1. From StaffLink, navigate to `Services > Training > Quantum`.  
2. Click the link for the **Complete Quantum User Guide**.  
3. Select **Online Help** to access menu-driven documentation.

### Menu Navigation

- `System -> Change Division` (Shortcut: Alt+D)  
- `System -> Change File Set`  
- `System -> AS/400 Command Line`  
- `System -> Show Workstation IDs`  
- `System -> Take Workstation ID` (Accounting Only)  
- `System -> Change My Password`  
- `Security -> Security Maintenance`  
- `Security -> Backup`  
- `System -> Work with DIS Report Printers`  
- `System -> Quantum Report Center`  
- `System -> My Printer Output`  
- `Archive -> Work with archive documents`  
- `OPT -> Master Menu`  
- `Services > Training > Quantum > Complete Quantum User Guide > Online Help`  
- `Support > Knowledge Base`  
- `Staff Tools > Switch`

### Business Rules & Constraints

- **User Sessions**: A single user ID may have up to five concurrent sessions. Avoid shared or generic user IDs to prevent session limits and maintain audit trails.  
- **Passwords**: User passwords cannot begin with a number and must not contain spaces or special characters.  
- **Security Maintenance**: Only one user may access Security Maintenance at a time.  
- **Multi-Division Operations**: Users must not perform tasks in one division and then switch to another within the same session to avoid data corruption. Use separate user profiles for each division.  
- **Deleting Divisions**: The "Delete Division" function must never be used.  
- **Transfer Account**: Every division must have a transfer account defined, even in single-division systems.  
- **Backup and EOD Jobs**: EOD jobs cannot be scheduled on days without a backup. Critical processes (e.g., payroll, immediate backups, applying enhancements, accounting month-end) will not be interrupted by backups.  
- **OPT Menu Settings**: Certain options, such as "Parts average costing," should not be changed after initial setup to avoid data corruption.  
- **Security Gate Password Changes**: Changing a security gate password resets access for all users; those without bypass authority must be informed of the new password.

### Configuration Options

- **Security Gates**: Enable password protection on nearly any menu option. Configure whether the password prompt appears every time or only once per session.  
- **Bypass Authority**: Grant specific users the ability to bypass security gate passwords.  
- **Division Information**: Configure division name, address, fiscal year start, current GL period, and interest calculation rules within Security Maintenance.  
- **Backup Schedule**: Set backup device, time, days of the week, and notification user.  
- **EOD Jobs**: Select which jobs run and define report output destinations.  
- **User Warnings**: Configure warning frequency and timeout before automatic logout during backups.  
- **Management 360 Access**: Control user access to Management 360 and Sales 360 modules via User Authority settings in Security Maintenance.  
- **Division Renaming**: Two separate fields exist for division names—one for standard reports and one for Management 360 preferred naming.

### Common Pitfalls & Warnings

- **Improper Session Closure**: Never close session windows using the window 'X' button; always use the system’s exit or sign-off commands to prevent sessions from becoming stuck.  
- **Shared User IDs**: Avoid generic shared IDs like "BOOKS" or "PARTS" to prevent hitting session limits and losing auditability.  
- **Working in Wrong Division**: Always verify the active division before performing actions, especially in multi-division environments, to avoid data misplacement.  
- **Taking Over Workstation IDs**: Exercise caution when taking another user’s workstation ID to avoid interrupting critical processes.  
- **Backup Media Management**: Disk backups can grow exponentially and consume excessive storage; tape backups are preferred but require initialization.  
- **Printer Paper**: Running out of paper during large EOD report printing can cause issues; consider using the Dummy Printer option to avoid printing.  
- **Changing OPT Menu Settings**: Modifying certain OPT menu options without full understanding can corrupt data.

### Key Terminology

- **NKD**: The DIS Knowledge Base, the primary documentation resource.  
- **File Set / File Group**: The highest level of data organization containing one or more divisions.  
- **Division / Branch / Store**: A subset of a File Set, typically representing a single location or business unit.  
- **Green Screen**: The text-based AS/400 interface used for system administration.  
- **QSECOFR**: The master security officer user profile on the AS/400 system.  
- **SUPPORT**: A special DIS support user ID with elevated privileges and no license consumption.  
- **WRKUSRPRF**: AS/400 command to "Work with User Profiles."  
- **WRKACTJOB**: AS/400 command to "Work with Active Jobs."  
- **Dummy Printer (NP/ZP)**: A virtual printer used for on-screen report viewing and exporting.  
- **Security Gate**: A password protecting specific menu options or application areas.  
- **StaffLink**: The internal employee portal for DIS staff, providing access to tools, knowledge bases, and training.  
- **Quantum**: The current-generation DIS software platform.  
- **Keystone**: The legacy DIS software and customer-facing portal view.  
- **Altera**: The upcoming next-generation DIS software platform.  
- **Management 360**: A reporting and analytics tool that uses a preferred branch/division name distinct from standard reports.

---