---
title: "Cleanup Make/Model Table Entries"
source: "combined_Quantum_docs.md"
tags: ["Quantum"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A document about Cleanup Make/Model Table Entries."
long_description: "This document provides information about Cleanup Make/Model Table Entries from the DIS Quantum system."
---

## Introduction
Unit Makes and Models are often incorrectly entered under different names. As a result, Makes and Models in your inventory or belonging to customers can be overlooked when working with Units. It is best practice to routinely search for and update Makes and Models that have been entered incorrectly. This document covers how to merge incorrect unit Makes and Models under the correct name.

## Merge Unit Makes
1. Select **Make/Model Table** (`Units | Make/Model Table`). The **Review Unit Make** screen opens.
   
   *Example Screen: Review Unit Make*
   | Long Make | Short Make | Allow Blank |
   | :-------- | :--------- | :---------- |
   | KUBOATA   | KUBOATA    | N           |
   | KUBOTA    | KUBOTA     | N           |
   | KUBTA     | KUBTA      | N           |

2. Click the **Merge Makes** button. The first **Merge Unit Makes** screen opens.

   *Example Screen: Merge Unit Makes (Step 1)*
   > Select the preferred spelling from the list below. On the next screen, select variations to be changed to the standard. Example: Select MAKE1 on this screen and on the next screen select variations to merge such as MAAK1 and MAKK1.
   
   | Long Make | Short Make | Allow Blank |
   | :-------- | :--------- | :---------- |
   | KUBOATA   | KUBOATA    | N           |
   | KUBOTA    | KUBOTA     | N           |
   | KUBTA     | KUBTA      | N           |

3. Locate and highlight the Make in the table that you would like to keep. This will be the Make version into which other Make versions will be merged. Click the **Select and Continue** button.
   > **Note:** You can locate the desired Make by entering the Long or Short make in the associated **Position To** field above the table and clicking **Enter**.

4. The second **Merge Unit Makes** screen opens positioned to the Make you just selected. While holding down the **Ctrl** key on your keyboard, click on all of the Makes currently displayed in the table that you would like to merge into the Make you selected on the first screen.

   *Example Screen: Merge Unit Makes (Step 2)*
   > Select all variations which will be merged to the standard KUBOTA which was selected on the previous screen. Example: Select MAAK1 and MAKK1.
   
   | Long Make   | Short Make  | Allow Blank |
   | :---------- | :---------- | :---------- |
   | KUBOATA     | KUBOATA     | N           |
   | KUBOTA      | KUBOTA      | N           |
   | KUBTA       | KUBTA       | N           |
   | KUHN        | KUHN        | Y           |
   | LAKE MARIO  | LAKE MARI   | N           |
   | MACDON      | MACDON      | Y           |

   > **Note:** To access Makes before the Make listed when the second Merge Unit Makes screen opens, click inside one of the **Position To** fields and click **Enter** to position to the beginning of the Make list or type a letter and click **Enter** to position to the first Make that begins with that letter.

5. Click the **Select and Continue** button. The makes are merged and the first **Merge Unit Makes** screen re-opens.
   > **Note:** You can only merge Makes that are currently displayed in the table. Each time you have to position to another Make not currently shown in the table, you will need to begin from Step 3 in these instructions.
   > For instance, if you also needed to merge a Make accidently entered as `Rubota` in addition to the Makes listed in the screenshot above, you would first need to merge `Kuboata` and `Kubta` and click the **Select and Continue** button. When you click the **Select and Continue** button, the first **Merge Unit Makes** screen re-opens. You would then choose `Kubota` again and maneuver to `Robota` in the table and select it.

6. Repeat the instructions in this section of the document to Merge any additional Makes.

## Merge Unit Models
1. Select **Make/Model Table** (`Units | Make/Model Table`). The **Unit Make** screen opens.

2. Select the Make containing the Model you wish to merge and click the **Display Models** button. The **Unit Model** screen opens.

3. Highlight the Model you wish to merge with another Make/Model, and click the **Delete Selected Model** button. The **Delete Model** screen opens.

4. Click the **Confirm Delete** button.

5. One of the following happens:
   - If the Model is not assigned to a unit, the Model will be deleted.
   - If the Model is assigned to a unit, the **Replace Make and Model** screen opens.

6. If the **Replace Make and Model** screen appears, you must reassign the units to a new model. Enter a **Long Make** in the provided field or click the **Long Make** button and select it from the table that displays.

7. Enter a **Long Model** in the provided field or click the **Long Model** button and select it from the list that appears.

8. Click **Enter**. The description assigned to the new Make/Model combination and a check box appears, allowing you to replace the description of the units assigned to the Make/Model being deleted with the description of the Make/Model that you are re-assigning the unit.

9. Select the checkbox "Replace all changed unit's descriptions with the new model description?" if desired and click **Enter**. A message displays at the bottom of the screen stating the Model has been deleted.

10. Repeat the instructions in this section for any other Models you would like to merge.


title: "New_Features_Guide_for_Quantum_21v2_-21v5"
source: "New_Features_Guide_for_Quantum_21v2_-21v5.pdf"
tags: ["Quantum", "software update", "new features", "21v2", "21v5", "Customer 360", "Management 360", "Parts", "Archiving"]
version: "1.0"
last_updated: "2026-01-17"
short_description: "This document outlines the primary new features and enhancements introduced in Quantum software releases 21v2 through 21v5. It covers updates to resolution, Customer 360, Management 360, Accounting (Payroll), Units, Parts, P.O.S. & Service, and Archiving functionalities."