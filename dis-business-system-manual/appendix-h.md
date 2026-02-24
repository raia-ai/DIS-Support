---
title: "APPENDIX H"
source: "DIS_Business_System_Manual_Formatted.md"
tags: ["DIS Business System Manual"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A chapter from the DIS Business System Manual about APPENDIX H."
long_description: "This document is a chapter from the DIS Business System Manual, focusing on APPENDIX H."
---

## FORMS ALIGNMENT OKIDATA 520 PRINTER

### INTRODUCTION

**NOTE:** Instructions assume "Form Tear Off for Rear Feed" is OFF.

Don't forget that this printer can use the very first check. The DIS software assumes that one check will be wasted (as it is on most printers) and that it begins on the second check. To compensate, you must remember to enter the first check number minus one (when prompted in Print Payables Checks, X12-8).

In this chapter you'll find instructions for lining up checks, statements, and invoices on Okidata printer, model 520. A sample check and statement are illustrated in Appendix A.

Although you'll find sections on HOW TO ALIGN CHECKS, STATEMENTS, and INVOICES in this chapter, the most important material is contained in here in the INTRODUCTION and the following section, SYSTEM MESSAGES. That's because forms alignment is not an exact science: printers of the same make and model may be calibrated differently. Your own printer won't maintain the same alignment forever. As any mechanic can tell you, anything with moving parts changes!

Even on the same printer, it helps to think about forms alignment as a process, not something that you do right the first time every time. The most important part of the process is to become comfortable with the system messages and how to answer them.

In general the process goes like this:

- Load the forms.
- Print the first line. Make adjustment.
- Print the next line. Make adjustment. Repeat this step until you are pretty sure you have the alignment OK.
- Let them print! If you need to make another minor adjustment, take the printer off-line temporarily. It will resume exactly where it left off when you put it back on-line. If you have a forms jam or other semi-catastrophe, see the section "WHAT CAN GO WRONG & WHAT TO DO."

## APPENDIX H: AS/400 FORMS ALIGNMENT OKIDATA 520 PRINTER

- Remove the special forms and reload standard paper.

Each step is controlled through system messages and your answers to them. Following the instructions about physical alignment will help you get started; however, you'll need to figure out what works best on your printer and mark the diagrams accordingly.

## SYSTEM MESSAGES

The DIS Business System recognizes 4 different forms for the system printer:

| Form | System Abbreviation |
| :--- | :--- |
| 1. Standard | STD or 0001 |
| 2. Checks | CHKS |
| 3. Statements | STAT |
| 4. Labels | LAB |

The stock paper used for reports is called "Standard," whether it is wide bar or 8 1/2" X 11" letter-size. To prevent your accidentally printing important things like checks on standard paper, or reports on expensive forms such as checks, the system always lets you know when it is time to change forms.

System messages tell you when to load special forms, such as checks, and when to reload regular standard paper; however, it must depend on your answers to the messages to "know" what kind of forms are currently in the printer. In addition, when your answer indicates that forms have been changed, the system provides a message to facilitate alignment. In its own clunky mechanical way, it is trying to make your job easier.

### APPENDIX H: FORMS ALIGNMENT OKIDATA 520 PRINTER

Although there seem to be dozens of messages the first time you try to align forms, there are really only 2 different messages:

1.  **Change Forms**, which comes at the beginning and end of a job that requires different forms.
2.  **Alignment**, which can be repeated as often as necessary.

Your success depends on having the forms almost right when you answer the Change Forms message and then controlling adjustments through the Alignment message.

When you run a job that requires a change of forms, look at the AS/400's "Work with Printer Output" screen. At any DIS menu, type: `D P [Enter]`. The screen is illustrated below. In the example, messages for Past Due Statements (X11-9) is illustrated; however, you will encounter the same messages in Monthly Billing or Print Payables Checks.


```
Work with Printer Output
System:      S1011024
User . . . . . . X             Name, *ALL, F4 for list

Type options below, then press Enter. To work with printers, press F22.
2=Change   3=Hold      4=Delete    5=Display   6=Release   7=Message
9=Work with printing status    10=Start printing   11=Restart printing

Opt  Printer/Output   Status
7    P1               X11901           Printer message (use Opt 7)


F1=Help      F3=Exit     F5=Refresh    F11=Dates/pages/forms   F12=Cancel
F14=Select other printer output   F22=Work with printers      F24=More keys
Bottom
```

The message in the column labeled "Status" tells you what to do. Type "7" in the column labeled "Opt" as illustrated above, and press [Enter] to see the Additional Message Information, which may be either the Change Forms message or the Alignment message.


**Change Forms Message:**

```
Additional Message Information

Message ID . . . . . . :   CPA3394              Severity . . . . . . :   99
Message type . . . . . :   INQUIRY
Job  . . . . . . . . . :   PRT01                User . . . . . . . . :   QSPLJOB      Number . . . . . . :   170161
Date sent  . . . . . . :   05/12/92             Time sent  . . . . . :   14:22:03
From program . . . . . :   QSPPRTWT             Instruction  . . . . :   0000

Message . . . . :   Load form type 'STAT' device PRT01 writer PRT01. (H C G I R)

Cause . . . . . :   The file on output queue PRT01 in library QUSRSYS requires
form type 'STAT' to be loaded on device PRT01. The form type for the file was all
blanks when '' appears as the form type.
Recovery  . . . :   Do one of the following:
  --Type H to hold the file and print the next file on the output queue.
  --Type C to cancel the writer.
  --Type G after the form type is loaded to begin printing the current file.

                                                                        More...
Type reply, press Enter.
Reply . . .

F3=Exit      F12=Cancel
```

To see more information, press [PgDn].

```
Additional Message Information

Message ID . . . . . . :   CPA3394              Severity . . . . . . :   99
Message type . . . . . :   INQUIRY

| -- Ignore the request and process the file.
R -- Retry by researching the output queue.
```


The Change Forms message, CPA3394, is the first message and it occurs once at the beginning and once at the end of the job. It is displayed when it is time to take the stock paper out of the printer and put checks or statements in or vice versa. The possible answers to this message are:

H = Hold
C = Cancel
G = Go. Answer with a "G" after the specified forms (checks or statements) are loaded. This is the answer you'll use most of the time. It signals the computer that forms have been changed to checks (CHKS) or statements (STAT).
| = Ignore the request for changing forms and use the forms currently on the printer.
R = Retry

The Change Forms message is issued again at the end of the job as soon as the system is ready to print a report or anything that uses forms other than checks or statements. The procedure is the same: Answer with a "G" after the specified forms are loaded.

A COMMON MISTAKE is to take out the checks or statements and reload standard paper before this message is received. The same problem arises when standard forms are removed and special forms loaded before the Change Forms message.

It then seems logical to answer the Change Forms message with an "I," which means you don't want to change forms and that you want to continue on the current forms. The trouble is that now you think "current forms" are standard but the system still thinks "current forms" are checks


or statements.

If you find yourself in this situation, follow the instructions in the section WHAT CAN GO WRONG & WHAT TO DO to change the forms number and restart the print job.

THE BEST PROCEDURE is:

- Don't do anything until you receive the Change Forms message.
- When you receive the message, don't answer it immediately.
- Change the forms as instructed.
- Answer with a "G" to indicate that you have done what the system requested.


Alignment Message:

```
Additional Message Information

Message ID . . . . . . . . :   CPA4002                Severity . . . . . . . :   99
Message type . . . . . . :   INQUIRY
Job  . . . . . . . . . . . :   PRT01                  User . . . . . . . . . :   QSPLJOB
                                                       Number . . . . . . . :   170161
Date sent  . . . . . . . . :   05/12/92               Time sent  . . . . . . :   14:24:34
From program . . . . . . . :   QWPXPRMA               Instruction  . . . . . :   0000

Message  . . . . :   Verify alignment on printer PRT01. (I C G N R)
Cause  . . . . . :   The forms may not be aligned correctly. The first line
for the file is 11.
Recovery . . . . :   Do one of the following and try the request again.
Possible choices for replying to message . . . . . . . . . . . . . . . . . . :
  I -- To continue printing aligned forms starting with the next line of the
       file, type an I.
  C -- To cancel processing, type a C.
  G -- To continue printing aligned forms skipping to the next form and
       printing the first line again, type a G.
                                                                        More...
Type reply, press Enter.
Reply . . .

F3=Exit      F12=Cancel
```

- To see more information, press [PgDn].


**Additional Message Information**

 :--- | :--- | :--- |
| **Message ID** | CPA4002 | **Severity** | 99 |
| **Message type** | INQUIRY 

**N** -- To print the first line again on the next form and to verify the alignment,
1. Press Stop only if Start and Stop are two keys, or press Reset.
2. Advance the paper to the next form by pressing Form Feed/New Page.
3. Adjust the alignment with the forms adjust control.
4. Press Ready, Start, or Start/Stop.
5. Type an N.

**R** -- To print the first line again on the current form and to verify the alignment if the forms are not aligned,
1. Press Stop only if Start and Stop are two keys, or press Reset.
2. Adjust the alignment with the forms adjust control.
3. Press Ready, Start, or Start/Stop.
4. Type an R.

Type reply, press Enter.
Reply . . .

F3=Exit F12=Cancel

The Alignment Message, CPA4402, is displayed immediately after the first line is printed. The possible answers to this message are:

**I =** To continue printing aligned forms starting with the next line of the file, type an I. Statements are printed without further messages.

**C =** To cancel processing, type a C. **DO NOT USE THIS OPTION**. You cannot re-run Monthly Billing or Print Payables Checks or Payroll unless you delete your data files and restore a backup, which means you may have to repeat a lot of work.


G = To continue printing aligned forms skipping to the next form and printing the first line again, type a G. The first check or statement is printed on the next form and no additional alignment messages are presented.

N = To print the first line again on the next form and to verify the alignment,

- Press Stop only if Start and Stop are two keys, or press Reset.
- Advance the paper to the next form by pressing Form Feed/New Page.
- Adjust the alignment with the forms adjust control.
- Press Ready, Start, or Start/Stop.
- Type an N.

R = To print the first line again on the current form and to verify the alignment if the forms are not aligned,

- Press Stop only if Start and Stop are two keys, or press Reset.
- Adjust the alignment with the forms adjust control.
- Press Ready, Start, or Start/Stop.
- Type an R.

### **Note**

Options G and N advance to the next form, which means that they should not be used with pre-numbered checks.


After you have "authorized" the printing job to proceed without further interruption, you can still make adjustments by taking the printer off-line temporarily. **Do not turn the printer off!** Pressing "Start/Stop" (or "Sel" button) simply suspends printing and the job resumes at exactly the same place in the file when the printer is placed back on-line. This allows you to roll the paper in tiny increments fine tuning alignment as the checks or statements are being printed.

## HOW TO ALIGN CHECKS


### **Warning!**

In Print Payables Checks (X12-8), the check register is printed before checks, do not change forms until you are prompted to do so.


- Mount the checks onto the tractors in the back. A small, white plastic guide comes with the printer to help you feed the form under the paper guide.
- Press "FF/LOAD."
- Press "TEAR." The printer feeds the checks up so that the perforation is even with the tear bar.


- Now go back to the Change Forms message at the console:
- Answer the message with a "G," which means that you have loaded the correct forms. The printer rolls the forms back down into the printer to print the first line.
- The first line of the first check, which is the check number, is printed, and you receive the Alignment message. The alignment should be just about perfect the first time. Make minor horizontal adjustments (left/right), if necessary.
- To print the next line and continue with no further messages, answer with an "I."
- To make an adjustment while the checks are being printed, take the printer off-line temporarily by pressing the "Sel" button. After the micro-adjustment, press "Sel" again to resume printing.
- If more than a micro-adjustment is needed, press "Sel." See the section, WHAT CAN GO WRONG & WHAT TO DO, which follows.
- Before the system prints a report that uses standard forms, it issues the Change Forms message prompting you to load form type 'STD'.
- Reload the paper you normally use. Answer the message with a "G," which signals the system that it is now using standard forms. This is your insurance that the system will "know" to alert you before attempting to print checks or statements.

ALIGNING STATEMENTS


Receivable and Past Due Billing Statements are printed on the same forms so the alignment is the same for both. Balance Forward statements are printed first. When it is time for the Open Item statements, the system issues both the Change Forms and Alignment messages again. Although no action is necessary, the messages are answered differently for open item statements.

**Balance Forward Statements:**

When the system is ready to print Balance Forward statements, you'll receive the Change Forms message.

- Mount the first statement onto the tractors in the back of the printer. A small, white plastic guide comes with the printer to help you feed the first statement under the paper guide.
- Press "FF/LOAD."
- Press "TEAR." The printer feeds the statements up so that the perforation is even with the tear bar.
- Now go back to the Change Forms message.
- Answer the message with a "G," which means that you have loaded the correct forms. The printer rolls the forms back down into the printer to print the first line.
- The first line of the first statement, which is the customer's name, is printed, and you receive the Alignment message. The alignment should be just about perfect the first time. Make minor horizontal adjustments (left/right), if necessary.


- To print the next line and continue with no further messages, answer with an "I."
- To make an adjustment while the statements are being printed, take the printer off-line temporarily by pressing the "Sel" button. After the micro-adjustment, press "Sel" again to resume printing.
- If more than a minor adjustment is needed, press the Stop button on the printer. See the section, WHAT CAN GO WRONG & WHAT TO DO, which follows.
- Before the system prints a report that uses standard forms, it issues the Change Forms message again.
- Reload the paper you normally use. Answer the message with a "G," which signals the system that it is now using standard forms. This is your insurance that the system will "know" to alert you before attempting to print checks or statements.

## WHAT CAN GO WRONG & WHAT TO DO

Sooner or later things will get messed up: alignment messes up for no apparent reason, forms jam, power fails, or a message is answered incorrectly.

### **Warning**

Take the printer off-line. Do not turn the printer off.

- As soon as you are aware that there is a problem, take the printer off-line by pressing the button labeled "Sel" (Start/Stop) on the front of the printer.
- If the alignment is slightly off. Decide which way the form is off. Do not adjust the form position manually.
    - Press "SEL" to take the printer off-line.
    - At the same time, press "SHIFT" and "Micro Feed"--
    - To print higher on the page, press Micro Feed Down to move the invoice down.
    - To print lower on the page, press Micro Feed Up to move the invoice up.
    - Press "SEL" to put the printer on-line.

## Starting Over

In case of a forms jam, it's better to start over than to lose several checks or statements. Since you can't run the jobs, such as Monthly Billing or Print Payables Checks, a second time, starting over means only the print job.


- Display the print spool. At any menu, type: D P [Enter].
- Locate the job. In the column labeled "Printer/Output" you'll see an entry that corresponds to the menu option you're using, as illustrated in the table below:

| DIS Menu Option | JOBNAME |
| :--- | :--- |
| Monthly Billing (X11-8) | X118*** |
| Past Due Billing (X11-9) | X119*** |
| Print Payables Checks (X12-8) | X128*** |

- Select option 3, Hold. Put this print job (and any other print jobs) on hold.
- Select option 2, Change. The "Change spooled print entries" options are displayed.
- Select option 2, Change forms number. The CHANGE COMMAND prompts are presented, as illustrated below:
- Change the forms to XXXX. The reason for this is to "trick" the system into sending the Change Forms and Alignment messages again when the print job is restarted.
- Press [Enter]. Press [Cmd7] to return to the first SPOOLJOB menu.
- Select option 4, Release entries. Release the print job. The print job will begin at the beginning.

### **Aligning Invoices**

Because it is customary to have a printer dedicated to invoices, they are not distinguished from standard forms. There is no special name, such as CHKS or STAT. Likewise, the system does not send messages regarding alignment for invoices.

Alignment of invoices on the Model 520 may require some trial and error the first time invoices are loaded. The following steps will help you get as close as possible and "Micro Feed" will do the rest.

- Establish the default printer for each user through Point of Sale Devices (X52-10). For Okidata model 520, use the following settings:
  Invoice Heading Lines = 0
  Spaces Left or Left Margin = 5

**Printer Configuration:**
CPI (Characters Per Inch) = 10
LPI (Lines Per Inch) = 8
Form Length = 7"
Rear Feed Eject = 1 second

- Mount the invoices onto the tractors in the back of the printer. A small, white plastic guide comes with the printer to help you feed the first invoice under the paper guide.

- Press "FF/LOAD."

- Press "TEAR." The printer feeds the invoices up so that the perforation is even with the tear bar.

**Horizontal Alignment**


Line the left perforation on the 0 (zero) of the numbered scale.

- Print a test invoice. If it isn't printed exactly right on the invoice, then follow the next instructions to make adjustments:

- Set the "Form Tear Off for the Rear Feed" to OFF.

- Remount the invoices on the tractor. Press "FF/LOAD." The forms do not advance to the tear bar at this point. Do not adjust the form position manually!

- Print a test invoice. If the print needs adjustment:

Press "SEL" to take the printer off-line.

At the same time, press "SHIFT" and "Micro Feed"--

To print higher on the page, press Micro Feed Down to move the invoice down.

To print lower on the page, press Micro Feed Up to move the invoice up.

Press "SEL" to put the printer on-line.

- Print another test invoice. Do not adjust the form position manual-ly.

- Repeat steps 7 and 8 until the text on the invoice is perfectly aligned.

- Set the Form Tear Off for the Rear Feed to 1 second. The invoice advances to the tear bar.

NOTE: If the invoice does not advance so that the perforation is exactly


at the tear bar, take these steps:

Press "SEL" to take the printer off-line.
At the same time, press "SHIFT" and "Micro Feed"--

To print higher on the page, press Micro Feed Down to move the invoice down.

To print lower on the page, press Micro Feed Up to move the invoice up.

Press "SEL" to put the printer on-line.


Notes: