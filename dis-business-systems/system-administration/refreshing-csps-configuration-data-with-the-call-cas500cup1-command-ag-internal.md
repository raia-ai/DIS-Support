---
title: "Refreshing CSPS Configuration Data with the CALL CAS500CUP1 command - Ag Internal"
source: "salesforce_articles.md"
tags: ["System Administration", "AG-Internal"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Refreshing CSPS Configuration Data with the CALL CAS500CUP1 command - Ag Internal."
long_description: "This document provides internal system administration information about Refreshing CSPS Configuration Data with the CALL CAS500CUP1 command - Ag Internal."
---

_Refreshing CSPS Configuration Data with the CALL CAS500CUP1 command - AG Internal_

Refreshing CSPS Configuration Data with the CALL CAS500CUP1 Command 
   
 Introduction 
 In the world of CNH communications, ensuring access to a full range of CSPS data is crucial for a seamless and efficient experience. However, there might be instances when certain categories or options are not visible as expected. This guide will walk you through a solution to this issue by utilizing the CALL CAS500CUP1 command. This command becomes particularly valuable when a new division is added to the system. By following these steps, you can ensure the presence of all CSPS data for a comprehensive and accurate CNH communication. 
   
 Step 1: Identifying the Problem 
 If you encounter a scenario where some of the shipping options you usually rely on through CSPS communications are not appearing, it's time to take action. This issue can arise due to various factors, but one effective approach to rectify it is by running the CALL CAS500CUP1 command. 
   
 Step 2: Understanding the CALL CAS500CUP1 Command 
 The CALL CAS500CUP1 command is a utility to resolve the missing CSPS data. This command initiates communications with CNH to download the data. By executing this command, you pave the way for comprehensive and accurate CSPS data. 
   
 Step 3: The Power of CALL CAS500CUP1 for New Divisions 
 One specific scenario where the CALL CAS500CUP1 command is most useful is when a new division is added to the system. Utilizing CALL CAS500CUP1 in this context ensures that the newly added division's CSPS data is seamlessly integrated. 
   
 Step 4: Executing the CALL CAS500CUP1 Command 
 To execute the CALL CAS500CUP1 command, follow these steps: 
 1. Access the command line (Alt + A) or green screen session. 
 2. Input the command "CALL CAS500CUP1" and press enter. 
 3. Allow the process to complete. This is an interactive job and will lock your session while it runs. 
   
 Step 5: Post-Execution Verification 
 Once the CALL CAS500CUP1 command has finished you’ll need to verify it ran successfully. To do this you can DSPSFM the CSPSSVC file and look for the new division’s dealer number and CSPS data. 
   
 Conclusion: 
 By running the CALL CAS500CUP1 command, you have a solution at your fingertips to address missing CSPS data, especially in the context of new divisions. Remember to verify the CSPSSVC file after running the command to ensure that all dealer numbers are correctly integrated.