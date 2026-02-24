---
title: "APPENDIX K"
source: "DIS_Business_System_Manual_Formatted.md"
tags: ["DIS Business System Manual"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A chapter from the DIS Business System Manual about APPENDIX K."
long_description: "This document is a chapter from the DIS Business System Manual, focusing on APPENDIX K."
---

## FORMS ALIGNMENT LEXMARK 238x/239x PLUS PRINTER

### INTRODUCTION

Don't forget that this printer can use the very first check. The DIS software assumes that one check will be wasted (as it is on most printers) and that it begins on the second check. To compensate, you must remember to enter the first check number minus one (when prompted in Print Payables Checks, X12-8).

In this chapter you'll find instructions for lining up checks, statements, and invoices on Lexmark 238x/239x Plus printers. On the last page, you'll find a table with macro suggestions and settings for invoices, reports, and checks or statements. A sample check and statement are illustrated in Appendix A.

Although you'll find sections on HOW TO ALIGN CHECKS, STATEMENTS, and INVOICES in this chapter, the most important material is contained here in the INTRODUCTION and the following section, SYSTEM MESSAGES. That's because forms alignment is not an exact science: printers of the same make and model may be calibrated differently. Your own printer won't maintain the same alignment forever. As any mechanic can tell you, anything with moving parts changes!

Even on the same printer, it helps to think about forms alignment as a process, not something that you do right the first time every time. The most important part of the process is to become comfortable with the system messages and how to answer them.

In general the process goes like this:

- Load the forms.
- Print the first line. Make adjustment.
- Print the next line. Make adjustment. Repeat this step until you are pretty sure you have the alignment OK.
- Let them print! If you need to make another minor adjustment, take the printer off-line temporarily. It will resume exactly where it left off when you put it back on-line. If you have a forms jam or other semi-catastrophe, see the section "WHAT CAN GO WRONG & WHAT TO DO."

## APPENDIX K: FORMS ALIGNMENT LEXMARK 238x/239x PLUS

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

System messages tell you when to load special forms, such as checks, and when to reload regular standard paper; however, it must depend on your answers to the messages to "know" what kind of forms are currently in the printer. In addition, when your answer indicates that forms have been changed, the system provides a message to facilitate alignment. In its own


clunky mechanical way, it is trying to make your job easier.

Although there seem to be dozens of messages the first time you try to align forms, there are really only 2 different messages:

1.  **Change Forms**, which comes at the beginning and end of a job that requires different forms.
2.  **Alignment**, which can be repeated as often as necessary.

Your success depends on having the forms almost right when you answer the Change Forms message and then controlling adjustments through the Alignment message.

When you run a job that requires a change of forms, look at the AS/400's "Work with Printer Output" screen. At any DIS menu, type: `D P [Enter]`. The screen is illustrated below. In the example, messages for Past Due Statements (X11-9) is illustrated; however, you will encounter the same messages in Monthly Billing or Print Payables Checks.


```
Work with Printer Output

System: S1011024
User . . . . . X Name, *ALL, F4 for list

Type options below, then press Enter. To work with printers, press F22.
2=Change 3=Hold 4=Delete 5=Display 6=Release 7=Message
9=Work with printing status 10=Start printing 11=Restart printing

Printer/
Opt Output Status
P1
7 X11901 Printer message (use Opt 7)

Bottom
F1=Help F3=Exit F5=Refresh F11=Dates/pages/forms F12=Cancel
F14=Select other printer output F22=Work with printers F24=More keys
```

The message in the column labeled "Status" tells you what to do. Type "7" in the column labeled "Opt" as illustrated above, and press [Enter] to see the Additional Message Information, which may be either the Change Forms message or the Alignment message.


**Change Forms Message:**

```
Additional Message Information

Message ID . . . . . : CPA3394      Severity . . . . . : 99
Message type . . . . : INQUIRY
Job  . . . . . . . . : PRT01        User . . . . . . . : QSPLJOB
  Number . . . . . :   170161
Date sent  . . . . . : 05/12/92       Time sent  . . . . :   14:22:03
From program . . . . : QSPPRTWT       Instruction  . . . :   0000

Message  . . . . :   Load form type 'STAT' device PRT01 writer PRT01. (H C G I R)

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

- To see more information, press [PgDn].

```
Additional Message Information

Message ID . . . . . : CPA3394      Severity . . . . . : 99
Message type . . . . : INQUIRY

| -- Ignore the request and process the file.
R -- Retry by researching the output queue.
```


The Change Forms message, CPA3394, is the first message and it occurs once at the beginning and once at the end of the job. It is displayed when it is time to take the stock paper out of the printer and put checks or statements in or vice versa. The possible answers to this message are:

- **H =** Hold
- **C =** Cancel
- **G =** Go. Answer with a "G" after the specified forms (checks or statements) are loaded. This is the answer you'll use most of the time. It signals the computer that forms have been changed to checks (CHKS) or statements (STAT).
- **I =** Ignore the request for changing forms and use the forms currently on the printer.
- **R =** Retry

The Change Forms message is issued again at the end of the job as soon as the system is ready to print a report or anything that uses forms other than checks or statements. The procedure is the same: Answer with a "G" after the specified forms are loaded.

**A COMMON MISTAKE** is to take out the checks or statements and reload standard paper before this message is received. The same problem arises when standard forms are removed and special forms loaded before the Change Forms message.


It then seems logical to answer the Change Forms message with an "I," which means you don't want to change forms and that you want to continue on the current forms. The trouble is that now you think "current forms" are standard but the system still thinks "current forms" are checks or statements.

If you find yourself in this situation, follow the instructions in the section WHAT CAN GO WRONG & WHAT TO DO to change the forms number and restart the print job.

**THE BEST PROCEDURE is:**

- Don't do anything until you receive the Change Forms message.
- When you receive the message, don't answer it immediately.
- Change the forms as instructed.
- Answer with a "G" to indicate that you have done what the system requested.

## Alignment Message:

```
Additional Message Information

Message ID . . . . . . :   CPA4002                 Severity . . . . . . :   99
Message type . . . . . :   INQUIRY
Job  . . . . . . . . . :   PRT01                   User . . . . . . . . :   QSPLJOB      Number . . . . . . :   170161
Date sent  . . . . . . :   05/12/92                Time sent  . . . . . :   14:24:34
From program . . . . . :   QWPXPRMA                Instruction  . . . . :   0000

Message . . . . :   Verify alignment on printer PRT01. (I C G N R)
Cause . . . . . :   The forms may not be aligned correctly. The first line
for the file is 11.
Recovery  . . . :   Do one of the following and try the request again.
Possible choices for replying to message . . . . . . . . . . . . . . . . . :
  I -- To continue printing aligned forms starting with the next line of the
       file, type an I.
  C -- To cancel processing, type a C.
  G -- To continue printing aligned forms skipping to the next form and
       printing the first line again, type a G.
                                                                      More...
Type reply, press Enter.
Reply . . .

F3=Exit             F12=Cancel
```

To see more information, press [PgDn].


```
Additional Message Information

Message ID . . . . . . . :   CPA4002      Severity . . . . . . . :   99
Message type . . . . . . :   INQUIRY

N -- To print the first line again on the next form and to verify the
     alignment,
     1. Press Stop only if Start and Stop are two keys, or press Reset.
     2. Advance the paper to the next form by pressing Form Feed/New Page.
     3. Adjust the alignment with the forms adjust control.
     4. Press Ready, Start, or Start/Stop.
     5. Type an N.

R -- To print the first line again on the current form and to verify the
     alignment if the forms are not aligned,
     1. Press Stop only if Start and Stop are two keys, or press Reset.
     2. Adjust the alignment with the forms adjust control.
     3. Press Ready, Start, or Start/Stop.
     4. Type an R.

Type reply, press Enter.
Reply . . .
                                                                    Bottom
F3=Exit   F12=Cancel
```

The Alignment Message, CPA4402, is displayed immediately after the first line is printed. The possible answers to this message are:

| = To continue printing aligned forms starting with the next line of the file, type an |. Statements are printed without further messages.

C = To cancel processing, type a C. DO NOT USE THIS OPTION. You cannot re-run Monthly Billing or Print Payables Checks or Payroll unless you delete your data files and restore a backup, which means you may have to repeat a lot of work.


**G =** To continue printing aligned forms skipping to the next form and printing the first line again, type a G. The first check or statement is printed on the next form and no additional alignment messages are presented.

**N =** To print the first line again on the next form and to verify the alignment,
- Press Stop only if Start and Stop are two keys, or press Reset.
- Advance the paper to the next form by pressing Form Feed/New Page.
- Adjust the alignment with the forms adjust control.
- Press Ready, Start, or Start/Stop.
- Type an N.

**R =** To print the first line again on the current form and to verify the alignment if the forms are not aligned,
- Press Stop only if Start and Stop are two keys, or press Reset.
- Adjust the alignment with the forms adjust control.
- Press Ready, Start, or Start/Stop.
- Type an R.

> **NOTE**
> Options G and N advance to the next form, which means that they should not be used with pre-numbered checks.

After you have "authorized" the printing job to proceed without further interruption, you can still make adjustments by taking the printer off-line temporarily. Do not turn the printer off! Pressing "Start/Stop" simply suspends printing and the job resumes at exactly the same place in the file when the printer is placed back on-line. This allows you to roll the paper in tiny increments fine tuning alignment as the checks or statements are being printed.

## HOW TO ALIGN CHECKS


### **Warning**

In Print Payables Checks (X12-8), the check register is printed before checks, do not change forms until you are prompted to do so.


- Mount the forms.

**Horizontal Alignment**

- Place the right edge of the left tractor feed on the [A mark, and lock it in place.
- Adjust the right tractor feed accordingly.
- Press "Macro."
- Press "Start/Stop." The printer feeds the checks up so that the perforation is even with the tear bar.


Now go back to the Change Forms message at the console:

- Answer the message with a "G," which means that you have loaded the correct forms. The printer rolls the forms back down into the printer to print the first line.
- The first line of the first check, which is the check number, is printed, and you receive the Alignment message. The alignment should be just about perfect the first time. Make minor horizontal adjustments (left/right), if necessary.
- To print the next line and continue with no further messages, answer with an "I."
- To make an adjustment while the checks are being printed, take the printer off-line temporarily by pressing Start/Stop. After the micro-adjustment, press Start/Stop again to resume printing.
- If more than a micro-adjustment is needed, press Start/Stop. See the section, WHAT CAN GO WRONG & WHAT TO DO, which follows.
- Before the system prints a report that uses standard forms, it issues the Change Forms message prompting you to load form type 'STD'.
- Reload the paper you normally use.
- While the printer is off-line, press Macro. Select the macro you use for reports (DIS suggests Macro 2).
- Answer the message with a "G," which signals the system that it is now using standard forms. This is your insurance that the system will "know" to alert you before attempting to print checks or statements.

## ALIGNING STATEMENTS

Receivable and Past Due Billing Statements are printed on the same forms so the alignment is the same for both. Balance Forward statements are printed first. When it is time for the Open Item statements, the system issues both the Change Forms and Alignment messages again. Although no action is necessary, the messages are answered differently for open item statements.

### Balance Forward Statements:

When the system is ready to print Balance Forward statements, you'll receive the Change Forms message.

- Make sure the printer is off-line by pressing Start/Stop.
- Mount the forms.

#### Horizontal Alignment

- Place the perforations on the [A mark, and lock the tractor feed in place.
- Adjust the right tractor feed accordingly.

- Press "Macro." Select the macro you use for statements (DIS suggests Macro 3).
- Press "Start/Stop." The printer feeds the checks up so that the perforation is even with the tear bar.
- Now go back to the Change Forms message.
- Answer the message with a "G," which means that you have loaded the correct forms. The printer rolls the forms back down into the printer to print the first line.
- The first line of the first statement, which is the customer's name, is


printed, and you receive the Alignment message. The alignment should be just about perfect the first time. Make minor horizontal adjustments (left/right), if necessary.

- To print the next line and continue with no further messages, answer with an "I."
- To make an adjustment while the statements are being printed, take the printer off-line temporarily by pressing Start/Stop. After the micro-adjustment, press "Start/Stop" again to resume printing.
- If more than a minor adjustment is needed, press the Start/Stop button on the printer. See the section, WHAT CAN GO WRONG & WHAT TO DO, which follows.
- Before the system prints a report that uses standard forms, it issues the Change Forms message again.
- Reload the paper you normally use. Answer the message with a "G," which signals the system that it is now using standard forms. This is your insurance that the system will "know" to alert you before attempting to print checks or statements.

## WHAT CAN GO WRONG & WHAT TO DO

Sooner or later things will get messed up: alignment messes up for no apparent reason, forms jam, power fails, or a message is answered incorrectly.

> **WARNING**
> Take the printer off-line. Do not turn the printer off. Do NOT attempt to set Top of Form in the middle of running checks or statements unless you put the spool on hold first.

- As soon as you are aware that there is a problem, take the printer off-line by pressing Start/Stop.
- If the alignment is slightly off. Decide which way the form is off. Do not adjust the form position manually.
- Make Micro adjustments:
    - To print higher on the page, press Micro Down to move the form down.
    - To print lower on the page, press Micro Up to move the form up.
    - Press Start/Stop to put the printer on-line.

## Starting Over

In case of a forms jam, it's better to start over than to lose several checks
or statements. Since you can't run the jobs, such as Monthly Billing or
Print Payables Checks, a second time, starting over means only the print
job.

- Display the print spool. At any menu, type: D P [Enter].
- Locate the job. In the column labeled "Printer/Output" you'll see an
  entry that corresponds to the menu option you're using, as illustrated in
  the table below:

| DIS Menu Option: | JOBNAME |
| :--- | :--- |
| Monthly Billing (X11-8) | X118*** |
| Past Due Billing (X11-9) | X119*** |
| Print Payables Checks (X12-8) | X128*** |

- Select option 3, Hold. Put this print job (and any other print jobs) on
  hold.
- Select option 2, Change. The "Change spooled print entries" options
  are displayed.
- Select option 2, Change forms number. The CHANGE COMMAND
  prompts are presented, as illustrated below:
- Change the forms to XXXX. The reason for this is to "trick" the system
  into sending the Change Forms and Alignment messages again when
  the print job is restarted.
- Press [Enter]. Press [Cmd3] to return to the first SPOOLJOB menu.
- Select option 4, Release entries. Release the print job. The print job will
  begin at the beginning.

## ALIGNING INVOICES

Because it is customary to have a printer dedicated to invoices, they are not distinguished from standard forms. There is no special name, such as CHKS or STAT. Likewise, the system does not send messages regarding alignment for invoices.

- Establish the default printer for each user through Point of Sale Devices (X52-10). For the LexMark 238x/239x, use the following settings:
    * Invoice Heading Lines = 0
    * Spaces Left or Left Margin = 5

- Printer Configuration:
    * CPI (Characters Per Inch) = 10
    * LPI (Lines Per Inch) = 8
    * Form Length = 42 Lines Per Page (or 5.25")

- Mount the invoices.
- Press Macro. Select the macro you use for Invoices (DIS suggests Macro 1).
- Press Load/Park. The printer feeds the invoices up so that the perforation is even with the tear bar.

### Horizontal Alignment

Align the right edge of the left tractor feed on the [A mark and lock it. Align the right tractor feed accordingly.

- Print a test invoice.

*If the alignment is slightly off. Decide which way the form is off. Do not adjust the form position manually.*

**APPENDIX**


- Press Start/Stop to take the printer off-line.
- To print higher on the page, press Micro Down to move the invoice down.
- To print lower on the page, press Micro Up to move the invoice up.
- Press Start/Stop to put the printer on-line.
- Print another test invoice. Do not adjust the form position manual-ly.
- Repeat until the text on the invoice is perfectly aligned.

## CHAPTER X1-1

## RECEIVABLES MENU

### INTRODUCTION

The accounts receivable applications are designed to assist you in managing one of the most important assets of your business - the money owed by your customers.

From the Receivables Menu you will:
- enter, review, and update customer information
- enter and update payments
- apply credits
- enter and configure warranty payments
- calculate and post interest
- print scheduled, interim, and past due statements
- create and print letters to your customers
- create and print receivables reports
- calculate the age of receivables

You will also be able to:
- age transactions from the transaction date to the session date, not by the billing process.
- charge different rates of interest to different customers
- start charging interest on an individual transaction at a future date

Even though interest charges are postponed, transactions age normally. You might want to keep this in mind when you compose messages that appear on statements. Transactions set to not charge interest for 999 days will be considered "permanently current" and will never age regardless. See also the OPT Menu X6379-7, 8 Aging vs. "Days Until Interest."

- post interest at any time

Although you can post interest at any time, interest is always calculated to the end of the month; therefore, you don't want to post it more than once a month. The date interest was posted last is displayed on the Calculate & Post Interest screen. Immediately after the conversion, the date of conversion is displayed. See Understanding Interest Calculations, which begins on page 8.

- print unposted interest on statements


2 	 X1-1 • RECEIVABLES MENU 	 RELEASE 2.2

Unposted interest is included in the total balance due. If a customer pays the unposted interest printed on a statement, post the unapplied credit, then make a journal entry to post the interest. Use Apply Credits to merge the payment with the interest.

- print statements more than once a month or print a statement for 1 customer
- print past due/interim statements at any time
- Current transactions are not merged into balance forward.
- change a customer's statement type from balance forward to open item at any time
- write letters to customers and attach a list of outstanding transactions

**CONTENTS**


| --- | --- |
| ENTRANCE SCREEN | 3 |
| RECEIVABLES MENU OPTIONS | 4 |
| UNDERSTANDING INTEREST CALCULATIONS | 8 |


X1-1 • RECEIVABLES MENU
3

**ENTRANCE SCREEN**

- From the Accounting Menu (X1), select option 1, Receivables Menu and press [Enter]. The Receivables Menu appears.

```
COMMAND MENU: X11 FA
(c) DIS Corp.

RECEIVABLES MENU

Customers
1. Receivables Inquiry
2. Receivables Maintenance
3. Group Code Maintenance
4. Apply Credits

Deposits
5. Enter Payments
6. Configure Payments

Warranty
7. Enter Warranty Payments
8. Configure Warranty Payments

Statements
9. Calculate and Post Interest
10. Print Statements
11. Print Interim/Past Due Statements

Letters
12. Letters Maintenance
13. Print Letters

Other
14. Receivables Report Menu
15. Calculate Receivables Aging

23. Return To Accounting Menu
Ready for option number or command
===>
```

Screen A: Receivables Menu

- To select a menu item, type the number of the item and press [Enter]. The entrance screen for that menu item appears.

- To return to the Accounting Menu, type 23 and press [Enter]. The Accounting Menu appears.


X1-1 • RECEIVABLES MENU
## RECEIVABLES MENU OPTIONS

The Receivables Menu includes the following options:

**1. Receivables Inquiry**

Select this option to review all information concerning your receivable customers including:

- source information entered in Receivables Maintenance
- statistics on the last invoice, the last payment, the last interest charged, and the last letter sent to each customer
- a summary history, from the first entry, of all invoices, payments and discounts for each customer
- all current and history transactions for each customer
- transaction detail for each invoice and payment

**2. Receivables Maintenance**

Select this option to manage customer account information including:

- open receivable accounts for new customers
- modify information on established receivable accounts, including credit card information
- delete customer accounts

**3. Group Code Maintenance**

Select this option to create, modify or delete group codes. Group codes are used to specify which receivable accounts will be included in reports.

**4. Apply Credits**

Select this option to merge payments (credits) with their corresponding invoices (debits), and to change the number of days for calculating interest for a particular invoice.

If you have entered receivables credits in Create Source Documents (X1-7) or Point Of Sale Invoicing (X5-1), you will merge them with the corresponding debits. If you enter all your payments from the Enter Payments (X11-5), you will use this option to merge the debits and credits.


X1-1 • RECEIVABLES MENU
5

5. Enter Payments
Select this option to enter the payments from your receivable customers. Under this option you are able to enter accounts receivable payments, enter cash receipts, and post these transactions to the general ledger. You can use this option to post your write-offs directly to your general ledger adjustment account. You can also post your accounts receivable discounts and adjustments.

6. Configure Payments
Select this option to customize your payments. Under this option you are able to set up receipt types, set up accounts receivable payments, and set up levels in the general ledger. These defaults are used in Enter Payments (X11-5).

7. Enter Warranty Payments
Select this option to enter your warranty payments and to apply them to your claim transactions. You can also transactions to adjust the differences between claim amounts and payment receipts. Also, you can process payments for a single warrantor per batch.

8. Configure Warranty Payments
Select this option to customize your warranty payments. Under this option you will set up the defaults that will appear in Enter Warranty Payments (X11-7).

9. Calculate and Post Interest
Select this option to calculate and post interest to your receivable accounts. During this procedure, the system will determine the number of days for calculating interest in the following order:
- Transaction, as specified in Apply Credits (X11-4)
- Customer, as specified in Receivables Maintenance (X11-2)
- Division, as specified in Security Maintenance (X6-6) for all the receivables
- If all these fields are blank, the default will be 30 days.

10. Print Statements
Select this option to print statements in a regular cycle. To print statements between cycles, run Print Interim/Past Due Statements (X11-11). From this option, you can also calculate interest that will print on statements without

## X1-1 RECEIVABLES MENU

posting the interest to the customer accounts. To calculate and post interest, run Calculate And Post Interest (X11-9).

### 11. Print Interim/Past Due Statements

Select this option to print interim or past due statements for selected receivables. You can print Interim/Past Due Statements at any time. Current transactions (activity since the most recent regular statement) will be listed. Customers can be selected based on the Number of Days That Make Collection Critical, which is set up by customer in Receivables Maintenance (X11-2). The Aged Receivables Collection Report, which shows trending information, is also based on the same field.

Print Interim/Past Due Statements will display all transactions since the last time Print Statements (X11-10) was run for both balance forward and open item statement types. Print Interim/Past Due Statements can be run repeatedly without affecting the status of transactions in accounts. Current transactions will not be merged into balance forward and will appear as current transactions the next time Print Statements is run.

### 12. Letters Maintenance

Select this option to write and save letters, which will be sent to charge customers. Only address numbers in the receivables file are used for letters. A list of outstanding invoices in any aging category may be attached as an appendix to any letter. Although variables, such as names and addresses, even balances, may be embedded in letters, the actual recipients are selected in option 13, Print Letters.

### 13. Print Letters

Select this option to print letters that were created in option 12, Letters Maintenance. Only receivables customers are eligible to receive letters. Letters can be sorted by Name, Address#, or Zip Code and addressed to customers selected by: G/L Account; Group Code; Address Number; Age Category; Area, Zip, Sort, or Edit Codes. An optional appendix may be attached listing outstanding transactions.

### 14. Receivables Report Menu

Select this option to access the menu of receivables reports. The reports include:

- three reports of chronological age
- a detailed list of all information concerning your receivables
- a summary list of information concerning your receivables
- a list of all customers that have exceeded their limit credit
- a list of the credit conditions of your receivable


X1-1 • RECEIVABLES MENU 7

- a list of all customers without statements
- a volume list
- an insurance expiration report
- a receivables master report

**15. Calculate Receivables Age**

Select this option to calculate the age of all receivables accounts for all of your divisions form their transaction dates to the current session date. To calculate the age for a particular receivable account, go to the Receivables Menu (X1-1), option 1, Receivables Inquiry. The age of all receivable accounts is calculated automatically during the end of day procedure.


8	X1-1 RECEIVABLES MENU	RELEASE 2.2

## UNDERSTANDING INTEREST CALCULATIONS

The purpose of this section is to explain how interest is calculated and suggest ways you can make it work effectively for your business.

Transactions are aged in real time, meaning that if you allow a 30-day grace period, a transaction is current until the 31st day after it is created. **Interest is charged for the whole month on transactions that will be over their allotted number of days as of the end of the month.**

**Example 1.** A transaction (T) charged on May 28 is still current (less than 30 days) on June 25, but it will be over 30 days old on June 30. If you calculate and post interest (I), then run statements (S) on June 25, interest will be charged on a current transaction for the entire month of June when it appears on the customer's statement for the first time.

**May 1998**

| Sun | Mon | Tue | Wed | Thurs | Fri | Sat |
|---|---|---|---|---|---|--- 1 | 2 |
| 3 | 4 | 5 | 6 | 7 | 8 | 9 |
| 10 | 11 | 12 | 13 | 14 | 15 | 16 |
| 17 | 18 | 19 | 20 | 21 | 22 | 23 |
| 24 | 25 | 26 | 27 | 28 T | 29 | 30 |
| 31 

> 5/28 transaction will be current but interest will be applied for the month of June

**June 1998**

| Sun | Mon | Tue | Wed | Thurs | Fri | Sat |
|---|---|---|---|---|---|--- 1 | 2 | 3 | 4 | 5 | 6 |
| 7 | 8 | 9 | 10 | 11 | 12 | 13 |
| 14 | 15 | 16 | 17 | 18 | 19 | 20 |
| 21 | 22 | 23 | 24 | 25 I/S | 26 | 27 |
| 28 | 29 | 30 

If you don't want this to happen, but you want to continue running statements on the 25th, you can change "Days Before Int" field in Security Maintenance (X6-6) to a number higher than 30. The number will be based on the day you actually run statements: 30 (Number of days in month) - 25 (Day you charge interest) = 5 (Difference); 30 (Current setting) + 5 (Difference) = 35 (New setting).

In the example above, with 35 days before interest is charged, the 5/28 transaction will be current until July 1, and no interest will be charged on June 25.

This setting can be changed as often as you like so it can accommodate February and months with 31 days. Don't forget that "Number of Days to Charge Interest"


ACCOUNTING	X1-1 • RECEIVABLES MENU	9

can be changed on the customer's master record (Receivables Maintenance X11-2) and at the invoice level in Apply Credits (X11-4).

**Example 2.** A transaction (T) charged on May 1 is still current (less than 30 days) on May 25, and it will still be current on May 31. If you calculate and post interest (I), then run statements (S) on May 25, no interest will be charged.

> 5/1 transaction will be current and no interest will be applied for the month of May

**May 1998**

| Sun | Mon | Tue | Wed | Thurs | Fri | Sat |
|---|---|---|---|---|---|--- 1 T | 2 |
| 3 | 4 | 5 | 6 | 7 | 8 | 9 |
| 10 | 11 | 12 | 13 | 14 | 15 | 16 |
| 17 | 18 | 19 | 20 | 21 | 22 | 23 |
| 24 | 25 I/S | 26 | 27 | 28 | 29 | 30 |
| 31 

**June 1998**

| Sun | Mon | Tue | Wed | Thurs | Fri | Sat |
|---|---|---|---|---|---|--- 1 | 2 | 3 | 4 | 5 | 6 |
| 7 | 8 | 9 | 10 | 11 | 12 | 13 |
| 14 | 15 | 16 | 17 | 18 | 19 | 20 |
| 21 | 22 | 23 | 24 P | 25 I/S | 26 | 27 |
| 28 | 29 | 30 

The 5/1 transaction falls into the 30-day category on June 4. If the transaction is paid (P) on June 24, the customer will not be charged any interest when it is calculated on June 25. In this case, the customer has enjoyed 20 additional interest-free days. However, if the transaction has not been paid when interest is calculated on June 25, interest will be charged for the entire month of June.

A strategy adopted by some dealers is to establish a due date, such as the 10th of the month. It is clearly indicated on the customer's statement that they must pay by the 10th to avoid interest charges. On the 11th, interest (I) is calculated and posted even though statements (S) are not printed until the 25th.

**June 1998**

| Sun | Mon | Tue | Wed | Thurs | Fri | Sat |
|---|---|---|---|---|---|--- 1 | 2 | 3 | 4 | 5 | 6 |
| 7 | 8 | 9 | 10 | 11 I | 12 | 13 |
| 14 | 15 | 16 | 17 | 18 | 19 | 20 |
| 21 | 22 | 23 | 24 P | 25 S | 26 | 27 |
| 28 | 29 | 30 

In this case, the 5/1 transaction that is paid (P) on the 24th is still charged interest (I) for the month of June on the statement (S) that is printed on the 25th.

### X1-1 • Receivables Menu

Remember to calculate and post interest only once a month! On the selection screen, which is illustrated below, make sure you are calculating interest for the current month only. In the example, note that interest was last calculated on 5/25/98. It is now 6/25/98. If you indicate that you want to calculate interest for a future month by entering 0798, interest will be calculated for 2 full months on every transaction. **If you make a mistake,** (you'll notice that the interest is too high), press Cmd1-End from the Update Interest screen. Do not post the batch unless you enjoy making corrections!

```
NW EQUIPMENT SALES                                   CALCULATE AND POST INTEREST                X11901-01
Division A                                           Select General Ledger Month

                                                     Current Month/Year
Enter G/L period for calculation of interest . . . . . . . . : 098 (MMYY)

Note: The last day of this period will be used for the interest
      calculation. For example, if G/L period 0598 is specified,
      interest will calculate as of May 31, 1998 regardless of the
      day on which this job is run.

Interest Transactions : Document number . . . . . . . . . . . : INTEREST
                      Description . . . . . . . . . . . . . .

Date interest last posted . . . . . : 52598
```

You should make sure you have run Apply Credits to merge unapplied payments.

Cmdl-End

## CHAPTER X1-11

## JOURNALS MENU

### INTRODUCTION

Journals, which are available through an OPT switch (General Ledger Menu, option 4), can be activated or de-activated at any time. The familiar ID code from Create Source Documents (X1-7) identifies each journal. A transaction report and recap by account number is produced for each journal when a batch is posted. On the Accounting End of Day Report, transactions are grouped and subtotaled by their respective journals. In addition, all journals are printed automatically at Accounting End of Month.

On the Journals Menu there are options for creating and describing as many Journal IDs as you need and for assigning Journal IDs to automatic transactions such as Monthly Billing. Transactions from Point of Sale are directed to specific journals through sales codes (see "Sales Codes").

The Journals Menu is illustrated below.

```
COMMAND MENU: X1B X1
(c) DIS Corp.

JOURNALS MENU

1. Journal Id Maintenance
2. Automatic Posting Id Maintenance
3. Journal Inquiry
4. Print Journals

23. Return To Accounting Menu

Ready for option number or command
```

## X1-11 JOURNALS MENU

The options on the Journals Menu are described below.

- Journal Id Maintenance
  Use Journal ID Maintenance to add, change, or delete journal IDs.

- Automatic Posting Id Maintenance
  Use Automatic Posting ID Maintenance to assign Journal IDs, which are set up in Journal ID Maintenance (X1.11-1), to jobs that post transactions automatically, such as Monthly Billing. This has the effect of posting automatic transactions to the specified journal.

- Journal Inquiry
  Use Journal Inquiry to look at transactions grouped by Journal ID. You can roll through transactions or skip directly to any ID or document number.

- Print Journals
  Use this job to print a report of all journals or select up to 10 journals. The report can be for one General Ledger month or for a date range. The security gate allows you to specify one division or request the same report for all divisions.

### SALES CODES

To associate various Point of Sale transactions with different journals, you can assign a journal ID to a sales code. The Sales Code Maintenance screen (X52-3) is illustrated below.

```
A & R SALES & LEASING CO	SALES CODE MAINTENANCE	X5230-101 1

Sales Code PC							2
Description	PARTS CUSTOMER
						Current Sales Code
```

| Format | | Description  Description |
| :--- | :- | :--- | :- | :--- | :--- |
| P | 'L' | Labor | 'P' | - | Parts  'D' | Misc. Description | 'C' | - | Prepayments  'M' | Misc. Quantity | 'A' | - | Received on Account  'U' | Misc. Units | 'W' | - | Unit Sales  'N' | Notes | 'S' | - | Misc. Cost  Debit | Credit | Discount | 'Wild Card' account #'s:  :--- | :--- | :--- | :--- | :--- | :--- |
| Customer Document | *AUTO | A3320 | A3320 | *AUTO | - any format |
| Internal Document | *ERROR | *ERROR | *ERROR | *SALE | - 'P' or 'W' |
| Warranty Document | *ERROR | *ERROR | | *ERROR | format only |
| Journal Id | -- | -- | | *ERROR | - any format |
| Override Tax Code | -- 
| Override Discount Code| -- 
| Vendor for Parts | VVV | (optional)  GST Rate  GST Account  |

```
Cmd1-End job	Cmd3-Go back	Cmd19-Delete this sales code
```

Note the new field labeled "Journal Id," which follows the G/L account assignments for Warranty Documents.


Notes:

## CHAPTER X1-12

## END OF YEAR MENU

### INTRODUCTION

Of course, not all of you end your accounting year on December 31; however, the process for ending a fiscal year is the same. There are also several jobs that must be run at the end of the calendar year, as well.

The End of Year Menu options pertain to the end of the calendar year and the end of the fiscal year. The jobs specifically for file maintenance should be run at the end of the fiscal year and other times as needed.

### Additional Products

DIS offers the following additional products related to End of Year procedures:

**U.S. & Canadian Tax Calculators**


**Sold Units Purge for S/36 & Y10 Users**

If you'd like to purge information on sold units, DIS has an additional product that will do it for you. If you want more information about it or would like to receive it, please call the Response Line.

### Calendar Year End Jobs

These are jobs that should be run at the end of the calendar year regardless of when your fiscal year starts.

**Parts End of Year**

This job is optional. It removes sales history over two years old from the parts files and helps save space on your disk. If you are running the job after December 31, your parts sales history will not reflect complete years. You should change the date on your terminal to December 31 before starting the job. To do that, just type DATE 123190 and press [Enter]. Run

## X1-12 END OF YEAR MENU

the job at the same terminal before signing off.




**Fiscal Year End Jobs**

If you're not certain when your fiscal year ends, go into Security Maintenance (X6-6) and check the screen for your division. The month your fiscal year starts can be found in the bottom right corner of the screen. The GL month listed above it is your oldest open month. Don't change these months! Just use them for reference.

**Accounting End of Year**

This procedure must be run after closing the last month of your fiscal year and before closing the first month of the new year. End of Year is very easy to run. Go to Menu X1-12 and take option 1. Post to the first day of the first month of your new fiscal year. Make sure the job has cleared the user board (D U) before you let anyone else back on the system. After it has completed, run a Financial Statement for your 1st month. All the Income Statement accounts (Sales, Cost, Income, and Expense) should be zeroed out and the balances posted to Retained Earnings.

**Accounting End of Year Adjustments**

Your adjustments can be made in the last month of your fiscal year if you want to get them in before you close the year. Often, you don't get the adjustments from your accountant until you're well into the new year. If you are expecting adjustments, keep the first month of your new year open until you can post them. It is possible to post them into any open month, but remember that if you close the first month and enter them into the second month, your first month's financial statement won't reflect the changes.

When you get the adjustments, go to Menu X1-12 and take option 2.


> **Note:**
> THIS JOB MUST BE DONE AFTER YOU HAVE RUN ACCOUNTING END OF YEAR.

Post the transactions to the first day of the first open month (hopefully, the first month of your new fiscal year.) After the batch has posted, run Financial Statements for the 13th month and the 1st month. The 13th month is always closed, by the way. The 13th month Statement should show the End of Year totals with the adjustments. The 1st month Statement should show any adjustments made to Balance Sheet accounts (Assets and Liabilities), and it should show the adjusted balance for Retained Earnings. Current Month and Year to Date figures on the Income Statement should be the same.

## Subledger Adjustments

If you posted any adjustments to accounts with edit codes (for example, Accounts Receivable, Accounts Payable, Units Cost or Inventory), you will have to adjust your subledgers separately because 13th Month Adjustments automatically overrides all edit codes. To adjust your subledger, go into Create Source Documents for the first open month and post your subledger adjustments, using the following examples as a guide:

**Debit to Accounts Receivable:**
D Accounts Receivable      include address #
< Accounts Receivable      no address #

**Credit to Units Inventory**
C Inventory                include stock #
> Inventory                no stock #


In other words, debit or credit the account you want to adjust, and credit or debit override the same account for the same amount. The first transaction puts the amount into the GL and the sub, and the override transaction takes it out of the GL account and leaves it in the sub. When you're done, run your subledger reports or the Subledger Balance Report (X14-5) and a current Financial Statement to make sure everything is in balance.

## Units End of Year

This job needs to be run by all users. Some of the things it does is move the Current Depreciation totals into Past Depreciation and it clears out the Rental Year-to-Date Utilization buckets. Go to Menu X1-12 and take option 4 to run it.

## End of Year File Maintenance

This job is available for Receivables, Payables, and General Ledger. All the options are on Menu X1-12. Make sure you have a dedicated system before you take the options for these jobs. You will receive a report of any accounts you have marked for deletion. If there are some you want to keep, reinstate them before you continue. If you want to purge them, continue to the next screen. Receivables and Payables address #'s will be removed from u.REM and u.PAM, and from u.ADM (u = user id) unless they have the edit codes from other applications such as POS Cash Customers or Rentals. General Ledger account numbers will be removed from u.GLM. Make sure the General Ledger accounts have had a zero balance for the past year before they are removed. Otherwise, you won't be able to run past Financial Statements with correct totals because they'll be out of balance by the amount in the accounts you deleted.

## LIFO End of Year

You will run this job only if you're using the DIS LIFO system. The LIFO Setup Procedure would have been run last January and the LIFO file u.ILA and u.ILM would have been saved to diskette (u = user id). Get this

**ACCOUNTING**


diskette and put it into S1. Type RESTORE u.ILA. <ENTER>. Repeat for u.ILM. After the files are restored, take the option on Menu X3- 11 for LIFO End of Year. Follow the directions on the screen. If you have any questions about what you're doing, press CMD10 for instructions.

## ACCOUNTING END OF YEAR

The Accounting End of Year job allows you to close your accounting year. After the year is closed, adjustments to the previous year are made in the thirteenth month. These adjustments are made in Accounting End of Year Adjustments and may be made all year long. If you have any questions about the Accounting End of Year process or concepts, refer to What is End of Year? and What is the Thirteenth Month? which are included in this chapter.

To reach the End of Year Menu (shown below), select option 12 from the Accounting Menu (X1). A summary of each option follows.

```
COMMAND                               MENU: X1C                       ES
(c) DIS Corp.

                           END OF YEAR MENU


1.  Accounting End Of Year                      (FISCAL)
2.  Accounting End Of Year Adjustments          (FISCAL)
4.  Depreciation End of Year                    (FISCAL)
5.  Receivables File Maintenance                (AS NEEDED)
6.  Payables File Maintenance                   (AS NEEDED)
8.  Rentals End of Year                         (CALENDAR)
10. Sold Units File Maintenance                 (AS NEEDED)

23. Return To Accounting Menu

Ready for option number or command
```

## OVERVIEW OF THE END OF YEAR MENU OPTIONS

The options on the End of Year Menu are described below.

**X1.12-1 Accounting End of Year (FISCAL)**
Accounting End of Year will close the books for the fiscal year. The accounts on the Operating Statement will be debited or credited automatically and the offsetting entry to Retained Earnings will be made. Accounting End of Year is divisional and must be run for each division.

**X1.12-2 Accounting End of Year Adjustments (FISCAL)**
Accounting End of Year Adjustment allows you to make manual adjustment entries to a thirteenth month. You can then run a Thirteenth Month Financial Statement with correct balances current profit/loss and the Operating Statement accounts on the Financial Statement for the previous year after the year has been closed.


**X1.12-4 Depreciation End of Year (FISCAL)**
Depreciation End of Year is for dealers who are using the system to depreciate units automatically. This job moves


the figures in the "Current Depr" field in Inquire/Update Units to the "Past Depr" field, and sets "Current Depr" to zero. This job should be run at fiscal year end. The job is divisional and must be run for each division.

**X1.12-5 Receivables File Maintenance (AS NEEDED)**

Receivables File Maintenance will remove all deleted receivables customer numbers from ADM, Address Master file, and REM, Receivables Master File where they are stored. Also deleted customer transactions are removed from REA, Receivables Transaction file and REH, Receivables History Transaction file. As a result, files will be smaller and there will be more room on the disk.

**X1.12-6 Payables File Maintenance (AS NEEDED)**

Payables File Maintenance will purge from the ADM, Address Master file, and PAM, Payables Master file all deleted vendor numbers. Also transactions for deleted vendors will be purged from PAH, Payables History Transaction file and PAA, Payables Transaction file. It is a divisional job. This will make more room on the disk of the computer. The files will be smaller.

**X1.12-8 Rentals End of Year (CALENDAR)**

Rentals End of Year sets Year-To-Date (YTD) figures to zero for Rental Status and the Utilization Report. Run it at the end of the calendar year. The job is divisional and must be run for each division individually.

**X1.12-10 Sold Units File Maintenance (AS NEEDED)**

Sold Units File Maintenance purges a selected unit or units sold before a user-specified date.


**X1-12 END OF YEAR MENU**

## WHAT IS ACCOUNTING END OF YEAR?

Those of you who understand the End of Year process and the Accounting End of Year Adjustments made to the Thirteenth Month Financial Statement may proceed to the chapter containing the job to be performed. If you have any questions regarding the process, read the following sections carefully before performing any of the jobs.

Accounting End of Year will close the books on the fiscal year. The operating accounts will be debited or credited automatically and the offsetting entry will be made to the Retained Earnings account.

Once the last month of the previous year is closed and you close the year, any adjustments that are going to be reflected in the profit/loss for the previous year will need to be made in Accounting End of Year Adjustments (X1.12-2). These changes for the previous year will appear on the Thirteenth Month Financial Statement.

Many people do not use thirteenth month adjustments. They simply leave the year open until they receive the adjustments necessary from their accountants. Because of disk space problems or the slowness of the accountant in recommending adjustments, leaving many months open may be very inconvenient.

With this system, you can close the fiscal year. You can then make adjustments to the thirteenth month. The Thirteenth Month Financial Statement will reflect the changes made to the previous year and give you a statement with accurate operating statement account balances and current profit/loss.

### What Is The Thirteenth Month?

Accounting End of Year Adjustments are made after a year is closed to reflect a change in the picture of profit and loss for the previous fiscal year. For example, closing the year debits or credits your operating statement accounts automatically and makes an offsetting entry to Retained Earnings. If an adjustment needs to be made to an expense for the previous year, post a thirteenth month batch. Retained Earnings will also be adjusted automatically on the current years statements to reflect the change.

The posting date for Accounting End of Year Adjustments should be the first date of the oldest open month of the new year.

Those of us familiar with manual systems remember obtaining the adjustments from our accountants two months after we have been assured that there will be no further adjustments. In the meantime, we have closed the year and delivered the financial statement to our bank for next year's credit line considerations.

Once those adjustments were received, we would take our pencil and erase the balance in the Retained Earnings account, credit or debit the Retained Earnings and make the offsetting adjustment to the Inventory account for example, and resubmit a corrected Financial Statement to the banker. Big headache.

The Accounting End of Year Adjustment job has basically the same effect. Once a general ledger month is closed, you cannot make any further entries to that month. For example, let's say that the year ends on

### **12** X1-12 End Of Year Menu

December 31,1986. If the month of December is closed, no further posting can be done to December. The next step is to close the year. If the year is closed, the January statement will show the profit or loss for the previous year in the Retained Earnings account. The Operating Statement accounts will have no balances for the previous year. The question is, how do you affect last year with these adjustments provided by the accountant?

Easy--do Accounting End of Year Adjustments (X1.12-2). The entries made will be posted to a thirteenth month. The thirteenth month equals the balances on the December Statement at the close of the month and all adjustments that need to be made. It has the effect of taking your eraser and adjusting the December Financial Statement for resubmission to the bank.

### **File Maintenance Jobs**

Some of the file maintenance jobs are used to purge out deleted address and account numbers from the files on the disk. Each number equals a record. Records take up room in files. Purging the numbers should create more room in your files.


Notes:

## CHAPTER X1-2

### PAYABLES MENU

**INTRODUCTION**

The Payables Menu is illustrated below:

```
COMMAND                                  MENU: X12                                      XA
(c) DIS Corp.

                               P A Y A B L E S   M E N U


1. Vendor Inquiry                          10. List of Vendors (Summary)
2. Vendor Maintenance                      11. List of Vendors (Detail)
3. Group Code Maintenance
4. Correct Due Dates and Discounts
5. Invoice Entry                           14. Aged Payables Summary Report
6. Cancel Invoices                         15. Aged Payables Detail Report
7. Print Payable Checks                    16. Payables Due Today
8. Enter Manual Checks                     17. Vendor Totals for 1099 Preparation
9. Cancel Checks


                               23. Return to Accounting Menu

Ready for option number or command
===>
```

## OVERVIEW

Options on the Payables Menu are briefly described below:

1.  **Vendor Inquiry**

    Vendor Inquiry allows you to review vendor information including current and history transactions. Vendor information is set up in Vendor Maintenance (X12-2). Transactions are posted by Invoice Entry (X12-5), Cancel Invoices (X12-6), Print Payable Checks (X12-7), Enter Manual Checks (X12-8), Create Source Documents (X1-7), or Post Point of Sale Documents (X55-2).

2.  **Vendor Maintenance**

    Use Vendor Maintenance to:

    *   Set up and maintain a vendor's master record (3 screens)
    *   Specify a general ledger account (credit entry) for the vendor
    *   Establish a distribution table of fixed amounts or percentages for one or more general ledger accounts (debit entry)
    *   Record notes pertaining to the vendor, which can be seen in Vendor Inquiry

## X1-2 PAYABLES MENU

3. Group Code Maintenance

   Group Code Maintenance allows you to create or modify groups to which vendors can be assigned. Checks and reports may be printed according to what group (if any) vendors are assigned.

4. Correct Due Dates & Discounts

   Use this job to change posted invoices. You may change discounts and due dates (Cmd2-Change), merge transactions (Cmd3=Merge), or split a transaction (Cmd4=Split). "Change," "Merge," and "Split" are referred to as "modes." You can search for (position to) a specific transaction by Invoice Number or Due Date. By pressing F9, you can display transactions sorted in order by Due Dates, Invoice Numbers, or Unit Numbers.

5. Enter Invoices

   Invoice Entry is a version of Create Source Documents, similar to Receivables Payment Entry. It is specifically designed to enter vendor invoices quickly. The batch is not posted until you press [Cmd12]-Post Invoices. This job is both interactive and recoverable.

6. Cancel Invoices

   Cancel Invoices allows you to completely undo any number of invoices created and posted with Invoice Entry (X12-5).


7. Print Payable Checks
   Print Payable Checks is selectable by: Due date, Including or Excluding (bypassing) vendors, G/L account, or Group code, or Vendor address number. Up to 3 lines of comments can be printed on each check. Comments can be the same for all vendors (global) or different for each vendor. Transactions can be displayed by due date or invoice number for any vendor who has been included. Discounts can be removed for all vendors or for an individual vendor, and they can be restored for individual vendors.

8. Enter Manual Checks
   Enter Manual Checks allows you to process checks that have not been generated with Print Payable Checks, including checks that have been written by hand. Checks can be written for invoices already in the system or for invoices created "on the fly."

9. Cancel Checks
   Cancel Checks allows you to delete a check and all the G/L transactions resulting from it.

10. List of Vendors (Summary)
    The List of Vendors produces a report that includes a summarized list of selected vendors, including each vendor's G/L account, terms, home number, work phone number, fax number, and work group.


11. List of Vendors (Detail)
The List of Vendors (Detail) produces a customized report that lists information about each vendor, including: home, work and fax numbers and address, G/L and tax accounts, including G/L distribution, phone and fax numbers for salespeople and A/R clerks.

12. List of Purchases Subj to Tax1
List of Purchases Subj to Tax1 lists and totals invoices that were entered with non-zero amounts in the Tax1 field. The Tax1 and Tax2 fields are ideal for Canadian dealers who wish to record GST and PST (this menu option is for Canadian dealers).

13. List of Purchases Subj to Tax2
List of Purchases Subj to Tax2 lists and totals invoices that were entered with non-zero amounts in the Tax2 field. The Tax1 and Tax2 fields are ideal for Canadian dealers who wish to record GST and PST (this menu option is for Canadian dealers).

14. Aged Payables Summary Rpt
The Aged Payables Summary Report contains two sections. The first projects amounts due, by vendor, over user-specified intervals of days. The second projects amounts due, by G/L account, over user-specified intervals of days.


**15. Aged Payables Detail Report**

The Aged Payables Detail Report contains two sections. The first projects the amounts due, by vendor, over user-specified intervals of days and a listing of all unpaid invoices. The second projects the amount due, by G/L account, over user-specified intervals of days and a listing of all unpaid invoices.

**16. Payables Due Today**

The Payables Due Today report lists all invoices that are due on or before a specified date. Invoices included in the report can be selected by general ledger account, group code, or vendor address. Within each vendor, invoices can be sorted by invoice number or due date. A total of all payables due by the specified date concludes the report.

**17. Vendor totals**

For American dealers, this job will appear on the payables menu as "Vendor Totals for 1099 Preparation." Vendor Totals lists selected vendor's tax numbers and year to date sales. Vendors can be selected by G/L account, group code, or address.

## CHAPTER X1-4

## GENERAL LEDGER MENU

### INTRODUCTION

The general ledger is the key to the DIS accounting system. This section will explain the way to set up the general ledger. The instructions provided will help you to create a chart of accounts that will be easy to use.

The General Ledger Menu contains the following options:

- **X14-1 Account Inquiry**
    Allows you to view a general ledger account. You can check the balance in the account and the way various general ledger accounts are set up. Printouts are available.

- **X14-2 Account Maintenance**
    Use this job to set up your chart of accounts. You can add new general ledger accounts or make changes to existing accounts.

- **X14-3 Chart of Accounts**
    This job prints a list of your general ledger account numbers. The list prints in general ledger account number order. The report can be run for one division or all divisions.

- **X14-4 Monthly General Ledger Report**
    Listed on this report is all activity for all open months. Also, the balances of closed months will be on the report. This report lists all general ledger accounts and could be very long. The report runs automatically when the month is closed.

- **X14-5 Subledger Balance Report**
    The Subledger Balance Report prints a list of General Ledger accounts that have edit codes of A (Receivables), F (Flooring), P (Payables), and W (Units). It shows the balance in the General Ledger account and compares it with the sum of the subledger balances.

## X1-4 GENERAL LEDGER MENU

X14-6 Check Reconciliation

Check Reconciliation summarizes transactions for sold units from General Ledger accounts related specifically to units: Units Inventory, Units Cost of Sale, and Flooring accounts ("W" and "F" edit codes). The reconciliation may include up to 7 different accounts for a particular month/year.

X14-7 General Schedule

A General Schedule can be printed for up to 7 General Ledger accounts. You can specify the sort order you prefer, and a date range for the report. Only transactions for open months are available; however, General Ledger Maintenance (X14-2) allows you to specify a number of "Months to Keep" if you need to print general schedules pertaining to closed G/L months.

If you have any questions regarding the general ledger set up or concepts of the system, read the following section carefully.

## WHAT MAKES UP A CHART OF ACCOUNTS?

There are many versions of charts of accounts; however, 6 types of accounts appear on all charts of accounts. They are: 1) assets, 2) liabilities (which include your owners equity), 3) sales, 4) cost of sales, 5) income, and 6) expense.

Assets are accounts that are controlled by specific business transactions and are expected to have future value to the business. Examples of asset accounts are cash, inventory, receivables, fixed assets and prepaids such as insurance.

Liabilities are debts or legal obligations of a company which are the result of acquiring assets from an organization or person other than those who share ownership of the business. Examples of liabilities are accounts payable, flooring, long term debt, and accruals.

The owners claim against the business is called owners equity. It is the difference between what is owned by the business (assets) and what is owed by the business to outside sources (liabilities). Owners equity is listed under liabilities.

The basic accounting equation is:

Assets = Liabilities + Owners Equity

Sales accounts are records of sales. Examples of sale accounts are parts sales, unit sales, labor sales, and miscellaneous sales.

Cost of sales are accounts that record how much a particular sale cost the business. In the DIS system, you cannot cost what is not sold. A cost of sale account must have a corresponding sale account. If there is a cost of


sale account associated with a sale account it must be unique to that sale account. The cost of sale account number can only be used once.

Income accounts record other incidental bits of income such as interest or rent taken from rentals of other fixed assets.

Expense accounts are used to track what is spent on items such as rent, utilities, dues, travel and entertainment.

The system uses a code to define the types of general ledger accounts. These are called Type Codes and are defined as follows:

 :--- | :--- | :--- |
| Assets | = | A |
| Liability | = | L |
| Sales | = | S |
| Cost of Sale | = | C |
| Income | = | I |
| Expense | = | E |

Type code will determine where the account will appear on the financial statement. The accounts will sort as listed above in numeric order.

## DEPARTMENTALIZING

Departmentalization is a way of keeping close track of all expenses, income, sales and cost of sales of a department of your company.

The department code is placed at the end of the account number. You can define your departments any way you choose. For example, the company has four departments and the codes are defined as in the example below:

| Department | Code |
| --- | --- |
| Administrative | 1 |
| Parts | 2 |
| Sales | 3 |
| Service | 4 |

If we have an expense account called rent, we could assign each of these departments a percentage of the rent expense based on the amount of space in the department. For purposes of illustration, we will divide the expense as follows:

| Department | Code | Percentage |
| --- | --- | --- |
| Parts | 1 | 30% |
| Service | 2 | 20% |
| Sales | 3 | 10% |
| Administrative | 4 | 40% |

If we posted all expenses, sales, cost of sales, and income as illustrated above, this would give us an idea of how much the department was making and the cost of running each department.

Also a financial statement can be requested for each department. This will give you an exact picture of what each department earned and the cost for maintaining each department.

Different companies departmentalize for different reasons. It would not be

## 6	X1-4 GENERAL LEDGER MENU

possible to cover every example. Examples of how and why to departmentalize follow.

- Here the parts department will be given credit for all parts sales regardless of which department actually sold them. This information can be used to pay commission on total parts sold.

| BEFORE | | AFTER  :--- | :--- | :--- | :--- |
| PARTS-WHOLESALE | D3300 | PARTS-WHOLESALE | D33001 |
| PARTS-INTERNAL | D3310 | PARTS-INTERNAL | D33101 |
| PARTS-COUNTER | D3320 | PARTS-COUNTER | D33201 |
| PARTS-SHOP | D3330 | PARTS-SHOP | D33301 |
| OTHER INCOME | D5050 | OTHER INCOME-PARTS | D50501  | OTHER INCOME-SERVICE | D50502  | OTHER INCOME-SALES | D50503  | OTHER INCOME-ADMIN. | D50504 |
| TELEPHONE EXPENSE | D6710 | TELEPHONE EXP.-PARTS | D67101  | TELEPHONE EXP.-SERV. | D67102  | TELEPHONE EXP.-SALES | D67103  | TELEPHONE EXP.-ADMIN. | D67104 |

- Here the goal is to offset excessive expenses incurred by the shop by crediting each department for parts sales.

| BEFORE | | AFTER  :--- | :--- | :--- | :--- |
| PARTS-WHOLESALE | D3300 | PARTS-WHOLESALE | D33001 |
| PARTS-INTERNAL | D3310 | PARTS-INTERNAL | D33103 |
| PARTS-COUNTER | D3320 | PARTS-COUNTER | D33201 |
| PARTS-SHOP | D3330 | PARTS-SHOP | D33302 |


| BEFORE | | AFTER  :--- | :--- | :--- | :--- |
| OTHER INCOME | D5050 | OTHER INCOME-PARTS | D50501  | OTHER INCOME-SERVICE | D50502  | OTHER INCOME-SALES | D50503  | OTHER INCOME-ADMIN. | D50504 |
| TELEPHONE EXPENSE | D6710 | TELEPHONE EXP.-PARTS | D67101  | TELEPHONE EXP.-SERV. | D67102  | TELEPHONE EXP.-SALES | D67103  | TELEPHONE EXP.-ADMIN. | D67104 |

If there is more than one division and the accounting is centralized, you may choose to departmentalize the two divisions. See the example below:

## BEFORE

| :--- | :--- |
| PARTS-SALES | D3300 |
| NEW EQUIPMENT SALES | D4300 |
| USED EQUIPMENT SALES | D4500 |
| OTHER INCOME | D5050 |
| TELEPHONE EXPENSE | D6710 |

## AFTER

| :--- | :--- |
| PARTS-SALES Dallas | D3300D |
| PARTS-SALES Austin | D3300A |
| NEW EQUIPMENT SALES Dallas | D4300D |
| NEW EQUIPMENT SALES Austin | D4300A |
| USED EQUIPMENT SALES Dallas | D4500D |
| USED EQUIPMENT SALES Austin | D4500A |
| OTHER INCOME Dallas | D5050D |
| OTHER INCOME Austin | D5050A |
| TELEPHONE EXPENSE Dallas | D6710D |
| TELEPHONE EXPENSE Austin | D6710A |


You can go even further and departmentalize accounts for these divisions:

| Description | Code |
| :--- | :--- |
| TELEPHONE EXPENSE Dallas-Parts | D6710D1 |
| TELEPHONE EXPENSE Dallas-Service | D6710D2 |
| TELEPHONE EXPENSE Dallas-Sales | D6710D3 |
| TELEPHONE EXPENSE Dallas-Admin. | D6710D4 |
| TELEPHONE EXPENSE Austin-Parts | D6710A1 |
| TELEPHONE EXPENSE Austin-Service | D6710A2 |
| TELEPHONE EXPENSE Austin-Sales | D6710A3 |
| TELEPHONE EXPENSE Austin-Admin. | D6710A4 |

## CHOOSING A NUMBERING SYSTEM

The general ledger account number accommodates 8 characters. The important thing to remember is that all "types" of accounts will appear together on a financial statement. The selection of an orderly numbering system produces a chart of accounts that is easy to use.

The first character of the general ledger number is reserved for the division information. It must be a letter. Use something that will make sense to you, something easy to remember. For example, if you have two stores, one in Dallas and one in Houston, you may want to use D for Dallas and H for Houston.

The first letter of the general ledger account number must match the first letter of the division code set up in Security Maintenance (X6-6). The division code will need to be set up before you can set up the General Ledger.

We recommend that the numbering for the second character be as follows:

 :--- | :--- | :--- |
| Asset | = | 1 |
| Liability | = | 2 |
| Sale | = | 3 |
| Cost of Sale | = | 4 |
| Income | = | 5 |
| Expense | = | 6 |

If you are pleased with your present chart of accounts in which all of the assets accounts begin with 6 and all expense accounts begin with 1, this is not a problem. The chart can be used. The main consideration is that all assets sort together, all expenses sort together, etc.

Make a reasonable compromise. After the division code, in the second


position, insert a 1 before every asset account, a 2 before each liability account, a 3 before sales, 4 before costs, 5 before income, 6 before expenses. Then beginning in the third position, use the account number you have now. Add zeros at the end for flexibility. Now your chart will be in conformance with the system and the integrity is maintained:

| Before  After ---|---|---|---|---|
| 101 | Advertising | E | D16120 Accounts Receivable | A |
| 205 | Other Income | I | D26400 Notes Payable | L |
| 612 | Accounts Receivable | A | D32540 Parts Sales | S |
| 640 | Notes Payable | L | D52050 Other Income | I |
| 254 | Parts Sales | S | D61010 Advertising | E |


Fill in the rest of the general ledger number as desired. To add flexibility to the numbering system, add an extra zero to the end of the general ledger number. This allows for growth. Try and make all general ledger numbers the same length. Posting errors will be easier to spot and the chart of accounts will be easy to read.


**COMPONENTS OF GENERAL LEDGER NUMBERS**

**Edit Code**

This is the code that is used to tie the subsidiary ledger to the particular general ledger. When a line is posted, an edit code makes sure that all the necessary information is present for both the general ledger and the subsidiary ledger. The line is edited for errors.

Some general ledger accounts have edit codes and some do not. If there is a subsidiary ledger for a general ledger balance, there will be an edit code. The edit code is the bridge from the general ledger to the subsidiary. The subsidiary is a breakdown of information such as:

| Account | Edit Code | Information Required |
| :--- | :--- | :--- |
| Receivables | A | Who owes how much |
| Units inventory | W | How much was paid for what |
| Trade Payables | P | How much you owe to whom |
| Notes Payable (flooring) | F | How much you owe whom on what |
| Accumulated Depreciation | X | How much on what |

The above are examples of accounts that may need edit codes. You do not need an edit if there is no subsidiary ledger. For example, if you have a payable account with a lump sum and want no detail, do not use an edit code.

### Account 1 & 2:

These fields are filled in with general ledger numbers that instruct the computer to debit or credit the account depending on what type of account it is and the edit code used.

Look at receivables for example. A receivables account has an "A" edit code. When the "A" edit code is present, who owes the money will need to be provided in order to post to the general ledger. The general ledger and subsidiary (who) are posted at the same time. This keeps them in balance.

Also, the "A" edit code triggers monthly billing to produce statements. If interest is to be charged, account 1 will hold the account number of the income account to be credited with the interest.

### Factor:

When a part is sold at Point of Sale, inventory is automatically credited and cost of sale is automatically debited for the cost of the part. This assumes that the parts inventory account is in the account 1 field and the parts cost of sales account is in the account 2 field.

If a part is not in inventory, there is no way for the computer to "know" what the cost of the part was. A factor is the percentage of the sale that should be cost of sales. The factor is only used if the part is not in inventory.


You can also use a factor for rentals. When a factor of 70 is used on a rental sales account, the account currently associated with the unit (inventory, or COS if the unit has been sold) will be credited for 70 percent of the sale and cost of sales will be debited for 70 percent of the sale. This assumes the rental revenue cost of sale account is in the account 2 field.


Here are some examples of automatic costing. The first is an example of automatic costing when a part is not in inventory. Non- inventoried parts are sold with a D or M format at Point of Sale.

| Cash or A/R | | Sales (Factor = 70) ---|---|---|---|
| Dr | Cr | Dr | Cr |
| 100.00  100.00 |

- Automatic Transactions

| Account 1 * Parts Inventory | | Account 2 * Parts Cost of Sale ---|---|---|---|
| Dr | Cr | Dr | Cr  70.00 | 70.00 | |


Next is an example of automatic transactions for rentals. The cost of the unit will be reduced by the dollar figure equal to the percentage of the sale that is cost. If the factor is 90% and the unit is rented for $100.00, the cost of the unit in inventory will be reduced by $90.00. If cost is recorded in inventory as $500.00, posting of the sale will make the cost of unit $410.00. The system credits the G/L account that is currently associated with the unit: inventory or COS (if the unit has been sold in the meantime).

| Cash or A/R | | Rental Revenue (Factor = 90%) ---|---|---|---|
| **Dr** | **Cr** | **Dr** | **Cr** |
| 100.00  100.00 |

- Automatic Transactions

| Account 1<br>* Units Inventory or COS | | Account 2<br>* Rental Revenue Cost of Sale ---|---|---|---|
| **Dr** | **Cr** | **Dr** | **Cr**  90.00 | 90.00 | |


Cost is automatic for parts that are in inventory. The factor is ignored and the cost is moved from inventory to cost of sales. If there is not cost posted in inventory for rentals or parts, no cost will be transferred.

**Type:**

This is a code to identify the type of account the general ledger will be. The types are defined below:

 :--- | :-: | :--- |
| Asset | = | A |
| Liability | = | L |
| Sale | = | S |
| Cost of Sale | = | C |
| Income | = | I |
| Expense | = | E |

Every general ledger account with the same type will sort together in numeric order on the financial statement.


**Cash acct?(Y):**

If the general ledger account being added is a cash account enter Y. If the account is designated as a cash account, debits and credits are kept track of on a Daily Operating Control report for review.

**General Schedule**

**Months to Keep:**

2 digits. Saves transaction detail for the specified number of months. Normally, transaction detail is removed from the DIS Business System when a general ledger month is closed; otherwise, disk space would be a real problem. If you use General Schedule (X14-7), you may want to keep transaction detail on selected accounts for several months.

### **Examples Of General Ledger Accounts**

Below are examples of how to open various types of general ledger accounts:

**Accounts Receivable**


|---|---|
| **ACCOUNT#** | D1110 |
| **TITLE** | ACCOUNTS RECEIVABLE |
| **EDIT CODE A** | requires at posting<br>1 receivable address |
| **does this work** | 1 monthly billing<br>2 receivables records for reports<br>3 transactions for 12 months |
| **ACCOUNT 1** | D5210 |
| **ACCOUNT 2** | Interest Income is credited |
| **FACTOR** | leave blank (the off-setting entry is a debit to the receivable for the interest) |
| **TYPE A** | leave blank (parts & rental only) |
| **CASH ACCOUNT?** | Asset |
| **GENERAL SCHEDULE** | N |
| **MONTHS TO KEEP** | Optional |


**Units inventory accounts...**


| :--- | :--- |
| **ACCOUNT#** | D1250 |
| **TITLE** | USED EQUIPMENT |
| **EDIT CODE** | W requires at posting 1 stock number |

_does this work_
_1 units records for reports_


| :--- | :--- |
| **ACCOUNT 1** | D3250 Corresponding sales account |
| **ACCOUNT 2** | D4250 Corresponding cost account |
| **FACTOR** | leave blank (parts & rental only) |
| **TYPE** | A Asset |
| **CASH ACCOUNT?** | N |
| **GENERAL SCHEDULE**  **MONTHS TO KEEP** | Optional |

Please take note of the correspondence in the inventory, sales, and cost of sales account numbers. This makes an orderly chart of accounts and is easy to remember.


Units - Accumulated depreciation accounts


| :--- | :--- |
| **ACCOUNT#** | D1251 |
| **TITLE** | ACCUMULATED DEPRECIATION |
| **EDIT CODE X** | requires at posting<br>1 stock number  does this work<br>1 depreciation records for reports |
| **ACCOUNT 1** | leave blank |
| **ACCOUNT 2** | leave blank |
| **FACTOR** | leave blank (parts & rental only) |
| **TYPE A** | Asset |
| **CASH ACCOUNT ?** | N |
| **GENERAL SCHEDULE**  **MONTHS TO KEEP** | Optional |


**Trade payables**


| :--- | :--- |
| **ACCOUNT#** | D2400 |
| **TITLE** | ACCOUNTS PAYABLE (things like parts, rent, supplies) |
| **EDIT CODE** | P  requires at posting<br>1 vendor address<br>2 due date<br>3 accepts discount, if any  does this work<br>1 writes checks<br>2 vendor records for reports<br>3 transactions for 3-12 months |
| **ACCOUNT 1** | D1020 |
| **ACCOUNT 2** | D5000 |
| **FACTOR** | Cash in bank is credited<br>Discounts earned |
| **TYPE** | L  leave blank (parts & rental only)<br>Liability |
| **CASH ACCOUNT ?** | N |
| **GENERAL SCHEDULE**  **MONTHS TO KEEP** | Optional |


|---|---|
| **ACCOUNT#** | D2250 |
| **TITLE** | NOTES PAYABLE USED EQUIPMENT (Flooring = Financing) |
| **EDIT CODE** | F | 

requires at posting
1. vendor address
2. due date
3. accepts discount, if any
4. stock number

does this work
1. writes checks
2. vendor records for reports
3. keeps records for current inventory and floored units reports
4. transactions for 3-12 months.

---|---|---|
| **ACCOUNT 1** | D1020 | Cash in bank credited |
| **ACCOUNT 2** | D5000 | Discounts earned |
| **FACTOR** | | leave blank (parts and rental only) |
| **TYPE** | L | Liability |
| **CASH ACCOUNT?** | N  **GENERAL SCHEDULE** 
| **MONTHS TO KEEP** | Optional | |

Flooring accounts are where you keep notes payable on equipment in inventory. You may choose to have one flooring account with several vendors, or you may prefer to have a separate account for each manufacturer.


23

**Note:** Prior to the release of DIS software, "999999" was used to indicate that a payables transaction had an "undefined" due date. Most often, this was used with an invoice associated with a floored unit. Once the unit was sold, the system automatically changed the due date field from "999999" to the current system date.

In V8L5A, all information in the date field must be in the form of a valid date, not "999999." To project a transaction as far in the future as possible, enter "123150" or December 31, 2050. This is the most distant date possible in the DIS system. Dates *after* December 31, 2050 will be interpreted by the computer as taking place in the 1900's. Thus, "010151" would be treated by the computer as January 1, 1951.

A more convenient solution to manually typing in "123150" every time your purchase a floored unit can be found in entering "999" (the largest number possible) in the "Number of Days/Due" field for the floored vendor in Vendor Maintenance (X12-2). When the due date field is left blank, this field will automatically be filled in with a date 999 days in the future, probably enough time for the unit to be sold. When the unit is sold, the due date field, regardless of what it is, will be filled in with the current system date. At this point, it will be treated by the system as a normal payables invoice.




| :--- | :--- |
| **ACCOUNT#** | D2600 |



| :--- | :--- |
| **EDIT CODE** | E | 

requires at posting
1. employee address
2. salary or hours
4. type of hours

does this work
2. employee records for reports


| :--- | :--- |
| **ACCOUNT 1** | D1020 | 
| **ACCOUNT 2** | D2590 |
| **FACTOR**  **TYPE** | L |
| **CASH ACCOUNT?** | N |
| **GENERAL SCHEDULE**  **MONTHS TO KEEP** | Optional |

Cash in bank is credited
leave blank (parts & rental only)
Liability


---


|---|---|
| **ACCOUNT** | D2590 |


**EDIT CODE G**

requires at posting
1. employee address

does this work
1. puts federal withholding, FICA, state tax, etc. where they belong
2. keeps year-to-date records


|---|---|
| **ACCOUNT 1** | leave blank |
| **ACCOUNT 2** | leave blank |
| **FACTOR** | leave blank (parts and rental only) |
| **TYPE L** | Liability |
| **CASH ACCOUNT ?** | N |
| **GENERAL SCHEDULE**  **MONTHS TO KEEP** | Optional |


| :--- | :--- |
| **ACCOUNT#** | D3250 |
| **TITLE** | USED EQUIPMENT SALES |
| **EDIT CODE** | S |

requires at posting
1. customer address
2. date warranty expires
3. type of warranty
4. stock number

does this work
1. remembers who bought what
2. remembers units on warranty
3. flags unit as sold
4. sets off automatic transaction to move unit from inventory to cost of sale account
5. sets flooring due date to date of sale


| :--- | :--- |
| **ACCOUNT 1** | D1250 |
| **ACCOUNT 2** | D4250 |
| **FACTOR**  **TYPE** | S |
| **CASH ACCOUNT ?** | N |
| **GENERAL SCHEDULE**  **MONTHS TO KEEP** | Optional |

Inventory is credited
Cost of sale is debited
leave blank (parts & rental only)
Sales


|---|---|
| **ACCOUNT#** | D4250 |
| **TITLE** | COST USED EQUIPMENT |
| **EDIT CODE W** | requires at posting<br>1 stock number<br><br>does this work<br>1 remembers how much units cost | 
| **ACCOUNT 1 D1250** | Inventory account from which unit was sold. |
| **ACCOUNT 2** | leave blank |
| **FACTOR** | leave blank (parts & rental only) |
| **TYPE C** | Cost |
| **CASH ACCOUNT?** | N |
| **GENERAL SCHEDULE**  **MONTHS TO KEEP** | Optional |


| :--- | :--- |
| **ACCOUNT#** | D3320 |
| **TITLE** | SALES - PARTS & ACCESSORIES |
| **EDIT CODE** | D  requires at posting  nothing  does this work  1 sets off automatic transaction to move cost<br>of a part from inventory to a cost of sale<br>account  2 records of part sales |
| **ACCOUNT 1** | D1320  Parts inventory is credited |
| **ACCOUNT 2** | D4320  Cost of sale is debited |
| **FACTOR** | 070 (example)  If part is not inventoried, system will credit<br>inventory & debit cost of sale for this<br>percentage (0-100%) of sales price. No<br>fractions, please. |
| **TYPE** | S  Sales |
| **CASH ACCOUNT ?** | N |
| **GENERAL SCHEDULE**  **MONTHS TO KEEP** | Optional |


| :--- | :--- |
| **ACCOUNT#** | D3280 |
| **TITLE** | RENTAL REVENUE |
| **EDIT CODE** | R  requires at posting<br>1 stock number  does this work<br>1 rental information<br>2 reduces cost of unit by a percentage of sales revenue IF factor is set |
| **ACCOUNT 1** | Leave blank. The system credits the account currently associated with the unit: inventory or cost of sale (if the unit has been sold). |
| **ACCOUNT 2** | D4280  Cost account is debited IF factor is set (cost account must be tied to sales account here even if there is no factor) |
| **FACTOR** | 090  System will credit the account currently associated with the unit and debit cost of rental revenue for this percentage (0-100%) of the revenue. No fractions, please.<br>Reduces cost of unit. A non-zero factor is required for costing to occur. |
| **TYPE** | S  Sales |
| **CASH ACCOUNT?** | N |
| **GENERAL SCHEDULE**  **MONTHS TO KEEP** | Optional |


| :--- | :--- |
| **ACCOUNT#** | D4280 |
| **TITLE** | COST - RENTAL REVENUE |
| **EDIT CODE C** | requires at posting<br>1 stock number<br><br>does this work<br>1 rental cost information |
| **ACCOUNT 1** | leave blank |
| **ACCOUNT 2** | leave blank |
| **FACTOR** | leave blank |
| **TYPE C** | Cost |
| **CASH ACCOUNT ?** | N |
| **GENERAL SCHEDULE**  **MONTHS TO KEEP** | Optional |


**Other sales accounts**


|---|---|
| ACCOUNT# | D3400 |
| TITLE | MACHINE CHARGES |
| EDIT CODE | Leave blank--this is a sale of something not represented in inventory |
| ACCOUNT 1 | Leave blank |
| ACCOUNT 2 | Corresponding cost of sale account. |
| FACTOR | leave blank (parts and rental only) |
| TYPE | S |
| CASH ACCOUNT ? | N |
| GENERAL SCHEDULE  MONTHS TO KEEP | Optional |


**COST ACCOUNTS MISSING FROM FINANCIAL STATEMENT**

Please take careful note of the following:

If you are going to have a cost of sale account, it must be unique to the sale account. You can not use the same cost of sale account for more than one sale account. Place the cost of sale account number in the Account 2 field of the sale account.

All cost of sale accounts must be tied to a sale account even if the sale account is not used. If the cost of sale is not tied as an Account 2 of a sale account, the cost of sale account will not appear on the financial statement.

### **Charts For Other Divisions**

If you are interested in obtaining a composite financial statement, each division must have the same chart of accounts. Only the division code (position 1 of the account number) changes.

THEN if customers and vendors are shared...

*Add Transfer Accounts!*

**Transfer Accounts**


| :--- | :--- |
| **Account#** | D1800 and H1800 |
| **Title** | INTERDIVISIONAL TRANSFER ACCOUNT |
| **Edit code** | none |
| **Acct 1** | none |
| **Acct 2** | none |
| **Factor** | none |
| **Type** | A |

The transfer account must be recorded in Security Maintenance (X6-6). Referring to the example above, the transfer account for Division D would be D1800; for Division H, H1800.


What happens when a customer from division D buys a tractor from division H?

| DIVISION D | | DIVISION H ---|---|---|---|
| Cash or A/R | | Sales H3200  **Dr** | **Cr** | **Dr** | **Cr** |
| 21000  21000 |

- Automatic Transactions

| Account 1 | | Account 2 ---|---|---|---|
| * Inventory H1200 | | * Cost of Sale H4200  **Dr** | **Cr** | **Dr** | **Cr**  16750 | 16750  * Transfer D1800 | | * Transfer H1800 ---|---|---|---|
| **Dr** | **Cr** | **Dr** | **Cr**  21000 | 21000 | |


Below are the results of division D selling one of their customers a tractor out of division H.

| DIVISION D | | DIVISION H |
| :--- | :--- | :--- |
| Cash or A/R 
| **Dr** | **Cr**  21000 
| W/G Sales D3200 
| **Dr** | **Cr**  | 21000 | |

*Automatic Transactions*

| Account 2 | | Account 1 |
| :--- | :--- | :--- |
| *Cost of Sale D4200I | | *Inventory H1200 |
| **Dr** | **Cr** | **Dr** | **Cr** |
| 16750  16750 |
| *Transfer D1800 | | *Transfer H1800 |
| **Dr** | **Cr** | **Dr** | **Cr**  16750 | 16750 | |

When all the decisions regarding your general ledger are made, the chart of accounts can be set up in General Ledger Maintenance (X14-2).

## GENERAL LEDGER SUMMARY SHEET

| GENERAL LEDGER ACCOUNT | EDIT CODE | ACCOUNT 1 | ACCOUNT 2 | FACTOR | TYPE CODE |
| --- | --- | --- | --- | --- | --- |
| D1020 CASH IN BANK | B  | A |
| D1110 ACCOUNTS RECEIVABLE | A | D5210 INTEREST INCOME  L |
| D2200 FLOORED PAYABLES | F | D1020 CASH IN BANK | D5000 CASH DISCOUNTS EARNED | | L |
| D2400 ACCOUNTS PAYABLE | P | D1020 CASH IN BANK | D5000 CASH DISCOUNTS EARNED | | L |
| D1200 NEW UNITS INVENTORY | W | D3200 SALES - NEW UNITS | D4200 COST OF SALES - NEW UNITS | | A |
| D3200 SALES - NEW UNITS | S | D1200 NEW UNITS INVENTORY | D4200 COST OF SALES - NEW UNITS | | S |
| D4200 COST OF SALES - NEW UNITS | W | D1200 NEW UNITS INVENTORY  C |
| D3280 RENTAL EQUIPMENT - REVENUE | R | See NOTE below | D4280 COST - RENTAL REVENUE | % cost | S |
| D4280 COST - RENTAL REVENUE | C  | C |
| D1590 ACCUMULATED DEPRECIATION | X  | A |
| D3320 SALES - PARTS SHOP | D | D1320 PARTS & ACCESSORIES | D4340 COST OF SALES - PARTS | % cost | S |
| D3340 SALES - LABOR | D | D6540 COMPENSATION-SERVICE | D4340 COST OF SALES - LABOR | % cost | S |
| D3* ALL OTHER SALES ACCOUNTS  D4* COST OF SALES | | S |
| **SCHEDULED ACCOUNTS**  By ADDRESS# | N 
| By DESCRIPTION | T 
| By DOCUMENT# | L 
| By UNIT# | U 
| By VIN | V 

**NOTE:** The recommended procedure is to leave Account 1 blank on the Rental Revenue account. The system credits the account currently associated with the unit (inventory or cost of sale). If, however, an Account 1 is entered, the system credits it in every case. If Account 1 is an inventory account and the unit has been sold when the transaction is posted, the G/L inventory account will be out-of-balance with its subledger. It is not a problem if Account 1 has no subledger, such as an expense account.

| ACCOUNT TYPES | | DEBIT |
| --- | --- | --- |
| G/L ACCOUNT | TYPE | EFFECT |
| ASSET | A | Up |
| LIABILITY | L | Down |
| SALES | S | Down |
| COST OF SALES | C | Up |
| INCOME | I | Down |
| EXPENSE | F | Up |

## CHAPTER X1-6

## TRANSACTION MENU

### INTRODUCTION

The Transaction Menu includes the following jobs:


|---|---|
| X16-1 | Source Document Inquiry, which allows you to:<br>- display all information included on any source document entered for any open General Ledger month. |
| X16-2 | Transaction Report Writer, which allows you to:<br>- request a report of different types of transactions for open months, and in some instances, closed General Ledger months.<br>- create and request a report according to your specifications. |
| X16-3 | Sales Tax Report<br>- The Sales Tax Report is based on general ledger transactions for open months. It is similar to transactions reports that can be printed using TRANSACTION REPORT WRITER (X16-2). It includes the detail and summary (or summary only) of all transactions that originated in Point of Sale or Create Source Documents and involve sales accounts. Selection is by general ledger month: you can specify one open month or a range of open months. |

## Transaction Report Writer


- Which file to access.

You may choose a file by entering a code. Look at the table below.

| CODE | FILE (file name) | AVAILABLE TRANSACTIONS |
| :--- | :--- | :--- |
| 01 | General Ledger (CUA) | All current transactions entered since the last accounting End of Month. |
| 02 | Payables (PAA) | All open payables invoices and credits. |
| 05 | Receivables (REA) | All current months receivables transactions for balance forward customers; all open item for open-item customers. |
| 06 | Receivables History (REH) | Closed receivables transactions for the past 11 months. |
| 07 | Wholegoods (WGA) | All units cost, rental revenue, and rental cost transactions. |
| 08 | Wholegoods (WGG) | Units sales transactions. |

## X1-6 TRANSACTION MENU

- How many subtotals you want to see.

For example, if you are creating a report sorted by posting date and by description, and you want a subtotal for both categories, enter 2 for SUBTOTALS.

- Which field(s) you want the computer to consider.

Each available field is given a number.

| NUMBER | NAME | LENGTH |
|---|---|---|
| 01 | ID or type | 1 |
| 02 | Post Date | 6 |
| 03 | Document # | 10 |
| 04 | D or C code | 1 |
| 05 | Account # | 8 |
| 06 | Amount | 9 |
| 07 | Description | 12 |
| 08 | Address # | 6 |
| 09 | Due Date | 6 |
| 10 | Discount | 9 |
| 11 | Stock # | 6 |
| 12 | Delete Code | 1 |
| 13 | G/L Month | 1 |


Which operator to use.

You may select an operator from the table below.

- EQ = Equal To
- NE = Not Equal To
- LT = Less Than
- GT = Greater Than
- LE = Less Than or Equal To
- GE = Greater Than or Equal To

The operator tells the computer how to look at the field and the constant. Example:

| FIELD NO | OPERATOR | CONSTANT |
| :--- | :--- | :--- |
| 02 | EQ | 061396 |

This means the posting dates (02) should be equal to June 13, 1996 (061396).

What constant should you use?

The field you select and the constant should have something in common.

For Example:

| In This Field: | You Would Need: |
| :--- | :--- |
| Post Date | a date |
| Document # | a document number (invoice number) |
| Description | the description found on the transactions you wanted listed |


Stock # valid stock number

If a blank is used in any position, only a blank in that position will be considered in the selection.

An exclamation point (!) may be used as a "wild card" constant. If an exclamation point is used in a position, any value in that position will be considered in the selection.

- How many lines of specifications to enter.

Up to 15 lines of specifications (field #, operator, constant) may be entered. There are two ways to enter specifications.

A. If more than one field selection is made on a screen the system interprets the selection as "field #, operator, constant AND field #, operator, constant". For example:

07 EQ T-PARTS AND 02 EQ 12 81
(description) (posting date)

This will result in only those transactions with "T-PARTS" in the description field and a posting date in December, 1981 being selected.

B. If more than one field selection screen is used, the system interprets the selection as "field selection screen one OR field selection screen two". For example:

07 EQ T-PARTS OR 07 EQ T-UNITS
(description) (description)


This will result in only those transactions with T-PARTS or T-UNITS in the description field being selected.

The information preceding is needed for making your field selections.

- How the computer should sort your report.

To arrange your report in a specific format you will need to make a few more decisions. This is done on the Sorting Order screen. If you don't enter anything on this screen, the report will automatically be sorted with deleted transaction records first and then the exact order that each transaction was recorded.

You may want to set up a sorting order. For each field that you have chosen, the computer needs to know the order in which you want the fields sorted. For example, date first, description second, type the same sort number for the entire field length.

EXAMPLE: You want Post Date (02) to be considered third. Post Date has a field length of six. (The field length is listed on the right side of the Field Table.) Under SORT ORDER you would type your threes (for third). It would look like:

| FIELD # | SORT ORDER |
|---|---|
| 02 | 123456789012345<br>333333 |

You can also sort parts of fields by placing your sort order in the correct position.

EXAMPLE: You still want to use Post Date (02) but you want your


report grouped by month. The days of the month would be in random order. The Sort Order would look like:

| FIELD # | SORT ORDER |
|---|---|
| 02 | 123456789012345<br>33 |

OR:

You want transactions grouped by the day of the month, i.e., all transactions for the 1st together, all for the 2nd together, etc., for all months sorted, but not grouped by month. The Sort Order would look like:

| FIELD # | SORT ORDER |
|---|---|
| 02 | 123456789012345<br>33 |

As you can see, the Transaction Report Writer relies on you to set up the guidelines. This means that with a little imagination, you can create almost any transaction report you need.

## Suggestions for Using the Transaction Report Writer

If you think this will be a useful tool, you should probably do some planning. A popular way to sort is by description. Here is an example of planning to use description for sorting.

Your business takes used equipment in as trade-ins on new unit sales. You post the sale transaction at full sales price - that is, you debit used equipment inventory at the full allowance value given to the customer and


you credit new equipment sales at the full purchase price. You have decided that you would like a report that would list, by month, all the over allowance transactions that were posted to used inventory and new unit cost of sales. This report would also list stock numbers.

From reading the previous section in this chapter, you realize that we need to identify these particular transactions by the fields used in Create Source Documents. The easiest way to extract the information you need is by using the Description field. If you post all over-allowance transactions using the characters OA in the beginning of the description field, we can create a report that will look specifically for these transactions.

### **Example**

This is an example of how to create a sample report.

**Step 1:**

The 'Generate Report From A Transaction File' screen appears. Since you are creating a new report (new specifications), press Enter to go to the next screen.

```
GENERATE REPORT FROM A TRANSACTION FILE

To produce an existing report, enter the report name

To create a new set of report specifications, press enter/rec adv

CMD 1 to end job
```

## Step 2:

The report name is UNIT, and the title is Unit Over-allowance Report. The general ledger was specified as the file you want to access with 1 subtotal. 1 subtotal will give you a subtotal by month. If you wanted a subtotal by G/L account within each month, you would specify 2 subtotals. Leaving subtotals blank or 0 will only give you a total for the entire report. Press Enter.

```
ABC COMPANY                                 GENERATE REPORT FROM TRANSACTION FILE
BELLINGHAM, WA                           E   *Specify Parameters*

Report name UNIT
Enter report title UNIT OVERALLOWANCE REPORT
Select the transaction file
To report:
     01 General ledger
Enter no. 01 02 Payables
     05 Receivables
     06 Receivable hist
     07 Whole goods
     08 Whole goods sld

Enter number of subtotals desired 01

Enter Y for a summary report (only subtotals and final totals)

Cmdl to end job
```

**ACCOUNTING**


**Step 3:**

You will be looking for transactions affecting the general ledger since the last Accounting End of Month with OA-in the beginning of the description field. The 9 exclamation marks which follow means to include any description following the OA-. If you left these exclamation marks off, the report would include transactions that only had OA- in the description field. Press Enter.

```
ABC COMPANY                               GENERATE REPORT FROM TRANSACTION FILE
BELLINGHAM, WA             E              *Field Selections*

Field No.  Operator  Constant----*      *----Field Table----*
                         123456789012345      Number Name           Length
07         EQ        OA-!!!!!!!!!         01     ID or type    1
           EQ                             02     Post date     6
           EQ                             03     Document #    10
           EQ                             04     D or C code   1
           EQ                             05     Account #     8
           EQ                             06     Amount        9
           EQ                             07     Description   12
           EQ                             08     Address #     6
           EQ                             09     Due date      6
           EQ                             10     Discount      9
           EQ                             11     Stock #       6
           EQ                             12     Delete code   1
           EQ                             13     G/L month     1
           EQ
           EQ
                         123456789012345      Cmd2 to continue to sort specification
Use ! as a 'wild card' character          Cmd1 to start report
Possible operators are EQ,NE,LT,GT,LE, and GE
```

**Step 4:**

Another Field Selection screen will appear. Since we have no other criteria to select, press Cmd2 to continue to sort specifications.


**Step 5:**
With this screen, specify the order in which you want your transactions sorted. In our example, we want to sort by G/L month. Let us also sort by Post Date within each month.

Field No. 7 has a 1 under the 1 in Sort Order. This is because we wish to sort first by G/L month and its field is 1 long. Field No. 2 has six 2's under Sort Order. This is because we wish to sort second by Post Date and its field is 6 long. Press Cmd1 to start the report.

```
ABC COMPANY                               GENERATE REPORT FROM TRANSACTION FILE
BELLINGHAM, WA              E             *Specify Sorting Order*

Field No.       Sort Order----*           *-------Field Table-------*
                123456789012345           Number Name           Length
13              1                         01     ID or type     1
02              222222                    02     Post date      6
                                          03     Document #     10
                                          04     D or C code    1
                                          05     Account #      8
                                          06     Amount         9
                                          07     Description    12
                                          08     Address #      6
                                          09     Due date       6
                                          10     Discount       9
                                          11     Stock #        6
                                          12     Delete code    1
                                          13     G/L month      1

                123456789012345
                                          Cmdl to start report
```


Step 6:
Below is the first page of the transaction report. Actually, it is a recap of what the user has requested. The title of the report is centered at the top. The file used and report name are listed along with the heading, levels, and summary options chosen. For selection requests it restates what you requested. In this example, it says it is looking for those transactions with Description EQUAL TO OA-.

```
ABC COMPANY                                            UNIT OVERALLOWANCE REPORT                      Date 9/25/86     Page      1
BELLINGHAM, WA                                                                                        Time 14.16.36    X1620-2A

**--REPORT PARAMETERS--**
File Used H.CUA          Report Name UNIT
****** HEADING          UNIT OVERALLOWANCE REPORT
****** LEVELS           01
****** SUMMARY          N
Selection Requests-----*
                         Connector Field Name      Operator      Constant-------*
                                                                 123456789012345
                    IF   Description               EQUAL TO      OA-
Sort Specifications----*
                         Field Name                Level
                         G/L month                 01
                         G/L month                 01
                         G/L month                 01
                         G/L month                 01
                         Post date                 02
                         Post date                 02
                         Post date                 02
                         Post date                 02
                         Post date                 02
                         Post date                 02
```


**Step 7:**

On the next screen is the report listing those transactions meeting the specifications requested. The report is formatted like the Post Source Documents screen.

**ABC COMPANY**
**BELLINGHAM, WA**

**UNIT OVERALLOWANCE REPORT**

Date: 9/25/86
Page: 1
Time: 14.16.36
X1620-2A

| I | GL | Posting | D | Mon | Date | Document | Account | Description | Number | Name | Amount | Discount | Due Date | Stock Number |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| E | B | | 8-15-86 | US45678 | D N400 | OA-UNIT SALE | 900.00  | 43808 |
| E | 6 | | 6-15-86 | US45678 | C N122 | OA-UNIT SALE | 900.00  | 00369 |
| E | 6 | | 6-15-86 | US45678 | D N400 | OA-UNIT SALE | 275.00  | 43812 |
| E | B | | 8-15-86 | US45678 | C N122 | OA-UNIT SALE | 275.00  | 43961 |
| E | 6 | | 8-15-86 | US45680 | D N400 | OA-UNIT SALE | 1100.00  | 43817 |
| E | B | | 8-15-86 | US45680 | C N122 | OA-UNIT SALE | 1100.00  | 43936 |
| E | 6 | | 8-15-86 | US45680 | D N400 | OA-UNIT SALE | 1900.00  | 43845 |
| E | B | | 8-15-86 | US45680 | C N122 | OA-UNIT SALE | 1900.00  | 43917  **... Level 1** | **4,175.00 D** | **4,175.00 C** 
| E | 9 | | 9-25-86 | US78945 | D N400 | OA-UNIT SALE | 7987.00  | 00336 |
| E | 9 | | 9-25-86 | US78945 | C N122 | OA-UNIT SALE | 7987.00  | 43984 |
| E | 9 | | 9-25-86 | US78945 | D N400 | OA-UNIT SALE | 2713.00  | 00339 |
| E | 9 | | 9-25-86 | US78945 | C N122 | OA-UNIT SALE | 2713.00  | 55321 |
| E | 9 | | 9-25-86 | US78952 | D N400 | OA-UNIT SALE | 3500.00  | 43887 |
| E | 9 | | 9-25-86 | US78952 | C N122 | OA-UNIT SALE | 3500.00  | 43953 |
| E | 9 | | 9-25-86 | US78952 | D N400 | OA-UNIT SALE | 8300.00  | 43909 |
| E | 9 | | 9-25-86 | US78952 | C N122 | OA-UNIT SALE | 8300.00  | 43953  **... Level 1** | **22,500.00 D** | **22,500.00 C**   | **... **Final** | **26,675.00 D** | **26,675.00 C** 


Notes:

## CHAPTER X1-7

## CREATE SOURCE DOCUMENTS

### INTRODUCTION

Create Source Documents is used to post to the general ledger. Although there are specialty jobs, such as RECEIVABLES PAYMENT ENTRY (X11-12) and PAYABLES ENTRY (X12-9), it is the only place in the DIS system where you can post all types of transactions to the general ledger. You can also enter Credit Card Sales manually through this option.

Create Source Documents eliminates many of the errors that took place on a manual system. There was the constant hassle of reconciling the general ledger to the sub ledgers. In Create Source Documents, all subledgers are posted at the same time the general ledger is posted. Consequently, the general ledgers should always balance to the subledgers.

The batches created will be edited for errors. If there are any errors in the batch, the batch can not be posted. Also, the debit and credit totals of the batch have to balance in order to post.

You can save a batch before posting for use at a future date. This will save you time. You will not have to type the whole batch again. A saved batch can be included with any other batches for posting. You can delete the batch or replace the batch with a new batch that is created.

### ENTERING THE TRANSACTIONS

After proceeding through the security gate, you will see a screen requesting the transaction date and the general ledger month for posting the batch. Today's date and the current month will be the defaults. You may change the date and month for posting. Press Enter.

Once a general ledger month is closed, you can not post to that closed month. If you enter a month that is closed, you will see on the verification screen that you are posting to a future month. You will be posting to that

## X1-7 CREATE SOURCE DOCUMENTS

month for the next year.

A screen displays requesting verification of the information just entered. If the posting date and month are correct, press Enter. If not, Cmd3 back a screen and make any changes you want. When the date and month are correct, press Enter. If you went back to change the date or month, press Enter twice.

If a batch was started and not posted for the workstation, the following screen will display:

```
CREATE SOURCE DOCUMENTS                                    X1700-001
A post source documents batch already exists for this workstation.

Enter one of the following options:
1. Return to the Accounting Menu.
2. Continue with the Check For Errors job for the existing job.
3. Delete the existing batch and begin creating a new batch.
```

Select the desired option. Press Enter.

If there is no previous batch, the Post Source Documents Document Entry screen will display.


**WEAVER'S EQUIPMENT**
**Division L**

**POST SOURCE DOCUMENTS**
**DOCUMENT ENTRY**

**7/16/97**
**X1700-101**
**July**

| ID Document# | Account# | Amount | Description | Addr# | Date | Discount | Stock# |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Current line 10  Next line 20 |

`Press Cmdl to end job; Cmd2 recurrent trans; Cmd3 show line#; Cmd4 show stock#`

The "Current line" will always be 10 when you are creating a new batch. The "Next line" will be 20. Each time a line is entered, the line count will go up by 10.

## Fields & Descriptions

The field limits are listed below. 5.2 digits means 5 digits including 2 decimal places, such as 123.45

**ID**
1 character
The cursor will be under the Document# field. Back space to the Id field. The ID is automatically duplicated on all lines unless it is changed. Some dealerships use the initial of the person creating the batch.

**ACCOUNTING**


Other dealerships will use the initial of the item being posted, P = Payables.

The important thing to remember is that the transactions sort by ID field on the End of Day report which is the accounting audit report. If you use an "R" on a debit to receivables, and an "s" on a credit to sales for the same transaction, this is how it will sort on the End of Day report. The debit will sort with all lines posted with an ID = "R" and the credit will sort with the lines containing an ID = "S". It may make it more difficult to locate each transaction if a question arises. If you use the initial of the person posting, all Mary's transactions will sort together, debits and credits.

### Document#

8 characters

Use anything that will mean something to you if you see it again. For example, use the number of the check if you are posting an expense.

The document number will display on the stub when payables checks are printed. You may want to use the vendors invoice number if you are posting payables.

### Debit or Credit

1 character

There is an invisible field between the Document# field and the Account# field. Type a C if you are crediting the account and a D if the account is to be debited.

| Account# | 8 characters. Type the general ledger account number for the line. |
| :--- | :--- |
| **Amount** | **9.2 digits**. Do not use decimals. Type $100.00 as 10000. |
| **Description** | **12 characters**. Optional. Type something you will recognize if you see it again. |

The fields mentioned so far should be filled in on all lines entered. They are to the left of the Description field. If you are posting to a general ledger account that has an edit code, one or more of the fields to the right of the Description field will need to be filled in. Depending on what edit code the general ledger account number has, fill in the following fields:

**Edit Code:**

A = Receivables

**Fields Required:**

Addr# 6 characters
Use the address number of the person who owes the money. You cannot post to a GL month that is more than one month less than or greater than the AR month in Security Maintenance. For example, if the AR month is 4, Accounts Receivable entries can be posted only to months 3 - 5.

P = Payables

Addr# 6 characters
The address number of the vendor you owe money to.


**F = Flooring**

**Date 6 digits**
The due date of the invoice. You will not be able to pay the invoice through the Payables Program until the due date you enter. Due Dates may be changed in Correct Due Dates and Discounts (X12-7).

**Discount 8.2 digits**
Amount of the discount from the vendor. If you do not get a discount, leave it blank. Discounts can be changed in Correct Due Dates and Discounts (X12-7).

**Addr# 6 characters**
The address number of the vendor flooring your units.

**Date 6 digits**
The due date of the invoice. When the unit is sold, due date becomes the date of the sale. Use 123150 if the due date is not known. Due Dates can be changed in Correct Due Dates and Discounts (X12-7). See note below.

**Discount 8.2 digits**
Amount of discount allowed by the vendor. If there is no discount, leave the field blank. Discounts can be changed in Correct Due Dates and Discounts (X12-7).

**Stock# 6 characters**
Unit number of the unit being floored.


> **Note:** Prior to the release of DIS software, "999999" was used to indicate that a payables transaction had an "undefined" due date. Most often, this was used with an invoice associated with a floored unit. Once the unit was sold, the system automatically changed the due date field from "999999" to the current system date.
> 
> In V8L5A, all information in the date field must be in the form of a valid date, not "999999." To project a transaction as far in the future as possible, enter "123150" or December 31, 2050. This is the most distant date possible in the DIS system. Dates after December 31, 2050 will be interpreted by the computer as taking place in the 1900's. Thus, "010151" would be treated by the computer as January 1, 1951.
> 
> A more convenient solution to manually typing in "123150" every time you purchase a floored unit can be found in entering "999" (the largest number possible) in the "Number of Days/Due" field for the floored vendor in Vendor Maintenance (X12-2). When the due date field is left blank, this field will automatically be filled in with a date 999 days in the future, probably enough time for the unit to be sold. When the unit is sold, the due date field, regardless of what it is, will be filled in with the current system date. At this point, it will be treated by the system as a normal payables invoice.

| Edit Code | Fields Required |
| :--- | :--- |
| W = Units | Addr# 6 characters |
| Inventory | Used to track washout. Use this field when posting a unit sale with a trade-in. On the debit to inventory for the trade-in, use the unit number of the unit being sold in the Addr# field. (If the unit number of the unit being sold has already been entered in the "Traded on Unit" field in Inquire/Update Units (X2-1), leave the Addr# field blank.) |

**ACCOUNTING**


S = Units Sales

Stock# 6 characters
Unit number of the unit being placed in inventory.

Addr# 6 characters
Address number of the person purchasing the unit.
Date 6 digits
Date the warranty on the unit expires.

Discount 8 digits
Warranty code. It is user defined and not recorded anywhere in the system. You make your warranty codes anything you choose. The warranty code is one digit, 1-9. You could use the following:

| Code | Warranty |
| :--- | :--- |
| 1 | 1 year |
| 2 | 2 year |
| 3 | 30 days |
| 4  5 | 50/50 used warranty |
| 6 | 60 days |
| 7 | No warranty |
| 8 | Special |
| 9 | 90 days |

Only you will know what the code means. Make a list of your warranty codes for reference.

R = Rental

Stock# 6 characters
Unit number of the unit being sold.

Stock# 6C.

Unit number of the unit being rented.

**C = Cost of Rental**
Unit number of the unit being rented.

**X = Units Depreciation**
Stock# 6 characters
Unit number of the unit being depreciated.

The following table summarizes the information required by the G/L for different kinds of transactions.

## Create Source Documents Posting Guide

| Account # | Description | Addr# | Date | Discount | Stock# |
| :--- | :--- | :--- | :--- | :--- | :--- |
| A/R | Open Item ROA=Doc# | Customer | No | No | No |
| A/P | Recommended | Vendor | Due Date | $ amount, if any | No |
| Flooring | Recommended | Vendor | Due Date | $ amount, if any | Required |
| Unit Sales | Recommended | Customer | Warr. Exp. | Warranty; 1-9 | Required |
| Units Inv/Cost | Recommended | No | No | No | Required |
| Units Inv. | Recommended | New Unit# | No | No | Trade-in# |

When the line is typed, press Enter. The next line comes up. You can


duplicate the information from the field above on the next line if the information being entered is exactly the same. For the S/36 and S/34, use the key labeled Dup. On the PC system, use the Shift and [Cmd6] keys.

The information will be duplicated exactly. If the field on the line above is blank, the field on the second line will be blank.

If a mistake is made on a line being entered, press Cmd3 to show the line numbers. The line number will show under the Stock# field. Move the cursor to the "Next line" field. Type the number of the line that needs correcting. Field Exit and press Enter. The cursor will be positioned on the line for correction. Change any field you wish. When the correction is made, press Enter. It may appear that the lines are out of order, but the machine "remembers" the numbering system. Press Cmd4 to view the Stock# field.

A batch contains various accounting transactions. Below are some examples of transactions and how they should be entered. The computer handles accounting transactions the same as you handled them on the manual system. It eliminates the need for journals and saves time by posting general ledger and subledgers at the same time.

## Units Transactions

## 1. Unit Acquisition:

| ID | DOC# | D/C | ACCT# | AMT | DESCRIPTION | ADDR# | DATE | DISC | STOCK# |
|---|---|---|---|---|---|---|---|---|---|
| Y | Y | D | INV | Y | (optional)  | Y |
| Y | Y | C | A/P or Cash | Y | (optional) | Vendor# | due | opt | Y |

## 2. Sale of a Unit without Trade-in:

| ID | DOC# | D/C | ACCT# | AMT | DESCRIPTION | ADDR# | DATE | DISC | STOCK# |
|---|---|---|---|---|---|---|---|---|---|
| Y | Y | D | A/R &/or Cash &/or Contracts in Transit &/or Program receivable | Y | Statement | Buyer#*  Y | Y | C | SALES | Y | (optional) | Buyer#* | War Expiration | War Code | Y |

- If not an established customer, set up an address number in Address Maintenance (X4-2) to track washout. Customer name will appear on the unit in the Sold to Information when inquiring on an unit (X2-1).

**War Expiration** = The date the warranty expires.

**War Code** = The warranty code, user defined.

### 3. Sale of a Unit with a Trade-in:

| ID | DOC# | D/C | ACCT | AMT | DESCRIPTION | ADDR# | DATE | DISC | STOCK# |
|---|---|---|---|---|---|---|---|---|---|
| Y | Y | D | INV | Y | Unit being traded in | Unit# being sold  Unit# being traded |
| Y | Y | D | A/R &/or Cash &/or Contracts in Transit &/or Program Receivable | Y | (statement) | *Buyer#  Y | Y | C | SALES | | (optional) | *Buyer# | War Expiration | War Code | Y |

*If not an established customer, set up an address number in Address Maintenance (X4-2) to track washout. Customer name will appear on the unit in the Sold to Information when inquiring on an unit (X2-1).*

`War Expiration = The date the warranty expires.`
`War Code = The warranty code, user defined.`

### 4. Return of a Unit:

| ID | DOC# | D/C | ACCT# | AMT | DESCRIPTION | ADDR# | DATE | DISC | STOCK# |
|---|---|---|---|---|---|---|---|---|---|
| Y | Y | C | A/R &/or Cash &/or Contracts in Transit & or Program Receivables | Y | (statement) | Buyer#*  Y | Y | D | SALES | Y | (optional) | Buyer#* | War Expiration | War Code | Y |

*If not an established customer, set up an address number in Address Maintenance (X4-2) to track washout. Customer name will appear on the unit in the Sold to Information when inquiring on an unit (X2-1).*

`War Expiration = The date the warranty expires.`


War Code = The warranty code, user defined.

**5. Overallowance:**

There are two methods commonly used for handling the overallowance on units that are traded in.

**FULL SALES PRICE** - Results in higher total sales.

Enter full sales price and the amount allowed on the trade-in as in transaction 4 above.

Then, in a separate batch, use the following entry to increase the cost of sale and decrease used inventory.

O/A = overallowance.

| ID | DOC# | D/C | ACCT# | AMT | DESCRIPTION | ADDR# | DATE | DISC | STOCK# |
|---|---|---|---|---|---|---|---|---|---|
| Y | Y | D | COST | O/A | (optional)  | # of Unit Sold |
| Y | Y | C | USED INV | O/A | (optional)  | # of Unit Traded-in |

**NET SALES PRICE** - Results in lower total sales.

The formula is Full Sales Price minus Overallowance equals Net Sales Price. Up front, lower the sale and do not give as much credit for the trade-in. Post as the example shows in step #3, but post the sales and inventory as they would be with the overallowance taken into consideration.


**6. Program Allowances from Flooring Vendors**

Dealers often receive rebates from manufacturers for selling certain units. The credit to the dealer will be posted on the flooring statement and often does not arrive until long after the sale.

Below are the steps:

Set up a general ledger account that is a Receivable Asset Account. Use an A edit code as with other receivable general ledger accounts. Set up a Receivable address number in Receivables Maintenance (X11-2). It will be easy to reference if you use the same address number assigned to your flooring vendor in Vendor Maintenance (X12-2). Tie the Receivable Address Number to the general ledger account set up for program receivables. Make sure the credit code field contains a N for no service charge.


**Post the program before the sale:**

| ID | DOC# | D/C | ACCT# | AMT | DESCRIPTION | ADDR# | DATE | DISC | STOCK# |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Y | Y | D | Program Rec G/L | Y | (statement) | Vendor# from Rec Maint (X12-2)  Y | Y | C | Inv | Y | (optional)  | Y |

**Or post the program after the sale:**

The transaction is the same as above except, credit cost of sale for the unit instead of the inventory.

**Post the rebate after receiving the flooring statement containing the credit:**

| ID | DOC# | D/C | ACCT# | AMT | DESCRIPTION | ADDR# | DATE | DISC | STOCK# |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Y | Y | D | Flooring | Y | (optional) | Vendor | Due | Opt | Y |
| Y | Y | C | Program Rec G/L | Y | (statement) | Vendor# from Receivables Maintenance  |

**7. After Sale Expense or Cost:**

| ID | DOC# | D/C | ACCT# | AMT | DESCRIPTION | ADDR# | DATE | DISC | STOCK# |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Y | Y | D | Cost of Unit sale | Y | (optional)  | Y |
| Y | Y | C | A/P or Expense | Y | (optional) | Vendor# | Due | Opt | Y (floored) |

### 8. Transferring a Unit to Another Dealer

The below example will demonstrate how to transfer a unit to another dealer. There are other methods, this is the one used most often.

| ID | DOC# | D/C | ACCT# | AMT | DESCRIPTION | ADDR# | DATE | DISC | STOCK# |
| :-- | :--- | :--- | :--- | :-: | :--- | :--- | :--- | :--- | :--- |
| Y | Y | D or C | SALES | 00 | Transfer | Dlr# being transferred to | War Exp | War Code | Y |

The transaction will not be out of balance because the dollar amount is zero. This generates an automatic transaction. The amount that was debited to inventory as cost will transfer to the cost of sales account. You can then make necessary adjustments to the cost of sales account in a different batch.

### 9. Transferring a Unit to a Different Inventory Account

| ID | DOC# | D/C | ACCT# | AMT | DESCRIPTION | ADDR# | DATE | DISC | STOCK# |
| :-- | :--- | :--- | :--- | :-: | :--- | :--- | :--- | :--- | :--- |
| Y | Y | D | Cash or Holding acct | Y | (optional) 
| Y | Y | C | Inv | Y | (optional)  | Y |

When the cost posted to a unit is zero, go to Inquire/Update Unit (X2-1) and change the inventory account number for the unit. Post the cost of the unit to the new inventory account.

| ID | DOC# | D/C | ACCT# | AMT | DESCRIPTION | ADDR# | DATE | DISC | STOCK# |
| :-- | :--- | :--- | :--- | :-: | :--- | :--- | :--- | :--- | :--- |
| Y | Y | D | New Inv | Y | (optional)  | Y |
| Y | Y | C | Cash or Holding acct | Y | (optional) 


**Rentals**

**1. Rental Revenue**

| ID | DOC# | D/C | ACCT# | AMT | DESCRIPTION | ADDR# | DATE | DISC | STOCK# |
| :-- | :--- | :-- | :--- | :- | :--- | :--- | :--- | :--- | :--- |
| Y | Y | D | A/R or Cash | Y | (optional) | Buyer#  Y | Y | C | Rental Revenue | Y | (optional)  | Y |

**2. Rental Cost of Sale**

| ID | DOC# | D/C | ACCT# | AMT | DESCRIPTION | ADDR# | DATE | DISC | STOCK# |
| :-- | :--- | :-- | :--- | :- | :--- | :--- | :--- | :--- | :--- |
| Y | Y | D | Rental Cost | Y | (optional)  | Y |
| Y | Y | C | Rental Inv or Expense | Y | (optional)  | N |

Please note that inventory will have to be credited and cost of sale debited for the cost of the rental unless the percentage has been set on the revenue account in General Ledger Maintenance (X14-2).

**Depreciation**

| ID | DOC# | D/C | ACCT# | AMT | DESCRIPTION | ADDR# | DATE | DISC | STOCK# |
| :-- | :--- | :-- | :--- | :- | :--- | :--- | :--- | :--- | :--- |
| Y | Y | D | Deprec Exp | Y | (optional)  | N |
| Y | Y | C | Accum Deprec | Y | (optional)  | Y |

## 18 X1-7 CREATE SOURCE DOCUMENTS

## Cash Sale

| ID | DOC# | D/C | ACCT# | AMT | DESCRIPTION | ADDR# | DATE | DISC | STOCK# |
|---|---|---|---|---|---|---|---|---|---|
| Y | Y | D | Cash | Y | (optional) 
| Y | Y | C | Sale | Y | (optional) 

(For unit sales, all the fields will have to be filled in. See how to post unit sales.)

## Charge Sale

| ID | DOC# | D/C | ACCT# | AMT | DESCRIPTION | ADDR# | DATE | DISC | STOCK# |
|---|---|---|---|---|---|---|---|---|---|
| Y | Y | D | A/R | Y | (statement) | Buyer#  Y | Y | C | Sales | Y | (optional) 

(For unit sales, all the fields will need to be filled in. See how to post the unit sale.)

## Sales Returns

To reverse a sale, reverse the entries illustrated in Cash Sales and Charge Sales.

## Received on Account

| ID | DOC | D/C | ACCT# | AMT | DESCRIPTION | ADDR# | DATE | DISC | STOCK# |
|---|---|---|---|---|---|---|---|---|---|
| Y | Y | D | Cash | Y  Y | Y | C | A/R | Y | (statement) | Cust#  |

**Payables or Flooring**

33ID DOC D/C ACCT# AMT DESCRIPTION ADDR# DATE DISC STOCK#

Y Y D Expense Y (optional)

or

Inv Y (optional) Y

Y Y C Payables Y (optional) Vendor Due Opt

or

Flooring Y (optional) Vendor Due Opt Y

### HOW THE TRANSACTIONS LOOK ON THE SCREEN

Below is an example of a Post Source Documents Document Entry screen with transactions entered.

```
WEAVER'S EQUIPMENT                                POST SOURCE DOCUMENTS          7/16/97  X1700-101
Division L                                        DOCUMENT ENTRY                 July ID Document#
Account#      Amount      Description      Addr#      Date      Discount      Stock#

J IN#42608    D L120      4350670   USED BACKHO
J IN#42608    C L220      4350670   USED BACKHO   AB0420   72686            UC4502
J PAYMENT     C L111      45000     RECD ON ACCT  JRCA40
J PAYMENT     C L111      22000     RECD ON ACCT  STAR01
J PAYMENT     C L111      2436      RECD ON ACCT  DFYU73
J BNKDEP      D L102      69436     RECD ON ACCT
J EXP         C L102      2456      TELEPHONE
J EXP         D L600      2456      TELEPHONE
J HDL CHG     C L658      5000      HAND ON UNIT
J HDL CHG     D L111      5000      HAND ON UNIT  COPE02
J IN#10672    C L320      4500000   CASE BACKHO   WEAV01   80187       2    TUNITI
J IN#10672    D L111      4500000   CASE BACKHO   WEAV01

Current line  130                                       Next line     140

Press Cmd1 to end job; Cmd2 recurrent trans; Cmd3 show line#; Cmd4 show stock#
```

Please take note of the valid Cmd keys listed at the bottom of the screen.

**Cmd1 to end job:**

This key ends this part of the job and moves you into the next job step. Do not press Cmd1 unless you are finished entering all the lines necessary to create your batch.


**Cmd2 recurrent trans:**

This allows you to save a copy of the batch before it is posted. Also you may recall a batch that is already saved to be posted with the batch you are creating. You may delete a saved batch. A saved batch can be replaced with another batch. This option is also an option off the Editor Correction Menu. It will be explained later in the chapter.

**Cmd3 show line#:**

If a mistake occurs when entering a line, press Cmd3 to see which line number contains the error. Move the cursor to the Next line field. Type the line number of the line that needs correcting. Field Exit and press Enter. The line displays. Make any necessary changes to any of the fields. When the corrections have been made, press Enter.

**Cmd4 show Stock#:**

The Stock# field is displayed normally. If Cmd3 is pressed to show line#, Press Cmd4 to redisplay the Stock# field.

When one screen is filled with lines, another screen will be displayed. At the top of the next screen will be the last line that was typed. The line is displayed to help you remember where you were when typing a batch.

When all the lines for the batch have been entered, press Cmd1 to end job. You will proceed to the next step of the job, editing the batch.

### Editing The Batch

When the Cmd1 is pressed, the following screen will display:

```
WEAVER'S EQUIPMENT SHOP	POST SOURCE DOCUMENTS	6/24/97 X1710-101
Division L			CHECK FOR ERRORS	June

Editing option: 1
1. Check document balancing.
2. Do not check document balancing.

Output option: 1
1. Display edit list -- with option to print later.
2. Print edit list.

Editing Division: L
You may change the division code to be used for
editing this posting batch.

Press Cmdl to return to Editor Correction Menu
```

On the Post Source Documents Check for Errors screen you select the editing option.

**Editing Option:**

- Check document balancing: The dollar figures on the debit and credit lines of the batch must balance before they will be posted This option asks whether the document numbers are the same on


the debit and credit lines.

Think about your batch. If what is typed on the debit line in the Document# field is the same as what is typed in the Document# field on the credit line of the transaction, then select option 1, Check document balancing. However if the two fields are filled in with different information, select option 2, Do not check document balancing.

If you select option 1, the lines that were typed will be broken down into documents. Every line that has the same document number in the Document# field will sort together on the screen. There will be a break between documents. This makes the transactions easier to read.

- Output option: Option 1 is the default. This will make the batch print on the screen. If there are any errors, the messages will print on the screen. This means you can make changes and save time. Option 2 will print a list and return to the editor correction menu if errors exist. You would then have to proceed to the batch and make corrections.

- Editing Division: The default will be the division you created the batch for. If your general ledger accounts are in another division, change the division code.

When your selections are made, press Enter. After a few minutes, The Post Source Documents Check for Errors screen is displayed.


```
WEAVER'S EQUIPMENT                                  POST SOURCE DOCUMENTS          7/16/97 X1710-501
Division L                                          CHECK FOR ERRORS               July
Current display: partial transactions
                                                    Update line #
Line#   Date      Document#   Account # E   Amount      Description      Addr #
10 J    7-16-97   IN#42608    D L120    W   43506.70    USED BACKHO
Stock number must be entered.                                                                  E010
20 J    7-16-97   IN#42608    C L220    F   43506.70    USED BACKHO      AB0420
Wrong General Ledger account number for this vendor.                                           E029

30 J    7-16-97   PAYMENT     C L111    A   450.00      RECD ON ACCT JRCA40
40 J    7-16-97   PAYMENT     C L111    A   220.00      RECD ON ACCT STAR01
50 J    7-16-97   PAYMENT     C L111    A   24.36       RECD ON ACCT DFYU73
The debit and credit totals on above document do not balance.                                  E034

60 J    7-16-97   BNKDEP      D L102        694.36      RECD ON ACCT
The debit and credit totals on above document do not balance.                                  E034

70 J    7-16-97   EXP         C L102        24.56       TELEPHONE
80 J    7-16-97   EXP         D L600        24.56       TELEPHONE

90 J    7-16-97   HDL CHG     C L658        50.00       HAND ON UNIT
100 J   7-16-97   HDL CHG     D L111    A   50.00       HAND ON UNIT COPE02
Press Cmdl to end job; Cmd2 partial transactions; Cmd3 full transactions;
Cmd4 recap; Cmd5 scan for error; Cmd6 more fields; roll keys
```

If there are any errors, an error message will display below the line the error is on. The cursor is positioned to the right of the Update line # field at the top of the screen. If a correction needs to be made to a line, type the line number, Field Exit and press Enter. The line is displayed. You may make any changes to the fields necessary.

You may also elect to delete the line. Enter Y by the field that reads: Existing Line, enter Y to delete. If the field reads: Deleted line, Enter y to reinstate, enter Y if you wish to add the line to the batch.

When all corrections to the line have been made, press Enter. The changes


made to the line are not visible on the screen. This is because the screen displays the picture taken when the editing option was selected. The batch will have to be reedited before it can be posted. When it is reedited, the changes will be visible.

```
WEAVER'S EQUIPMENT                                  POST SOURCE DOCUMENTS     8/26/97  X1710-502
Division L                                          CHECK FOR ERRORS          August

ID  Document#   Account#    Amount  Description Addr#   Date      Line #    10
                                                                  Discount  Stock
J   IN#12890    C L33110    12436   PARTS INV

    Actual      Percent
    Costing     Costing
                12436

The above fields are only used for parts
and rental revenue costing. (Edit codes 'D' and 'R')

                                                    Existing line, enter 'Y' to delete

Press Cmdl to return without update
```

The above example is a credit line to the parts sales account.

Please note the figure in the "Percent Costing" field. This is the amount of the sale in dollars that is to be multiplied by the factor tied to the general ledger account in General Ledger Maintenance. The field will always contain the figure in the "Amount" field unless it is changed. In the example, the total of the parts sold on document #12890 was $124.36. The percentage tied to this sale account at General Ledger Maintenance is 80%. 80% of $124.36 will be credited to the inventory account and


debited to the cost of sale account.

You may find that the percentage of cost on the sale is not enough. For example, you are having a promotion and are selling hats at $1.00 for the month of July. The hats cost you 3.00 each. The cost that would be transferred on the sale would be .80 (1.00 X 80%). To post the actual cost of the hat, Field Exit through the figure in the "Percent Costing" field. Type the actual cost, $3.00, in the "Actual Costing" field. Field Exit and Enter. You will show a loss on the sale and the accounting will be correct. See the following example:

```
WEAVER'S EQUIPMENT                                POST SOURCE DOCUMENTS              8/26/97 X1710-502
Division L                                        CHECK FOR ERRORS                   August
                                                                                     Line #      10

ID Document#   Account#      Amount  Description  Addr#   Date      Discount  Stock
J IN01609 #* C L33113       100     PM T

Actual         Percent
Costing        Costing
300

The above fields are only used for parts
and rental revenue costing. (Edit codes 'D' and 'R')

                                                   Existing line, enter 'Y' to delete

Press Cmdl to return without update
```


**Correcting Errors**

Below are some common error messages and how to correct these errors:

> Stock number must be entered. This type of message indicates that a required field was left blank. Bring up the line and enter the stock number.

> Customer address number does not exist. This message tells you that customer address number has not been set up in Receivables Maintenance. Any message that tells you that your subledger number does not exist requires that you go to the proper maintenance job and open the number.

Press Cmd1 to end the job. Select option 3, End job without printed edit list. Press Enter. The following menu displays:

```
COMMAND                                  MENU: X17                  INQUIRY CA
(c) DIS Corp.

EDITOR CORRECTION MENU

1. Check for Errors
2. Receivables Maintenance
3. Vendor Maintenance

5. General Ledger Maintenance
6. Inquire/Update Units
7. Correction & Recurring Transactions
20. Cancel Post Source Documents

23. Return to Previous Menu

Ready for option number or command
```


Select the proper maintenance job. Press Enter. When Cmd1 is pressed from the maintenance job, the Editor Correction Menu will redisplay.

Select option 1, Check For Errors. Select the editing options. Press Enter. The batch is edited. When the batch displays, the changes made will show on the screen. Make any additional changes to the batch.

- Wrong General Ledger account number for this vendor. This message tells you that the general ledger number entered in the Account # field is not the correct account number for the subledger information entered in the Addr # field.

Proceed to the appropriate maintenance job and change the general ledger account that the subledger is tied to.

> **WARNING!**
> You can only change the general ledger account number if there is no balance posted to the subledger.

Follow the instructions in step 2 to go to maintenance.

Make sure the address number entered in the Addr # field is the number you want. If not, bring up the line and change the address number.

- Stock number has been sold or Stock number has not been sold. If one of these messages appears, you are attempting to post cost to the wrong account.

If you see the message, Stock number has been sold, you are attempting


to post cost to the inventory account of a sold unit. Change the general ledger account number entered in the Account # field to the cost of sale account for the unit. If the wrong unit number has been entered in the stock# field, bring up the line and change the stock number.

If you see the message, Stock number has not been sold, you are attempting to post cost to a cost of sale account when the unit is still in inventory. At the time the sale is made, an automatic transaction occurs. The cost for the unit in inventory is transferred to the cost of sale account. Any additional costs should be posted to the cost of sale account. Change the general ledger account number entered in the Account # field to the cost of sale account for the unit. If the wrong unit number has been entered in the Stock# field, bring up the line and change the unit number.

- The debit and credit totals on the above document do not balance. There are two possible reasons for this error. The first is that the batch is really out of balance. Check the figures on the credit and debit lines to make sure they are in balance.

The other possibility is that the wrong editing option was selected. Option 1, Check document balancing, was selected when the Document# when the Document # field on the debit line contained different information than the credit line. Press Cmd1. Select option 3, End job without printed edit list. From the Editor Correction Menu, select option 1. When the Post Source Documents Check for Errors screen displays, change the Editing option. Select option 2, Do not check for document balancing and press Enter.

- Receivables transactions cannot be posted to this general ledger month.


You are trying to post to an account with an A code for a GL month which is more than one month less than or greater than the AR month in Security and Configuration. Delete the lines from the batch and reenter the transaction in a new batch posted to an acceptable GL month; or save the batch and include it in a new batch posted to a correct month.

Note the Cmd keys at the bottom of the screen

```
WEAVER'S EQUIPMENT                                POST SOURCE DOCUMENTS   7/16/97 X1710-501
Division L                                        CHECK FOR ERRORS        July
Current display: partial transactions                                 Update line #

Line#   Date      Document#   Account #   E   Amount      Description    Addr #
10 J    7-16-97   IN#42608    D L120      W   43506.70    USED BACKHO
20 J    7-16-97   IN#42608    C L220      F   43506.70    USED BACKHO    AB0420

30 J    7-16-97   PAYMENT     C L111      A   450.00      RECD ON ACCT   JRCA40
40 J    7-16-97   PAYMENT     C L111      A   220.00      RECD ON ACCT   STAR01
50 J    7-16-97   PAYMENT     C L111      A   24.36       RECD ON ACCT   DFYU73
60 J    7-16-97   PAYMENT     D L102          694.36      RECD ON ACCT

70 J    7-16-97   EXP         C L102          24.56       TELEPHONE
80 J    7-16-97   EXP         D L600          24.56       TELEPHONE
90 J    7-16-97   HDL CHG     C L658          50.00       HAND ON UNIT
100 J   7-16-97   HDL CHG     D L111      A   50.00       HAND ON UNIT   COPE01

---------------------------------- End of transactions ----------------------------------
Press Cmd1 to end job; Cmd2 partial transactions; Cmd3 full transactions;
Cmd4 recap: Cmd5 scan for error; Cmd6 more fields; roll keys
```

**Cmd1 to end job:** Use Cmd1 will advance you to the next step of this job.

**Cmd2 partial transactions:** Partial transactions are displayed when the Post Source Documents Check For Errors


**Cmd3 full transactions:** screen is first displayed. Only the first part of the lines can be viewed. To view the Date, Discount and Stock # fields, press Cmd3 or Cmd6. Allows you to view the Due Date, Discount and Stock Number Fields. Use Cmd2 to return to partial transactions.

**Cmd4 recap:** Displays the general ledger accounts and the amounts to be debited and credited to each account. You can see if debits equal credits. If not, the "Out of balance by" amount is calculated and displayed. Also it is helpful to see the account numbers and names of the accounts on the same screen. This may help to catch errors up front.

**Cmd5 scan for error:** This will roll through the screens of the batch to locate errors. It will stop on each line that needs correcting.

**Cmd6 more fields:** Displays the Due Date, Discount and Stock Number fields. To return to partial transactions, press Cmd6 again.

**Roll keys:** Roll through the screens to view each invoice. You can roll either up or down. The last line of the screen will be the first line of the following screen. This feature is designed to help you keep track of where you are in a batch.

When all corrections have been, press Cmd1.

## POSTING A BATCH

When Cmd1 is pressed, the following screen displays:

```
WEAVER'S EQUIPMENT SHOP                               POST SOURCE DOCUMENTS       6/24/97   X1710-503
Division L                                          CHECK FOR ERRORS          June

End of job option: 1
1. Return to processing -- do not end job
2. End job with printed edit list
3. End job without printed edit list
4. Create new edit list.

Corrections have been made. This batch must be re-edited before it can be posted.
```

## Options and when they are used

- **Return to processing -- do not end job**

    This option will take you back a step. The previous screen will display. Use this option if you want to change anything else in the batch.

- **End job with printed edit list**

    Ending with this option will give you a list of what is in the batch. If the batch has errors or corrections have been made, you will not be able to post the batch. Having a print out of the batch may make it easier to locate errors. You can read the line number that needs correcting off the print. It may be easier than rolling through the screens looking for errors.


You will return to the Editor Correction Menu. Select option 1, Check for errors. This will return you to the batch to make corrections.

If there are no errors, you will get a printed edit list and the option to post. The edit lists will also be on the End of Day report. If you want to know what was posted before running End of Day, this report will be helpful.

- End job without printed edit list:

If there are errors or corrections to the batch, the option to post will not display. Instead, you will return to the Editor Correction Menu.

Select option 1, Check for Errors to return to the batch. Press Enter. You will have the opportunity to change the editing option. If, for example, you elected not to check for document balancing, you can change that choice. Select option 1 to check for document balancing.

When all the editing options are selected, press Enter. The batch will display. Make any corrections necessary.

If no errors exist and no corrections have been made, the option to post will display. Your print of the edit list will be on the End of Day report.

- Create new edit list:

If corrections have been made, you will need to create a new edit list before you can post. Remember, the corrections you made did not display on the screen. It was a picture of the batch as it was when you requested the first edit. The batch will be displayed with the changes you made.


Pay attention to the messages on the Post source documents check for errors screen on the previous page. In the example, the message reads: Corrections have been made. This batch must be re-edited before it can be posted. If this message displayed, you would select option 4. Press Enter.

Repeat the above steps as necessary. When the following screen displays, you are ready to post.

```
WEAVER'S EQUIPMENT SHOP                                POST SOURCE DOCUMENTS                        6/24/97 X1710-503
Division L                                             CHECK FOR ERRORS                             June

End of job option: 1
1. Return to processing -- do not end job
2. End job with printed edit list
3. End job without printed edit list
4. Create new edit list.

No errors have been detected. This batch may be posted.
```

Select option 2 or 3 depending on whether you want an edit list. Press Enter.


The following screen displays:
```
COMMAND MENU: X171 CA
(c) DIS Corp.

END OF EDITOR OPTION MENU


No Errors Have Been Detected

1. Post Source Documents

23. Return To Editor Correction Menu

Ready for option number or command
```

Select option 1, Post Source Documents. Press Enter. The batch is posted.

## HOW TO POST CREDIT CARD SALES

If, for any reason, it is necessary to enter credit card sales through Create Source Documents, make sure that:

- The 2 characters "$C" are in the last 2 positions of the debit to the customer's account.
- The same document number is used for all lines.
- The document number is in the description field of the credit to the customer's account.
- The 2-character credit card code is in the last 2 positions of the debit to the credit card account.

```
A&R EQUIPMENT SALES                                POST SOURCE DOCUMENTS                3/18/97  X1700-101
Division A                                         Document Entry                       June
ID Document#   Account#                            Amount     Description    Addr#      Date     Discount    Stock#

C CT00800      D A1110                             80000      $C VANP01
C CT00800      C A3360                             80000      VANP01
C CT00800      C A1110                             80000      CT00800        VANP01
C CT00800      D A1110                             80000      VANP01         FP FARMPL
C C
Current Line   60                                                                       Next Line     70


Cmd1-End job Cmd2-recurrent transactions      Cmd3-Show Line#  Cmd4-Show Stock#
```

### How To Save A Batch

Most dealerships post depreciation on a monthly basis. The same accounts are debited and credited month after month. There is a way to create the batch, store the batch and recall the batch for use at a later date.

When all the errors have been corrected in the batch and you are ready to post the batch, save the batch to use at a later date. The batch must be saved before you post it. Cmd1 to end the job as if you were going to post. The following screen displays:

```
WEAVER'S EQUIPMENT SHOP
Division L

End of job option: 1

POST SOURCE DOCUMENTS
CHECK FOR ERRORS

6/24/97 X1710-503
June

1. Return to processing -- do not end job
2. End job with printed edit list
3. End job without printed edit list
4. Create new edit list.

No errors have been detected. This batch may be posted.
```

Select option 2 or 3 depending on whether you want an edit list. Press Enter.


The following screen displays:

```
COMMAND MENU: X171 CA
(c) DIS Corp.

END OF EDITOR OPTION MENU

No Errors Have Been Detected

1. Post Source Documents

23. Return To Editor Correction Menu

Ready for option number or command
```


Select option 23, Return to Editor Correction Menu. Press Enter. The menu will display:

```
COMMAND                                  MENU: X17                      INQUIRY CA (c)
DIS Corp.


                        EDITOR CORRECTION MENU


    1.  Check For Errors
    2.  Receivables Maintenance
    3.  Vendor Maintenance

    5.  General Ledger Maintenance
    6.  Inquire/Update Units
    7.  Correction & Recurring Transactions

    20. Cancel Post Source Documents
    23. Return to Previous Menu


Ready for option number or command
```

Select option 7. Press Enter. The following screen will display:


```
WEAVER'S EQUIPMENT                                POST SOURCE DOCUMENTS          7/16/97   X1770-101
Division L                                        CORRECTION BY LINE #           July
Line #
```

Press Cmd1 to end job; Cmd2 recurrent transactions

Press Cmd2 recurrent transactions. The following screen displays:

```
WEAVER'S EQUIPMENT                                POST SOURCE DOCUMENTS          7/16/97   X1700-201
Division L                                        RECURRENT TRANSACTIONS         July

Group Name.................. WDEPREC
Action...................... SAVE
INCLUDE/SAVE/REPLACE/DELETE
```

Press Cmd1 to end job Cmd2 to list group names


The batch will have to be named. Think up a name that will mean something to you when you see it again. All the batches that are saved will be listed together and you will have to pick which one you want to recall. The name can be up to 8 characters long. Type the name in the Group Name field.

In the Action field, type SAVE. Field Exit and press Enter. The batch is saved. If you attempt to save a batch with the same name as another saved batch, a message will display informing you that the name has been used. Press Cmd2 to see a list of saved batches.

If you are never going to use a batch again, you can delete the batch. In the Group Name field, type the name of the batch to be deleted. In the Action field, type DELETE. Field Exit and press Enter. The batch is deleted.

If a batch that is saved is outdated, you can replace the batch with the batch that is being set up now. In the Group Name field, type the name of the batch to be replaced. In the Action field, type REPLACE. Field Exit and press Enter. The batch with the name that was typed will contain the new information.

## HOW TO INCLUDE A BATCH

### Including a Saved Batch With a Current Batch

If you want to include a batch that is saved to the current batch, type the name of the batch to be included in the Group Name field. Type INCLUDE in the Action field. The batch will be included with the current


batch at Create Source Documents. Press Enter. The following screen displays:

```
WEAVER'S EQUIPMENT                                POST SOURCE DOCUMENTS     7/16/97  X1700-201
Division L                                        RECURRENT TRANSACTIONS    July

Group Name.................. WDEPREC

Action...................... INCLUDE

Work/Due Date (mmddyy)...... 082397
```


If you fill in a new Work/Due Date, the DATE field in the batch will be updated with the new date. This would mass update the due date of a payables batch. If you do not want to change the date, leave the Work/Due Date field blank. The option to change the Work/Due Date is only available with the INCLUDE option. Press Enter.

The Post Source Documents Recurrent Transaction screen is displayed again. To edit and post the batch, Cmd1. See the Editing the Batch and Posting a Batch sections of this manual for instructions.

**Including a Saved Batch if it is the Only Batch to be Posted**

If all you want to do is to post a batch that is saved, proceed to Create Source Documents as if you were going to type in the batch. See the screen below:


```
WEAVER'S EQUIPMENT                                  POST SOURCE DOCUMENTS       7/16/97  X1700-101
Division L                                          DOCUMENT ENTRY              July

ID Document#   Account#   Amount   Description   Addr#   Date       Discount   Stock#

Current line   10                                                               Next line   20
```

Press Cmdl to end job; Cmd2 recurrent trans; Cmd3 show line#; Cmd4 show stock#

Instead of typing the lines, press Cmd2, recurrent transactions. The following screen displays:


```
WEAVER'S EQUIPMENT                                POST SOURCE DOCUMENTS        7/16/97 X1700-201
Division L                                      RECURRENT TRANSACTIONS       July

Group Name................... WDEPREC
Action....................... SAVE
INCLUDE/SAVE/REPLACE/DELETE
```

Press Cmdl to end job Cmd2 to list group names

If you do not remember the name of the batch to be included, press Cmd2 for a list of saved batches.

Enter the name of the batch to be included in the Group Name field. Type INCLUDE in the Action field. Press Enter. The following screen will display:

```
WEAVER'S EQUIPMENT                                POST SOURCE DOCUMENTS        7/16/97 X1700-201
Division L                                      RECURRENT TRANSACTIONS       July

Group Name................... WPAYMENT
Action....................... INCLUDE
Work/Due Date (mmddyy)....... 082397
```


If you fill in a new Work/Due Date, the DATE field in the batch will be updated with the new date. This would mass update the due date of a payables batch. If you do not want to change the date, leave the Work/Due Date field blank. The option to change the Work/Due Date is only available with the INCLUDE option. Press Enter.

The Post Source Documents Recurrent Transaction screen is displayed again. To edit and post the batch, Cmd1. See the Editing the Batch and Posting a Batch sections of this manual for instructions.

## CANCELING A BATCH

If you are entering a batch and decide that you do not want to post the batch, the batch must be canceled before you can exit the Create Source Documents job.

If you have corrected the batch once, Cmd1 to end job. Select option 3, End job without printed edit list. The Editor Correction Menu displays. Select option 20, Cancel Post Source Documents. Press Enter.

If you have just entered the lines at Create Source Documents and have not checked the batch for errors, Cmd1 to end job. Cmd1 again to return to Editor Correction Menu. At the Editor Correction Menu, select option 20, Cancel Post Source Documents. Press Enter. The following screen displays:


```
Cancel Post Source Documents

CAUTION!

You are about to cancel the Post Source Documents batch for this workstation.

If you intend to recall this batch sometime in the future, you must first save the batch before cancelling. If you have not already saved this batch and wish to, enter "NO" below and request the "Correct Source Documents" job. From the correction job, you use CMD 2 To "SAVE" a batch.

If you are sure you want to cancel the batch now enter "YES" below to continue.

Do you want to continue (YES/NO)
```

**Do you want to continue (YES/NO)**

If you want to cancel the batch, type YES, and Press Enter. You will return to the Accounting Menu.

If you do not want to cancel the batch, type NO, and press Enter. You may decide not to cancel the batch if it should be saved for posting at a later time and you have not yet saved it. You will return to the Editor Correction Menu. Select option 7, Correction and Recurring Transactions. Press Enter. Press Cmd2, recurrent transactions to save a batch. See the section titled How to Save a Batch for more instructions.

### OTHER OPTIONS ON THE EDITOR CORRECTION MENU

The chapter has discussed most of the options on the Editor Correction Menu. To display the Editor Correction Menu, press Cmd1 from the batch. Select option 3, End job without printed edit list. The following menu displays:

```
COMMAND			MENU: X17			INQUIRY CA (c)
DIS Corp.

			EDITOR CORRECTION MENU

1. Check For Errors
2. Receivables Maintenance
3. Vendor Maintenance

5. General Ledger Maintenance
6. Inquire/Update Units
7. Correction & Recurring Transactions

20. Cancel Post Source Documents

23. Return to Previous Menu

Ready for option number or command
```

Option 1, Check For Errors. This option is used after corrections have been made to the batch. It will give you the opportunity to change the editing options if the wrong one was chosen.


Options 2 - 6 are used for maintenance. If an error message is displayed while editing the batch, you may proceed to the proper maintenance job to correct the error.

**Option 7 Correction and Recurring Transactions.** When you select option 7, the following screen displays:

```
WEAVER'S EQUIPMENT                                POST SOURCE DOCUMENTS      7/16/97  X1770-101
Division L                                        CORRECTION BY LINE #       July
Line #
```

Press Cmdl to end job; Cmd2 recurrent transactions

You may enter any line from the batch you are currently working on and correct or delete it.

Here is an example of why you would want to use this option. If you have a lot of errors, Cmd1 from the batch, to end the job. Select option 2, End job with printed list. You will return to the Editor Correction Menu. Select option 7. You can then check off the printed list the lines as you correct them. Each time you enter a line number, the amount from the last line number used will display. This is to help you keep track of the last line

**ACCOUNTING**


that was corrected. Type over the amount, if you want to change it. When all corrections have been made, Cmd1 back to the Editor Correction Menu. Select option 1, Check For Errors and reedit the batch.

Cmd2 will take you to recurring transactions. This is where a batch is saved before posting to be used at a later time. See the sections titled How to Save a Batch and How to Include a batch for instructions.

Option 20 Cancel Post Source Documents. If you begin a batch that you do not want to post, the batch must be cancelled before you can leave Create Source Documents. See How to Cancel a Batch.

Option 23. DO NOT USE THIS OPTION.


CREATE SOURCE DOCUMENTS (X1-7)

[Cmd2]-Recurrent Transactions

**DOCUMENT ENTRY**
- Current Batch
- Lines

[Cmd1]-End job

**CHECK FOR ERRORS**
- Editing Options

[Enter]

**CHECK FOR ERRORS**
- Current Batch
- Lines

[Cmd1]-End Job

**CHECK FOR ERRORS**
- End of Job Options
- Option 4 Create New Edit List
- Option 1. Return to processing
- Option 2 or 3 With Errors
- No re-edit
- Option 2 or 3 No Errors
- No re-edit

**END OF EDITOR OPTION MENU**
1. Post
23. Ed. Corr. Menu

**RECURRENT TRANSACTIONS**
- Group Name
- Action

Recurrent Batch Actions:
- INCLUDE a saved batch in the current batch
- SAVE the current batch
- REPLACE a saved batch with the current batch
- DELETE a saved batch

[Cmd1]

Option 1. Check for Errors

[Cmd1]

**EDITOR CORRECTION MENU.**

**PRINTED EDIT LIST (Opt. 2)**

Option 23. Editor Correction Menu

Option 7. Correction & Recurring Transactions

**CORRECTIONS BY LINE#**
- Line#

[Cmd2]-Recurrent Transactions

Option 20. Cancel Post Source Documents

**ACCOUNTING MENU**

**CAUTION!**

YES

Batch is Canceled

## CREATE SOURCE DOCUMENTS (X1-7) POSTING GUIDE

| ID | DOCUMENT# | D/C | ACCOUNT# | AMOUNT | DESCRIPTION | ADDR# | DATE | DISCOUNT | STOCK# |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Required  A/R | Required | Open Item ROA=Document # | Customer | No | No | No |
| Required  A/P | Required | Recommended | Vendor | Due date | $ Amount, if any | No |
| Required  Flooring | Required | Recommended | Vendor | Due date | $ Amount, if any | Required |
| Required  Units Sales | Required | Recommended | Customer | Warr. Expir. | Warranty: 1-9 | Required |
| Required  Units Inv./Cost | Required | Recommended | No | No | No | Required |
| Required  Units Inv. (Trade) | Required | Recommended | New Unit# | No | No | Trade-in# |

| ID | DOCUMENT# | D/C | ACCOUNT# | AMOUNT | DESCRIPTION | ADDR# | DATE | DISCOUNT | STOCK# |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |

## CHAPTER X1-8

## X1-8 COMPUTING HOURS FOR TIME CARDS

See the Stop/Start screen below:

```
TIME CONVERSION PROGRAM

Enter time as hours and minutes or decimal hours as
instructed below then press enter to perform desired function.

           Hours  Minutes
Start time   00      00
Stop time    00      00

Elapsed time
Hours-minutes
Decimal hours
```

**Control commands:**

- **CMD 1** - end of job
- **CMD 2** - start-stop calculation
- **CMD 3** - hours-minutes to decimal hours conversion
- **CMD 4** - hours-minutes addition
- **CMD 5** - decimal hours addition

### Fields & Descriptions

The fields are described below:

| Field                  | Type In                  | Press       |
| ---------------------- | ------------------------ | ----------- |
| Starting Time Hours    | Starting time in hours.  | FIELD EXIT  |
| Starting Time Minutes  | Starting time in minutes. | FIELD EXIT  |
| Stopping Time Hours    | Stopping time in hours.  | FIELD EXIT  |
| Stopping Time Minutes  | Stopping time in minutes. | ENTER       |


RESULT: The elapsed time will be displayed in hours and minutes and in decimal hours. Jot down the time in the format you prefer if you plan to add two or more job times together.

Enter the next start or stop time. The job will continue to calculate hours worked until CMD 1 is used.

- Press CMD 3 to convert hours and minutes to decimal hours. See the conversion screen below:

```
TIME CONVERSION PROGRAM

Enter time as hours and minutes or decimal hours as
instructed below then press enter to perform desired function.
Hours  Minutes    Decimal hours
  00     00

Control commands:
CMD 1 - end of job
CMD 2 - start-stop calculation
CMD 3 - hours-minutes to decimal hours conversion
CMD 4 - hours-minutes addition
CMD 5 - decimal hours addition
```

## Fields & Descriptions

| Field | Type In | Press |
| :--- | :--- | :--- |
| Hours | The number of hours worked. | FIELD EXIT |
| Minutes | The number of minutes worked. | FIELD EXIT  | ENTER |

**RESULT:** The hours and minutes will be converted to decimal hours for you in the DECIMAL HOURS field.

Enter another time to be converted, or press CMD 1 to end the job.


Press CMD 4 to add the hours and minutes.
See the addition screen below:

```
TIME CONVERSION PROGRAM

Enter time as hours and minutes or decimal hours as
instructed below then press enter to perform desired function.

Hours Minutes

Total
```

Control commands:
- CMD 1 - end of job
- CMD 2 - start-stop calculation
- CMD 3 - hours-minutes to decimal hours conversion
- CMD 4 - hours-minutes addition
- CMD 5 - decimal hours addition

### Fields & Descriptions

The fields are described below:

| Field   | Type In                                                                                             | Press      |
| :------ | :-------------------------------------------------------------------------------------------------- | :--------- |
| Hours   | Hour(s) you want to add.                                                                             Minutes | Minutes you want to add.                                                                                     | Type the hours and minutes as one number. EX: 6 hours and 11 minutes would be typed 0611.           | FIELD EXIT                                                                                                      | ENTER       Type the next hours & minutes.                                                                      | FIELD EXIT                                                                                                      | ENTER      |

**RESULT:** The TOTAL field will keep a running total of all the time additions.

Repeat the steps above until you've added all the hours and minutes you need to. Press CMD 1 to end the job.


Press CMD 5 to add decimal hours.
See the decimal hours screen below:

```
TIME CONVERSION PROGRAM

Enter time as hours and minutes or decimal hours as
instructed below then press enter to perform desired function.

Decimal hours


Total
```

Control commands:
CMD 1 - end of job
CMD 2 - start-stop calculation
CMD 3 - hours-minutes to decimal hours conversion
CMD 4 - hours-minutes addition
CMD 5 - decimal hours addition

### Fields & Descriptions

The fields are described below:

| Field | Type In | Press |
| :--- | :--- | :--- |
| Decimal hours | Hour(s) in decimal form to add.<br>There are 3 places after the decimal<br>so 5 hours and 15 minutes would be<br>typed 5250. | FIELD EXIT<br>ENTER  Type the next decimal hour(s). | FIELD EXIT<br>ENTER |

RESULT: The TOTAL field will keep a running total of your additions.

Repeat the steps above until you've added all the hours you need to. Press CMD 1 to end the job.

## CHAPTER X1-9

## END OF DAY PROCEDURES

### INTRODUCTION

End of Day Procedures print an audit trail of the Accounting Department's daily activity. The following audit reports are printed:

- Daily Posting Log & Recap
- Daily Maintenance Log
- Subledger Balance Report (optional by DIS OPT switch)

Keep these reports! If you are audited by a government agency, these are the reports that will answer questions.

### PREPARATION

- Make sure all Accounting Jobs clear the User Board.
- Run this job at least once a day. Accounting End of Day is an option available at Backup (X6-1). If the option is taken at daily backup, you do not need to run it again.

## X1-9 END OF DAY PROCEDURES

### **How To Run**

End of Day Procedures is a divisional job and must be performed on each division.

From the Accounting Menu, select option 9, End of Day Procedures. After passing the security gate, the following screen appears.

```
LEE'S RENTAL COMPANY	TIME DELAY	X0008-201 1
			Accounting End of Day

Time to start job . . . . . . . . 0932

Cmdl-Cancel	Cmd9-No Delay
```

Enter the time you want the End of Day Procedures to begin and press [Enter]. If you have the optional Finance and Insurance applications, you may see the following screen before End of Day is evoked.


```
Accounting End of Day                                           XFI40-001

Units inventory has been changed and should be transferred
to the F&I system.

If a transfer is desired, press Cmdl to return to a menu, then
hot key to the PC side, start the F&I system and take option 9
from the 'Other' screen for the transfer menu.

Otherwise, press Enter to continue.

Cmdl-End      Enter-continue
```

If this screen appears, information on your unit inventory has been changed. If you wish to continue with End of Day, press Enter. If you wish to transfer F&I information now, press Cmd1 to return to the menu.

## TRANSFER F&I INFORMATION (Optional DIS product)

On your PC, Hot Key to the F&I software. The F&I Deal Screen will be displayed.

```
APR : 0.00%                 NEW CUSTOMER
TAX : 6.50%                 Aug 3 1997      DATA CONSULTANTS FINE CARS

F1 Price................D F6 Trade..................aF6 Def I.................

F2 Down...................F7 Lien...................aF7 Def II................

F3 DMV....................F8 Ins. Code..............aF8 Def III...............

F4 Rate...................F9 Svc. Cont..............aF9 O/S Loan..............

F5 Term...................F10 Payment...............aF10 Collision............

                                ENTER : 0

A: Buyer Info     F: Recall Deal   K: New Loan      P: Maintenance   V: Term Pmts
B: Vehicle Info   G: Review Deal   L: New Lease     Q: LAHA Pmts     X: Exchange
C: Misc Info      H: Delete Deal   M: M-T-D         R: Quick View    Y: A.M.O.'s
D: Credit Check   I: Print Forms   N: Inventory     S: Smog Fees     Z: High Penny
E: Store Deal     J: Recap Deal    O: Other         T: Time
```

To select the Other Menu, type the letter O. The Other Menu will be displayed.


```
Other                               NEW CUSTOMER                        Aug 3 1997

0. Return To Main Screen            5. Telecommunications
1. Change Data                      6. Update System Files
2. Exit F&I System                  7. Software Revision Code
3. Sales Aids                       8. Transfer Inventory From S/36
4. Delete Sidekick Files            9. Transfer M-T-D To S/36


Enter Desired Selection < 0 - 9 >

Touch Enter After Each Entry

F1=Help                                                                  Esc=Exit
```

To continue to the Transfer Inventory from the S/36 screen, select option 8. Press Enter. The Inventory Transfer screen will be displayed.


```
Inventory Transfer          DATA CONSULTANTS FINE CARS          Aug 3 1997

0. Return To Main Screen
1. Transfer Changed Units Only
2. Transfer All Units Available

Enter Division Code: A
Transfer All Divisions?

Setting Up Gateway To System 36 --
Enter Desired Selection < 0 - 2 > 1
```

This screen will transfer up-to-date unit information from the System/36 to the F&I System. Fill in the following information:

- **Division Code**
    Enter your division code.
- **Transfer All Divisions?**
    Type N to transfer unit information for only your division. Type Y to transfer unit information for all divisions. Shows when company has more than one division.


**OPTIONS**

1) Transfer Changed Units Only - Transfer unit information on only those units that have been updated.
2) Transfer All Units Available - Transfers information from all units available for sale.

