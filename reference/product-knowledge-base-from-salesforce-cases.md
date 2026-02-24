---
title: "Product Knowledge Base (from Salesforce Cases)"
source: "salesforce_case_derivative.md"
tags: ["Reference", "Troubleshooting", "Salesforce"]
version: "1.0"
last_updated: "2026-02-24"
short_description: "A knowledge base derived from Salesforce support cases."
long_description: "This document provides structured troubleshooting guidance for common issues, derived from an analysis of historical support cases."
---

## Product Knowledge Base

This knowledge base provides structured troubleshooting guidance for AI and human support agents. It is derived from analysis of historical support cases and focuses on recurring, high-impact issues. All personally identifiable information (PII), customer names, company names, email addresses, phone numbers, URLs, and other unique identifiers have been removed to ensure privacy and compliance. The content is generalized to be applicable across multiple customer environments.

The knowledge base is organized by issue category and follows a consistent structure: Problem, Symptoms, Root Causes, Resolution Steps, Validation, Prevention, and Escalation. This format is designed to enable rapid diagnosis and resolution while minimizing risk.

## Support Agent Operating Guidelines

When using this knowledge base, follow these principles to ensure safe and effective support:

**Triage and Diagnosis:** Begin by asking clarifying questions to understand the user's issue. Match the reported symptoms to the articles in this knowledge base. If the issue does not clearly match any article, gather more information before proceeding.

**Information Gathering:** Request specific, non-sensitive information to aid diagnosis. This may include screenshots of error messages, relevant system logs (with PII redacted), configuration settings, and steps to reproduce the issue. Do not request or store customer names, email addresses, phone numbers, or other personally identifiable information unless absolutely necessary for account lookup, and handle such data according to privacy policies.

**Resolution Execution:** Follow the resolution steps in the relevant article exactly as written. Do not skip steps or deviate from the documented procedure unless you have explicit guidance from a senior engineer. If a step is unclear or does not apply to the user's environment, pause and escalate rather than guessing.

**Validation:** After completing the resolution steps, confirm with the user that the issue is fully resolved. Ask them to test the functionality and verify that no new issues have been introduced. Document the outcome in the case notes.

**Escalation:** If the issue persists after following the documented resolution, if the issue is not covered in this knowledge base, or if the issue is critical and time-sensitive, escalate to Tier 2 support or the appropriate engineering team. Provide a clear summary of the issue, the steps already taken, and any relevant logs or screenshots.

**Safety and Compliance:** Never modify production data without explicit user consent and a clear understanding of the impact. Never share internal system details, database queries, or proprietary information with users. Always follow your organization's data handling and privacy policies.

## Downloading Images from Altura Work Orders

**Category:** Service Management

**Applies to:** Altura Work Orders, Service Logistics

### Problem

Users need to download or extract images that were uploaded to work orders in Altura for reporting, documentation, or audit purposes.

### Symptoms

- Unable to locate image download option in work order view
- Need to extract multiple images from completed work orders
- Images are visible but cannot be saved locally

### Likely Root Causes

- User is unfamiliar with the image download workflow
- Attempting to download from Service Logistics app instead of Altura web interface
- Work order status may affect image availability

### Resolution Steps

1. Open the work order in the Altura web interface (not the Service Logistics mobile app)
2. Scroll down to the "Images" section within the work order
3. Click "Edit/Upload Image(s)"
4. Click "Download All" to save all images as a zip file
5. Note: This works for work orders in any status (Open, Invoiced, Completed)
6. If using the Service Logistics mobile app, image download is not currently supported; use the web interface instead

### Validation

Verify that the downloaded zip file contains all expected images and that they are readable.

### Prevention

Train users on the difference between the Altura web interface and the Service Logistics mobile app. Document that bulk image downloads must be performed via the web interface.

### Escalation

If images are missing or corrupted, collect the work order number, expected image count, and any error messages. Escalate to Tier 2 support.


## Work Order Stuck in Incorrect Status or "In Use"

**Category:** Service Management

**Applies to:** Altura Work Orders, Service Logistics

### Problem

A work order is displaying an incorrect status, stuck in "Pending Verification," or showing as "In Use" and cannot be edited or processed.

### Symptoms

- Work order status does not match actual completion state
- Work order shows as "In Use" but no user is actively editing it
- Cannot edit or update work order due to locked status
- Work order remains in "Pending Verification" despite completion

### Likely Root Causes

- Session lock was not properly released when user closed the app
- System error during status transition
- User was unassigned from work order while editing
- Database record inconsistency

### Resolution Steps

1. Run PCVIEW utility to check the work order lines and current status
2. Run SA930 utility to clear the "In Use" lock on the work order
3. Verify the work order status has been updated correctly
4. If the user is unassigned from the work order, they must contact their back office to have the work order reassigned before editing
5. For status discrepancies, verify the workflow rules and manually update the status if necessary

### Validation

Attempt to open and edit the work order. Confirm the status reflects the actual state of the work. Check that no lock warnings appear.

### Prevention

Ensure users properly close work orders rather than force-closing the app. Implement periodic cleanup jobs to release stale locks.

### Escalation

If the lock persists or the status cannot be corrected, collect the work order number, user ID, and current status. Escalate to Tier 2 support with database access.


## Missing or Deleted Invoices

**Category:** Accounting

**Applies to:** Invoicing, Invoice History, Batch Processing

### Problem

Invoices that were expected to be generated or printed are missing, or invoice files appear to have been deleted.

### Symptoms

- No invoices available in the morning or after batch processing
- Invoice list is empty or incomplete
- Invoices exist in invoice history but not in the current file

### Likely Root Causes

- Invoice files were accidentally deleted
- Batch process failed to generate invoices
- File corruption or system error during invoice generation
- Incorrect file path or permissions

### Resolution Steps

1. Check invoice history to confirm the invoices were originally generated
2. Run PC300/R utility to regenerate invoice files from the previous day
3. Verify that the regenerated invoices match the invoice history records
4. If invoices are still missing, check for batch processing errors or file system issues
5. Review system logs for any errors during the invoice generation process

### Validation

Confirm that all expected invoices are now present and match the invoice history. Verify that users can access and print the invoices.

### Prevention

Implement automated backups of invoice files. Set file permissions to prevent accidental deletion. Monitor batch processing for errors.

### Escalation

If invoices cannot be regenerated or if there is evidence of data corruption, collect the date range, invoice numbers, and system logs. Escalate to Tier 2 support immediately.


## Transaction Merge Failures and Inventory Balance Discrepancies

**Category:** Accounting

**Applies to:** Inventory, Flooring, Transaction Processing

### Problem

Transactions cannot be merged due to missing data, or inventory/flooring balances do not update correctly after a merge.

### Symptoms

- Cannot merge transactions due to missing stock number or other required field
- Flooring balance on a unit does not reflect merged transactions
- Transaction status shows as "H" (history) but balance remains incorrect
- Inventory reports show discrepancies after transaction processing

### Likely Root Causes

- Required field (e.g., stock number) was not entered during transaction creation
- Database record inconsistency prevents automatic balance update
- Transaction merge logic did not trigger balance recalculation

### Resolution Steps

1. Locate the transaction with the missing required field (e.g., stock number)
2. Add the missing data to the transaction record
3. Attempt to merge the transactions again
4. If the merge succeeds but the balance does not update, manually update the flooring or inventory balance
5. For flooring balance: update WGI flooring balance to the correct value
6. Verify that inventory and flooring reports are now in balance
7. Check subledger to confirm all transactions are properly reconciled

### Validation

Run inventory and flooring reports to confirm balances are correct. Verify that all related transactions show the correct status.

### Prevention

Implement validation rules to require all necessary fields during transaction entry. Train users on proper transaction entry procedures.

### Escalation

If balances cannot be corrected or if there are widespread discrepancies, collect the unit number, transaction IDs, and current balance reports. Escalate to Tier 2 support with database access.


## Stuck or Unwanted Print Jobs

**Category:** System Administration

**Applies to:** Printing, Report Center, Batch Processing

### Problem

A print job is stuck in the print queue, continuously printing unwanted documents, or cannot be canceled, wasting paper and toner.

### Symptoms

- Printer continuously prints old or duplicate documents
- Cannot cancel or stop a print job
- Report Center shows jobs that should not be printing
- Print queue is jammed or unresponsive

### Likely Root Causes

- Print job was not properly canceled and remains in the queue
- Report scheduling error caused duplicate or incorrect print jobs
- Printer driver or spooler issue
- System error during batch report generation

### Resolution Steps

1. Attempt to cancel the print job from the Report Center or print queue
2. If the job cannot be canceled remotely, physically stop the printer
3. Clear the print queue on the server or workstation
4. Restart the print spooler service if necessary
5. Review the Report Center for any scheduled jobs that may be causing the issue
6. If the print job completes before intervention, review the printed output to determine if it indicates a system error
7. Contact the user to confirm whether the printed reports are needed or can be discarded

### Validation

Confirm the print queue is clear and no unwanted jobs are running. Verify that scheduled reports are configured correctly.

### Prevention

Review and clean up scheduled report jobs regularly. Ensure users understand how to cancel print jobs. Implement alerts for long-running or large print jobs.

### Escalation

If the print queue cannot be cleared or if the issue recurs, collect the print job details, Report Center configuration, and system logs. Escalate to Tier 2 support.


## User Account Locked Out or Login Failure

**Category:** User Access

**Applies to:** User Authentication, Login, Account Management

### Problem

Users are unable to log in to the system, receiving "locked out" or "access denied" messages.

### Symptoms

- User receives "locked out" message when attempting to log in
- Login fails despite correct credentials
- Multiple users report being unable to access the system
- Mobile app crashes immediately after login attempt

