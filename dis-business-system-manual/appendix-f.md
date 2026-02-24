---
title: "APPENDIX F"
source: "DIS_Business_System_Manual_Formatted.md"
tags: ["DIS Business System Manual"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A chapter from the DIS Business System Manual about APPENDIX F."
long_description: "This document is a chapter from the DIS Business System Manual, focusing on APPENDIX F."
---

## FORMS ALIGNMENT IBM PROPRINTER & PROPRINTER XL

### INTRODUCTION


### THE ZEN OF ALIGNMENT


Even on the same printer, it helps to think about forms alignment as a process, not something that you do right the first time every time. The most important part of the process is to become comfortable with the system messages and how to answer them.

In general the process goes like this:
- Load the forms.
- Print the first line. Make adjustment.
- Print the first line again. Make adjustment. Repeat this step until you are pretty sure you have the alignment OK. On the AS/400, you do not have the option to print one line at a time. Your choices are to print the same line on the same form, print the same line on the next form, or print the next line and continue without further messages. You don't

## APPENDIX F: FORMS ALIGNMENT IBM PROPRINTER & PROPRINTER XL

ever want to cancel the print job. Of course, with pre-printed checks you don't even want to skip to the next form, so your choices are even more limited.

- Let them print! If you need to make another minor adjustment, take the printer off-line temporarily. It will resume exactly where it left off when you put it back on-line. If you have a forms jam or other semi-catastrophe, see the section TROUBLESHOOTING.
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


System messages tell you when to load special forms, such as checks, and when to reload regular standard paper; however, it must depend on your answers to the messages to "know" what kind of forms are currently in the printer. In addition, when your answer indicates that forms have been changed, the system provides a message to facilitate alignment. In its own clunky mechanical way, it is trying to make your job easier.

Although there seem to be dozens of messages the first time you try to align forms, there are really only 2 different messages:

- Load Forms, which comes at the beginning and end of a job that requires different forms.
- Alignment, which can be repeated as often as necessary.

Your success depends on having the forms almost right when you answer the Load Forms message and then controlling adjustments through the Alignment message.

When you run a job that requires a change of forms, look at the AS/400's "Work with Printer Output" screen. At any DIS menu, type: `D P [Enter]`. The screen is illustrated below. In the example, messages for Past Due Statements (X11-11) is illustrated; however, you will encounter the same messages in Print Statements, Print Payables Checks, printing Letters (new A/R) and Labels.

## Work with Printer Output Screen

Watch the printer output screen to know when your special forms are ready to be printed. At a command Line, type: `D P` [Enter].

```
Work with Printer Output
User . . . . . . . . . EBS      Name, *ALL, F4 for list      System:   S1011024

Type options below, then press Enter. To work with printers, press F22.
2=Change   3=Hold   4=Delete   5=Display   6=Release   7=Message
9=Work with printing status   10=Start printing   11=Restart printing

| Opt | Printer/ Output | Status |
|---|---|---|
| 7 | P1 X12700 | Printer message (use Opt 7)  P9 X51088 | Printer stopped (use Opt 10)  X51088 | Printer stopped (use Opt 10)  X51088 | Printer stopped (use Opt 10)  X51088 | Printer stopped (use Opt 10)  X51088 | Printer stopped (use Opt 10)  X51088 | Printer stopped (use Opt 10)  X51088 | Printer stopped (use Opt 10) |

F1=Help   F3=Exit   F5=Refresh   F11=Dates/pages/forms   F12=Cancel   More...
F14=Select other printer output   F20=Include system output   F24=More keys
```

> NOTE: If the format of your screen doesn't look like this, press F24=More Keys, then F21=Select assistance level and select level 1=Basic.

The message in the column labeled "Status" tells you what to do. Type "7" in the column labeled "Opt" as illustrated above, and press [Enter] to see the Additional Message Information, which may be either the Load Forms message or the Alignment message.


**Load Forms Message**

```
Additional Message Information

Message ID . . . . . . :   CPA3394         Severity . . . . . . . . :   99
Message type . . . . . :   Inquiry
Date sent  . . . . . . :   07/02/97        Time sent  . . . . . . . :   10:10:54

Message  . . . . :   Load form type 'CHKS' device PRT01 writer PRT01. (G B I H R C)
Cause  . . . . . :   The file on output queue PRT01 in library QUSRSYS requires
  form type 'CHKS' to be loaded on device PRT01. The form type for the file
  was all blanks when '' appears as the form type.
Possible choices for replying to message . . . . . . . . . . . . . . . .
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

To see more information, press [PgDn].

The **Load Forms** message, CPA3394, is the first message and it occurs once at the beginning and once at the end of the job. It is displayed when it is time to take the stock paper out of the printer and put checks or statements in or vice versa. The possible answers to this message are:

- **H =** Hold
- **C =** Cancel
- **G =** Go. Answer with a "G" after the specified forms (checks or statements) are loaded. This is the answer you'll use most of the time. It signals the computer that forms have been changed to checks (CHKS) or statements (STAT).


| = Ignore the request for changing forms and use the forms currently on the printer.

R = Retry

The Load Forms message is issued again at the end of the job as soon as the system is ready to print a report or anything that uses forms other than checks or statements. The procedure is the same: Answer with a "G" after the specified forms are loaded.

A COMMON MISTAKE is to take out the statements and reload standard paper before this message is received. The same problem arises when standard forms are removed and special forms loaded before the Load Forms message.

It then seems logical to answer the Load Forms message with an "I," which means you don't want to change forms and that you want to continue on the current forms. The trouble is that now you think "current forms" are standard but the system still thinks "current forms" are checks or statements.

If you find yourself in this situation, follow the instructions in the section TROUBLESHOOTING to change the forms number and restart the print job.

THE BEST PROCEDURE is:
- Don't do anything until you receive the Load Forms message.
- When you receive the message, don't answer it immediately.
- Change the forms as instructed.
- Answer with a "G" to indicate that you have done what the system requested.

## Alignment Message

```
Additional Message Information

Message ID . . . . . . . :   CPA4002                 Severity . . . . . . . :   99
Message type . . . . . . :   Inquiry
Date sent  . . . . . . . :   07/02/97                Time sent  . . . . . . . :   10:13:38

Message  . . . . . . . . :   Verify alignment on printer PRT01. (I G N R E C)
Cause  . . . . . . . . . :   The forms may not be aligned correctly. The first line for the file is 7.
Possible choices for replying to message . . . . . . . . . . . . . . . . . . .
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

The Alignment message, CPA4002, is displayed immediately after the first line is printed. The possible answers to this message are:

- **I =** To continue printing aligned forms starting with the next line of the file, type an I. Statements are printed without further messages.
- **C =** To cancel processing, type a C. **DO NOT USE THIS OPTION.** You cannot re-run Print Statements or Print Payables Checks or Payroll unless you restore a backup, which means you may have to repeat a lot of work.
- **G =** To continue printing aligned forms skipping to the next

**APPENDIX**


form and printing the first line again, type a G. The first check or statement is printed on the next form and no additional *Alignment* messages are presented.

N = To print the first line again on the NEXT form and to verify the alignment,

- Press Stop only if Start and Stop are two keys, or press Reset.
- Advance the paper to the next form by pressing Form Feed/New Page.
- Adjust the alignment with the forms adjust control.
- Press Ready, Start, or Start/Stop.
- Type an N.

> This is the option to take when you have an alignment form.

R = To print the first line again on the current form and to verify the alignment if the forms are not aligned,

- Press Stop only if Start and Stop are two keys, or press Reset.
- Adjust the alignment with the forms adjust control.
- Press Ready, Start, or Start/Stop.
- Type an R.

After you have "authorized" the printing job to proceed without further interruption, you can still make adjustments by taking the printer off-line temporarily. **Do not turn the printer off!** Pressing "Start/Stop" simply suspends printing and the job resumes at exactly the same place in the file when the printer is placed back on-line. This allows you to roll the paper in tiny increments fine tuning alignment as the checks or statements are being printed.

You may want to save output before printing, in case you are having problems with alignment or would simply like additional copies. The following is an example of saving output from statements; however, you



- At a command line, type: D P [Enter].
- Select X11A00 with 3=hold. Place all the entries on hold.
- Press F5=Refresh.
- When the status of X11A00 is "Held," select it with 2=change.
- Press F10=Additional parameters, page down one page.
- Change "Save file" to *YES [Enter].
- Press F5=Refresh.
- Select X11A00 with 6=Release.
- Press F5=Refresh (screen says Printer Message).
- Select X11A00 with 7=to display the Load Forms message.
- Answer message with G.
- Press F5 to refresh printer message.
- Select X11A00 with 7=Message to display the alignment message.
- Answer the message with R to print same line again, or with I to continue.
- Refer to the section for the job you are performing. Realign the forms and proceed with the job.

After the checks have been printed and the first printout is requested, the Load Forms message will be generated again to prompt you to change forms back to standard paper. You'll notice that whatever you requested is not printed immediately.

- To see the message, type: D P [Enter]. The Work with Printer Output screen is displayed (see screen on page 4).
- Find the printer the checks were printed on.
- Find the job you requested.
- Select it with 7=Message to display the Load Forms message.

## Load STD Forms Message

```
Additional Message Information

Message ID . . . . . . . . :   CPA3394         Severity . . . . . . . . :   99
Message type . . . . . . :   Inquiry
Date sent  . . . . . . . . :   07/02/97        Time sent  . . . . . . . . :   10:44:24

Message . . . . :   Load form type '*STD' device PRT01 writer PRT01.  (G B I H R C)
Cause . . . . . :   The file on output queue PRT01 in library QUSRSYS requires form type '*STD' to be loaded on device PRT01. The form type for the file was all blanks when '' appears as the form type.
Possible choices for replying to message . . . . . . . . . . . . . . . :
G -- Begin processing the current file after loading the form type.
B -- Begin processing the current file after loading and aligning the form type (no alignment message is sent  same as option 1 on System/36).
| -- Ignore the request to load the form type. Print the file on the current formtype (same as option 0 on System/36).
                                                                        More...
Type reply below, then press Enter.
Reply . . . . . . . . . . . .   G

F3=Exit   F6=Print   F9=Display message details   F12=Cancel
F21=Select assistance level
```

- Load standard paper if you haven't already done so.
- Answer the message with a G. The next job will be printed.

## PAYABLES CHECKS

When printing payables checks, do not change the forms to checks until prompted to do so by the machine. The check register prints first. If the forms have been changed to checks, the register will print on the checks.

When the check register finishes printing, a *Load Forms* message is generated.

- To see the message, type: `D P [Enter]`. The Work with Printer Output screen is displayed on page 4.
- Look for the printer you use for checks. In the Output column, locate X12700.
- Select X12700 with 7=Message to display the *Load Forms* message, which is illustrated on page 5.
- Before you answer the message, put the checks in the printer. Take the printer off line and press the Form Feed button. Press the On Line button again. Then align the checks as follows:

## Horizontal Alignment

The left perforation should be even with the bold vertical line to the left of the silver numbered scale.

## Vertical Alignment

Use the first check for alignment. Draw a line on the bottom of the first check stub 1/2 inch above the perforation. This line should be even with the top of the print head.


- When the checks are properly loaded, answer with a **G** and press [Enter]. At the bottom of the screen, you'll see a message: “Reply sent to message.” The check number of the first check will print.
- Press [Enter] again to return to the Work with Printer Output screen, where the status of X12700 will be: “*Status changed (use F5).”
- Press F5=Refresh. The status changes to “Message waiting (use Opt 7).
- Select X12700 with 7=Message to display the Alignment message (see screen on page 7).

If the checks are loaded as described, they should only need minor adjustments.

- If a minor adjustment is necessary, roll up or down for adjustment.

- If you want to reprint the 1st line on the same check to verify the alignment before letting all your checks print, answer this message with an **R**. The first line of the check will be printed again on the same check. At the bottom of the screen, you'll see: “Reply sent to message.” The Alignment message will be generated again.

- When you are satisfied with the alignment, answer the message with an **I**, which will print the 2nd line on the same check and continue printing without further messages

- If the alignment needs more than a minor adjustment, press the On Line button to stop the printer. See the section titled TROUBLESHOOTING.

- If you want to save output for extra copies or if you're having problems with special forms, refer back to the steps on page 9.

## APPENDIX F: FORMS ALIGNMENT IBM PROPRINTER & PROPRINTER XL 15

## RECEIVABLE STATEMENTS & PAST DUE STATEMENTS

Regular and interim/past due statements are printed on the same forms. Alignment is the same for both jobs.

When statements are ready to be printed the Load Forms message will be generated to prompt you to load the statements. The balance forward statements will print first, followed by the open item. You will be prompted to change and align forms for both types of statements. When open item statements are ready to print, they will be aligned correctly and all you will have to do is answer the messages.

Do not load the statements until prompted to do so. An error report prints before statements. If statements are loaded, the report will print on the statements.

Before you answer the message, align the forms as follows:

**Horizontal Alignment**
The perforation should be lined up even with the 0 (zero) on the silver numbered scale.

**Vertical Alignment**
The first statement is used for alignment. Feed the first statement up until the top line of the bottom box is even with the print head.

When the forms are properly aligned, answer the Load Forms message with a G. The first line of the address of the first balance forward customer is printed and the Alignment message is generated.

If a minor adjustment is needed use the roll wheel to move up or down.


If you want to reprint the 1st line on the same statement to verify the alignment before letting all your statements print, answer this message with an R. The first line of the statement will be printed again on the same check. At the bottom of the screen, you'll see: "Reply sent to message." The Alignment message will be generated again.

When you are satisfied with the alignment, answer the message with an I, which will print the 2nd line on the same statement and continue printing without further messages.

If the alignment needs more than a minor adjustment, press the On Line button to stop the printer. See the section titled TROUBLESHOOTING.

- If you want to save output for extra copies or if you're having problems with special forms, refer to the steps on page 9.

The message will display again when open item statements are ready to be printed. Answer the Load Forms message with a G. Answer the Alignment message with an I. The forms are already aligned.

After statements have been printed and the first printout is requested, the Load Forms message will be generated again to prompt you to change forms back to standard paper.

## INVOICES

You will not be prompted to change the paper to invoices. Align the invoices as follows:

### Horizontal Alignment

Line the left perforation on the 0 (zero) of the silver numbered scale.

### Vertical Alignment

Align the print head 1/4" above the top line of the SOLD TO box on the invoice.

Create the invoice. Cmd2, Print and Close or Cmd3, Print and Hold will print the invoice. To make minor adjustments, use the wheel to roll up or down.

## TROUBLESHOOTING

Sooner or later things will get messed up: alignment messes up for no apparent reason, forms jam, power fails, or a message is answered incorrectly.

DO NOT TURN PRINTER OFF. Be sure you have stopped the printer by pressing the On Line button and taking the printer off line.

- Display the print spool. At any menu, type: `D P [Enter]`.
- Locate the job. In the column labeled "Printer/Output" you'll see an entry that corresponds to the menu option you're using, as illustrated in the table below:


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


Notes: