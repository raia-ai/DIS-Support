---
title: "Creating and Disabling User Profiles"
source: "combined_Quantum_docs.md"
tags: ["Quantum"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Creating and Disabling User Profiles."
long_description: "This document provides information about Creating and Disabling User Profiles from the DIS Quantum system."
---

## INTRODUCTION

DIS recommends that you create a unique user profile for each user on your system to ensure better security and auditing as well as more control over printing issues.

DIS has supplied generic profiles (PARTS and BOOKS) to use as a template for copying and creating new profiles (The generic profiles are not intended for use). The generic profiles have all of the necessary system values.

This document provides instruction for creating and disabling user profiles. Note the File Set and Division that the user will work in as they will need to supply this information the first time they sign in - It is listed at the top of the screen when you are signed in as a normal user.

## Create User Profile

1.  Sign into Quantum using the security office user profile `QSECOFR`.

2.  The OS/Main Menu screen opens.

3.  Type `WRKUSRPRF *ALL` in the command line and click **Enter** (put a space before the asterisk). The Work with User Profiles screen opens.

4.  Scroll down and select the **Books** user profile, then click the **Copy** button.

5.  The Create User Profile screen opens.

6.  Enter information for the new user in the following fields:
    *   **User Profile** - Will be entered as User in Sign On screen.
    *   **User Password**
    *   **Text 'description'** – To identify user

7.  Click **Enter** when finished.
    > **Note:** A message may display stating "User class and special authorities do not match system supplied values." This is a normal operating system message and DOES NOT prevent using the user profile.

8.  When you have finished adding new users, click the **Exit** button. The OS/main menu re-opens. Click the **Sign Off** option.

9.  When the user signs in using the User name and password you just supplied, they will be prompted to enter the company File Set and the Division that they work in.

## Disable User Profile

Deleting a user profile is not recommended as all objects on your business system are owned by user profiles and deleting the user profile will delete their objects. Transferring a user profile's objects is a lengthy process and requires a dedicated system. Therefore, it is highly recommended that you simply disable the user profile to ensure it is not used again.

1.  Sign into Quantum using the security office user profile `QSECOFR`.

2.  The OS/Main Menu screen opens.

3.  In this example the user profile name we want to disable is `JOES`, so `WRKUSRPRF JOES` would be typed in the command line. Substitute the user profile you want to disable for `JOES`. Click **Enter**.

4.  The Work with User Profiles screen opens displaying the user profile.

5.  Select the User Profile and click the **Change** button. The Change User Profile screen opens.

6.  Change the following fields:
    *   **User Password** – Change and keep private
    *   **Status** - Change to `*DISABLED`
    *   **Text 'description'** – Change to `DISABLED`

7.  Click **Enter**. The User Profile is now disabled and unable to be used. Only those who can log in under the `QSECOFR` profile can re-activate (enable) the user profile.