After the transfer is complete, Hot Key back to the System/36 menu. You are now ready to re-run Accounting End of Day.

After Accounting End of Day is evoked, the audit reports are printed.


1. ACCOUNTING END OF DAY DAILY POSTING LOG

The report shows all batches that have been posted in CREATE SOURCE DOCUMENTS (X1-7) and all Point of Sale Batches. Below is a sample report:.

 --- |--- |--- |--- |--- |--- |--- |--- |--- |--- |--- |--- |
| **Id** | **Date** | **Mth** | **Documents** | **Account** | **Edit** | **Amount** | **Description** | **Addr** | **Name** | **Due Date** | **Discount** | **Stock#**  08-15-96 | AUG | US4578 | C D1200 | | 5115.67 | TILLAGE  43808  08-15-96 | AUG | US4578 | C D1200 | N | 1114.25 | MOWER  43812  08-15-96 | AUG | US4578 | D D490C | W | 5115.67 | TILLAGE | | ADWIG2 WILLIAM ADAMS  43808  08-15-96 | AUG | US4578 | D N4000 | W | 1114.25 | MOWER | | ADW102 WILLIAM ADAMS  43812  08-15-96 | AUG | US4579 | C 01200 | N | 5533.18 | TRACTOR  43817  08-15-96 | AUG | US4579 | C D1200 | W | 8759.27 | PLOW  43845  08-15-96 | AUG | US4579 | D D400G | W | 5582.18 | TRACTOR | | GRLE15 LEROY GRADY  43817  08-15-96 | AUG | US4579 | D D4000 | | 8759.27 | PLOW | | GRLE15 LERCY GRADY  43345  09-25-96 | SEP | US4587 | C D1200 | W | 37427.67 | TRACTOR  00336  09-25-96 | SEP | US4587 | C D1200 | N | 7541.09 | BALER  00339  09-25-96 | SEP | US4567 | D D4090 | | 37427.67 | TRACTOR | | ADWIG2 WILLIAM ADAMS  00336  09-25-96 | SEP | US4587 | D D4000 | | 7541.09 | BALER | | ADWICZ WILLIAM ADAMS  00339  09-25-96 | SEP | US4589 | C D1200 | | 43014.12 | TRACTOR  43887  09-25-96 | SEP | US4589 | C D1200 | W | 64602.40 | TRACTOR  43909  09-25-96 | SEP | US4569 | D D4000 | W | 48014.12 | TRACTOR | | GRLE15 LEROY GRADY  43887  09-25-96 | SEP | US4569 | D D4000 | W | 64602.40 | TRACTOR | | GRLE15 LEROY GRADY  43909 |
| E | 08-15-96 | AUG | US45678 | C D1220 | | 900.00 | CA-UNIT SALE  00369 |
| E | 08-15-96 | AUG | US45678 | C D1220 | N | 275.00 | OA-UNIT SALE  43961 |
| E | 08-15-96 | AUG | US45678 | D D4000 | W | 900.00 | OA-UNIT SALE  43808 |
| E | 08-15-96 | AUG | US45678 | D D4000 | W | 275.00 | OA-UNIT SALE  43812 |


