# Automated Payment Follow-Up System

## 1. Project Overview
The **Automated Payment Follow-Up System** is a workflow automation project built using Zapier, Google Sheets, and Gmail. It identifies pending invoices, sends personalized payment reminder emails, and maintains payment follow-up records in a spreadsheet.

## 2. Project Objective
- Automate repetitive payment follow-up activities.
- Identify invoices with pending payment status.
- Send personalized reminder emails to the appropriate recipients.
- Maintain an updated record of reminder activity.
- Reduce manual effort and improve consistency.

## 3. Tools and Technologies
- **Zapier:** Workflow automation and task scheduling.
- **Google Sheets:** Invoice tracking and payment status management.
- **Gmail:** Sending automated payment reminder emails.
- **Excel/CSV:** Invoice data management and sample records.

## 4. System Architecture

The system connects the invoice data source with the automation platform and email service.

```text
       ┌─────────────────────────┐
       │   Schedule by Zapier    │
       │  Daily Trigger: 9 AM    │
       └────────────┬────────────┘
                    │
                    ▼
       ┌─────────────────────────┐
       │ Google Sheets           │
       │ Retrieve Invoice Records│
       └────────────┬────────────┘
                    │
                    ▼
       ┌─────────────────────────┐
       │ Filter Pending Invoices │
       │ Check Recipient Email   │
       └────────────┬────────────┘
                    │
                    ▼
       ┌─────────────────────────┐
       │ Route by Payment Type   │
       │ Maintenance / Project   │
       └────────────┬────────────┘
                    │
                    ▼
       ┌─────────────────────────┐
       │ Gmail                   │
       │ Send Reminder Email     │
       └────────────┬────────────┘
                    │
                    ▼
       ┌─────────────────────────┐
       │ Update Google Sheets    │
       │ Record Reminder Status  │
       └─────────────────────────┘
```

## 5. Workflow Explanation

1. **Scheduled Trigger:** Zapier starts the workflow daily at 9:00 AM.
2. **Retrieve Records:** The workflow retrieves invoice information from Google Sheets.
3. **Filter Pending Payments:** Only invoices marked `Pending` are selected.
4. **Validate Email:** The workflow checks whether a recipient email address is available.
5. **Route by Payment Type:** The workflow directs invoices to the appropriate recipient:
   - **Maintenance:** `sadicsha.khandait@associates.scit.edu`
   - **Project:** `mehak.chhabra@associates.scit.edu`
6. **Send Reminder:** Gmail sends a personalized payment reminder containing relevant invoice details.
7. **Update Records:** Google Sheets records the reminder activity or updated status.

## 6. Sample Invoice Data

The invoice tracker contains fields such as:

| Field | Description |
|---|---|
| Invoice ID | Unique invoice reference |
| Payment Type | Maintenance or Project |
| Customer Name | Name associated with the invoice |
| Amount | Invoice amount |
| Bank Name | Bank information in the sample dataset |
| Account Number | Sample account information |
| Payment Status | Pending, Completed, or Reminder Sent |
| Recipient Email | Email address for follow-up |

## 7. Expected Outcomes
- Faster and more consistent payment follow-ups.
- Less manual effort in identifying pending invoices.
- Personalized email reminders for different payment categories.
- Improved visibility into invoice and reminder status.

## 8. Project Files
- `data/` — Sample invoice spreadsheet and CSV dataset.
- `docs/` — Workflow blueprint and architecture documentation.
- `screenshots/` — Workflow, spreadsheet, and email reference screenshots.
- `templates/` — Payment reminder email template.

## 9. Security Considerations
- Use authorized test data and recipient email addresses.
- Keep passwords, API keys, and authentication credentials private.
- Avoid publishing real bank or personal information in a public repository.

## 10. Implementation Note
This repository documents the proposed workflow and includes supporting project files. The actual Zap must be configured and tested in Zapier before the automation can be considered fully operational.