### Likely Root Causes

- Account locked due to multiple failed login attempts
- Password expired and requires reset
- User permissions have been revoked or changed
- System-wide authentication service outage
- License expiration affecting user access

### Resolution Steps

1. Verify the user account status in the user management system
2. If the account is locked, unlock it and notify the user
3. If the password has expired, initiate a password reset
4. Check user permissions and roles to ensure they have not been inadvertently changed
5. If multiple users are affected, check the authentication service status
6. For mobile app crashes, verify the app version is up to date and compatible with the current system version
7. If a license has expired, coordinate with the account manager to renew the license

### Validation

Have the user attempt to log in again. Confirm they can access their normal functions and data.

### Prevention

Implement proactive password expiration notifications. Monitor for unusual patterns of failed login attempts. Ensure license renewal reminders are sent well in advance.

### Escalation

If the account cannot be unlocked or if there is a system-wide authentication issue, collect the user ID, error messages, and authentication logs. Escalate to Tier 2 support immediately.


## Creating, Changing, or Deleting Status Codes

**Category:** Configuration

**Applies to:** POS, Time Clock, Table Maintenance, Status Codes

### Problem

Users need to create new status codes, modify existing ones, or delete unused status codes to match their business processes.

### Symptoms

- Required status code is not available in the system
- Status code list does not match business requirements
- Need to standardize status codes across multiple locations
- Unused status codes clutter the interface

### Likely Root Causes

- Status codes have not been configured for the specific location or module
- User is unfamiliar with the table maintenance interface
- Status codes were set up during initial implementation and have not been updated

### Resolution Steps

1. Navigate to POS > Time Clock > Table Maintenance
2. Select the status code table
3. To create a new status code: click "Add," enter the code and description, and save
4. To change an existing status code: select the code, modify the description or settings, and save
5. To delete a status code: select the code and click "Delete" (note: codes in use cannot be deleted)
6. If standardizing across locations, export the status code table from the primary location and import it to other locations
7. Verify the changes by checking the status code dropdown in the relevant module

### Validation

Confirm the new or modified status codes appear correctly in the system. Test by creating a transaction or record using the new status code.

### Prevention

Document status code standards in your configuration guide. Review and update status codes during system audits or process changes.

### Escalation

If status codes cannot be created or modified, or if there are database errors, collect the module name, error messages, and screenshots. Escalate to Tier 2 support.


## Scheduled Reports Did Not Run or Print

**Category:** Reporting

**Applies to:** Report Center, Scheduled Jobs, Batch Processing

### Problem

Scheduled reports that normally run overnight or at specific times did not execute, or the output is missing.

### Symptoms

- Reports did not print or appear in the Report Center
- Report output files are missing
- Unexpected or incorrect reports were generated
- Report Center shows errors or incomplete jobs

### Likely Root Causes

- Scheduled job failed due to system error
- Report parameters were incorrect or changed
- Printer or output destination was unavailable
- System maintenance or downtime during scheduled run time
- Report scheduling configuration was accidentally modified

### Resolution Steps

1. Check the Report Center for job status and any error messages
2. Review the report schedule to confirm the job is still configured correctly
3. Manually run the report to verify it executes without errors
4. If the report runs successfully, check the output destination (printer, file path, email) to ensure it is accessible
5. Review system logs for any errors or maintenance activities during the scheduled run time
6. If the report output is unusual, verify the report parameters and date range
7. Reschedule the job if necessary and monitor the next execution

### Validation

Confirm the report runs successfully on the next scheduled execution. Verify the output is complete and accurate.

### Prevention

Implement monitoring and alerting for scheduled report failures. Document report schedules and parameters. Test reports after any system changes.

### Escalation

If reports continue to fail or if there is evidence of a system-wide issue, collect the report name, schedule, error messages, and system logs. Escalate to Tier 2 support.


## Glossary

**Altura:** Service management module for work order scheduling, technician dispatch, and mobile service operations.

**Batch Processing:** Automated execution of multiple transactions or reports, typically run overnight or at scheduled intervals.

**End-of-Year (EOY):** Annual payroll and accounting close process, including tax form generation and data archiving.

**Flooring:** Inventory financing arrangement where a lender provides funds for inventory purchases; flooring balance tracks the amount owed.

**Invoice History:** Archive of all generated invoices, used for reporting and audit purposes.

**PC300/R:** Utility to regenerate invoice files from invoice history.

**PCVIEW:** Utility to view and inspect work order or transaction details.

**SA930:** Utility to clear locks on work orders or records that are stuck in "In Use" status.

**Service Logistics:** Mobile application for field technicians to manage work orders, record time, and capture images.

**Status Code:** User-defined code to categorize transactions, work orders, or time entries according to business processes.

**T4:** Canadian tax form summarizing employee income and deductions for the year.

**Work Order:** Service request or job ticket in the Altura system, tracking labor, parts, and completion status.

