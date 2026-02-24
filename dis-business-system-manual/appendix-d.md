---
title: "APPENDIX D"
source: "DIS_Business_System_Manual_Formatted.md"
tags: ["DIS Business System Manual"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A chapter from the DIS Business System Manual about APPENDIX D."
long_description: "This document is a chapter from the DIS Business System Manual, focusing on APPENDIX D."
---

## FORMS ALIGNMENT IBM 4226 PRINTER

### INTRODUCTION

*Don't forget that this printer can use the very first check. The DIS software assumes that one check will be wasted (as it is on most printers) and that it begins on the second check. To compensate, you must remember to enter the first check number minus one (when prompted in Print Payables Checks, X12-7).*

In this chapter you'll find instructions for lining up checks and statements on the IBM 4226 printer. A sample check and statement are illustrated in Appendix A.

### THE ZEN OF ALIGNMENT

Forms alignment is not an exact science: printers of the same make and model may be calibrated differently. Your own printer won't maintain the same alignment forever. As any mechanic can tell you, anything with moving parts changes!

Even on the same printer, it helps to think about forms alignment as a *process*, not something that you do right the first time every time. The most important part of the process is to become comfortable with the system messages and how to answer them.

In general the process goes like this:
- Load the forms.
- Print the first line. Make adjustment.
- Print the first line again. Make adjustment. Repeat this step until you are pretty sure you have the alignment OK. On the AS/400, you do not have the option to print one line at a time. Your choices are to print the same line on the same form, print the same line on the next form, or print the next line and continue without further messages. You don't *ever* want to cancel the print job. Of course, with pre-printed checks you don't even want to skip to the next form, so your choices are even more limited.
- Let them print! If you need to make another minor adjustment,

## APPENDIX D: FORMS ALIGNMENT IBM 4226 PRINTER

take the printer off-line temporarily. It will resume exactly where it left off when you put it back on-line. If you have a forms jam or other semi-catastrophe, see the section TROUBLESHOOTING.

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
| 5. Letters | LETT |

The stock paper used for reports is called "Standard," whether it is wide bar or 8 1/2" X 11" letter-size. To prevent your accidentally printing important things like checks on standard paper, or reports on expensive forms such as checks, the system always lets you know when it is time to change forms.

System messages tell you when to load special forms, such as checks, and when to reload regular standard paper; however, it


must depend on your answers to the messages to "know" what kind of forms are currently in the printer. In addition, when your answer indicates that forms have been changed, the system provides a message to facilitate alignment. In its own clunky mechanical way, it is trying to make your job easier.

Although there seem to be dozens of messages the first time you try to align forms, there are really only 2 different messages:

- Load Forms, which comes at the beginning and end of a job that requires different forms.
- Alignment, which can be repeated as often as necessary.

Your success depends on having the forms almost right when you answer the Load Forms message and then controlling adjustments through the Alignment message.

When you run a job that requires a change of forms, look at the AS/400's "Work with Printer Output" screen. At any DIS menu, type: D P [Enter]. The screen is illustrated below. In the example, messages for Past Due Statements (X11-11) is illustrated; however, you will encounter the same messages in Print Statements, Print Payables Checks, printing Letters (new A/R) and Labels.


Work with Printer Output Screen

Watch the printer output screen to know when your special forms are ready to be printed. At a command line, type: D P [Enter].

```
Work with Printer Output
System: S1011024
User . . . . . . EBS Name, *ALL, F4 for list

Type options below, then press Enter. To work with printers, press F22.
2=Change 3=Hold 4=Delete 5=Display 6=Release 7=Message
9=Work with printing status 10=Start printing 11=Restart printing

| Opt | Printer/ Output | Status |
|---|---|--- P1  7 | X12700 | Printer message (use Opt 7)  P9  | X51088 | Printer stopped (use Opt 10)  X51088 | Printer stopped (use Opt 10)  X51088 | Printer stopped (use Opt 10)  X51088 | Printer stopped (use Opt 10)  X51088 | Printer stopped (use Opt 10)  X51088 | Printer stopped (use Opt 10)  X51088 | Printer stopped (use Opt 10) |

More...
F1=Help F3=Exit F5=Refresh F11=Dates/pages/forms F12=Cancel
F14=Select other printer output F20=Include system output F24=More keys
```

> NOTE: If the format of your screen doesn't look like this, press F24=More Keys, then F21=Select assistance level 1=Basic.

The message in the column labeled "Status" tells you what to do. Type "7" in the column labeled "Opt" as illustrated above, and press [Enter] to see the Additional Message Information, which may be either the Load Forms message or the Alignment message.

## Load Forms Message

```
Additional Message Information

Message ID . . . . . . :   CPA3394      Severity . . . . . . :   99
Message type . . . . . :   Inquiry
Date sent  . . . . . . :   07/02/97     Time sent  . . . . . :   10:10:54

Message  . . . . . . :   Load form type 'CHKS' device PRT01 writer PRT01.  (G B I H R C)
Cause  . . . . . . . :   The file on output queue PRT01 in library QUSRSYS requires
form type 'CHKS' to be loaded on device PRT01. The form type for the file
was all blanks when '' appears as the form type.
Possible choices for replying to message . . . . . . . . . . . . . .
  G -- Begin processing the current file after loading the form type.
  B -- Begin processing the current file after loading and aligning the form
       type (no alignment message is sent - same as option 1 on System/36).
  I -- Ignore the request to load the form type. Print the file on the
       current formtype (same as option 0 on System/36).
                                                                      More...
Type reply below, then press Enter.
Reply  . . . . . . .   G

F3=Exit   F6=Print   F9=Display message details   F12=Cancel
F21=Select assistance level
```

To see more information, press [PgDn].

The Load Forms message, CPA3394, is the first message and it occurs once at the beginning and once at the end of the job. It is displayed when it is time to take the stock paper out of the printer and put checks or statements in or vice versa. The possible answers to this message are:

- **H =** Hold
- **C =** Cancel
- **G =** Go. Answer with a "G" after the specified forms (checks or statements) are loaded. This is the answer


**APPENDIX D: FORMS ALIGNMENT IBM 4226 PRINTER**

you'll use most of the time. It signals the computer that forms have been changed to checks (CHKS) or statements (STAT).

| = Ignore the request for changing forms and use the forms currently on the printer.

R = Retry

The *Load Forms* message is issued again at the end of the job as soon as the system is ready to print a report or anything that uses forms other than checks or statements. The procedure is the same: Answer with a "G" after the specified forms are loaded.

**A COMMON MISTAKE** is to take out the statements and reload standard paper before this message is received. The same problem arises when standard forms are removed and special forms loaded before the *Load Forms* message.

It then seems logical to answer the *Load Forms* message with an "I," which means you don't want to change forms and that you want to continue on the current forms. The trouble is that now you think "current forms" are standard but the system still thinks "current forms" are checks or statements.

If you find yourself in this situation, follow the instructions in the section TROUBLESHOOTING to change the forms number and restart the print job.

**THE BEST PROCEDURE is:**

- Don't do anything until you receive the *Load Forms* message.
- When you receive the message, don't answer it immediately.
- Change the forms as instructed.
- Answer with a "G" to indicate that you have done what the system requested.

## Alignment Message

```
Additional Message Information

Message ID . . . . . . :   CPA4002      Severity . . . . . . :   99
Message type . . . . . :   Inquiry
Date sent  . . . . . . :   07/02/97     Time sent  . . . . . :   10:13:38

Message . . . . :   Verify alignment on printer PRT01. (I G N R E C)
Cause . . . . . :   The forms may not be aligned correctly. The first line for the file is 7.
Possible choices for replying to message . . . . . . . . . . . . . . . . :
  I -- To continue printing aligned forms starting with the next line of the file, type an I.
  G -- To continue printing aligned forms skipping to the next form and printing the first line again, type a G.
  N -- To print the first line again on the next form and to verify the alignment,
       1. Press Stop only if Start and Stop are two keys, or press Reset.
                                                                    More...
Type reply below, then press Enter.
Reply . . . . .

F3=Exit   F6=Print   F9=Display message details   F12=Cancel
F21=Select assistance level
```

To see more information, press [PgDn].

The *Alignment message*, CPA4002, is displayed immediately after the first line is printed. The possible answers to this message are:

- **I =** To continue printing aligned forms starting with the next line of the file, type an I. Statements are printed without further messages.
- **C =** To cancel processing, type a C. **DO NOT USE THIS OPTION**. You cannot re-run Print Statements or Print Payables Checks or Payroll unless you restore a backup, which means you may have to repeat a lot of work.


**G =** To continue printing aligned forms skipping to the next form and printing the first line again, type a G. The first check or statement is printed on the next form and no additional Alignment messages are presented.

**N =** To print the first line again on the NEXT form and to verify the alignment,
- Press Stop only if Start and Stop are two keys, or press Reset.
- Advance the paper to the next form by pressing Form Feed/New Page.
- Adjust the alignment with the forms adjust control.
- Press Ready, Start, or Start/Stop.
- Type an N.

> This is the option to take when you have an alignment

**R =** To print the first line again on the current form and to verify the alignment if the forms are not aligned,
- Press Stop only if Start and Stop are two keys, or press Reset.
- Adjust the alignment with the forms adjust control.
- Press Ready, Start, or Start/Stop.
- Type an R.

After you have "authorized" the printing job to proceed without further interruption, you can still make adjustments by taking the printer off-line temporarily. **Do not turn the printer off!** Pressing "Start/Stop" simply suspends printing and the job resumes at exactly the same place in the file when the printer is placed back on-line. This allows you to roll the paper in tiny increments fine tuning alignment as the checks or statements are being printed.



- At a command line, type: `D P`[Enter].
- Select X11A00 with 3=hold. Place all the entries on hold.
- Press F5=Refresh.
- When the status of X11A00 is “Held,” select it with 2=change.
- Press F10=Additional parameters, page down one page.
- Change “Save file” to `*YES` [Enter].
- Press F5=Refresh.
- Select X11A00 with 6=Release.
- Press F5=Refresh (screen says Printer Message).
- Select X11A00 with 7=to display the *Load Forms* message.
- Answer message with G.
- Press F5 to refresh printer message.
- Select X11A00 with 7=Message to display the alignment message.
- Answer the message with R to print same line again, or with I to continue.
- Refer to the section for the job you are performing. Realign the forms and proceed with the job.

After the checks have been printed and the first printout is requested, the *Load Forms* message will be generated again to prompt you to change forms back to standard paper. You’ll notice that whatever you requested is not printed immediately.

To see the message, type: `D P` [Enter]. The Work with Printer


Output screen is displayed (see screen on page 4).

- Find the printer the checks were printed on.
- Find the job you requested.
- Select it with 7=Message to display the Load Forms message.

## Load STD Forms Message

```
Additional Message Information

Message ID . . . . . . . :   CPA3394     Severity . . . . . . . :   99
Message type . . . . . . :   Inquiry
Date sent  . . . . . . . :   07/02/97    Time sent  . . . . . . :   10:44:24

Message  . . . . :   Load form type '*STD' device PRT01 writer PRT01.  (G B I H R C)
Cause  . . . . . :   The file on output queue PRT01 in library QUSRSYS requires
  form type '*STD' to be loaded on device PRT01. The form type for the file
  was all blanks when '' appears as the form type.
Possible choices for replying to message . . . . . . . . . . . . . . . . :
  G -- Begin processing the current file after loading the form type.
  B -- Begin processing the current file after loading and aligning the form
       type (no alignment message is sent - same as option 1 on System/36).
  I -- Ignore the request to load the form type.  Print the file on the
       current formtype (same as option 0 on System/36).
                                                                      More...
Type reply below, then press Enter.
Reply  . . . . .   G

F3=Exit   F6=Print   F9=Display message details   F12=Cancel
F21=Select assistance level
```

- Load standard paper if you haven't already done so.
- Answer the message with a **G**. The next job will be printed.

## PRINTER FUNCTION SETTINGS

### Changing Function Settings

- Press Stop/Start to take the printer off line.
- Press Menu/Quit to enter the function menu.
- Press Item (arrow up or down) until the desired function menu appears on the display.
- Press Scroll (arrow up or down) until the desired value appears on the display.
- Press Store to save the selected value.
- Repeat the previous 3 steps to change other values as necessary.
- Optional. Print the function settings by pressing Item (arrow up or down) until Print Setting appears on the display. Press Start/Stop. The current values are printed.

### Suggested Settings

DIS has used these settings for all forms; however, other settings may also be satisfactory.

| Setting | Value |
|---|---|
| Language | English |
| Epson Emulation | Off |
| Font | Fast Draft |
| Pitch | 10 CPI |
| Auto Tear Off | On |
| Line Length | 13.6 |
| Lines Per Inch | 6 |
| Form Length | 66 or 51 LPP |
| Emphasized | Off |
| Character Size | Normal |
| Character Set | 1 |
| Code Page | 437 |
| Download Page Code | 437 |
| NLQ Print | Bidirectional |
| Automatic CR | Off |
| Automatic LF | Off |
| Slashed Zero | On |
| Alarm | Enable |
| Buffer Size | Maximum |
| Interface | Parallel |

### How To Align Checks


### **Warning!**

In Print Payables Checks (X12-7), the check register is printed before checks, do not change forms until you are prompted to do so.


Emulating PCs only. Make sure your printer parameters are:
6 lines per inch
10 characters per inch

Load the checks. The first check is used for alignment.

| Vertical alignment: | Top perforation at Top of Form |
| :--- | :--- |
| Horizontal alignment: | Left edge of the form at 14th marking on the horizontal rule bar. |

- Press Load/Unload to retract paper already loaded.
- Press Load/Unload. Paper moves up into place.
- Press Menu/Quit. "Set Line 1" appears.


- Press Micro (arrow down) to move form down to the top of the print head. Note that it can be seen through the top of the printer. Opening and closing the printer door forces the print head to the far right.
- Press Start/Stop. An "H" is printed on the form, which is moved up where it can be seen.
- Check the alignment, and press Tear Off. This moves the form back down into the printer.
- Press Micro (arrow up or down) to adjust alignment.
- Press Start/Stop. The "H" is reprinted, and the form moves up again.
- Repeat steps until the vertical alignment is correct.
- When the alignment is correct, press Tear Off, which moves the form down.
- Press Tear Off again to store the new top of form.
- Press Menu/Quit to exit set up.
- Press Start/Stop to make printer ready.
- Now go back to the Change Forms message at the console:
- Answer the message with a "G," which means that you have loaded the correct forms.
- The first line of the first check, which is the check number, is printed, and you receive the Alignment


message.

- Because of the 4226 printer's alignment procedures, the alignment should be just about perfect, and you can answer the message with an "I," which means that the checks continue to print without further messages.

- To make minor adjustments, press Start/Stop and Micro (arrow up or down) accordingly. Press Start/Stop again to resume printing.

After the checks have printed successfully, follow these steps:

- Emulating PCs Only. Change the printer parameters back to the correct settings for standard forms, regular or compressed print.

- Before the system prints a report that uses standard forms, it issues the Change Forms message prompting you to load form type 'STD'.

- Reload the paper you normally use. Answer the message with a "G," which signals the system that it is now using standard forms. This is your insurance that the system will "know" to alert you before attempting to print checks or statements.

## ALIGNING STATEMENTS

Regular and interim/past due statements are printed on the same forms so the alignment is the same for both. Balance Forward statements are printed first. When it is time for the Open Item statements, the system issues both the Change Forms and Alignment messages again. Although no action is necessary, the messages are answered differently for open item statements.

## Balance Forward Statements

When the system is ready to print Balance Forward statements, you'll receive the Change Forms message.

- Load the statements. The first statement is used for alignment. See the diagram on the following page.

| Vertical alignment: | Top perforation at Top of Form |
| :--- | :--- |
| **Horizontal alignment:** | Left edge of the form at 15th marking on the horizontal rule bar. |


- Press Load/Unload to retract paper already loaded.
- Press Load/Unload. Paper moves up into place.
- Press Menu/Quit. "Set Line 1" appears.
- Press Micro (arrow down) to move form down to the top of the print head. Note that it can be seen through the top of the printer. Opening and closing the printer door forces the print head to the far right.
- Press Start/Stop. An "H" is printed on the form, which is moved up where it can be seen.
- Check the alignment, and press Tear Off. This moves the form back down into the printer.
    - • Press Micro (arrow up or down) to adjust alignment.
    - • Press Start/Stop. The "H" is reprinted, and the form moves up again.
- Repeat steps until the vertical alignment is correct.
- When the alignment is correct, press Tear Off, which moves the form down.
- Press Tear Off again to store the new top of form.
- Press Menu/Quit to exit set up.
- Press Start/Stop to make printer ready.
- Now go back to the Change Forms message.


- Answer the message with a "G," which means that you have loaded the correct forms.
- The first line of the first statement, which is the customer's name, is printed, and you receive the Alignment message.
- To make minor adjustments, press Start/Stop and Micro (arrow up or down) accordingly. Press Start/Stop again to resume printing.

## Open Item Statements

Following balance forward statements, open item statements are printed. No further alignment is necessary.

When the statements have printed successfully, follow these steps:

- Emulating PCs Only. Change the printer parameters back to the correct settings for standard forms, regular or compressed print.
- Before the system prints a report that uses standard forms, it issues the Change Forms message again.
- Reload the paper you normally use. Answer the message with a "G," which signals the system that it is now using standard forms. This is your insurance that the system will "know" to alert you before attempting to print checks or statements.

## TROUBLESHOOTING

Sooner or later things will get messed up: alignment messes up for no apparent reason, forms jam, power fails, or a message is answered incorrectly.

> **WARNING!**
> Take the printer off-line. Do not turn the printer off.

### Alignment Problems

- As soon as you are aware that there is a problem, take the printer off-line by pressing **Start/Stop**.
- To make minor adjustments, press **Micro** (arrow up or down) accordingly. Press **Start/Stop** again to resume printing.

### Starting Over

In case of a forms jam, it's better to start over than to lose several checks or statements. Since you can't run the jobs, such as Print Statements or Print Payables Checks, a second time, starting over means only the print job.

- Display the print spool. At any menu, type: `D P [Enter]`.


Locate the job. In the column labeled "Printer/Output" you'll see an entry that corresponds to the menu option you're using, as illustrated in the table below:

| DIS Menu Option: | JOB NAME |
| :--- | :--- |
| Print Statements (X11-10) | X11A*** |
| Past Due Statements (X11-11) | X11B*** |
| Print Payables Checks (X12-7) | X127*** |

- Select option 3=Hold. Put this print job (and any other print jobs) on hold.
- When the status of each entry is held press F24 (twice)=More keys.
- Press F21=Select Assistance Level. This option is not always obvious, just try to remember to press F24=More Keys, until you get to this level.
- Answer the Assistance Level message with 1=Basic or with 2=Intermediate [Enter].
- Find the jobs you have placed on hold and select with 2=Change [Enter].
- Change the form type to XXXX. Because all printer buffers are set differently, the current page spooled to the printer may or may not be the actual page printing. We recommend starting back 5 to 10 pages when choosing a page number to start to reprint. Change the next page to print [Enter].
- Press F5=Refresh.


- Select with 6=Release [Enter].
- Press F5=Refresh the Load Forms message.
- Select with 7=to display the Load Forms message [Enter].
- Answer message with G [Enter].
- Press F5=Refresh the Alignment message.
- Select with 7= to display Alignment message [Enter].
- Answer the message with R to print the same line again or with I to continue.

### **Aligning Invoices**

Because it is customary to have a printer dedicated to invoices, they are not distinguished from standard forms. There is no special name, such as CHKS or STAT.

Likewise, the system does not send messages regarding alignment for invoices. Align the invoices as follows:

**Horizontal Alignment**

Align the left perforation on the 0 (zero) of the numbered scale.

**Vertical Alignment**

Align the invoice perforation 1/2" below Top of Form.

After the first invoice is printed, make minor adjustments as necessary.

Other issues pertaining to Point of Sale follow.

**Default Printer**

You can establish the default printer for each user in Point of Sale through Point of Sale Devices (X52-10). For the IBM 4226, use the following settings:

Invoice Heading Lines = 0

Spaces Left or Left Margin = 0