2. ACCOUNTING END OF DAY RECAP

This report lists the total of debits and credits posted to each general ledger since the End of Day Procedures was last run. Below is a sample report:

| ABC COMPANY | | ACCOUNTING END OF DAY | 10/31/96 | PAGE 1 |
|---|---|---|---|---|
| WHYNOT, CO | D | RECAP | | X1900-2A  | DEBIT | CREDIT |
|---|---|---|---|
| ACCOUNTS RECEIVABLE | D1100 | 220426.65  NEW INVENTORY | D1200 | | 178157.65 |
| USED INVENTORY | D1220 | | 26675.00 |
| NEW EQUIPMENT | D3000 | | 220426.65 |
| COST OF SALES-NEW | D4000 | 204832.65  **TOTAL** | | **425259.30** | **425259.30** |


10	X1-9 END OF DAY PROCEDURES

3. ACCOUNTING END OF DAY DAILY MAINTENANCE LOG

This report shows all changes or additions made in all accounting maintenance jobs. Below is a sample report:

 |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| ABC COMPANY  ACCOUNTING END OF DAY | 10/02/96 | PAGE 1  WHYNOT, CO  DAILY MAINTENANCE LOG | | X1900-3A  ID 
| DAC ADWI02 | WILLIAM ADAMS | | RT 1, BOX 933  | 0206 123 4567 W R | N 71 M DAC ADWI02 LINE #2 | ARLINGTON, WA | 98226 
| DAC GRLE15 | LEROY GRADY | | RT 1  555 789 4567 | R | N 51B | | EVERSON, WA | 98210  DAC GRLE15 | LINE #2  DGCN101 | CASH ON HAND | 000 P AC 
| DGCN102 | CASH IN BANK | GGO P AC 
| DGCN110 | ACCOUNTS RECEIVABLE | N342 | 000 A P AC  DGCN116 | ACCOUNTS RECEIVABLE | N342 | 000 A P A  DRC ADW102 N110 | 00000 2  DRC GRLE15 N110 | 00000 B  |

**Fields & Descriptions**

### **Id**

Comprised of 3 positions. This ID indicates where changes were made since last End of Day.

**1st position =**
First character of your division code where the changes were made.

**2nd position =**
The application changed:
R = Receivables
G = General Ledger
P = Payables
E = Payroll
A = Address Maintenance
U = Units


3rd position = The third area is the type of change: A = Add, C = Change, or D = Delete.

The remaining fields vary depending on which application maintenance was done on. Review the maintenance screens for each application to see the specific fields changed and listed on this report, if you need additional information.


Notes:


---