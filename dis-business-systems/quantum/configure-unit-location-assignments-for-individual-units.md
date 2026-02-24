---
title: "Configure Unit Location Assignments for Individual Units"
source: "combined_Quantum_docs.md"
tags: ["Quantum"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Configure Unit Location Assignments for Individual Units."
long_description: "This document provides information about Configure Unit Location Assignments for Individual Units from the DIS Quantum system."
---

## Introduction

In addition to making unit locator service assignments by entire make/model combinations, you can also make assignments to individual units through the Inquire/Update Units option. Assignments can be changed as desired.

1.  Select **Inquire/Update – Complete Access** (Units | Inquire/Update – Complete Access). The Unit Selection screen opens.

2.  Select the unit that you would like to make Unit Locator service assignments for and click the **Update Unit** button. The Unit Information screen opens displaying basic information.

    

title: "Creating and Disabling User Profiles Quantum"
source: "Creating_and_Disabling_User_Profiles_Quantum.pdf"
tags: ["User Profile Management", "Quantum", "DIS", "User Creation", "User Disabling", "Security", "QSECOFR", "WRKUSRPRF", "System Administration"]
version: "1.0"
last_updated: "2024-05-17"
short_description: "A guide for system administrators on creating and disabling user profiles within the DIS Quantum software. It covers logging in as the security officer (QSECOFR), using generic templates, and the step-by-step process for both creation and disabling to ensure system security and auditing."
long_description: "This document provides detailed, step-by-step instructions for managing user accounts in the DIS Quantum system. It is intended for security officers or system administrators. The guide is divided into two main sections: 'Create User Profile' and 'Disable User Profile'. The creation process involves signing in with the `QSECOFR` profile, navigating to the `Work with User Profiles` screen using the `WRKUSRPRF *ALL` command, and copying a generic profile (like `BOOKS`) to create a new one. It specifies the necessary fields to complete for the new user, such as User Profile, Password, and Text description. The disabling process is recommended over deletion to preserve object ownership. It details how to find a user profile, change its status to `*DISABLED`, and update its password and description to reflect the change, thereby preventing future logins while maintaining system integrity. The document includes screenshots at each step to guide the user through the interface."